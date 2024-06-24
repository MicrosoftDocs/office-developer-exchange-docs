---
title: "ContentOwner"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: a1741eda-c232-4d89-8abc-50b2627ad29b
description: "The ContentOwner element specifies the name of the content owner."
---

# ContentOwner

The **ContentOwner** element specifies the name of the content owner. 
  
```XML
<ContentOwner></ContentOwner>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RightsManagementLicenseData](rightsmanagementlicensedata.md) <br/> |Specifies information about the rights management license.  <br/> |
   
## Text value

The text value of the ContentOwner element is a string that specifies the expiration date of the content.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

