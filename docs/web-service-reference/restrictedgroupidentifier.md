---
title: "RestrictedGroupIdentifier"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RestrictedGroupIdentifier
api_type:
- schema
ms.assetid: a3ea3c81-9f99-4836-8cb4-2384ea63f093
description: "The RestrictGroupIdentifier element represents the group security identifier (SID) and attributes for a restricted group within a user token."
---

# RestrictedGroupIdentifier

The **RestrictGroupIdentifier** element represents the group security identifier (SID) and attributes for a restricted group within a user token. 
  
```
<RestrictedGroupIdentifier Attributes="">
   <SecurityIdentifier/>
</RestrictedGroupIdentifier>
```

 **SidAndAttributesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Attributes** <br/> |Contains group attributes.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SecurityIdentifier](securityidentifier.md) <br/> |Represents the security descriptor definition language (SDDL) form of a security identifier.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RestrictedGroupSids](restrictedgroupsids.md) <br/> |Represents a collection of restricted groups within a user token. Token serialization is not supported.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

