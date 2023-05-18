---
title: "ReplyBody"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ReplyBody
api_type:
- schema
ms.assetid: bb184144-3e4b-4419-a883-cc9fab1085e6
description: "The ReplyBody element contains an Out of Office (OOF) message and the language used for the message."
---

# ReplyBody

The **ReplyBody** element contains an Out of Office (OOF) message and the language used for the message. 
  
```XML
<ReplyBody xml:lang="">
   <Message/>
</ReplyBody>
```

 **ReplyBody**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|xml:lang  <br/> |Specifies the language used in the **ReplyBody** contents. This attribute is optional. The possible values of this attribute are defined by IETF RFC 3066.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Message (Availability)](message-availability.md) <br/> |Contains the out of office (OOF) response.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[OutOfOffice](outofoffice.md) <br/> |Defines the OOF response message and a duration time for sending the response message for a mailbox.  <br/> |
   
## Text value

None.
  
## Remarks

This element is required.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

