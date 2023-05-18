---
title: "UpdateItem operation (task)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: b0a7f114-d040-40eb-a8f3-05ea6489e472
description: "The UpdateItem operation is used to update task item properties in the Exchange store."
---

# UpdateItem operation (task)

The UpdateItem operation is used to update task item properties in the Exchange store.
  
## Remarks

You cannot use Exchange Web Services to send task requests. Exchange Web Services can return task requests that are created by MicrosoftOfficeOutlook. If a task request has already been sent, a request to update the task will return an error.
  
## Updating the Current Occurrence of a Recurring Task

The result of an UpdateItem operation on recurring tasks differs from the result of the UpdateItem operation on a single, nonrecurring task. Changes to an occurrence of a recurring task cause one-off tasks to be generated when the following updates are made:
  
1. The status property of a regenerating or nonregenerating recurrent task is set to **Completed**.
    
2. The start date or end date of a nonregenerating recurrent task is changed.
    
For example, if an **UpdateItem** request sets the Completed value of a recurring task to **true**, the **UpdateItemResponse** will include a new Id and ChangeKey that represent a newly created one-off task. The Id that was included in the request is still valid and the recurring task that is represented by that Id has been updated to represent the next occurrence. The ChangeKey that was included in the request is no longer valid because the recurring task has been updated. 
  
You can use the [GetItem operation](getitem-operation.md) to get the latest **ChangeKey** for the recurring task. 
  
For nonrecurring tasks or for the last occurrence of a recurring task, the UpdateItem response returns the same **Id** that was passed to it and returns the associated updated **ChangeKey**.
  
## See also



[UpdateItem operation](updateitem-operation.md)

