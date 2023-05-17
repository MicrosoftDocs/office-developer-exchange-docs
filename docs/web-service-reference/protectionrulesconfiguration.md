---
title: "ProtectionRulesConfiguration"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ProtectionRulesConfiguration
api_type:
- schema
ms.assetid: e5b4699a-476e-4053-bb52-873eb921c046
description: "The ProtectionRulesConfiguration element contains service configuration information for the protection rules service."
---

# ProtectionRulesConfiguration

The **ProtectionRulesConfiguration** element contains service configuration information for the protection rules service. 
  
```XML
<ProtectionRulesConfiguration RefreshInterval="">
   <Rules/>
   <InternalDomains/>
</ProtectionRulesConfiguration>
```

 **ProtectionRulesServiceConfiguration**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**RefreshInterval** <br/> |Specifies how often, in whole hours, the client should request protection rules from the server. This attribute is required and its value must be an integer that is equal to or greater than 1.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Rules ](rules-ex15websvcsotherref.md) <br/> |An array of protection rules. This element is required.  <br/> |
|[InternalDomains (SmtpDomainList)](internaldomains-smtpdomainlist.md) <br/> |Identifies the list of internal SMTP domains of the organization. This element is required.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contains service configuration settings.  <br/> |
   
## Text value

None.
  
## Remarks

The protection rules service configuration is comprised of a list of rules, internal domains, and a refresh interval.
  
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

