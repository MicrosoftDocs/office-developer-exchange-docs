---
title: "FolderIds"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FolderIds
api_type:
- schema
ms.assetid: 3ff9d15a-7220-4785-ae6b-583a7eb82005
description: "The FolderIds element contains an array of folder identifiers that are used to identify folders to copy, move, get, delete, or monitor for event notifications."
---

# FolderIds

The **FolderIds** element contains an array of folder identifiers that are used to identify folders to copy, move, get, delete, or monitor for event notifications. 
  
```xml
<FolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</FolderIds>
```

 **NonEmptyArrayOfBaseFolderIdsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contains the identifier and change key of a folder.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifies Microsoft Exchange Server folders that can be referenced by name.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetFolder](getfolder.md) <br/> |Defines a request to get a folder from the Exchange store.  <br/> The following is the XPath expression to this element:  `/GetFolder` <br/> |
|[DeleteFolder](deletefolder.md) <br/> |Defines a request to delete folders from the Exchange store.  <br/> The following is the XPath expression to this element:  `/DeleteFolder` <br/> |
|[EmptyFolder](emptyfolder.md) <br/> |Defines a request to delete folders from the Exchange store.  <br/> The following is the XPath expression to this element:  `/EmptyFolder` <br/> |
|[MoveFolder](movefolder.md) <br/> |Defines a request to move a folder in the Exchange store.  <br/> The following is the XPath expression to this element:  `/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |Defines a request to copy a folder in the Exchange store.  <br/> The following is the XPath expression to this element:  `/CopyFolder` <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Represents a subscription to a push-based event notification subscription.  <br/> |
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Represents a subscription to a pull-based event notification subscription.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages and https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Messages schema; Types schema  <br/> |
|Validation File  <br/> |Messages.xsd; Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetFolder operation](getfolder-operation.md)
  
[DeleteFolder operation](deletefolder-operation.md)
  
[MoveFolder operation](movefolder-operation.md)
  
[CopyFolder operation](copyfolder-operation.md)
  
[Subscribe operation](subscribe-operation.md)

