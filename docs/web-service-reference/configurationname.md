---
title: "ConfigurationName"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ConfigurationName
api_type:
- schema
ms.assetid: 3b524a2f-9c6b-4550-9f3d-f78d176b0f7b
description: "The ConfigurationName element specifies the requested service configurations by name."
---

# ConfigurationName

The **ConfigurationName** element specifies the requested service configurations by name. 
  
```xml
<ConfigurationName>MailTips or UnifiedMessagingConfiguration or ProtectionRules</ConfigurationName>
```

 **ServiceConfigurationType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RequestedConfiguration](requestedconfiguration.md) <br/> |Contains the requested service configurations.  <br/> |
   
## Text value

The following table lists the possible values for the **ConfigurationName** element. 
  
**ConfigurationName element values**

|**Value**|**Description**|
|:-----|:-----|
|MailTips  <br/> |Identifies the MailTips service configuration.  <br/> |
|UnifiedMessagingConfiguration  <br/> |Identifies the Unified Messaging service configuration.  <br/> |
|ProtectionRules  <br/> |Identifies the Protection Rules service configuration.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

