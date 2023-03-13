---
title: "Status (UM web service - SetOofStatus)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- Status
api_type:
- schema
ms.assetid: 893bcff1-ccdc-493f-b366-ce8a68c813bd
description: "The Status element defines the value to use in a SetOofStatus operation (UM web service) request."
 
 
---

# Status (UM web service - SetOofStatus)

The **Status** element defines the value to use in a [SetOofStatus operation (UM web service)](setoofstatus-operation-um-web-service.md) request. 
  
[SetOofStatus (UM web service)](setoofstatus-um-web-service.md)
  
[Status (UM web service - SetOofStatus)](status-um-web-servicesetoofstatus.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SetOofStatus (UM web service)](setoofstatus-um-web-service.md) <br/> |Defines a request to set the Unified Messaging Out of Office (OOF) status for the user who makes the request.  <br/> |
   
## Text value

A Boolean value is required. The following are the possible values:
  
- True
    
- False
    
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[SetOofStatus operation (UM web service)](setoofstatus-operation-um-web-service.md)

