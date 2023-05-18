---
title: "CreateManagedFolder"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: cfdf01a9-0191-47c7-a7ad-5254d8bdee4a
description: "The CreateManagedFolder element defines a request to add managed custom folders to a mailbox."
---

# CreateManagedFolder

The **CreateManagedFolder** element defines a request to add managed custom folders to a mailbox. 
  
```xml
<CreateManagedFolder>
   <FolderNames/>
   <Mailbox/>
</CreateManagedFolder>
```

 **CreateManagedFolderRequestType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderNames](foldernames.md) <br/> |Contains an array of named managed folders to add to a mailbox.  <br/> |
|[Mailbox](mailbox.md) <br/> |Identifies a mail-enabled Active Directory directory service object.  <br/> |
   
### Parent elements

None.
  
## Remarks

The account of the person who is making the request must have FullAccess permissions on the mailbox where the managed folders are created. You can use the _ -AccessRights _ parameter with the Exchange Management Shell **Add-MailboxPermission** cmdlet to assign the FullAccess permission. 
  
Although you can use Exchange Web Services to add managed folders to a mailbox, you cannot use Exchange Web Services to access the list of managed folders that are available. To obtain a list of available managed folders, use the **get-managedfolder** Exchange Management Shell cmdlet. The list that is returned by the **get-managedfolder cmdlet** will contain both managed custom folders and managed default folders. You can only add folders of type **managedcustomfolder** to the mailbox by using the CreateManagedFolder operation. 
  
> [!NOTE]
> You can also get a list of managed folders by using the DirectoryServices API of the Microsoft .NET Framework. 
  
You can use the [FindFolder operation](findfolder-operation.md) to find managed folders in a mailbox. Managed folders can be distinguished by setting the [BaseShape](baseshape.md) element to AllProperties in the request. The response will contain a [ManagedFolderInformation](managedfolderinformation.md) element to distinguish the managed folders from the Exchange store folders. You can delete managed folders in the same manner that you delete other folder types. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[CreateManagedFolder operation](createmanagedfolder-operation.md)
  
[FindFolder operation](findfolder-operation.md)


[Finding Folders](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adding Managed Folders](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

