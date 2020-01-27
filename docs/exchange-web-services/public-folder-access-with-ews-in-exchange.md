---
title: "Public folder access with EWS in Exchange"
 
 
manager: sethgros
ms.date: 7/17/2015
ms.audience: Developer
 
 
ms.assetid: d9372057-1deb-45de-8f98-b9149604429a
description: "Learn about how to use EWS and the EWS Managed API to access public folders and route public folder requests in Exchange."
localization_priority: Priority
---

# Public folder access with EWS in Exchange

Learn about how to use EWS and the EWS Managed API to access public folders and route public folder requests in Exchange.
  
Public folders provide a shared repository of items that users in your organization can access. Office 365, Exchange Online, and on-premises versions of Exchange starting with Exchange 2013 introduce a new architecture for public folders. Public folders in Exchange use a specialized mailbox design (instead of a public folder database) to store the public folder hierarchy and public folder content. Public folder permissions are managed through Role Based Access Control (RBAC).
  
Client access technologies, like Exchange Web Services (EWS) and the EWS Managed API, provide programmatic access to both the public folder hierarchy and content items in a public folder database. This article provides information about how you can use EWS and the EWS Managed API to access public folders and public folders and public folder data. 
  
## EWS operations and EWS Managed API methods for public folder access
<a name="bk_functionality"> </a>

Most of the core EWS operations support public folder access. You can use the folder and item operations and the EWS Managed API methods listed in the following table to work with public folders.
  
