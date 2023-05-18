---
title: "FolderClass"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FolderClass
api_type:
- schema
ms.assetid: 0041d135-2869-4612-89a5-d1aa86aa1093
description: "The FolderClass element represents the folder class for a folder."
---

# FolderClass

The **FolderClass** element represents the folder class for a folder. 
  
```xml
<FolderClass/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Represents a folder in a mailbox.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Represents a calendar folder in a mailbox.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Represents a contacts folder in a mailbox.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Represents a search folder in a mailbox.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Represents a task folder in a mailbox.  <br/> |
   
## Text value

A text value is required. Folder classes typically start with "IPF."
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

