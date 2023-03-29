---
title: "TokenIssuers (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: "The TokenIssuers elements represents the TokenIssuer (SOAP) collection."
 
 
---

# TokenIssuers (SOAP)

The **TokenIssuers** elements represents the [TokenIssuer (SOAP)](tokenissuer-soap.md) collection. 
  
```XML
<TokenIssuers>
    <TokenIssuer/>
</TokenIssuers>
```

 **TokenIssuers**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[TokenIssuer (SOAP)](tokenissuer-soap.md) <br/> |Specifies the [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md) for the security token service.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |Contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response.  <br/> |
   
## Remarks

The **TokenIssuers** represents a collection of [TokenIssuer (SOAP)](tokenissuer-soap.md) elements to be used in the Autodiscovery. 
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[Autodiscover web service reference for Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[SOAP Autodiscover XML elements for Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

