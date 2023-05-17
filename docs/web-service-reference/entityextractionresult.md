---
title: "EntityExtractionResult"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 643b99ab-ff90-4411-864c-1077623028d6
description: "The EntityExtractionResult element specifies the EntityExtractionResult property of an item."
---

# EntityExtractionResult

The **EntityExtractionResult** element specifies the **EntityExtractionResult** property of an item. 
  
```XML
<EntityExtractionResult>
    <Addresses/>
    <MeetingSuggestions/>
    <TaskSuggestions/>
    <EmailAddresses/>
    <Contacts/>
    <Urls/>
    <PhoneNumbers/>
</EntityExtractionResult>
```

 **EntityExtractionResultType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Addresses (ArrayOfAddressEntitiesType)](addresses-arrayofaddressentitiestype.md) <br/> |Specifies an array of **AddressEntity** elements.  <br/> |
|[MeetingSuggestions](meetingsuggestions.md) <br/> |Specifies an array of **MeetingSuggestion** elements.  <br/> |
|[TaskSuggestions](tasksuggestions.md) <br/> |Specifies an array of **TaskSuggestion** elements.  <br/> |
|[EmailAddresses (ArrayOfEmailAddressEntitiesType)](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |Specifies an array of email address entities.  <br/> |
|[Contacts (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |Specifies an array of contacts.  <br/> |
|[Urls (ArrayOfUrlEntitiesType)](urls-arrayofurlentitiestype.md) <br/> |Specifies an array of URLs.  <br/> |
|[PhoneNumbers (ArrayOfPhoneEntitiesType)](phonenumbers-arrayofphoneentitiestype.md) <br/> |Specifies an array of phone numbers.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Item](item.md) <br/> |Represents a generic item in the Exchange store.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Type|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

