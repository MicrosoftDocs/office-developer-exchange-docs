---
title: "SetFolderField"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetFolderField
api_type:
- schema
ms.assetid: 8c69db7b-54b5-4ae2-abca-4d6e0937a790
description: "The SetFolderField element represents an update that sets the value for a single property on a folder in an UpdateFolder operation."
---

# SetFolderField

The **SetFolderField** element represents an update that sets the value for a single property on a folder in an UpdateFolder operation. 
  
```xml
<SetFolderField>
   <FieldURI/>
   <Folder/>
</SetFolderField>
```

 **SetFolderFieldType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifies frequently referenced properties by URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifies individual members of a dictionary.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifies extended MAPI properties.  <br/> |
|[Folder](folder.md) <br/> |Identifies a folder to update.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Represents a folder that primarily contains calendar items.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Represents a Contacts folder in a mailbox.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Represents a search folder that is contained in a mailbox.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Represents a Tasks folder that is contained in a mailbox.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Updates (Folder)](updates-folder.md) <br/> |Contains a set of elements that defines append, set, and delete changes to folder properties.  <br/> |
   
## Remarks

If the property exists, the property value is set to the specified value. If the property does not exist, the property is created with the specified value.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[UpdateFolder operation](updatefolder-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

