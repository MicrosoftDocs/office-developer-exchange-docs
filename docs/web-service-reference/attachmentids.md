---
title: "AttachmentIds"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AttachmentIds
api_type:
- schema
ms.assetid: 46ce3ad7-4b20-43ae-8c63-39f1e3c2666b
description: "The AttachmentIds element contains an array of attachment identifiers."
---

# AttachmentIds

The **AttachmentIds** element contains an array of attachment identifiers. 
  
```xml
<AttachmentIds>
   <AttachmentId Id=""/>
</AttachmentIds>
```

 **NonEmptyArrayOfRequestAttachmentIdsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AttachmentId (GetAttachment and DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) <br/> |The element that identifies a single attachment.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DeleteAttachment](deleteattachment.md) <br/> |The element that defines a request to delete an attachment from the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/DeleteAttachment` <br/> |
|[GetAttachment](getattachment.md) <br/> |The element that defines a request to get an attachment from the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/GetAttachment` <br/> |
   
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
- [GetAttachment operation](getattachment-operation.md)

