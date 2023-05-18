---
title: "ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: a7034730-210d-4916-b992-dda342f890f8
description: "The ExtendedProperties element specifies an array of additional properties."
---

# ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)

The **ExtendedProperties** element specifies an array of additional properties. 
  
```XML
<ExtendedProperties>
    <ExtendedProperty/>
</ExtendedProperties>
```

 **NonEmptyArrayOfExtendedPropertyType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ExtendedProperty](extendedproperty.md) <br/> |Identifies extended MAPI properties on folders and items.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ImGroup](imgroup.md) <br/> |Represents an instant messaging group.  <br/> |
|[SearchPreviewItem](searchpreviewitem.md) <br/> |Specifies the first 256 characters of a mailbox item for preview without opening the item.  <br/> |
   
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

