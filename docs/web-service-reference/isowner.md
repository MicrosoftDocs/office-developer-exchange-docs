---
title: "IsOwner"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: ea0f0afc-32fe-46cb-8530-62a6ce9490f6
description: "The IsOwner element specifies whether the specified email user is the owner."
---

# IsOwner

The **IsOwner** element specifies whether the specified email user is the owner. 
  
```XML
<IsOwner>true | false</IsOwner>
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
|[RightsManagementLicenseData](rightsmanagementlicensedata.md) <br/> |Specifies information about the rights management license.  <br/> |
   
## Text value

A text value of **true** for the **IsOwner** element indicates that the user is the owner of rights issued on an item. A value of **false** indicates that the user is not the owner of rights issued on an item. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

