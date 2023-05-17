---
title: "AlternatePublicFolderItemId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AlternatePublicFolderItemId
api_type:
- schema
ms.assetid: a67df9b9-8fdb-42de-b9c5-8377b71fa3d9
description: "The AlternatePublicFolderItemId element describes a public folder item identifier to convert to another identifier format. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# AlternatePublicFolderItemId

The **AlternatePublicFolderItemId** element describes a public folder item identifier to convert to another identifier format. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
- [ConvertId](convertid.md)
  
- [SourceIds](sourceids.md)
  
- [AlternatePublicFolderItemId](alternatepublicfolderitemid.md)
  
```xml
<AlternatePublicFolderItemId FolderId="" Format="" ItemId=""/>
```

 **AlternatePublicFolderItemIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|FolderId  <br/> |Identifies the public folder that contains the public folder item. This attribute is required.  <br/> |
|Format  <br/> |Identifies the format that describes the public folder item identifier to convert. This attribute is required.  <br/> |
|ItemId  <br/> |Identifier the public folder item to convert. This attribute is required.  <br/> |
   
#### Format attribute values

|**Value**|**Description**|
|:-----|:-----|
|EwsLegacyId  <br/> |Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.  <br/> |
|EwsId  <br/> |Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.  <br/> |
|EntryId  <br/> |Describes MAPI identifiers, as in the PR_ENTRYID property.  <br/> |
|HexEntryId  <br/> |Describes a hexadecimal-encoded representation of the PR_ENTRYID property. This is the format of availability calendar event identifiers.  <br/> |
|StoreId  <br/> |Describes Exchange store identifiers.  <br/> |
|OwaId  <br/> |Describes an Outlook Web Access identifier.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |Contains the source identifiers to convert. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [ConvertId operation](convertid-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
- [Converting Identifiers](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

