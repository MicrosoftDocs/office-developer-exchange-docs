---
title: "BaseShape"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- BaseShape
api_type:
- schema
ms.assetid: 42c04f3b-abaa-4197-a3d6-d21677ffb1c0
description: "The BaseShape element identifies the set of properties to return in an item or folder response."
---

# BaseShape

The **BaseShape** element identifies the set of properties to return in an item or folder response. 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 **DefaultShapeNamesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.<br/><br/>The following are the XPath expressions to this element:<br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.<br/><br/>The following are the XPath expressions to this element:<br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## Text value

A text value is required. The following table lists the possible text values.
  
**Text values for the BaseShape element**

|**Value**|**Description**|
|:-----|:-----|
|IdOnly  <br/> |Returns only the item or folder ID.  <br/> |
|Default  <br/> |Returns a set of properties that are defined as the default for the item or folder.  <br/> |
|AllProperties  <br/> |Returns all the properties used by the Exchange Business Logic layer to construct a folder.  <br/> |
   
The following table lists the default properties that are returned for a FindFolder request. All subfolders of a given folder are returned in order by name.
  
**Default properties**

|**Folder**|**Default Properties**|
|:-----|:-----|
|Inbox  <br/> |FolderId, display name, unread count, total count, subfolder count  <br/> |
|Contacts  <br/> |FolderId, display name, total count, subfolder count  <br/> |
|Calendar  <br/> |FolderId, display name, subfolder count  <br/> |
|Drafts  <br/> |FolderId, display name, unread count, total count, subfolder count  <br/> |
|Deleted items  <br/> |FolderId, display name, unread count, total count, subfolder count  <br/> |
|Other folders  <br/> |FolderId, display name, unread count, total count, subfolder count  <br/> |
|Outbox  <br/> |FolderId, display name, unread count, total count, subfolder count  <br/> |
|Tasks  <br/> |FolderId, display name, past due count, total count, subfolder count  <br/> |
|Notes  <br/> |FolderId, display name, total count, subfolder count  <br/> |
   
## Remarks

To return properties in addition to those identified by the [BaseShape](baseshape.md) element, use the [AdditionalProperties](additionalproperties.md) element. 
  
## Example

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [FolderShape](foldershape.md)
- [ItemShape](itemshape.md)

