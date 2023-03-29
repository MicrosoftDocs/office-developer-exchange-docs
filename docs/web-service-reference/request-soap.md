---
title: "Request (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 75696436-997e-49f1-a31b-eb9a8c3526f3
description: "The Request element contains the requested configuration settings and the target users."
 
 
---

# Request (SOAP)

The **Request** element contains the requested configuration settings and the target users. 
  
```XML
<Request>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</Request>
```

 **GetUserSettingsRequest**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Users (SOAP)](users-soap.md) <br/> |Represents a collection of e-mail addresses of the users for whom settings should be retrieved.  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Contains the names of the requested configuration settings.  <br/> |
|[RequestedVersion (SOAP)](requestedversion-soap.md) <br/> |Specifies the specific server version that the provider would like to use.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetUserSettingsRequestMessage (SOAP)](getusersettingsrequestmessage-soap.md) <br/> |Represents a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.  <br/> |
   
## Text value

None.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)

