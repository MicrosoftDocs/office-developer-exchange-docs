---
title: "UnifiedMessagingConfiguration"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- UnifiedMessagingConfiguration
api_type:
- schema
ms.assetid: cbdb4268-077e-44ed-8ec2-9d759c84cc6d
description: "The UnifiedMessagingConfiguration element contains service configuration information for the Unified Messaging service."
---

# UnifiedMessagingConfiguration

The **UnifiedMessagingConfiguration** element contains service configuration information for the Unified Messaging service. 
  
```XML
<UnifiedMessagingConfiguration>
   <UmEnabled/>
   <PlayOnPhoneDialString/>
   <PlayOnPhoneEnabled/>
</UnifiedMessagingConfiguration>
```

 **UnifiedMessageServiceConfiguration**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[UmEnabled](umenabled.md) <br/> |Indicates whether Unified Messaging is enabled for an account. This element is required.  <br/> |
|[PlayOnPhoneDialString (Exchange Web Services)](playonphonedialstring-exchange-web-services.md) <br/> |Identifies the Play-on-Phone dial string. This element is required.  <br/> |
|[PlayOnPhoneEnabled](playonphoneenabled.md) <br/> |Indicates whether the Play-on-Phone feature is enabled. This element is required.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contains service configuration settings.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

