---
title: "NormalizedBody"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: "The NormalizedBody element specifies an HTML representation of the Body property of an item as a fragment that can be inserted into another HTML body."
---

# NormalizedBody

The **NormalizedBody** element specifies an HTML representation of the **Body** property of an item as a fragment that can be inserted into another HTML body. 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 **BodyType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|BodyType  <br/> |Indicates the body type. The value of **Text** for the **BodyType** attribute indicates that the body is in plain text form. The value of **HTML** for the **BodyType** attribute indicates that the body is in HTML form. The **BodyType** attribute is required.  <br/> |
|IsTruncated  <br/> |Indicates that the body contents have been truncated. A text value of **false** for the **IsTruncated** attribute indicates that the body contents have not been truncated. The normalized body will be truncated if the normalized body length is longer than the value set in the [MaximumBodySize](maximumbodysize.md) element.  <br/> |
   
### Child elements

None.
  
### Parent elements

[Item](item.md) | [Message](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [Task](task.md) | [PostItem](postitem.md) | [CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md)
  
## Text value

The text value of the **NormalizedBody** element is the normalized body of the item. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

