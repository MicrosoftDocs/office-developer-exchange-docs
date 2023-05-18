---
title: "ParentId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: bb7aaa46-3a04-4197-aebb-8881ff10603f
description: "The ParentId element specifies the identifier of the parent item in a search preview."
---

# ParentId

The **ParentId** element specifies the identifier of the parent item in a search preview. 
  
```XML
<ParentId Id="" ChangeKey=""/>
```

**ItemIdType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |The text value of the **Id** attribute is the identifier of the parent item.  <br/> |
|ChangeKey  <br/> |The text value of the **ChangeKey** attribute is the change key of the parent item.  <br/> |
   
### Child elements

None.
  
### Parent elements

[SearchPreviewItem](searchpreviewitem.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |true  <br/> |
   

