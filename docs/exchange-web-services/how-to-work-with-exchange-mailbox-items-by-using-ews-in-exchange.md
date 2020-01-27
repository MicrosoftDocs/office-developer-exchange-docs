---
title: "Work with Exchange mailbox items by using EWS in Exchange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 721deb84-f85d-45d0-84c1-0ed55f359969
description: "Learn how to create, get, update, and delete items by using the EWS Managed API or EWS in Exchange."
localization_priority: Priority
---

# Work with Exchange mailbox items by using EWS in Exchange

Learn how to create, get, update, and delete items by using the EWS Managed API or EWS in Exchange.
  
You can use the EWS Managed API or EWS to work with items in a mailbox. You can use generic items — EWS Managed API [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) objects or EWS [Item](https://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) types — to perform some operations (getting an item or deleting an item by using the item's identifier); however, most of the time you'll have to use a [strongly typed item](folders-and-items-in-ews-in-exchange.md#bk_item) to perform a get or update operation because you'll need access to the properties that are specific to the strongly typed item. 

For example, you can't use a generic item to retrieve an item that contains a start and end date - you need an EWS Managed API [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object or an EWS [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) type to do that. And if you're using the EWS Managed API, you always have to create strongly typed items, because the generic **Item** class does not have a constructor. If you're working with an item that is not strongly typed, you can always use the base **Item** class to work with the item. 
  
**Table 1. EWS Managed API methods and EWS operations for working with items**

|**In order to…**|**EWS Managed API method**|**EWS operation**|
|:-----|:-----|:-----|
|Create a generic item  <br/> |None. You can only create specific item types by using the EWS Managed API; you cannot create generic items.  <br/> |[CreateItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
|Get an item  <br/> |[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|Update an item  <br/> |[Item.Update](https://msdn.microsoft.com/library/office/dd635915%28v=exchg.80%29.aspx) <br/> |[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Delete an item  <br/> |[Item.Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
In this article, you'll learn when you can use the generic base class and when you need to use a strongly typed item to complete your task. The code examples will show you how to use the base class, and what to do when you can't use the base class or it doesn't fit your needs.
  
## Create an item by using the EWS Managed API
<a name="bk_createewsma"> </a>

The EWS Managed API does not have a publicly available constructor for the [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) class, so you must use the constructor for the specific item type you want to create in order to create an item. For example, use the [EmailMessage class constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) to create a new email message, and the [Contact class constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) to create a new contact. Likewise, the server never returns generic **Item** objects in responses; all generic items are returned as **EmailMessage** objects. 
  
When you know the type of item to create, you can complete the task in just a few steps. The steps are similar for all item types:
  
1. Initialize a new instance of one of the [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) classes with the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object as a parameter. 
    
2. Set properties on the item. The schemas are different for each item type, so different properties are available for different items.
    
3. Save the item, or save and send the item.
    
For example, you can create an [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object, set the [Subject](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx), [Body](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx), and [ToRecipients](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx) properties, and then send it by using the [EmailMessage.SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method. 
  
```cs
// Create an email message and provide it with connection 
// configuration information by using an ExchangeService object named service.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.Subject = "Company Soccer Team";
message.Body = "Are you interested in joining?";
message.ToRecipients.Add("sadie@contoso.com");
// Send the email message and save a copy.
// This method call results in a CreateItem call to EWS.
message.SendAndSaveCopy();
```

To learn how to create a meeting or appointment item by using the EWS Managed API, see [Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).
  
## Create an item by using EWS
<a name="bk_createews"> </a>

You can create a generic item or a strongly typed item by using EWS. The steps are similar for all item types:
  
1. Use the [CreateItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) operation to create an item in the Exchange store. 
    
2. Use the [Items](https://msdn.microsoft.com/library/0811a73e-bf1f-4889-9219-73902dd47639%28Office.15%29.aspx) element to contain one or more items to create. 
    
3. Set properties on the item.
    
For example, you can create an email message and send it by using the code in the following example. This is also the XML request that the EWS Managed API sends when you call the [SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com </t:EmailAddress>
              </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message. 
  
To learn how to create a meeting or appointment item by using EWS, see [Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).
  
## Get an item by using the EWS Managed API
<a name="bk_getewsma"> </a>

To use the EWS Managed API to get an item if you know the [Item.Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to retrieve, you simply call one of the [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) methods on the item, and the item is retrieved. As a best practice, we recommend that you limit the properties returned to only those that are required. This example returns the item **Id** property and the **Subject** property. 
  
This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server. The local variable  *itemId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update. 
  
```cs
// As a best practice, limit the properties returned to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.Subject);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId, propSet);

```

If you're searching for an item that meets specific criteria, do the following:
  
1. Bind to the folder that contains the items to get.
    
2. Instantiate a [SearchFilter.SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) or a [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) to filter the items to return. 
    
3. Instantiate an [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) or [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) object to specify the number of items to return. 
    
4. Call the [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) or [ExchangeService.FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method. 
    
For example, if you want to retrieve unread email messages in the Inbox, use the code in the following example. This example uses a **SearchFilterCollection** to limit the results of the **FindItems** method to unread messages, and limits the **ItemView** to limit results to one item. This particular code only works on [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) objects because the [EmailMessageSchema.IsRead](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessageschema.isread%28v=exchg.80%29.aspx) value is part of the **SearchFilter**. 
  
```cs
// Bind the Inbox folder to the service object.
Folder inbox = Folder.Bind(service, WellKnownFolderName.Inbox);
// The search filter to get unread email.
SearchFilter sf = new SearchFilter.SearchFilterCollection(LogicalOperator.And, new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false));
ItemView view = new ItemView(1);
// Fire the query for the unread items.
// This method call results in a FindItem call to EWS.
FindItemsResults<Item> findResults = service.FindItems(WellKnownFolderName.Inbox, sf, view);
```

Alternatively, you can use a [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) to limit the results of the search as shown in the following code example. This example uses the [FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to retrieve up to five appointments that occur in the next 30 days. This code of course only works on calendar items. 
  
```cs
// Initialize values for the start and end times, and the number of appointments to retrieve.
DateTime startDate = DateTime.Now;
DateTime endDate = startDate.AddDays(30);
const int NUM_APPTS = 5;
// Bind the Calendar folder to the service object.
// This method call results in a GetFolder call to EWS.
CalendarFolder calendar = CalendarFolder.Bind(service, WellKnownFolderName.Calendar, new PropertySet());
// Set the start and end time and number of appointments to retrieve.
CalendarView cView = new CalendarView(startDate, endDate, NUM_APPTS);
// Limit the properties returned to the appointment's subject, start time, and end time.
cView.PropertySet = new PropertySet(AppointmentSchema.Subject, AppointmentSchema.Start, AppointmentSchema.End);
// Retrieve a collection of appointments by using the calendar view.
// This method call results in a FindAppointments call to EWS.
FindItemsResults<Appointment> appointments = calendar.FindAppointments(cView);
```

Note that the information the server returns in the **Bind** method response is different than the information that the server returns for a **FindItem** or **FindAppointment** method response. The **Bind** method can return all the schematized properties, whereas the **FindItem** and **FindAppointment** methods do not return all the schematized properties. So if you need full access to the item, you'll have to use the **Bind** method. If you don't have the item **Id** of the item you'd like to retrieve, use the **FindItem** or **FindAppointment** methods to retrieve the Id, and then use the **Bind** method to retrieve the properties you need. 
  
To learn how to get a meeting or appointment item by using the EWS Managed API, see [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## Get an item by using EWS
<a name="bk_getews"> </a>

If you know the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the item to retrieve, you can get the item by using the [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) operation. 
  
The following example shows the XML request to get the [Subject](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) of an item with a specific **ItemId**. This is also the XML request that the EWS Managed API sends when calling the [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method on an **ItemId**. The values of some attributes and elements have been shortened for readability.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="GJc/NAAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

The following example shows the XML response that the server returns after it processes the **GetItem** operation. The response indicates the item was retrieved successfully. The values of some attributes and elements have been shortened for readability. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="GJc/NAAA=" ChangeKey="CQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAGJd9Z"/>
              <t:Subject>Company Soccer Team</t:Subject>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

If you do not know the **ItemId** of the item you want to retrieve, you can use the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find the item. In order to use the **FindItem** operation, you must first identify the folder that you're searching. You can identify the folder by using its **DistinguinguishedFolderName** or by using the [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx). You can use either the [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) or [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operations to get the **FolderId** you need. Then use the **FindItem** operation to search that folder for results that match the search filter. Unlike the EWS Managed API, EWS does not provide a separate find operation for appointments. The **FindItem** operation retrieves items of all types. 
  
The following example shows the XML **FindItem** operation request that is sent to the server to find appointments in the Calendar folder that occur in the next 30 days. The values of some attributes and elements have been shortened for readability. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView MaxEntriesReturned="5" StartDate="2013-10-16T17:04:28.722Z" EndDate="2013-11-15T18:04:28.722Z" />
      <m:ParentFolderIds>
        <t:FolderId Id="AAAEOAAA=" ChangeKey="AgAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAAAA3" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

The server responds to the **FindItem** request with a [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes the [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the operation completed successfully. If any calendar items meet the filtering criteria, they are included in the response.
  
Note that the information the server returns in the **GetItem** operation response is different than the information the server returns in a **FindItem** or **FindAppointment** operation response. The **GetItem** operation can return all the schematized properties, whereas the **FindItem** and **FindAppointment** operations do not return all the schematized properties. So if you need full access to the item, you'll have to use the **GetItem** operation. If you don't have the **ItemId** of the item you'd like to retrieve, use the **FindItem** or **FindAppointment** operations to retrieve the **ItemId**, and then use the **GetItem** operation to retrieve the elements you need. 
  
To learn how to get a meeting or appointment item by using EWS, see [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## Update an item by using the EWS Managed API
<a name="bk_updateewsma"> </a>

The steps to update an item by using the EWS Managed API are similar for all item types; however, the item properties are different for each item type, and the [Update](https://msdn.microsoft.com/library/office/dd635915%28v=exchg.80%29.aspx) method has many overloaded methods to choose from. To update an item: 
  
1. Use the [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method to get the latest version of the item, unless you already have it. To update properties specific to a strongly typed item, you'll have to bind to that item type. To update properties available on the generic item type, you can bind to the [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object. 
    
2. Update the properties on the item.
    
3. Call the **Update** method. 
    
For example, you can update the subject of an email by using the generic item type, as shown in the code in the following example.
  
This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server. The local variable  *itemId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update. 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Update the Subject of the email.
item.Subject = "New subject";
// Save the updated email.
// This method call results in an UpdateItem call to EWS.
item.Update(ConflictResolutionMode.AlwaysOverwrite);
```

To learn how to update a meeting or appointment item by using the EWS Managed API, see [Update appointments and meetings by using EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## Update an item by using EWS
<a name="bk_updateews"> </a>

To update an item by using EWS, do the following:
  
1. Use the [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) operation to get the latest version of the item, unless you already have it. 
    
2. Use the [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) operation to specify fields to update and assign new values to those fields. 
    
The following example shows the XML **UpdateItem** operation request that is sent to the server to update the [Subject](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) value of the email message. The values of some attributes and elements have been shortened for readability. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AlwaysOverwrite">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAPdgr" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>New subject</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

The server responds to the **UpdateItem** request with a [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes the a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the item update was successful.
  
To learn how to update a meeting or appointment item by using EWS, see [Update appointments and meetings by using EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## Delete an item by using the EWS Managed API
<a name="bk_deleteewsma"> </a>

You can delete items by moving them to the Deleted Items folder or to the dumpster. If you know the [ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to delete, just call the [Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) method on the item. 
  
If you need to find the item before deleting it, do the following:
  
1. Call the [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) or [FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to find the item to delete. 
    
1. Instantiate a [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) and limit it to the properties to return, or use a [SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) to find specific items. 
    
2. Instantiate an [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) or [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) to specify the number of items to return. 
    
2. Call the [Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) method. 
    
For example, the following code shows how to move an email message to the Deleted Items folder.
  
This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server. The local variable  *itemId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update. 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Delete the item by moving it to the Deleted Items folder.
// This method call results in a DeleteItem call to EWS.
item.Delete(DeleteMode.MoveToDeletedItems);
```

For more details about deleting items, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md). To learn how to delete a meeting or appointment item by using the EWS Managed API, see [Delete appointments and cancel meetings by using EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).
  
## Delete an item by using EWS
<a name="bk_deleteews"> </a>

You can delete an item by using the [DeleteItem](../web-service-reference/deleteitem-operation.md) operation. 
  
The following example shows the XML request that is sent to the server to move the email message to the Deleted Items folder. The values of some attributes and elements have been shortened for readability.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:DeleteItem DeleteType="MoveToDeletedItems">
      <m:ItemIds>
        <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAANIFzC" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

The server responds to the **DeleteItem** request with a [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) message that includes the a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the item deletion was successful.
  
For more details about deleting items, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md). To learn how to delete a meeting or appointment item by using EWS, see [Delete appointments and cancel meetings by using EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).
  
## Move or copy items to another mailbox
<a name="bk_movecopybtnmailboxes"> </a>

You can move or copy items between mailboxes by using the [ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) and [UploadItems](https://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) operations. To learn more, see [Exporting and importing items by using EWS in Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md).
  
## See also

- [Folders and items in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)    
- [Work with folders by using EWS in Exchange](how-to-work-with-folders-by-using-ews-in-exchange.md)    
- [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md)
    

