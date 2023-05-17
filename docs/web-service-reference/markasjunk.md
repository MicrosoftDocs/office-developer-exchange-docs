---
title: "MarkAsJunk"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: "The MarkAsJunk element specifies the request to move an item to the junk mail folder and to add the sender to the blocked sender list."
---

# MarkAsJunk

The **MarkAsJunk** element specifies the request to move an item to the junk mail folder and to add the sender to the blocked sender list. 
  
```XML
<MarkAsJunk IsJunk="true | false" MoveItem="true | false">
   <ItemIds/>
</MarkAsJunk>
```

 **MarkAsJunkType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|IsJunk  <br/> |A text value of **true** for the **IsJunk** attribute indicates that the email sender is added to the blocked sender list. A value of **false** indicates that the email sender is removed from the blocked sender list, if the email sender is already on the list.  <br/> |
|MoveItem  <br/> |A text value of **true** for the **MoveItem** attribute indicates that the item is moved to the default junk mail folder. A value of **false** indicates that the item is not moved to the default junk mail folder.  <br/> |
   
### Child elements

[ItemIds](itemids.md)
  
### Parent elements

None.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |messages.xsd  <br/> |
|Can be empty  <br/> ||
   

