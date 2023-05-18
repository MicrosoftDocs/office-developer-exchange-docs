---
title: "UserParameters"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: bad7311f-7ecd-4f0c-b8e7-dd8f7d378f55
description: "The UserParameters element contains a list of enabled and disabled client extensions."
---

# UserParameters

The **UserParameters** element contains a list of enabled and disabled client extensions. 
  
```XML
<UserParameters UserId="" EnabledOnly="">
   <UserEnabledExtensions/>
   <UserDisabledExtensions/>
</UserParameters>
```

 **GetClientExtensionUserParametersType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|UserId  <br/> |The text value of the **UserId** attribute is the identifier of the user.  <br/> |
|EnabledOnly  <br/> |The text value of the **EnabledOnly** indicates whether the response only contains the enabled extensions.  <br/> |
   
### Child elements

[UserEnabledExtensions](userenabledextensions.md) | [UserDisabledExtensions](userdisabledextensions.md)
  
### Parent elements

[GetClientExtension](getclientextension.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
