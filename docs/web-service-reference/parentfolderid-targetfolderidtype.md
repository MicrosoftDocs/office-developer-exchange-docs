---
title: "ParentFolderId (TargetFolderIdType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 0e3e6e5f-06d0-499b-8ca4-d36036521658
description: "The ParentFolderId element identifies the folder in which a new folder is created or the folder to search for the FindConversation operation."
---

# ParentFolderId (TargetFolderIdType)

The **ParentFolderId** element identifies the folder in which a new folder is created or the folder to search for the [FindConversation operation](findconversation-operation.md).
  
```xml
<ParentFolderId>
   <DistinguishedFolderId/>
</ParentFolderId>
```

```xml
<ParentFolderId>
   <FolderId/> 
</ParentFolderId>
```

**TargetFolderIdType**

## Attributes and elements

The **ParentFolderId** element contains two child elements. The child elements are mutually exclusive in the schema. 
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contains the required identifier and the optional change key of a folder in which a new folder is created or the folder that is searched for the [FindConversation operation](findconversation-operation.md). Using this element excludes the use of the [DistinguishedFolderId](distinguishedfolderid.md) element.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifies default Microsoft Exchange Server 2007 folders. Using this element excludes the use of the [FolderId](folderid.md) element.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CreateFolder](createfolder.md) <br/> |Defines a request to create a folder in the Exchange database.  <br/> The following is the XPath expression to this element:  `/CreateFolder` <br/> |
|[FindConversation](findconversation.md) <br/> |Defines a request to find conversations in a mailbox.  <br/> |
   
## Text value

None.
  
## Remarks

The two child elements are used to define the folder that will contain the new folder. You must select either the [FolderId](folderid.md) or the [DistinguishedFolderId](distinguishedfolderid.md) element to identify the parent folder of the new folder. You cannot use both elements at the same time. This element is required to create folders. 
  
The [ParentFolderId](parentfolderid.md) element describes the location of existing items and folders. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [CreateFolder operation](createfolder-operation.md)
- [FindConversation operation](findconversation-operation.md)
- [Creating Folders (Exchange Web Services)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