For information about EWS Managed API methods, see [EWS Managed API namespaces](https://msdn.microsoft.com/library/jj220535%28v=exchg.80%29.aspx).
  
|**EWS operation**|**EWS Managed API method**|
|:-----|:-----|
|[CreateFolder operation](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |**Folder.Save()** <br/> |
|[UpdateFolder operation](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |**Folder.Update()** <br/> |
|[DeleteFolder operation](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |**Folder.Delete()** <br/> |
|[MoveFolder operation](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx)<sup>1</sup> <br/> |**Folder.Move()** <br/> |
|[CopyFolder operation](https://msdn.microsoft.com/library/c7ea0d68-9793-4144-b378-d99536776db9%28Office.15%29.aspx)<sup>2</sup> <br/> |**Folder.Copy()** <br/> |
|[GetFolder operation](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |**Folder.Bind()** <br/> |
|[EmptyFolder operation](https://msdn.microsoft.com/library/98161486-e2f2-480f-8d5d-708ba81b208a%28Office.15%29.aspx)<sup>3</sup> <br/> |**Folder.Empty()** <br/> |
|[FindFolder operation](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |**ExchangeService.FindFolders()** <br/> **Folder.FindFolders()** <br/> |
|[CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |**Item.Save()** <br/> |
|[MoveItem operation](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |**Item.Move()** <br/> |
|[CopyItem operation](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |**Item.Copy()** <br/> |
|[UpdateItem operation](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |**Item.Update()** <br/> |
|[DeleteItem operation](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |**Item.Delete()** <br/> |
|[FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)<sup>4</sup> <br/> |**ExchangeService.FindItems()** <br/> **Folder.FindItems()** <br/> |
|[GetItem operation](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |**Item.Bind()** <br/> |
|[ConvertId operation](https://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx)<sup>5</sup> <br/> |**ExchangeService.ConvertId()** <br/> **ExchangeService.ConvertIds()** <br/> |
   
<sup>1</sup> Moving folders between a public folder and private folder is not available in versions of Exchange starting with Exchange 2013. 
  
<sup>2</sup> This operation is only applicable to public folders in Exchange Server 2007 and Exchange Server 2010. 
  
<sup>3</sup> This operation is only applicable to public folders in Exchange 2010. 
  
<sup>4</sup> Full text indexed search within a single public folder by means of the QueryString search option is supported in versions of Exchange starting with Exchange 2013. 
  
<sup>5</sup> The ConvertId operation does not correctly convert public folder identifiers from the EWS identifier to the store identifier. You can manually update the identifier that is returned as a [workaround](https://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx#bk_usingConvertId).
  
The following operations are not supported, or are partially supported, for public folders in versions of Exchange starting with Exchange 2013:
  
- **CopyFolder** (not supported). You can use **CreateFolder** with the **CopyItems** operation to implement **CopyFolder** operation functionality. 
    
- **EmptyFolder** (not supported). You can use **FindItem** with the **DeleteItem** operation to implement **EmptyFolder** operation functionality. 
    
- **MoveFolder** (partially supported). You cannot move folders between private and public folders. You can move folders between private and public folders in Exchange 2007 and Exchange 2010. You can move folders within a public folder in all versions of Exchange. 
    
EWS and the EWS Managed API do not support the following functionality for public folders:
  
- Using **SyncFolderHierarchy**. Use the **FindFolder**, **GetFolder** and **SyncFolderItems** operations to synchronize items and folders in a public folder mailbox. 
    
- Deep-traversal searches of a public folder hierarchy. Use recursive **FindFolder** operation calls to traverse the public folder hierarchy. 
    
- Using the **CreateFolderPath** operation to create a folder hierarchy for public folders. You will need to use the **CreateFolder** operation for each folder level in a distinct folder hierarchy when you target a public folder mailbox. 
    
- Using the **CreateItem** operation to save copies of sent email messages. Instead, use the **MoveItem** operation to move a copy of the message into a public folder. 
    
## Scenarios for using EWS and the EWS Managed API to work with public folders
<a name="bk_scenarios"> </a>

Public folders enable many important scenarios for Exchange mailbox users. You can empower users by using EWS and the EWS Managed API to implement custom solutions for accessing and using public folders and their contents. 
  
### Programmatically access email messages that have been sent to distribution lists

Exchange mailbox users can use public folders to store email messages that are sent to distribution lists. This is a convenient way to save distribution list history. You can use the [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) in EWS or the **ExchangeService.FindItems()** and **Folder.FindItems()** methods in the EWS Managed API to access stored distribution list email messages. 
  
### Share important email messages and other mailbox items

Mailbox users can use public folders as a shared repository for mailbox items. Different users in an organization can share important email messages or contacts by using public folders. EWS can provide the access to these shared mailbox items. You can use the [MoveItem operation](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) in EWS or the **Item.Move()** method in the EWS Managed API to move email messages, contacts, and other mailbox items into and out of a public folder. 
  
### Public discussions with post items

Public folders are a convenient container for post items. Post items provide a way to use threaded conversations without having to send email messages between users. Users can use public folders and post items to host and maintain threaded conversations between different mailbox users in an organization. This way, mailbox users can access the shared history of a conversation that uses post items even if they were not part of the conversation. You can use the [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) in EWS or the **Item.Save()** method in the EWS Managed API to both create and respond to post items stored in a public folder. 
  
## Routing public folder requests
<a name="bk_routing"> </a>

Public folder content can be stored on multiple mailbox servers. The public folder hierarchy can be stored on one mailbox, while the content for the public folder is stored on another. And each of these servers can be different than the mailbox server for the user requesting the information. In these situations, it's important to include the additional X-AnchorMailbox and X-PublicFolderMailbox headers in your public folder requests to receive accurate information about public folders.
  
The value for the X-AnchorMailbox and X-PublicFolderMailbox can differ depending on whether you're performing a request related to the folder hierarchy or the folder content. The following table identifies which procedure to follow for each EWS Managed API method or EWS operation.
  
**EWS Managed API methods and EWS operations for routing public folder requests**

|**When calling these methods**|**When calling these operations**|**Use this procedure**|
|:-----|:-----|:-----|
|[Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [Folder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [Folder.Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [MoveFolder](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |Routing public folder hierarchy requests  <br/> |
|[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [Item.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [Item.Copy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [Item.Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [Item.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |Routing public folder content requests  <br/> |
   
## Version differences
<a name="VersionDifferences"> </a>

In Exchange 2007 and Exchange 2010, the **ConvertId** operation works as expected when converting public folder identifiers from the EWS identifier to the store identifier. 
  
## See also


- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)
    
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [Public folder limits](https://technet.microsoft.com/library/dn594582%28v=exchg.150%29.aspx)
    
- [FAQ: Public Folders](https://technet.microsoft.com/library/jj552408.aspx)
    
- [Public Folder Procedures](https://technet.microsoft.com/library/jj657481.aspx)
    

