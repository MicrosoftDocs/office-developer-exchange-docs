---
title: "RetentionAction"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: "The RetentionAction element specifies the action performed on items with the retention tag."
---

# RetentionAction

The **RetentionAction** element specifies the action performed on items with the retention tag. 
  
```XML
<RetentionAction> None | MoveToDeletedItems | MoveToFolder | DeleteAndAllowRecovery | PermanentlyDelete | MarkAsPastRetentionLimit | MoveToArchive <RetentionAction>
```

 **RetentionActionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[RetentionPolicyTag](retentionpolicytag.md)
  
## Text value

The text value of the **RetentionAction** element is the action performed on items. The following list contains the text values for the **RetentionAction** element. 
  
> **None** - No action is performed on the item. 
    
> **MoveToDeletedItems** - The item is moved to the default Deleted Items folder. 
    
> **MoveToFolder** - The item is moved to a specified folder. 
    
> **DeleteAndAllowRecovery** - The item is deleted and put into the Dumpster. 
    
> **PermanentlyDelete** - The item is permanently deleted from the mailbox. 
    
> **MarkAsPastRetentionLimit** - The item is marked as having exceeded the retention time limit. 
    
> **MoveToArchive** - The item is moved to the archive mailbox. 
    
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   