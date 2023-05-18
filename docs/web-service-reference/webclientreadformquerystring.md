---
title: "WebClientReadFormQueryString"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- WebClientReadFormQueryString
api_type:
- schema
ms.assetid: 13e8871a-32a6-4bb9-9493-864c4c07efff
description: "The WebClientReadFormQueryString element represents a URL to concatenate to the Outlook Web App endpoint to read an item in Outlook Web App."
---

# WebClientReadFormQueryString

The **WebClientReadFormQueryString** element represents a URL to concatenate to the Outlook Web App endpoint to read an item in Outlook Web App. 
  
```XML
<WebClientReadFormQueryString/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[Item](item.md) <br/> |Represents an item in the Exchange store.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation in the Exchange store.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response in the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an Exchange e-mail message.  <br/> |
|[PostItem](postitem.md) <br/> |Represents a post item in the Exchange store.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Removes an item from the Exchange store.  <br/> |
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
   
## Text value

A text value that represents a string is required if this element is used.
  
## Remarks

The item identifier for an Outlook Web App URL is the EWS identifier of the item. You can URL-encode the EWS item identifier and append it to the query string to get the Outlook Web App URL for an item.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
### Version differences

Versions of Exchange starting with major version 15 and ending with Exchange Server 2013 build 15.0.775.38 (CU3) and Exchange Online version 15.00.0775.009 do not return a correct query string fragment in the **WebClientReadFormQueryString** element. 
  
In versions of Exchange earlier than major version 15, the item identifier for the Outlook Web App URLs is an Outlook Web App identifier. If you are targeting a version of Exchange earlier than major version 15, you have to use the [ConvertId operation](convertid-operation.md) to convert the identifier. 
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
