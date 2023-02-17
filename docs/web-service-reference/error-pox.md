---
title: "Error (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 91c63b62-ab68-4c32-a2f7-5a87c188335b
description: "The Error element contains an Autodiscover error response."
 
 
---

# Error (POX)

The **Error** element contains an Autodiscover error response. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Error (POX)](error-pox.md)
  
```xml
<Error Time="" Id="">
   <ErrorCode/>
   <Message/>
   <DebugData/>
</Error>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Time  <br/> |Represents the time when the error response was returned.  <br/> |
|Id  <br/> |Represents a hash of the name of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ErrorCode (POX)](errorcode-pox.md) <br/> |Contains the error code for an error Autodiscover response.  <br/> |
|[Message (POX)](message-pox.md) <br/> |Contains the error message for an error Autodiscover response.  <br/> |
|[DebugData (POX)](debugdata-pox.md) <br/> |Contains the debug data for an error Autodiscover response.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Account (POX)](account-pox.md) <br/> |Contains an Autodiscover error response.  <br/> |
   
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

