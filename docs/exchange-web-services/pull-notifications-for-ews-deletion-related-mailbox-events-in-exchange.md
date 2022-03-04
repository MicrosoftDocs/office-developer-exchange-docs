---
title: "Pull notifications for EWS deletion-related mailbox events in Exchange"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: 83511eea-e0b5-4ef0-83b1-0c5434e6d3ab
description: "Discover which mailbox events are raised when you delete items by using EWS in Exchange."
---

# Pull notifications for EWS deletion-related mailbox events in Exchange

Discover which mailbox events are raised when you delete items by using EWS in Exchange.
  
When you [delete items and folders from a mailbox](deleting-items-by-using-ews-in-exchange.md), this triggers a mailbox event. Different versions of Exchange return different mailbox events in response to changes to items and folders in a mailbox. The following table identifies the mailbox events that are returned for deletions when you use pull notifications to subscribe to mailbox events. 
  
**Table 1: Deletion-related mailbox events for pull notifications**

|**Type of deletion and the EWS operation**|**Exchange 2010 notification when you specify each folder identifier**|**Exchange 2010 notification when you specify all folders**|**Exchange Online and Exchange 2013 notification when you specify each folder identifier**|**Exchange Online and Exchange 2013 when you specify all folders**|
|:-----|:-----|:-----|:-----|:-----|
|Soft delete via the [DeleteItem operation](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |DeletedEvent for the item.  <br/> ModifiedEvent for the item's parent folder.  <br/> |DeletedEvent for the item.  <br/> ModifiedEvent for the item's parent folder.  <br/> |MovedEvent for the item. This specifies both the old and new parent folder identifiers. The item is moved to the Deletions folder in the dumpster.  <br/> ModifiedEvent for the item's parent folder.  <br/> |DeletedEvent for the item.  <br/> DeletedEvent for the item from the AllItems default search folder.  <br/> ModifiedEvent for the item's parent folder.  <br/> |
|Hard delete via the [DeleteItem operation](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |DeletedEvent for the item.  <br/> ModifiedEvent for the item's parent folder.  <br/> |DeletedEvent for the item.  <br/> ModifiedEvent for the item's parent folder.  <br/> |DeletedEvent for the item.  <br/> ModifiedEvent for the item's parent folder.  <br/> |DeletedEvent for the item.  <br/> DeletedEvent for the item from the AllItems default search folder.  <br/> ModifiedEvent for the item's parent folder.  <br/> |
|Move to the Deleted Items folder via the [DeleteItem operation](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |MovedEvent for the item. This specifies both old and new parent folder identifiers.  <br/> ModifiedEvent for the item's old parent folder.  <br/> ModifiedEvent for the item's new parent folder, which is the Deleted Items folder.  <br/> |MovedEvent for the item. This specifies both old and new parent folder identifiers.  <br/> ModifiedEvent for the item's old parent folder.  <br/> ModifiedEvent for the item's new parent folder, which is the Deleted Items folder.  <br/> |MovedEvent for the item. This specifies both old and new parent folder identifiers.  <br/> ModifiedEvent for the item's old parent folder.  <br/> ModifiedEvent for the item's new parent folder, which is the Deleted Items folder.  <br/> |DeletedEvent from the AllItems default search folder.  <br/> CreatedEvent for the item in the AllItems folder.  <br/> ModifiedEvent for the item's original parent folder.  <br/> ModifiedEvent for the Deleted Items folder.  <br/> |
|Soft delete via the [DeleteFolder operation](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent for the folder.  <br/> ModifiedEvent for the folder's parent folder.  <br/> |DeletedEvent for the folder.  <br/> ModifiedEvent for the folder's parent folder.  <br/> |DeletedEvent for the folder.  <br/> ModifiedEvent for the folder's parent folder.  <br/> |DeletedEvent for the folder.  <br/> ModifiedEvent for the folder's parent folder.  <br/> |
|Hard delete via the [DeleteFolder operation](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent for the folder.  <br/> ModifiedEvent for the folder's parent folder.  <br/> |DeletedEvent for the folder.  <br/> ModifiedEvent for the folder's parent folder.  <br/> |DeletedEvent for the folder.  <br/> ModifiedEvent for the folder's parent folder.  <br/> |DeletedEvent for the folder.  <br/> ModifiedEvent for the folder's parent folder.  <br/> |
|Move to the Deleted Items folder via the [DeleteFolder operation](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |MovedEvent for the folder. This specifies both old and new parent folder identifiers.  <br/> ModifiedEvent for the folder's old parent folder.  <br/> ModifiedEvent for the folder's new parent folder, which is the Deleted Items folder.  <br/> |MovedEvent for the folder. This specifies both old and new parent folder identifiers.  <br/> ModifiedEvent for the folder's old parent folder.  <br/> ModifiedEvent for the folder's new parent folder, which is the Deleted Items folder.  <br/> |MovedEvent for the folder. This specifies both old and new parent folder identifiers.  <br/> ModifiedEvent for the folder's old parent folder.  <br/> ModifiedEvent for the folder's new parent folder, which is the Deleted Items folder.  <br/> |ModifiedEvent for the folder's old parent folder.  <br/> ModifiedEvent for the folder's new parent folder which is the Deleted Items folder.  <br/> |
   
## See also


- [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Handling deletion-related errors in EWS in Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    

