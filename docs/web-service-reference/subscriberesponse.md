---
title: "SubscribeResponse"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SubscribeResponse
api_type:
- schema
ms.assetid: fd87e9b7-c231-44fa-9f5b-19ae96cda5cc
description: "The SubscribeResponse element defines a response to a Subscribe request."
---

# SubscribeResponse

The **SubscribeResponse** element defines a response to a Subscribe request. 
  
[SubscribeResponse](subscriberesponse.md)
  
```xml
<SubscribeResponse>
   <ResponseMessages/>
</SubscribeResponse>
```

 **SubscribeResponseType**
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

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |True  <br/> |
   
## See also

- [Subscribe operation](subscribe-operation.md)