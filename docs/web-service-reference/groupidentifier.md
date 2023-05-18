---
title: "GroupIdentifier"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GroupIdentifier
api_type:
- schema
ms.assetid: bdc6fc1e-4979-42da-a35b-e3017988c7d3
description: "The GroupIdentifier element represents a single security identifier and attribute for an Active Directory directory service object group of which the account is a member."
---

# GroupIdentifier

The **GroupIdentifier** element represents a single security identifier and attribute for an Active Directory directory service object group of which the account is a member. 
  
```xml
<GroupIdentifier>
   <SecurityIdentifier/>
</GroupIdentifier>
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
|[SecurityIdentifier](securityidentifier.md) <br/> |Represents the security descriptor definition language (SDDL) form of a security identifier ([SID](sid.md)) that represents the group.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GroupSids](groupsids.md) <br/> |Represents a collection of Active Directory group object security identifiers that make up an account token for token serialization. Token serialization is not supported.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|Element|Type|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

