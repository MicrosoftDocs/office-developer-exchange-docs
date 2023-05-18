---
title: "BaseFolderIds"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- BaseFolderIds
api_type:
- schema
ms.assetid: bdaa6093-f960-469a-b338-0e75aaa536c6
description: "The BaseFolderIds element represents the collection of folders that will be mined to determine the contents of a search folder."
---

# BaseFolderIds

The **BaseFolderIds** element represents the collection of folders that will be mined to determine the contents of a search folder. 
  
```xml
<BaseFolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</BaseFolderIds>
```

 **NonEmptyArrayOfBaseFolderIdsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contains the identifier and change key of a folder.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SearchParameters](searchparameters.md) <br/> |Represents the parameters that define a search folder.  <br/> |
   
## Remarks

The **BaseFolderIds** element must contain at least one [FolderId](folderid.md) or [DistinguishedFolderId](distinguishedfolderid.md) element. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

