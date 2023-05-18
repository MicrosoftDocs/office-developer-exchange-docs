---
title: "SavedItemFolderId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SavedItemFolderId
api_type:
- schema
ms.assetid: 4b8b475c-9ca5-48c9-acb0-8848b53be1ce
description: "The SavedItemFolderId element identifies the target folder for operations that update, send, and create items in a mailbox."
---

# SavedItemFolderId

The **SavedItemFolderId** element identifies the target folder for operations that update, send, and create items in a mailbox. 
  
```xml
<SavedItemFolderId>
   <FolderId/>
</SavedItemFolderId>
```

```xml
<SavedItemFolderId>
   <DistinguishedFolderId/>
</SavedItemFolderId>
```

**TargetFolderIdType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contains the identifier and change key of a target folder for operations that update, send, and create items in the Exchange store.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifies a target folder by a named identifier for operations that update, send, and create items in the Exchange store.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CreateItem](createitem.md) <br/> |Defines a request to create an item in the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/CreateItem` <br/> |
|[UpdateItem](updateitem.md) <br/> |Defines a request to update an item in the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/UpdateItem` <br/> |
|[SendItem](senditem.md) <br/> |Defines a request to send an item in the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/SendItem` <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   

