---
title: "RootItemId"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RootItemId
api_type:
- schema
ms.assetid: f613c705-17ce-48ce-aa64-4dc2cea25e31
description: "The RootItemId element identifies the root item of a deleted attachment."
---

# RootItemId

The **RootItemId** element identifies the root item of a deleted attachment. 
  
[DeleteAttachmentResponse](deleteattachmentresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md)
  
[RootItemId](rootitemid.md)
  
```xml
<RootItemId RootItemId="" RootItemChangeKey="" />
```

 **RootItemIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**RootItemId** <br/> |Identifies the root item of a deleted attachment.  <br/> |
|**RootItemChangeKey** <br/> |Identifies the new change key of the root item of a deleted attachment.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Contains the status and result of a DeleteAttachment request.  <br/> |
   
## Remarks

The **RootItemId** element is only used in DeleteAttachment responses. This identifies the root item identifier, and more importantly, the new change key to the parent item. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[DeleteAttachment](deleteattachment.md)
  
[DeleteAttachment operation](deleteattachment-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

