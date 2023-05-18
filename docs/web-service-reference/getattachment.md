---
title: "GetAttachment"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 9443cf96-b451-4530-b868-490dff798673
description: "The GetAttachment element is the root element in a request to get an attachment from the Exchange store."
---

# GetAttachment

The **GetAttachment** element is the root element in a request to get an attachment from the Exchange store. 
  
```xml
<GetAttachment>
   <AttachmentShape/>
   <AttachmentIds/>
</GetAttachment>
```

 **GetAttachmentType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AttachmentShape](attachmentshape.md) <br/> |Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request. This element is optional.  <br/> |
|[AttachmentIds](attachmentids.md) <br/> |Contains an array of attachment identifiers.  <br/> |
   
### Parent elements

None.
  
## Remarks

The [AttachmentShape](attachmentshape.md) element is not required to identify the properties returned in the response. The [GetAttachment operation](getattachment-operation.md) returns the Name, ContentType, ContentId, ContentLocation, and the Content properties for file attachments. For item attachments, the returned properties are the Name, ContentType, ContentId, ContentLocation, and all the attached item's properties. This is equivalent to using the AllProperties base shape in a [GetItem](getitem.md) request. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetAttachment operation](getattachment-operation.md)
  
[GetAttachmentResponse](getattachmentresponse.md)

