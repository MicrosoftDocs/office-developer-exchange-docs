---
title: "Guid"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 49dcf69f-bf8d-4be6-a24c-03bbd13f4fe5
description: "The Guid element specifies the globally unique identifier of the mailbox."
---

# Guid

The **Guid** element specifies the globally unique identifier of the mailbox. 
  
```XML
<Guid></Guid>
```

 **GuidType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SearchableMailbox](searchablemailbox.md) <br/> |Specifies a mailbox returned from a **GetSearchableMailboxes** request.  <br/> |
   
## Text value

The text value of the **Guid** element is a GUID value that uniquely identifies a mailbox. 
  
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

