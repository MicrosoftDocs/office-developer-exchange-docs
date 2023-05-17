---
title: "SearchParameters"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SearchParameters
api_type:
- schema
ms.assetid: 34602cb1-dc33-4552-a98c-3e77f614daa3
description: "The SearchParameters element represents the parameters that define a search folder."
---

# SearchParameters

The **SearchParameters** element represents the parameters that define a search folder. 
  
```xml
<SearchParameters Traversal="">
   <Restriction/>
   <BaseFolderIds/>
</SearchParameters>
```

 **SearchParametersType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Traversal** <br/> |Describes how a search folder traverses the folder hierarchy. The options are for either a **Deep** or a **Shallow** search.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.  <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Represents the collection of folders that will be mined to determine the contents of a search folder.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SearchFolder](searchfolder.md) <br/> |Represents a search folder that is contained in a mailbox.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

