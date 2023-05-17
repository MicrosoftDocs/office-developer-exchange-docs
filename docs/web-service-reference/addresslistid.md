---
title: "AddressListId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: a3334bb2-90dc-4fe1-96d9-890b13d9ff30
description: "The AddressListId element specifies the identifier of an address list."
---

# AddressListId

The **AddressListId** element specifies the identifier of an address list. 
  
```XML
<AddressListId Id="">
</AddressListId>
```

 **AddressListIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Id** <br/> |A string address list identifier. This attribute is required.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Indicates the folder that is targeted for actions that use folders. This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Specifies the identifier of the folder to which email items are copied.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indicates the destination folder for copy and move actions.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Specifies the identifier of the folder to which email items are moved  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

