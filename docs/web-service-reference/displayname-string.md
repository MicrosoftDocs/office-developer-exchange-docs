---
title: "DisplayName (string)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DisplayName
api_type:
- schema
ms.assetid: e7efbbe1-6629-4d11-bed1-ed899e3f9d77
description: "The DisplayName element defines the display name of a folder, contact, distribution list, delegate user, location, or rule."
---

# DisplayName (string)

The **DisplayName** element defines the display name of a folder, contact, distribution list, delegate user, location, or rule. 
  
```XML
<DisplayName/>
```

 **String**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Represents a calendar folder in a mailbox.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Represents a contact folder in a mailbox.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[Folder](folder.md) <br/> |Represents a folder in a mailbox.  <br/> |
|[Rule (RuleType)](rule-ruletype.md) <br/> |Represents a rule in a user's mailbox.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Represents a search folder in a mailbox.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Represents a task folder in a mailbox.  <br/> |
|[UserId](userid.md) <br/> |Identifies a delegate user or a user who has folder access permissions.  <br/> |
   
## Text value

A text value that represents the display name is required if this element is used.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Example

This following example shows how to create a new folder and to set the DisplayName of the folder to "TestFolder".
  
```cs
FolderType folder = new FolderType();
folder.DisplayName = "TestFolder";
```

## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

