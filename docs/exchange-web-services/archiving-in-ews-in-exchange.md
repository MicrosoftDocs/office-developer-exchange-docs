---
title: "Archiving in EWS in Exchange"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: "Learn about archiving in EWS in Exchange."
---

# Archiving in EWS in Exchange

Learn about archiving in EWS in Exchange.
  
Archive mailboxes are secondary mailboxes that are associated with a user. Archive mailboxes are typically used to manage email storage limits. For example, older email items might periodically be moved from the Inbox to the archive mailbox. 
  
Exchange Online, Exchange Online as part of Office 365, and Exchange Server 2013 introduce two new Exchange Web Services (EWS) operations that you can use to archive a set of mail items from a primary mailbox. Archiving Inbox items in this way preserves the folder hierarchy of the items. In addition, archive mailboxes can now be stored either locally on a client, or remotely, in a way that is mostly opaque to a user, by using a folder path to point to the contents of the archive.
  
## Archiving operations in EWS

The following table lists the archiving operations that were introduced in Exchange 2013. 
  
|**Operation name**|**Description**|
|:-----|:-----|
|[ArchiveItem](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |Moves an item from the primary mailbox to the archive mailbox.  <br/> |
|[CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |Creates a URI that points to the storage location for the archive mailbox.  <br/> |
   
## See also

- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)
    
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [EWS client design overview for Exchange](ews-client-design-overview-for-exchange.md)
    

