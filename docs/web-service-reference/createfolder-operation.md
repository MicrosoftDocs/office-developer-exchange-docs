---
title: "CreateFolder operation"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolder
api_type:
- schema
ms.assetid: 6f6c334c-b190-4e55-8f0a-38f2a018d1b3
description: "The CreateFolder operation creates folders, calendar folders, contacts folders, tasks folders, and search folders."
---

# CreateFolder operation

The CreateFolder operation creates folders, calendar folders, contacts folders, tasks folders, and search folders.
  
## CreateFolder Request Example

### Description

The following example of a CreateFolder request shows how to form a request to create two new folders in the mailbox root.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ParentFolderId>
        <t:DistinguishedFolderId Id="msgfolderroot"/>
      </ParentFolderId>
      <Folders>
        <t:Folder>
          <t:DisplayName>Folder1</t:DisplayName>
        </t:Folder>
        <t:Folder>
          <t:DisplayName>Folder2</t:DisplayName>
        </t:Folder>
      </Folders>
    </CreateFolder>
  </soap:Body>
</soap:Envelope>
```

### Request Elements

The following elements are used in the request:
  
- [CreateFolder](createfolder.md)
    
- [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [DisplayName (string)](displayname-string.md)
    
> [!NOTE]
> The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed. 
  
To find other options for the request message of the CreateFolder operation, explore the schema hierarchy. Start at the [CreateFolder](createfolder.md) element. 
  
> [!NOTE]
> If you create a search folder with a restriction by using the **calendar:Organizer** property, a subsequent get folder call will return the restriction with the **message:from** property in its place. These two properties map to the same underlying MAPI property. 
  
The CreateFolder operation supports the creation of a custom folder class only when you create the folder by using a generic folder type element and set the **FolderClass** element. 
  
## Successful CreateFolder Response Example

### Description

The following example shows a successful response to the CreateFolder request. In this example, the response returns the identifiers of the new folders.
  
> [!NOTE]
> The folder ID and the change key have been shortened to preserve readability. 
  
### Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn==" />
            </t:Folder>
          </m:Folders>
        </m:CreateFolderResponseMessage>
        <m:CreateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn==" />
            </t:Folder>
          </m:Folders>
        </m:CreateFolderResponseMessage>
      </m:ResponseMessages>
    </CreateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### Successful Response Elements

The following elements are used in the response:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateFolderResponse](createfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateFolderResponseMessage](createfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
To find other options for the response message of the CreateFolder operation, explore the schema hierarchy. Start at the [CreateFolderResponse](createfolderresponse.md) element. 
  
## CreateFolder Error Response

### Description

The following example shows an error response to a CreateFolder request.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A folder with the specified name already exists.</m:MessageText>
          <m:ResponseCode>ErrorFolderExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:CreateFolderResponseMessage>
      </m:ResponseMessages>
    </CreateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### Error Response Elements

The following elements are used in the error response:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateFolderResponse](createfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateFolderResponseMessage](createfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
To find other options for the error response message of the CreateFolder operation, explore the schema hierarchy. Start at the [CreateFolderResponse](createfolderresponse.md) element. 
  
## See also



[FindItem operation](finditem-operation.md)
  
[FindFolder operation](findfolder-operation.md)
  
 **CreateFolderType**


[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Creating Folders (Exchange Web Services)](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

