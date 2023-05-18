---
title: "EffectiveRights"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- EffectiveRights
api_type:
- schema
ms.assetid: bf5278eb-3a1a-4d27-9d16-b8be043bb023
description: "The EffectiveRights element contains the client's rights based on the permission settings for the item or folder. This element is read-only."
---

# EffectiveRights

The **EffectiveRights** element contains the client's rights based on the permission settings for the item or folder. This element is read-only. 
  
```XML
<EffectiveRights>
   <CreateAssociated/>
   <CreateContents/>
   <CreateHierarchy/>
   <Delete/>
   <Modify/>
   <Read/>
   <ViewPrivateItems/>
</EffectiveRights>
```

 **EffectiveRightsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[CreateAssociated](createassociated.md) <br/> |Indicates whether a client can create an associated contents table. This property is only used on folder objects.  <br/> |
|[CreateContents](createcontents.md) <br/> |Indicates whether a client can create a contents table. This property is only used on folder objects.  <br/> |
|[CreateHierarchy](createhierarchy.md) <br/> |Indicates whether a client can create a hierarchy table. This property is only used on folder objects.  <br/> |
|[Delete](delete.md) <br/> |Indicates whether a client can delete a folder or item.  <br/> |
|[Modify](modify.md) <br/> |Indicates whether a client can modify a folder or item.  <br/> |
|[Read](read.md) <br/> |Indicates whether a client can read a folder or item.  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |Indicates whether a private item can be viewed.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Represents a folder in a mailbox.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Represents a tasks folder in a mailbox.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Represents a contacts folder in a mailbox.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Represents a calendar folder in a mailbox.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Represents a search folder in a mailbox.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[Item](item.md) <br/> |Represents a generic Exchange item.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation in the Exchange store.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response in the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an Exchange e-mail message.  <br/> |
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
|[PostItem](postitem.md) <br/> |Represents a post item in the Exchange store.  <br/> |
   
## Text value

None.
  
## Remarks

**EffectiveRights** is supported in the GetFolder, GetItem, FindFolder, FindItem, SyncFolderHierarchy, and SyncFolderItems responses. The **EffectiveRights** property is exposed in the **AllProperties** shape for folders and items. 
  
This **EffectiveRights** property provides access to the same information that is provided in the **PR_ACCESS MAPI** property. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
- [Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

