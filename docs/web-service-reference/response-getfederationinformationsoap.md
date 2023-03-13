---
title: "Response (GetFederationInformation) (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: ca48a4b3-5006-4bb7-973e-d9137ce67e16
description: "The Response element contains the GetFederationInformation operation (SOAP) response information."
 
 
---

# Response (GetFederationInformation) (SOAP)

The **Response** element contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response information. 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <ApplicationUri/>
   <Domains/>
</Response>
```

 **GetFederationInformationResponse**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Represents an error code that is returned by the Autodiscover service.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Represents a message that is associated with an error code that is returned by the Autodiscover service.  <br/> |
|[ApplicationUri (SOAP)](applicationuri-soap.md) <br/> |Defines the location of an application.  <br/> |
|[Domains (SOAP)](domains-soap.md) <br/> |Represents the domain collection the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), or the domains that the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetFederationInformationResponseMessage (SOAP)](getfederationinformationresponsemessage-soap.md) <br/> |Defines a response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.  <br/> |
   
## Text value

None.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md)

