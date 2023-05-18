---
title: "FieldUri (Rule)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: cecdea78-de9c-48be-ae31-03877feafeec
description: "The FieldURI element specifies the URI to the rule field that caused the validation error."
---

# FieldUri (Rule)

The **FieldURI** element specifies the URI to the rule field that caused the validation error. 
  
```XML
<FieldURI/>
```

 **RuleFieldURIType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Error](error.md) <br/> |Represents a single validation error on a particular rule property value, predicate property value, or action property value.  <br/> |
   
## Text value

The text value for this element is restricted to one of the following strings:
  
- RuleId
    
- DisplayName
    
- Priority
    
- IsNotSupported
    
- Actions
    
- Condition:Categories
    
- Condition:ContainsBodyStrings
    
- Condition:ContainsHeaderStrings
    
- Condition:ContainsRecipientStrings
    
- Condition:ContainsSenderStrings
    
- Condition:ContainsSubjectOrBodyStrings
    
- Condition:ContainsSubjectStrings
    
- Condition:FlaggedForAction
    
- Condition:FromAddresses
    
- Condition:FromConnectedAccounts
    
- Condition:HasAttachments
    
- Condition:Importance
    
- Condition:IsApprovalRequest
    
- Condition:IsAutomaticForward
    
- Condition:IsAutomaticReply
    
- Condition:IsEncrypted
    
- Condition:IsMeetingRequest
    
- Condition:IsMeetingResponse
    
- Condition:IsNDR
    
- Condition:IsPermissionControlled
    
- Condition:IsReadReceipt
    
- Condition:IsSigned
    
- Condition:IsVoicemail
    
- Condition:ItemClasses
    
- Condition:MessageClassifications
    
- Condition:NotSentToMe
    
- Condition:SentCcMe
    
- Condition:SentOnlyToMe
    
- Condition:SentToAddresses
    
- Condition:SentToMe
    
- Condition:SentToOrCcMe
    
- Condition:Sensitivity
    
- Condition:WithinDateRange
    
- Condition:WithinSizeRange
    
- Exception:Categories
    
- Exception:ContainsBodyStrings
    
- Exception:ContainsHeaderStrings
    
- Exception:ContainsRecipientStrings
    
- Exception:ContainsSenderStrings
    
- Exception:ContainsSubjectOrBodyStrings
    
- Exception:ContainsSubjectStrings
    
- Exception:FlaggedForAction
    
- Exception:FromAddresses
    
- Exception:FromConnectedAccounts
    
- Exception:HasAttachments
    
- Exception:Importance
    
- Exception:IsApprovalRequest
    
- Exception:IsAutomaticForward
    
- Exception:IsAutomaticReply
    
- Exception:IsEncrypted
    
- Exception:IsMeetingRequest
    
- Exception:IsMeetingResponse
    
- Exception:IsNDR
    
- Exception:IsPermissionControlled
    
- Exception:IsReadReceipt
    
- Exception:IsSigned
    
- Exception:IsVoicemail
    
- Exception:ItemClasses
    
- Exception:MessageClassifications
    
- Exception:NotSentToMe
    
- Exception:SentCcMe
    
- Exception:SentOnlyToMe
    
- Exception:SentToAddresses
    
- Exception:SentToMe
    
- Exception:SentToOrCcMe
    
- Exception:Sensitivity
    
- Exception:WithinDateRange
    
- Exception:WithinSizeRange
    
- Action:AssignCategories
    
- Action:CopyToFolder
    
- Action:Delete
    
- Action:ForwardAsAttachmentToRecipients
    
- Action:ForwardToRecipients
    
- Action:MarkImportance
    
- Action:MarkAsRead
    
- Action:MoveToFolder
    
- Action:PermanentDelete
    
- Action:RedirectToRecipients
    
- Action:SendSMSAlertToRecipients
    
- Action:ServerReplyWithMessage
    
- Action:StopProcessingRules
    
- IsEnabled
    
- IsInError
    
- Conditions
    
- Exceptions
    
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

