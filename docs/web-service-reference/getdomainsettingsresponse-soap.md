---
title: "GetDomainSettingsResponse (SOAP)"
manager: lindalu
ms.date: 03/22/2022
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 43ebd17b-3a70-4878-9254-97a4c2c87b77
description: "The GetDomainSettingsResponse element represents the response to a GetDomainSettings operation (SOAP), which returns the domain settings."
 
---

# GetDomainSettingsResponse (SOAP)

The **GetDomainSettingsResponse** element represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), which returns the domain settings.

```XML
<GetDomainSettingsResponse>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</GetDomainSettingsResponse>
```

 **GetDomainSettingsResponse**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.

### Attributes

None.

### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |Contains an array of responses for each requested domain's settings.  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Represents an error code that is returned by the Autodiscover service.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Represents a message that is associated with an error code that is returned by the Autodiscover service.  <br/> |
   
### Parent elements

None.

## Text value

None.

## Element information

| **Element** | **Example** |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

[GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)
