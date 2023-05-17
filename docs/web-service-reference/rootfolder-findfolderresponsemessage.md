---
title: "RootFolder (FindFolderResponseMessage)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 5089c815-663f-46be-bc59-aed9ee20f94a
description: "The RootFolder element contains the results of a search of a single root folder during a FindFolder operation."
---

# RootFolder (FindFolderResponseMessage)

The **RootFolder** element contains the results of a search of a single root folder during a [FindFolder operation](findfolder-operation.md).
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Folders/>
</RootFolder>
```

 **FindFolderParentType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|IndexedPagingOffset  <br/> |Represents the next index that should be used for the next request when using an indexed paging view.  <br/> |
|NumeratorOffset  <br/> |Represents the new numerator value to use for the next request when using fractional page views.  <br/> |
|AbsoluteDenominator  <br/> |Represents the next denominator to use for the next request when doing fractional paging.  <br/> |
|IncludesLastItemInRange  <br/> |Indicates whether the current results contain the last folder in the query, such that further paging is not needed.  <br/> |
|TotalItemsInView  <br/> |Represents the total number of folders that pass the restriction.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Folders](folders-ex15websvcsotherref.md) <br/> |Contains an array of folders found by using the [FindFolder operation](findfolder-operation.md).  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Contains the status and result of a [FindFolder operation](findfolder-operation.md) request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[FindFolder operation](findfolder-operation.md)


[Finding Folders](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

