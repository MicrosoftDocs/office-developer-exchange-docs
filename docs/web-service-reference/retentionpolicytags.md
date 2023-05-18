---
title: "RetentionPolicyTags"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 8ed4a48a-d510-4cbe-a172-145c33ffb297
description: "The RetentionPolicyTags element contains a list of retention tags returned in the response of the GetUserRetentionPolicyTags WSDL operation."
---

# RetentionPolicyTags

The **RetentionPolicyTags** element contains a list of retention tags returned in the response of the **GetUserRetentionPolicyTags** WSDL operation. 
  
```XML
<RetentionPolicyTags>
   <RetentionPolicyTag/>
</RetentionPolicyTags>
```

 **ArrayOfRetentionPolicyTagsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[RetentionPolicyTag](retentionpolicytag.md)
  
### Parent elements

[GetUserRetentionPolicyTagsResponse](getuserretentionpolicytagsresponse.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |messages.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

