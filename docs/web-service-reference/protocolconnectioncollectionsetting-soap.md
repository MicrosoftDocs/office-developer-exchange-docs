---
title: "ProtocolConnectionCollectionSetting (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 51f84364-9a5f-4ef2-ba82-f6ef7c65f7cb
description: "The ProtocolConnectionCollectionSetting element represents a collection of server protocol connection settings."
 
 
---

# ProtocolConnectionCollectionSetting (SOAP)

The **ProtocolConnectionCollectionSetting** element represents a collection of server protocol connection settings. 
  
```XML
<ProtocolConnectionCollectionSetting/>
   <Name/>
   <ProtocolConnections/>
</ProtocolConnectionCollectionSetting>
```

 **ProtocolConnectionCollectionSetting**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Name (SOAP)](name-soap.md) <br/> |Represents the name of a setting.  <br/> |
|[ProtocolConnections (SOAP)](protocolconnections-soap.md) <br/> |Contains zero or more protocol connections.  <br/> |
   
### Parent elements

None.
  
## Text value

None.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
  
- [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)
  
- [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md)
