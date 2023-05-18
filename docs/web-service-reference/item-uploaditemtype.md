---
title: "Item (UploadItemType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: ab7058f2-615f-4393-a0d4-af76727f37e9
description: "The Item element represents a single item to upload into a mailbox."
---

# Item (UploadItemType)

The **Item** element represents a single item to upload into a mailbox. 
  
[UploadItems](uploaditems.md)
  
[Items (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md)
  
[Item (UploadItemType)](item-uploaditemtype.md)
  
```XML
<Item CreateAction="" IsAssociated="">
   <ParentFolderId/>
   <ItemId/>
   <Data/>
</Item>
```

 **UploadItemType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**CreateAction** <br/> |Specifies the action for uploading an item into a mailbox. This attribute is required.  <br/> |
|**IsAssociated** <br/> |Specifies whether the uploaded item is a folder associated item. This attribute is a Boolean value. A value of **true** indicates that the item is a folder associated item. This attribute is optional.  <br/> |
   
#### CreateAction Attribute

|**Value**|**Description**|
|:-----|:-----|
|**CreateNew** <br/> |Indicates that a new copy of the original item is uploaded to the mailbox. The [ItemId](itemid.md) element must not be present if the CreateNew value is used. The new item identifier is returned in the response.  <br/> |
|**Update** <br/> |Specifies that the item indicated by the **ItemId** element will be updated. An error is returned if the **ItemId** element is not present or if the item does not exist in the folder identified by the [ParentFolderId](parentfolderid.md) element.  <br/> |
|**UpdateOrCreate** <br/> |Indicates that an attempt is first made to update the item. If the item does not exist in the folder specified by the **ParentFolderId** element, a new item is created.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ParentFolderId](parentfolderid.md) <br/> |Represents the identifier of the parent folder where a new item is created or that contains the item to update.  <br/> |
|[ItemId](itemid.md) <br/> |Contains the unique identifier and change key of an item to create or update in the Exchange store.  <br/> |
|[Data (base64Binary)](data-base64binary.md) <br/> |Contains the data of a single item to upload into a mailbox.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Items (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md) <br/> |Contains an array of item to upload into a mailbox.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[ExportItems operation](exportitems-operation.md)
  
[UploadItems operation](uploaditems-operation.md)

