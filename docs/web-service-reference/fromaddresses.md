---
title: "FromAddresses"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FromAddresses
api_type:
- schema
ms.assetid: b219f315-c20a-4633-af3e-94bd3e4526b6
description: "The FromAddresses element indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply."
---

# FromAddresses

The **FromAddresses** element indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply. 
  
```XML
<FromAddresses>
   <Address/>
</FromAddresses>
```

 **ArrayOfEmailAddressesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Address (EmailAddressType)](address-emailaddresstype.md) <br/> |Represents a fully resolved e-mail address.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Conditions](conditions.md) <br/> |Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.  <br/> |
|[Exceptions](exceptions.md) <br/> |Represents all the available rule exception conditions for an Inbox rule.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Code**|**Value**|
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

