---
title: "IsMembershipGroup"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 0dc3e285-8f49-48ad-b844-37041c0d782b
description: "The IsMembershipGroup element specifies a Boolean value that indicates whether the entity is a distribution group or a mailbox."
---

# IsMembershipGroup

The **IsMembershipGroup** element specifies a Boolean value that indicates whether the entity is a distribution group or a mailbox. 
  
```XML
<IsMembershipGroup>true | false</IsMembershipGroup>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SearchableMailbox](searchablemailbox.md) <br/> |Specifies a mailbox returned from a **GetSearchableMailboxes** request.  <br/> |
   
## Text value

A text value of **true** for the **IsMembershipGroup** element indicates that the entity is a distribution group or a mailbox. A value of false indicates that the entity is not a distribution group or a mailbox. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

