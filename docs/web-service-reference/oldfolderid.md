---
title: "OldFolderId"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- OldFolderId
api_type:
- schema
ms.assetid: da554a97-ab87-4950-9fc4-26b1972381bb
description: "The OldFolderId element contains the original identifier of a folder that was moved or copied."
---

# OldFolderId

The **OldFolderId** element contains the original identifier of a folder that was moved or copied. 
  
```xml
<OldFolderId Id="" ChangeKey=""/>
```

 **FolderIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Id** <br/> |Contains a string that identifies a folder in the Exchange store. This attribute is required.  <br/> |
|**ChangeKey** <br/> |Contains a string that identifies a version of a folder that is identified by the Id attribute. This attribute is optional. Use this attribute to make sure that the correct version of a folder is used.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CopiedEvent](copiedevent.md) <br/> |Represents an event in which an item or folder is copied.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Represents an event in which an item or folder is moved from one parent folder to another parent folder.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[Subscribe operation](subscribe-operation.md)
  
[GetEvents operation](getevents-operation.md)
  
[Unsubscribe operation](unsubscribe-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

