---
title: "DeliveryReportEnabled (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
ms.assetid: 2ab522bc-40ea-4e43-aa57-6d2562db35e9
description: "The DeliveryReportEnabled element represents the DeliveryReportEnabled() flag. The DeliveryReportEnabled element is for internal use only. This element is not used by clients."
---

# DeliveryReportEnabled (SOAP)

The **DeliveryReportEnabled** element represents the **DeliveryReportEnabled()** flag. The **DeliveryReportEnabled** element is for internal use only. This element is not used by clients. 
  
```XML
<DeliveryReportEnabled>true | false</DeliveryReportEnabled>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Represents a list of organization relationships for a single organization.  <br/> |
   
## Text value

A text value of true for the DeliveryReportEnabled element indicates that the delivery reports from users in the organization can be used. A value of false indicates that the delivery reports should suppressed.
  
## Remarks

Use this element to allow or suppress delivery reports from the server.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

