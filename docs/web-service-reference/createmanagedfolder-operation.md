---
title: "CreateManagedFolder operation"
 
 
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
ms.assetid: 60a668a2-b4e9-4db9-ac76-9b181e47b302
description: "The CreateManagedFolder operation creates a managed folder in the Exchange store."
---

# CreateManagedFolder operation

The CreateManagedFolder operation creates a managed folder in the Exchange store.
  
## Using the CreateManagedFolder Operation

The CreateManagedFolder operation adds a managed custom folder to a user's mailbox. You can use the Exchange Management Shell **Get-ManagedFolder** cmdlet to find available managed folders to add. Although this cmdlet returns both managed custom folders and managed default folders, only managed custom folders can be added. Managed custom folders are identified by the ManagedCustomFolder folder type. The System.DirectoryServices namespace also includes types that can be used to discover the names of available managed folders. 
  
> [!NOTE]
> You cannot use Exchange Web Services to find the names of available managed folders to add to a mailbox. 
  
You can use the FindFolder and GetFolder operations to access managed folders. FindFolder is used to search for folders in a specified parent folder. This can be used so that managed folders can be discovered in a folder before trying to add a duplicate managed custom folder to the same directory. GetFolder is used after the FindFolder operation to get more information about a managed custom folder.
  
## Remarks

For information about how to set up messaging records management (MRM) policy, see [How to Create a Managed Folder Mailbox Policy](https://go.microsoft.com/fwlink/?LinkId=100975).
  
For information about how to remove managed custom folders from a mailbox, see [Remove-ManagedFolder](https://go.microsoft.com/fwlink/?LinkId=100976).
  
## CreateManagedFolder request example

### Description

The following example of a CreateManagedFolder request shows how to add a managed folder named Test Managed Folder to a mailbox.
  
> [!NOTE]
> You can also use delegate access to add managed custom folders. 
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateManagedFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderNames>
        <t:FolderName>Test Managed Folder</t:FolderName>
      </FolderNames>
    </CreateManagedFolder>
  </soap:Body>
</soap:Envelope>
```

### Request elements

The following elements are used in the request:
  
- [CreateManagedFolder](createmanagedfolder.md)
    
- [FolderNames](foldernames.md)
    
- [FolderName](foldername.md)
    
To find other options for the request message of the CreateManagedFolder operation, explore the schema hierarchy. Start at the [CreateManagedFolder](createmanagedfolder.md) element. 
  
## Successful CreateManagedFolder Response

### Description

The following code example shows a successful response to a CreateManagedFolder request.
  
> [!NOTE]
> The **Id** and **ChangeKey** attribute values have been shortened to preserve readability. 
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS0AdX=" ChangeKey="AACADA=="/>
            </t:Folder>
          </m:Folders>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### Successful response elements

The following elements are used in the response: 
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
To find other options for the response messages of the CreateManagedFolder operation, explore the schema hierarchy. Start at the [CreateManagedFolderResponse](createmanagedfolderresponse.md) element. 
  
## CreateManagedFolder error response

### Description

The following code example shows an error response to a CreateManagedFolder request.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A specified managed folder already exists in the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorManagedFolderAlreadyExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders/>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### Error response elements

The following elements are used in the error response:
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
## See also



[GetFolder operation](getfolder-operation.md)
  
[FindFolder operation](findfolder-operation.md)


[Finding Folders](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adding Managed Folders](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

