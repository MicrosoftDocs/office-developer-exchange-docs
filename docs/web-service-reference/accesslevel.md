---
title: "AccessLevel"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 09475586-00fa-4e82-a915-5ca263ab4d1c
description: "The AccessLevel element specifies the access level for an online meeting."
---

# AccessLevel

The **AccessLevel** element specifies the access level for an online meeting. 
  
```XML
<AccessLevel/>
```

 **OnlineMeetingSettingsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[OnlineMeetingSettings](onlinemeetingsettings.md) <br/> |Specifies the settings for online meetings.  <br/> |
   
## Text value

The following table lists the text values for the **AccessLevel** element. 
  
**AccessLevel element text values**

|**Value**|**Description**|
|:-----|:-----|
|Everyone  <br/> |The access level is open to all.  <br/> |
|Internal  <br/> |The access level is internal only.  <br/> |
|Invited  <br/> |The access level is invited participants only.  <br/> |
|Locked  <br/> |The access level is locked.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
This element was introduced in Exchange Server 2013.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Type schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

