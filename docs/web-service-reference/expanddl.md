---
title: "ExpandDL"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: affe84a5-ad98-4aba-83f4-8732938b763d
description: "The ExpandDL element defines a request to expand a distribution list."
---

# ExpandDL

The **ExpandDL** element defines a request to expand a distribution list. 
  
```xml
<ExpandDL>
   <Mailbox/>
</ExpandDL>
```

 **ExpandDLType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |Identifies a fully resolved e-mail address or a distribution list. This mailbox represents the distribution list to expand.  <br/> |
   
### Parent elements

None.
  
## Remarks

A distribution list expansion will only be performed for a single distribution list. A distribution list expansion is not recursive.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[ExpandDL operation](expanddl-operation.md)

