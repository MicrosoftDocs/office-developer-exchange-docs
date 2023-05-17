---
title: "IndexedPageFolderView"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- IndexedPageFolderView
api_type:
- schema
ms.assetid: c6dac232-244b-4db0-9a15-5e01b8aa7a7d
description: "The IndexedPageFolderView element describes how paged item information is returned in a FindFolder response."
---

# IndexedPageFolderView

The **IndexedPageFolderView** element describes how paged item information is returned in a [FindFolder](findfolder.md) response. 
  
[FindFolder](findfolder.md)
  
[IndexedPageFolderView](indexedpagefolderview.md)
  
```xml
<IndexedPageFolderView MaxEntriesReturned="" Offset="" BasePoint="" />
```

 **IndexedPageViewType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Describes the maximum number of folders to return in the response. This attribute is optional.  <br/> |
|**Offset** <br/> |Describes the offset from the **BasePoint**. Offset must be greater than or equal to zero. If **BasePoint** is equal to Beginning, the offset is positive. If **BasePoint** is equal to End, the offset is handled as if it were negative.  <br/> This identifies which folder will be the first folder delivered in the response. This attribute is required.  <br/> |
|**BasePoint** <br/> |Describes whether the page of folders will start from the start or the end of the set of folders that are found with the search criteria. Seeking from the end always searches backward. This attribute is required.  <br/> |
   
#### BasePoint Attribute

|**Value**|**Description**|
|:-----|:-----|
|Beginning  <br/> |The paged view starts at the beginning of the found folder set.  <br/> |
|End  <br/> |The paged view starts at the end of the found folder set.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Defines a request to find folders in a mailbox.  <br/> The following is the XPath expression to this element:  <br/>  `/FindFolder` <br/> |
   
## Remarks

Seeking from end involves moving to the origin identified by the offset. Additionally, the pointer is moved back by the number of requested records. For example, if there are 100 records and the offset is 25 from the end, the search starts from 75. If 10 records are returned, the pointer is moved backward an additional 10 records to 65 and returns records 65 through 75. The next index is 64. The next offset from the end for a page is 100 minus 64 which equals 36. The value for the next offset from the end to get the next indexed page is 36.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   

