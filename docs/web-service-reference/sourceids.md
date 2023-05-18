---
title: "SourceIds"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SourceIds
api_type:
- schema
ms.assetid: 0043abd5-ba9c-4d67-8832-325f32bf7651
description: "The SourceIds element contains the source identifiers to convert."
---

# SourceIds

The **SourceIds** element contains the source identifiers to convert. 
  
[ConvertId](convertid.md)
  
[SourceIds](sourceids.md)
  
```xml
<SourceIds>
   <AlternateId/>
   <AlternatePublicFolderId/>
   <AlternatePublicFolderItemId/>
</SourceIds>
```

 **NonEmptyArrayOfAlternateIdsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AlternateId](alternateid.md) <br/> |Describes an item or folder identifier to convert.  <br/> |
|[AlternatePublicFolderId](alternatepublicfolderid.md) <br/> |Describes a public folder identifier to convert.  <br/> |
|[AlternatePublicFolderItemId](alternatepublicfolderitemid.md) <br/> |Describes a public folder item identifier to convert.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ConvertId](convertid.md) <br/> |Defines a request to convert item and folder identifiers between Exchange supported formats.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[ConvertId operation](convertid-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Converting Identifiers](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

