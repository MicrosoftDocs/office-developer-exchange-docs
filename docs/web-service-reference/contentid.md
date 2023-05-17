---
title: "ContentId"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ContentId
api_type:
- schema
ms.assetid: bc59100d-6079-414b-a6e0-7c15feaa3184
description: "The ContentId element represents an identifier for the contents of an attachment. ContentId can be set to any string value. Applications can use ContentId to implement their own identification mechanisms."
---

# ContentId

The **ContentId** element represents an identifier for the contents of an attachment. **ContentId** can be set to any string value. Applications can use **ContentId** to implement their own identification mechanisms. 
  
```xml
<ContentId/>
```

 **String**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |Represents an Exchange item that is attached to another Exchange item.  <br/> |
|[FileAttachment](fileattachment.md) <br/> |Represents a file that is attached to an item in the Exchange store.  <br/> |
   
## Text value

The string value represents the identifier to the contents of an attachment.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

