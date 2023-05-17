---
title: "GetItemResponse"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GetItemResponse
api_type:
- schema
ms.assetid: 8b66de1b-26a6-476c-9585-a96059125716
description: "The GetItemResponse element defines a response to a GetItem request."
---

# GetItemResponse

The **GetItemResponse** element defines a response to a GetItem request. 
  
```xml
<GetItemResponse>
   <ResponseMessages/>
</GetItemResponse>
```

 **GetItemResponseType**
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

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[GetItem](getitem.md)
  
[GetItemResponseMessage](getitemresponsemessage.md)
  
[GetItem operation](getitem-operation.md)

