---
title: "FindFolder"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FindFolder
api_type:
- schema
ms.assetid: b8a59740-d978-454c-9629-a10792385ba0
description: "The FindFolder element defines a request to find folders in a mailbox."
---

# FindFolder

The **FindFolder** element defines a request to find folders in a mailbox. 
  
```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <IndexedPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <FractionalPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

**FindFolderType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Traversal  <br/> |Defines how a search is performed. This attribute is required.  <br/> |
   
#### Traversal attribute values

|**Value**|**Description**|
|:-----|:-----|
|Shallow  <br/> |Instructs the FindFolder operation to search only the identified folder and to return only the folder IDs for items that have not been deleted. This is called a shallow traversal.  <br/> |
|Deep  <br/> |Instructs the FindFolder operation to search in all child folders of the identified parent folder and to return only the folder IDs for items that have not been deleted. This is called a deep traversal.  <br/> |
|SoftDeleted  <br/> |Instructs the FindFolder operation to perform a shallow traversal search for deleted items.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Identifies the folder properties to include in a FindFolder response.  <br/> |
|[IndexedPageFolderView](indexedpagefolderview.md) <br/> |Describes how paged item information is returned in a FindFolder response. This element is optional.  <br/> |
|[FractionalPageFolderView](fractionalpagefolderview.md) <br/> |Describes where the paged view starts and the maximum number of folders returned in a FindFolder request. This element is optional.  <br/> |
|[Restriction](restriction.md) <br/> |Defines a restriction or query that is used to filter folders in a FindFolder operation. This element is optional.  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifies folders for the FindFolder operation to search.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Example

The following example of a FindFolder request shows how to form a request to find all the folders located in an Inbox.
  
```xml
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
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [FindFolder operation](findfolder-operation.md)

