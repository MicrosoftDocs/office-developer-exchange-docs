---
title: "MimeContentUTF8"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 31544c95-5231-4b57-958c-2a689464d29b
description: "The MimeContentUTF8 element contains the UTF-8 MIME stream of an object that is represented in base64Binary format and supports email address internationalization and [RFC6530]."
---

# MimeContentUTF8

The **MimeContentUTF8** element contains the UTF-8 MIME stream of an object that is represented in base64Binary format and supports email address internationalization and [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).
  
```XML
<MimeContentUTF8 CharacterSet="" />
```

 **MimeContentType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**CharacterSet** <br/> |If set, the value for this attribute is ignored by the server.  <br/> |
   
### Child elements

None.
  
### Parent elements

[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)
  
## Text value

A text value that represents a base64binary MIME stream is required if this element is used.
  
## Remarks

The message content goes through the following three levels of encoding before it is stored in the **MimeContentUTF8** value: 
  
1. Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.
    
2. MIME stream — This is the UTF8 encoding of the message text for the **MimeContentUTF8** element, or the ASCII encoding of the message text for the [MimeContent](mimecontent.md) element. 
    
3. XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.
    
Each level is independent of the level that precedes it.
  
The **MimeContentUTF8** element might contain the same data that other properties that are returned with an item contain. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
### Version differences

This element is available in versions of Exchange starting with build 15.00.0986.00.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

