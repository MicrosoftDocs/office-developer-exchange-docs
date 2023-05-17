---
title: "ArchiveTag"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: c4cb0718-37cd-41aa-86e7-b492c4bb86aa
description: "The ArchiveTag element specifies the retention identifier of the archive tag set on an item or folder."
---

# ArchiveTag

The **ArchiveTag** element specifies the retention identifier of the archive tag set on an item or folder. 
  
```XML
<ArchiveTag IsExplicit=""></ArchiveTag>
```

 **RetentionTagType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**IsExplicit** <br/> |Specifies whether the retention policy is explicitly set on an item or folder or whether it is inherited from a parent folder.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Represents a folder that primarily contains calendar items.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[Contact](contact.md) <br/> |Represents a contact item in the Exchange store.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Represents a contacts folder that is contained in a mailbox.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[Folder](folder.md) <br/> |Defines a folder to create, get, find, synchronize, or update.  <br/> |
|[Item](item.md) <br/> |Represents a generic item in the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents a Microsoft Exchange email message.  <br/> |
|[PostItem](postitem.md) <br/> |Represents a post item in the Exchange store.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Represents a search folder that is contained in a mailbox.  <br/> |
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Represents a tasks folder that is contained in a mailbox.  <br/> |
   
## Text value

The text value of the **ArchiveTag** element is a GUID that identifies the retention policy. 
  
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

