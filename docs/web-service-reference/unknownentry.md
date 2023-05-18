---
title: "UnknownEntry"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- UnknownEntry
api_type:
- schema
ms.assetid: 3cb4c62e-052a-4326-8639-8c41dfd047b2
description: "The UnknownEntry element represents a single unknown permission entry that cannot be resolved against the Active Directory directory service. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# UnknownEntry

The **UnknownEntry** element represents a single unknown permission entry that cannot be resolved against the Active Directory directory service. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<UnknownEntry/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[UnknownEntries](unknownentries.md) <br/> |Contains an array of unknown permission entries that cannot be resolved against Active Directory. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Text value

The text value represents a permission entry that cannot be resolved against Active Directory. The text value represents a security identifier (SID).
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

