---
title: "AddBlankTargetToLinks"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 30180298-2501-4369-9b8f-2f7663f02336
description: "The AddBlankTargetToLinks element specifies that the target attribute in HTML links are set to open a new window."
---

# AddBlankTargetToLinks

The **AddBlankTargetToLinks** element specifies that the target attribute in HTML links are set to open a new window. 
  
```XML
<AddBlankTargetToLinks> true | false </AddBlankTargetToLinks>
```

**xs:Boolean**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> | Identifies the item properties and content to include in a **GetItem**, **FindItem**, **GetConversationItems** or **SyncFolderItems** response.<br/><br/>  The following are the XPath expressions to this element:<br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/>  `/GetConversationItems/ItemShape` <br/> |
   
## Text value

A text value of **true** for the **AddBlankTargetToLinks** element indicates that all HTML links will be set to open a new window. A value of **false** indicates that HTML links will open in the current window. 
  
## Remarks

This element is optional.
  
This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Element**|**Example**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

