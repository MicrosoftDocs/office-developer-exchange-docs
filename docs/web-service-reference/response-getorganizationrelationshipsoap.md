---
title: "Response (GetOrganizationRelationship) (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: e6bbe800-3cbc-48b2-87b3-2043f575e88b
description: "The Response element contains the GetOrganizationRelationshipSettings operation (SOAP) response information. The Response element is for internal use only. This element is not used by clients."
 
 
---

# Response (GetOrganizationRelationship) (SOAP)

The **Response** element contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response information. The **Response** element is for internal use only. This element is not used by clients. 
  
```XML
<GetOrganizationRelationshipSettingsResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <OrganizationRelationshipSettingsCollection/>
</GetOrganizationRelationshipSettingResponse>
```

 **GetOrganizationRelationshipSettingsResponse**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Represents an error code that is returned by the Autodiscover service.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Represents a message that is associated with an error code that is returned by the Autodiscover service.  <br/> |
|[OrganizationRelationshipSettingsCollection (SOAP)](organizationrelationshipsettingscollection-soap.md) <br/> |Represents a list of organization relationships that match the query.  <br/> |
   
### Parent elements

None.
  
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



[GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

