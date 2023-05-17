---
title: "Flag"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 7b47bc74-a60d-4308-8674-5d52444a1753
description: "The Flag element specifies a flag on a mailbox item."
---

# Flag

The **Flag** element specifies a flag on a mailbox item. 
  
```XML
<Flag>
    <FlagStatus/>
    <StartDate/>
    <DueDate/>
    <CompleteDate/>
</Flag>
```

 **FlagType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FlagStatus](flagstatus.md) <br/> |Contains the aggregated flag status for items in the current folder.  <br/> |
|[StartDate](startdate.md) <br/> |Represents the start date of an item.  <br/> |
|[DueDate](duedate.md) <br/> |Represents the date when an item is due.  <br/> |
|[CompleteDate](completedate.md) <br/> |Represents the date on which an item was completed.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |Contains a single action to be applied to a single conversation.  <br/> |
|[Item](item.md) <br/> |Represents a generic item in the Exchange store.  <br/> |
   
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

