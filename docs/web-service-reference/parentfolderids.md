---
title: "ParentFolderIds"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ParentFolderIds
api_type:
- schema
ms.assetid: e7998023-e5e0-465c-91fa-2aa6d1559f64
description: "The ParentFolderIds element identifies folders for the FindItem and FindFolder operations to search."
---

# ParentFolderIds

The **ParentFolderIds** element identifies folders for the FindItem and FindFolder operations to search. 
  
```xml
<ParentFolderIds>
   <DistinguishedFolderId/>
<ParentFolderIds>
```

```xml
<ParentFolderIds>
   <FolderId/> 
<ParentFolderIds>
```

**NonEmptyArrayOfBaseFolderIdsType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contains the identifier and change key of a folder. The **ParentFolderIds** element must use either this element or the [DistinguishedFolderId](distinguishedfolderid.md) element.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifies Microsoft Exchange Server 2007 folders that can be referenced by name. The **ParentFolderIds** element must use either this element or the [FolderId](folderid.md) element.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Defines a request to identify folders in a mailbox.  <br/> |
|[FindItem](finditem.md) <br/> |Defines a request to find items in a mailbox.  <br/> |
|[ResolveNames](resolvenames.md) <br/> |Defines a request to resolve ambiguous names.  <br/> |
   
## Remarks

The **ParentFolderIds** element must use either the [FolderId](folderid.md) or the [DistinguishedFolderId](distinguishedfolderid.md) element. An unlimited number of folders can be defined for the search. 
  
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

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [FindFolder operation](findfolder-operation.md)  
- [FindItem operation](finditem-operation.md) 
- [ResolveNames operation](resolvenames-operation.md)

