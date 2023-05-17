---
title: "Data (base64Binary)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Data
api_type:
- schema
ms.assetid: 26d8c2d0-bed2-4aed-b381-20e2ace6892f
description: "The Data element contains the data of a single exported item or an item to upload into a mailbox."
---

# Data (base64Binary)

The **Data** element contains the data of a single exported item or an item to upload into a mailbox. 
  
```XML
<Data/>
```

**xs:base64Binary**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |Contains the status and results of a request to export a single mailbox item.  <br/> |
|[Item (UploadItemType)](item-uploaditemtype.md) <br/> |Represents a single item to upload into a mailbox.  <br/> |
   
## Text value

The **Data** element contains the property names and values for an exported item or an item that will be uploaded into a mailbox. 
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [ExportItems operation](exportitems-operation.md)
- [UploadItems operation](uploaditems-operation.md)

