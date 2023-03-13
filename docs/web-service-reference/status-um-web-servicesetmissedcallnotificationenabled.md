---
title: "Status (UM web service - SetMissedCallNotificationEnabled)"
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
ms.assetid: e272d905-1a66-44f6-bb1d-59fa9e4d8dea
description: "The Status element defines the value to use in a SetMissedCallNotificationEnabled operation (UM web service) request."
 
 
---

# Status (UM web service - SetMissedCallNotificationEnabled)

The **Status** element defines the value to use in a [SetMissedCallNotificationEnabled operation (UM web service)](setmissedcallnotificationenabled-operation-um-web-service.md) request. 
  
[SetMissedCallNotificationEnabled (UM web service)](setmissedcallnotificationenabled-um-web-service.md)
  
[Status (UM web service - SetMissedCallNotificationEnabled)](status-um-web-servicesetmissedcallnotificationenabled.md)
  
```xml
<SetMissedCallNotificationEnabled>
  <status/>
</SetMissedCallNotificationEnabled>
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
|SetMissedCallNotificationEnabled  <br/> |Defines a request for a [SetMissedCallNotificationEnabled operation (UM web service)](setmissedcallnotificationenabled-operation-um-web-service.md) request.  <br/> |
   
## Text value

A Boolean text value is required. The following are the possible values:
  
- True
    
- False
    
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[SetMissedCallNotificationEnabled operation (UM web service)](setmissedcallnotificationenabled-operation-um-web-service.md)

