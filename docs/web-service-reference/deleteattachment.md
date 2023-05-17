---
title: "DeleteAttachment"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DeleteAttachment
api_type:
- schema
ms.assetid: 43d0c1cb-92ca-4399-9b3a-acb2b5c22624
description: "The DeleteAttachment element is the root element in a request to delete an attachment from the Exchange store."
---

# DeleteAttachment

The **DeleteAttachment** element is the root element in a request to delete an attachment from the Exchange store. 
  
```xml
<DeleteAttachment>
   <AttachmentIds/>
</DeleteAttachment>
```

**DeleteAttachmentType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AttachmentIds](attachmentids.md) <br/> |Contains an array of attachment identifiers that are used to delete the attachments.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [DeleteAttachment operation](deleteattachment-operation.md)

