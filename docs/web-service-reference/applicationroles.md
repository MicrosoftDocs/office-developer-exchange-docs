---
title: "ApplicationRoles"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 00003b9b-f8f1-4452-a0af-157f789f8892
description: "The ApplicationRoles element specifies the application roles that the calling partner application uses for the current call."
---

# ApplicationRoles

The **ApplicationRoles** element specifies the application roles that the calling partner application uses for the current call. 
  
```XML
<ApplicationRoles>
    <Role></Role>
</ApplicationRoles>
```

 **NonEmptyArrayOfRoleType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Role](role.md) <br/> |Specifies a string that represents a management role.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ManagementRole](managementrole.md) <br/> |Specifies the management role.  <br/> |
   
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

