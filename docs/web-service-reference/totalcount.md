---
title: "TotalCount"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- TotalCount
api_type:
- schema
ms.assetid: c48c6388-8449-4622-bc38-6f0e84293872
description: "The TotalCount element represents the total count of items within a given folder."
---

# TotalCount

The **TotalCount** element represents the total count of items within a given folder. 
  
```xml
<TotalCount/>
```

 **int**
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

The text value represents an integer value. This property is read-only.
  
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

