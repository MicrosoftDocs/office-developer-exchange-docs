---
title: "BlockExternalImages"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 5c754dfc-a9e9-4272-9b5f-5fe3db537e62
description: "The BlockExternalImages element specifies whether external images are blocked in HTML text bodies."
---

# BlockExternalImages

The **BlockExternalImages** element specifies whether external images are blocked in HTML text bodies. 
  
```XML
<BlockExternalImages> true | false </BlockExternalImages>
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
|[FolderShape](foldershape.md) <br/> |Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.  <br/> |
|[ItemShape](itemshape.md) <br/> |Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.  <br/> |
   
## Text value

A text value of **true** for **BlockExternalImages** element indicates that external images are blocked in HTML bodies. A value of **false** indicates that external images are allowed. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

