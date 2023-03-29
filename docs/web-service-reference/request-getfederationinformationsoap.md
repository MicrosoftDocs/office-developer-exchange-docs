---
title: "Request (GetFederationInformation) (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: beeb5371-f57b-4346-9753-035dd42c6bee
description: "The Request element represents a GetFederationInformationRequest (SOAP) request."
 
 
---

# Request (GetFederationInformation) (SOAP)

The **Request** element represents a [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md) request. 
  
```XML
<Request>
   <Domain/>
</Request>
```

 **GetFederationInformationRequest**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Domain (GetFederationInformation) (SOAP)](domain-getfederationinformationsoap.md) <br/> |Identifies the domain that has a federation trust.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetFederationInformationRequestMessage (SOAP)](getfederationinformationrequestmessage-soap.md) <br/> |Prepares a call to the server to request configuration data for the security token service (STS).  <br/> |
   
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[Working with Autodiscover](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

