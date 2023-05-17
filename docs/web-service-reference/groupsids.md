---
title: "GroupSids" 
manager: lindalu
ms.date: 03/22/2022
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GroupSids
api_type:
- schema
ms.assetid: ebb00653-83f0-4080-a902-c38df6719800
description: "The GroupSids element represents a collection of Active Directory directory service group object security identifiers."
---

# GroupSids

The **GroupSids** element represents a collection of Active Directory directory service group object security identifiers. 
  
```xml
<GroupSids>
   <GroupIdentifier/>
</GroupSids>
```

 **NonEmptyArrayOfGroupIdentifiersType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.

### Attributes

None.

### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[GroupIdentifier](groupidentifier.md) <br/> |Represents a single security identifier and attribute for an Active Directory object group of which the account is a member.  <br/> |
 
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SerializedSecurityContext](serializedsecuritycontext.md) <br/> |Used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication. Token serialization is not supported.  <br/> |
 
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.

## Element information

|**Element**|**Example**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
 
## See also

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
