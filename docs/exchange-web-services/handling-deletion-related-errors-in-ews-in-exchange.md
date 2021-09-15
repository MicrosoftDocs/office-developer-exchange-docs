---
title: "Handling deletion-related errors in EWS in Exchange"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: 1bbe8507-7730-45e5-9232-c4f6fc39c2d9
description: "Find out how to handle deletion-related errors in applications that you develop by using the EWS Managed API or EWS in Exchange."
---

# Handling deletion-related errors in EWS in Exchange

Find out how to handle deletion-related errors in applications that you develop by using the EWS Managed API or EWS in Exchange.
  
If your application [deletes items and folders](deleting-items-by-using-ews-in-exchange.md), you might have to handle deletion-related errors. You can handle these errors at runtime, or while you are developing your EWS application.
  
**Table 1: Deletion-related errors and how to handle them**

|**Error**|**Occurs when you try to…**|**Handle it by…**|
|:-----|:-----|:-----|
|ErrorAffectedTaskOccurrencesRequired  <br/> |Delete an instance of a recurring task, and the **AffectedTaskOccurrence** property is not set.  <br/> |Setting the **AffectedTaskOccurrence** property, and retrying the deletion.  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> |Update a calendar item located in the Deleted Items folder when the update would result in sending a meeting invite to attendees.  <br/> |Canceling the update or moving the calendar item back to the default Calendar folder and updating the calendar item.  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |Reference a deleted occurrence of a recurring appointment.  <br/> |Removing a reference to a deleted occurrence.  <br/> |
|ErrorCannotDeleteObject  <br/> |Delete an item that cannot be deleted.  <br/> |Quitting attempts to delete the item.  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |Delete an occurrence of a nonrecurring task or delete the last occurrence of a recurring task.  <br/> |Deleting a nonrecurring task or quitting attempts to delete the last occurrence of a recurring task.  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |Delete a distinguished folder.  <br/> |Indicating that default folders cannot be deleted.  <br/> |
|ErrorItemNotFound  <br/> |Access a permanently deleted item.  <br/> |Removing references to an item when it is deleted from the store. If an item is recovered, make sure that you reinstate required references to the client.  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |Delete a calendar item without specifying whether meeting cancellations should be sent.  <br/> |Specifying that meeting cancellations should or should not be sent.  <br/> |
   
## See also


- [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Pull notifications for EWS deletion-related mailbox events in Exchange](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [Delete appointments and cancel meetings by using EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

