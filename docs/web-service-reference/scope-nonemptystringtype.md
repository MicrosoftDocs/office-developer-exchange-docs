---
title: "Scope (NonEmptyStringType)"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
api_name:
- Scope
api_type:
- schema
ms.assetid: 7efb6fd9-1615-469e-96f6-0f7846ad9b44
description: "The Scope element specifies the scope of the message tracking report."
---

# Scope (NonEmptyStringType)

The **Scope** element specifies the scope of the message tracking report. 
  
```XML
<Scope>Organization | Forest | Site</Scope>
```

 **NonEmptyStringType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

[FindMessageTrackingReport](findmessagetrackingreport.md) | [GetMessageTrackingReport](getmessagetrackingreport.md)
  
## Text value

The following table lists the possible values for the **Scope** element. 
  
|**Value**|**Description**|
|:-----|:-----|
|Organization  <br/> |The message tracking scopes spans across an organization.  <br/> |
|Forest  <br/> |The message tracking scopes spans across a forest.  <br/> |
|Site  <br/> |The message tracking scopes spans across a site.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

