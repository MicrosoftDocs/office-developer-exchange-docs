---
title: "DeleteAttachmentResponse"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DeleteAttachmentResponse
api_type:
- schema
ms.assetid: 24099a88-4ab6-4bf3-8ed5-efec8e07b9b9
description: "The DeleteAttachmentResponse defines a response to a DeleteAttachment request."
---

# DeleteAttachmentResponse

The **DeleteAttachmentResponse** defines a response to a DeleteAttachment request. 
  
```xml
<DeleteAttachmentResponse>
   <ResponseMessages/>
</DeleteAttachmentResponse>
```

**DeleteAttachmentResponseType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services request.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [DeleteAttachment operation](deleteattachment-operation.md)  
- [DeleteAttachment](deleteattachment.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

