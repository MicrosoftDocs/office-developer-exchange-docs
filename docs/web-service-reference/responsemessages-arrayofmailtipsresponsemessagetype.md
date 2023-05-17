---
title: "ResponseMessages (ArrayOfMailTipsResponseMessageType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: 00878187-fac2-45b9-ba1c-df7ffac71089
description: "The ResponseMessages element represents a list of mail tips response messages."
---

# ResponseMessages (ArrayOfMailTipsResponseMessageType)

The **ResponseMessages** element represents a list of mail tips response messages. 
  
```XML
<ResponseMessages>
   <MailTipsResponseMessageType/>
</ResponseMessages>
```

 **ArrayOfMailTipsResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MailTipsResponseMessageType](mailtipsresponsemessagetype.md) <br/> |Represents mail tips settings.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetMailTipsResponse](getmailtipsresponse.md) <br/> |Represents the response message for the [GetMailTips operation](getmailtips-operation.md).  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetMailTips operation](getmailtips-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

