---
title: "AttachmentId (GetAttachment and DeleteAttachment)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AttachmentId
api_type:
- schema
ms.assetid: 4bea1cb5-0a0f-4e14-9b09-f91af8cf9899
description: "The AttachmentId element identifies a single attachment."
---

# AttachmentId (GetAttachment and DeleteAttachment)

The **AttachmentId** element identifies a single attachment. 
  
```xml
<AttachmentId Id="" />
```

 **RequestAttachmentIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Id** <br/> |Specifies the attachment identifier.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AttachmentIds](attachmentids.md) <br/> | Contains an array of attachment identifiers.<br/><br/>  The following are the XPath expressions to this element:<br/><br/>`/DeleteAttachment/AttachmentIds`<br/><br/>`/GetAttachment/AttachmentIds` <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [DeleteAttachment operation](deleteattachment-operation.md)
- [GetAttachment operation](getattachment-operation.md)

