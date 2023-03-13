---
title: "PlayOnPhone (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 206a2ad1-a01d-4e71-99a1-90c2530423da
description: "The PlayOnPhone element defines a request to play an item on a telephone."
 
 
---

# PlayOnPhone (UM web service)

The **PlayOnPhone** element defines a request to play an item on a telephone. 
  
[PlayOnPhone (UM web service)](playonphone-um-web-service.md)
  
```xml
<PlayOnPhone>
  <entryId>   </entryId>
  <DialString>   </DialString>
</PlayOnPhone>
```

 **complexType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[entryId (UM web service)](entryid-um-web-service.md) <br/> |Contains the value that represents the identifier of the item to play on the telephone in a [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) request.  <br/> |
|[dialString (UM web service)](dialstring-um-web-service.md) <br/> |Contains the value for the telephone number to dial.  <br/> |
   
### Parent elements

None.
  
## Text value

None.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md)
