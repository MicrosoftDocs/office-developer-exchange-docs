---
title: "Properties and extended properties in EWS in Exchange"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.assetid: 68623048-060e-4602-b3fa-62617a94cf72
description: "Discover how you can define and access properties on items and folders by using EWS in Exchange."
localization_priority: Priority
---

# Properties and extended properties in EWS in Exchange

Discover how you can define and access properties on items and folders by using EWS in Exchange.
  
An Exchange mailbox contains a large number of items, including email messages, appointments, meetings, and so on. Those items are made up of properties; the properties describe the items. You can use item properties to perform a [search](search-and-ews-in-exchange.md), [synchronize item changes](mailbox-synchronization-and-ews-in-exchange.md), and [create custom property types](https://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a). This article provides an overview of properties and how you can work with properties in your application.
  
## Exchange item properties
<a name="ItemsAreProperties"> </a>

Items and folders in Exchange are essentially rows in tables. The main property that identifies an item or folder is its [EWS identifier](ews-identifiers-in-exchange.md). Although there are other identifier-related properties in the Exchange database, for EWS, the EWS identifier acts as the primary key for the collection of properties that describe an item. The EWS identifier property contains two parts:
  
- An [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) or [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) property that identifies the item 
    
- A **ChangeKey** property that contains stateful information about whether an item or folder has changed 
    
All items in a mailbox are stored in the same Exchange database and use the same database schema. Items are distinguished by a combination of the [ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) property, property constraints, and the business logic layers that affect how they are managed in the Exchange store. Table 1 shows how properties are applied across different item types; in this example, email and appointment items. Both items have a value for the [Subject](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) property. But notice that the [IsAllDayEvent](https://msdn.microsoft.com/library/29140a64-9d7a-4a14-a10d-c98197c9831b%28Office.15%29.aspx) property is not set on the email item, and the **IsReadReceiptRequested** property is not set on the appointment. Fortunately, you don't need to know which properties are applicable for each item class; EWS handles this for you. 
  
**Table 1. Comparison of appointment and email properties**

|**Item type**|**Item class**|**Subject**|**IsAllDayEvent**|**IsReadReceiptRequested**|
|:-----|:-----|:-----|:-----|:-----|
|Email  <br/> |IPM.Note  <br/> |Status report: Project X complete  <br/> |NULL  <br/> |true  <br/> |
|Appointment  <br/> |IPM.Appointment  <br/> |Contoso company meeting  <br/> |false  <br/> |NULL  <br/> |
   
The EWS schema supports many of the constraints managed by the Exchange database and the business logic layers between EWS and the Exchange database. The EWS schema applies a defined a set of properties to each item type. The following are the strongly-typed Exchange database items provided by EWS: 
  
- Email messages
    
- Appointments
    
- Contacts
    
- Distribution lists
    
- Meeting messages
    
- Meeting requests
    
- Meeting responses
    
- Meeting cancellations
    
- Tasks
    
- Post items
    
Generic items are returned by EWS as email messages. The EWS Managed API implements all these item types.
  
> [!NOTE]
> Response objects are only sent by the client to the server in response to items received from other people. They do not exist in the Exchange database. 
  
## What are properties in EWS?
<a name="WhatAreEWSProperties"> </a>

The EWS schema describes the data that is sent between an EWS client and Exchange. A large part of the schema describes the item and folder properties that you can access in the Exchange database. The EWS schema describes the XML representation of the Exchange database properties that are available to your application. The actual properties, in terms of which properties are available, what form they take, and the values they return, vary based on what you trying to do. For example, the **Body** property will only return the first 512 characters in a **FindItem** operation, but the **GetItem** operation returns the full text of the item. Although most properties are both settable and retrievable, some properties are only set by Exchange. Each property exists in the schema in an XML format that either reflects the property as it is stored in the Exchange database, or is computed from properties stored in the Exchange database. The **Subject** property is an example of a settable property; the **UnreadCount** property on a folder is an example of a computed property. A core set of properties are common to the core item types. 
  
The following factors determine the property set that your application gets from Exchange: 
  
- The operation that your application is calling
    
- The base response shape
    
- The item type
    
- The specified property paths
    
It is important to understand how these different factors affect the data that you can access. As with the example of the **Body** property mentioned earlier, some information is conditionally available depending on various factors. Understanding these factors might save you time by helping you choose the correct options to access the information you want. To discover which properties are accessible, you will need to test these factors to determine how to access the properties your application needs. This section describes how these different factors affect which properties are returned in EWS responses. 
  
### EWS response shapes

Exchange stores a lot of information about items. Sometimes, your application doesn't need all of that information, and in many cases, it is best not to get it all. [EWS response shapes](property-sets-and-response-shapes-in-ews-in-exchange.md), also called property shapes, indicate which properties are returned from the server. The core element of the response shape is the base shape. A base shape is a default preset property bag for strongly typed items. The EWS Managed API equivalent of the base shape is the [BasePropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx). EWS includes three default response shapes.
  
**Table 2. Default response shapes**

|**Default response shape name**|**EWS Managed API equivalent**|**Description**|
|:-----|:-----|:-----|
|IdOnly  <br/> |BasePropertySet.IdOnly value  <br/> |Only the EWS identifier and change key are returned. Unless the client uses all the properties returned by the AllProperties or Default shape, use the IdOnly shape and specify additional properties by using the property path set on the **PropertySet** class. Most applications should use the IdOnly response shape with additional properties specified. This reduces the amount of unused data that is requested by clients.  <br/> |
|Default  <br/> |N/A  <br/> |A set of standard properties for the item type. Only use this response shape if your application uses all the properties.  <br/> |
|AllProperties  <br/> |BasePropertySet.FirstClassProperties value  <br/> |A larger set of properties than the Default shape. Although the name implies it, this option does not return all properties on an item. This property set returns the properties that client applications use most often. If you need additional properties, you can request them by their property path.  <br/> If your application doesn't use all the properties returned with this response shape, use the IdOnly response shape with additional properties specified.  <br/> |
   
Many EWS operations return items and their properties. Regardless of the response shapes that you specify, different operations can return different property sets. Different item types also return different properties, depending on the operation and the response shape specified. The following operations use response shapes to identify which properties to return.
  
**Table 3. Operations that use response shapes**

|**EWS operation**|**EWS Managed API method**|
|:-----|:-----|
|[GetConversationItems](https://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> |[ExchangeService.GetConversationItems method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) <br/> |
|[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |[Folder.Bind method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> |
|[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |[Item.Bind method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [ExchangeService.BindToItems method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |
|[FindConversation](https://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> |[ExchangeService.FindConversation method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) <br/> |
|[FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |[Folder.FindFolders method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.FindFolders method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) <br/> |
|[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |[Folder.FindItems method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> [ExchangeService.FindItems method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |
|[FindPeople](https://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |Not implemented.  <br/> |
|[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |[ExchangeService.ResolveNames method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |
|[SearchMailboxes](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[ExchangeService.SearchMailboxes method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSearchMailboxes method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsearchmailboxes%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderHierarchy method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderItems method](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) <br/> |
   
Property shapes are one, rudimentary way to identify the properties that you want your application to return. Sometimes, however, your application needs a more refined set of specific properties. For this, you can use the property path.
  
### Choose properties by their property path

An EWS property path is metadata that is used to identify properties in either a request or response. 
  
**Table 4. Property path types**

|**Property path type**|**Schema type**|**EWS Managed API implementation**|**Description**|
|:-----|:-----|:-----|:-----|
|FieldUri  <br/> |PathToUnindexedFieldType  <br/> |Types that inherit from [ServiceObjectSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceobjectschema%28v=exchg.80%29.aspx).  <br/> |The most common property path. FieldUri property paths are specified on a **PropertySet** object in the EWS Managed API. Most EWS properties can be specified by the FieldUri property path. This is described by the UnindexedFieldURIType in the EWS schema.  <br/> The FieldUri property path XML looks like this:  <br/> ```XML<FieldURI FieldURI="item:Subject"/>```This property path is the equivalent of ItemSchema.Subject in the EWS Managed API.  <br/> |
|IndexedFieldUri  <br/> |PathToIndexedFieldType  <br/> |Types that inherit from [ItemSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx).  <br/> |Identifies dictionary properties that require a property index to specify the value to return. Use this path when a property can have more than one value. This is described by the **DictionaryURIType** property in the EWS schema. **DictionaryURIType** property paths are specified on a **PropertySet** object in the EWS Managed API.  <br/> The IndexedFieldUri property path XML looks like this:  <br/> ```XML<IndexedFieldURI FieldURI="contacts:PhysicalAddress:Street FieldIndex="Home"/>```|
|ExtendedFieldUri  <br/> |PathToExtendedFieldType  <br/> |[ExtendedPropertyDefinition](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |Identifies an extended property definition that identifies custom or non-schematized properties on items.  <br/> The ExtendedFieldUri property path XML looks like this:  <br/> ```XML<ExtendedFieldURI> PropertyTag="0x1234" PropertyType="Integer" />```|
|ExceptionFieldUri  <br/> |ExceptionFieldURI  <br/> |[ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) <br/> |Specifies properties that are associated with an error in an EWS response. This is described by the **ExceptionPropertyURIType** type in the EWS schema. This only occurs in the **MessageXml** element of error responses that occur when you are working with calendar recurrence patterns.  <br/> |
   
As a best practice, when you request properties, use the IdOnly base shape ([BasePropertySet.IdOnly](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) in the EWS Managed API) and then request only the properties your application needs by specifying the property paths. 
  
### Schematized properties

Most of the properties that your EWS client needs are described by the EWS schema. The primary folder and item type definitions, which contain the property definitions, are found in the types.xsd schema. The following schema types contain the property definitions for most objects that you can use.
  
**Table 5. Schema types that contain property definitions**

|**EWS schema type**|**EWS Managed API type equivalent**|**Defines the…**|
|:-----|:-----|:-----|
|**ItemType** <br/> |[Item class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) <br/> |Base item type property set. This type can be created from a client but is never returned by Exchange. Exchange returns a MessageType object for all generic objects.  <br/> |
|**MessageType** <br/> |[EmailMessage class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |Email message object property set and the property set for all generic objects.  <br/> |
|**CalendarItemType** <br/> |[Appointment class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |Calendar item property set; this includes single and recurring appointments.  <br/> |
|**ContactItemType** <br/> |[Contact class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |Contact item property set.  <br/> |
|**DistributionListType** <br/> |[ContactGroup class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) <br/> |Personal distribution list property set.  <br/> |
|**MeetingMessageType** <br/> |[MeetingMessage class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingmessage%28v=exchg.80%29.aspx) <br/> |Meeting message type property set.  <br/> |
|**MeetingRequestMessageType** <br/> |[MeetingRequest class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequest%28v=exchg.80%29.aspx) <br/> |Meeting request type property set.  <br/> |
|**MeetingResponseMessageType** <br/> |[MeetingResponse class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingresponse%28v=exchg.80%29.aspx) <br/> |Meeting response type property set.  <br/> |
|**MeetingCancellationMessageType** <br/> |[MeetingCancellation class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingcancellation%28v=exchg.80%29.aspx) <br/> |Meeting cancellation type property set.  <br/> |
|**TaskType** <br/> |[Task class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |Task type property set.  <br/> |
|**PostItemType** <br/> |[PostItem class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.postitem%28v=exchg.80%29.aspx) <br/> |Postitem type property set.  <br/> |
|**FolderType** <br/> |[Folder class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) <br/> |Folder type property set.  <br/> |
|**CalendarFolderType** <br/> |[CalendarFolder class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx) <br/> |SearchFolder type property set.  <br/> |
|**ContactsFolderType** <br/> |[ContactsFolder class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx) <br/> |ContactsFolder type property set.  <br/> |
|**SearchFolderType** <br/> |[SearchFolder class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) <br/> |SearchFolder type property set.  <br/> |
|**TasksFolderType** <br/> |[TasksFolder class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) <br/> |TasksFolder type property set.  <br/> |
|**UserConfigurationType** <br/> |[UserConfiguration class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration%28v=exchg.80%29.aspx) <br/> |UserConfiguration type property set.  <br/> |
   
While the properties in the EWS schema are sufficient for many applications, you can't implement some scenarios by using only what is described in the schema. For those scenarios, you can extended properties. 
  
### Extended properties (aka non-schematized properties)

Extended properties enable you to create custom properties, which give you access to properties on items and folders in the Exchange store that are not defined in the EWS schema. You can use them to access the native MAPI item and folder properties in the Exchange database. You can use extended properties to access all the schematized properties, because under the covers, those schematized properties are nothing more than MAPI properties in the Exchange database. 
  
The PathToExtendedFieldType schema type, located in the types.xsd schema, defines the XML that represents an extended property. This schema type defines the [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element in XML instances; in other words, it defines the XML that is sent between the service and client. The ExtendedPropertyType schema type defines both the [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element and the value or array of values that an extended property contains. The following table shows the approximate mapping of the extended property XML and how it is implemented on items in the EWS Managed API. 
  
**Table 6. Extended property XML as implemented in the EWS Managed API**

|**EWS Managed API implementation**|**What it contains**|**What it maps to**|
|:-----|:-----|:-----|
|[Item.ExtendedProperties property](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.extendedproperties%28v=exchg.80%29.aspx) <br/> |A collection of extended properties on an item.  <br/> |One or more instances of extended properties on an item.  <br/> |
|[ExtendedProperty class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedproperty%28v=exchg.80%29.aspx) <br/> |The extended property definition and values.  <br/> |The ExtendedPropertyType schema type.  <br/> |
|[ExtendedPropertyDefinition class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |An extended property definition.  <br/> |The PathToExtendedFieldType schema type.  <br/> |
   
If you want to learn more about how you can use extended properties in your application, you can explore the following code samples: 
  
- [MFCMapi](http://mfcmapi.codeplex.com/)
    
- [Exchange 2013: Provision custom X-headers programmatically](https://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [Exchange 2013: Access a property by its property tag](https://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-719875ac)
    
- [Exchange 2013: Access a named property by its identifier](https://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-02dbe22f)
    
- [Exchange 2013: Access a named property by its name](https://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-6556e183)
    
- [Exchange 2013: Access a property by property set GUID and name](https://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-4021f971)
    
- [Exchange 2013: Create custom extended properties programmatically](https://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a)
    
## In this section
<a name="bk_inthissection"> </a>

- [Provision x-headers by using EWS in Exchange](how-to-provision-x-headers-by-using-ews-in-exchange.md)
    
- [EWS property-related errors](ews-property-related-errors.md)
    
## See also


- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [MFCMapi](http://mfcmapi.codeplex.com/)
    

