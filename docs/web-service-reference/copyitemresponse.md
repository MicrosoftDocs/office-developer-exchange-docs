---
title: "CopyItemResponse"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CopyItemResponse
api_type:
- schema
ms.assetid: ae402bc1-4589-45e0-a929-f368c916a7e4
description: "The CopyItemResponse element defines a response to a CopyItem request."
---

# CopyItemResponse

The **CopyItemResponse** element defines a response to a CopyItem request. 
  
```xml
<CopyItemResponse>
   <ResponseMessages/>
</CopyItemResponse>
```

 **CopyItemResponseType**
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



[CopyItem operation](copyitem-operation.md)
  
[CopyItem](copyitem.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

