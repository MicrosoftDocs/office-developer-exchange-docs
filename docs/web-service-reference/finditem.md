---
title: "FindItem"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FindItem
api_type:
- schema
ms.assetid: f7624f5c-c390-4563-ab9a-08f1024fb914
description: "The FindItem element defines a request to find items in a mailbox."
---

# FindItem

The **FindItem** element defines a request to find items in a mailbox. 
  
```xml
<FindItem Traversal="">
   <ItemShape/>
   <IndexedPageItemView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <IndexedPageItemView/>
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <ContactsView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <ContactsView/> 
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <CalendarView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <FractionalPageItemView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <FractionalPageItemView/>
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```


**FindItemType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Traversal** <br/> |Defines whether the search finds items in folders or the folders' dumpsters. This attribute is required.  <br/> |
   
#### Traversal attribute values

|**Value**|**Description**|
|:-----|:-----|
|Shallow  <br/> |Returns only the identities of items in the folder.  <br/> |
|SoftDeleted  <br/> |Returns only the identities of items that are in a folder's dumpster. Note that a soft-deleted traversal combined with a search restriction will result in zero items returned even if there are items that match the search criteria.  <br/> |
|Associated  <br/> |Returns only the identities of associated items in the folder.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifies the item properties and content to include in a [FindItem operation](finditem-operation.md) response.  <br/> |
|[IndexedPageItemView](indexedpageitemview.md) <br/> |Describes how paged item information is returned for a **FindItem** request. This element is optional.  <br/> |
|[FractionalPageItemView](fractionalpageitemview.md) <br/> |Describes where the paged view starts and the maximum number of items returned in a **FindItem** request. The paged view offset from the beginning of the set of found items is described by a fraction. This element is optional.  <br/> |
|[CalendarView](calendarview.md) <br/> |Provides time span limits to define a search for calendar items. This element is optional.  <br/> |
|[ContactsView](contactsview.md) <br/> |Defines a search for contact items based on alphabetical display names. This element is optional.  <br/> |
|[GroupBy](groupby.md) <br/> |Specifies arbitrary groupings for **FindItem** queries. This element is optional.  <br/> |
|[DistinguishedGroupBy](distinguishedgroupby.md) <br/> |Provides standard groupings for **FindItem** queries. This element is optional.  <br/> |
|[Restriction](restriction.md) <br/> |Defines the restriction or query that is used to filter items or folders in **FindItem**/ **FindFolder** and search folder operations. This element is optional.  <br/> |
|[SortOrder](sortorder.md) <br/> |Defines how items are sorted in a FindItem request. This element is optional.  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifies folders to search for the FindItem and FindFolder operations.  <br/> |
|[QueryString (QueryStringType)](querystring-querystringtype.md) <br/> |Contains a mailbox query string based on Advanced Query Syntax (AQS).  <br/> |
   
### Parent elements

None.
  
## Remarks

Only one of the [IndexedPageItemView](indexedpageitemview.md), [FractionalPageItemView](fractionalpageitemview.md), [CalendarView](calendarview.md), or [ContactsView](contactsview.md) elements can be included in a **FindItem** request. Only one of the [GroupBy](groupby.md) or [DistinguishedGroupBy](distinguishedgroupby.md) elements can be included in a **FindItem** request. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [FindItem operation](finditem-operation.md)
- [Finding Items](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

