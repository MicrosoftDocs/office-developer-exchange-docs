---
title: "SendItem"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SendItem
api_type:
- schema
ms.assetid: a966da19-b05a-4504-ac98-91acc1667b9a
description: "The SendItem element is the root element in a request to send an item in the Exchange store."
---

# SendItem

The **SendItem** element is the root element in a request to send an item in the Exchange store. 
  
```xml
<SendItem SaveItemToFolder="">
   <ItemIds/>
   <SavedItemFolderId/>
</SendItem>
```

 **SendItemType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**SaveItemToFolder** <br/> |Identifies whether a copy of the sent item is saved. The save action depends on the value of **SaveItemToFolder** and whether a [SavedItemFolderId](saveditemfolderid.md) element is present in the request. This element is required.  <br/> |
   
#### SaveItemToFolder Attribute

|**Value**|**Description**|
|:-----|:-----|
|**true** <br/> |If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is saved in the Sent Items folder. If the [SavedItemFolderId](saveditemfolderid.md) element is present, the item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element.  <br/> |
|**false** <br/> |If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is not saved. If the [SavedItemFolderId](saveditemfolderid.md) element is present, an error response will be returned with a [ResponseCode](responsecode.md) element that contains the **ErrorInvalidSendItemSaveSettings** value.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.  <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifies the target folder for operations that update, send, and create items in the Exchange store.  <br/> |
   
### Parent elements

None.
  
## Remarks

If an item in the Sent Items folder is sent, the sent item is deleted and a copy of it is put in the Sent Items folder.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[SendItem operation](senditem-operation.md)

