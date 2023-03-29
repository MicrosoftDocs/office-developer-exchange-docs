---
title: "Request (GetOrganizationRelationship) (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 85dc155c-fad0-4756-b9a8-dedf5040a7c6
description: "The Request element represents a GetOrganizationRelationshipSettingsRequest (SOAP) request. The Request element is for internal use only. This element is not used by clients."
 
 
---

# Request (GetOrganizationRelationship) (SOAP)

The **Request** element represents a [GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) request. The **Request** element is for internal use only. This element is not used by clients. 
  
```XML
<Request>
   <Domains/>
</Request>
```

 **GetOrganizationRelationshipSettingsRequest**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Domains (SOAP)](domains-soap.md) <br/> |Represents the domains for which Autodiscover is to be run and that are to be used in a query.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetOrganizationRelationshipSettingsRequestMessage (SOAP)](getorganizationrelationshipsettingsrequestmessage-soap.md) <br/> |Represents a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation request.  <br/> |
   
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



[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md)


[Working with Autodiscover](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

