---
title: "RequestedVersion (SOAP)"
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 962036c9-9b13-4669-bed2-2502c0f5aabe
description: "The RequestedVersion element specifies the minimum service version that the client wants the request to be processed on."
 
 
---

# RequestedVersion (SOAP)

The **RequestedVersion** element specifies the minimum service version that the client wants the request to be processed on. 
  
```XML
<RequestedVersion/>
```

 **ExchangeVersion**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Request (SOAP)](request-soap.md) <br/> |Contains the requested configuration settings and the target users.  <br/> |
|[Request (GetDomainSettings) (SOAP)](request-getdomainsettingssoap.md) <br/> |Represents a request to get domain settings.  <br/> |
   
## Text value

The text value for the **RequestedVersion** element can be Exchange2010, Exchange2010_SP1, Exchange2010_SP2, or Exchange2013.
  
## Remarks

If this element is not present, the latest service version is used.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)

