---
title: "EditAllowed"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: e63c4f7e-77c0-4826-b4e2-43b795d03914
description: "The EditAllowed element specifies whether Information Rights Management can be edited."
---

# EditAllowed

The **EditAllowed** element specifies whether Information Rights Management can be edited. 
  
```XML
<EditAllowed> true | false </EditAllowed>
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

A text value of **true** for the **EditAllowed** element indicates that Information Rights Management (IRM) can be edited. A value of **false** indicates that IRM cannot be edited. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
