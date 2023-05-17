---
title: "Exceptions"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Exceptions
api_type:
- schema
ms.assetid: 7cd63ac2-3441-4ed4-915b-6f90af4b28fc
description: "The Exceptions element identifies the exceptions that represent all the available rule exception conditions for an Inbox rule."
---

# Exceptions

The **Exceptions** element identifies the exceptions that represent all the available rule exception conditions for an Inbox rule. 
  
```XML
<Conditions>
   <Categories/>
   <ContainsBodyStrings/>
   <ContainsHeaderStrings/>
   <ContainsRecipientStrings/>
   <ContainsSenderStrings/>
   <ContainsSubjectOrBodyStrings/>
   <ContainsSubjectStrings/>
   <FlaggedForAction/>
   <FromAddresses/>
   <FromConnectedAccounts/>
   <HasAttachments/>
   <Importance/>
   <IsApprovalRequest/>
   <IsAutomaticForward/>
   <IsAutomaticReply/>
   <IsEncrypted/>
   <IsMeetingRequest/>
   <IsMeetingResponse/>
   <IsNDR/>
   <IsPermissionControlled/>
   <IsReadReceipt/>
   <IsSigned/>
   <IsVoicemail/>
   <ItemClasses/>
   <MessageClassifications/>
   <NotSentToMe/>
   <SentCcMe/>
   <SentOnlyToMe/>
   <SentToAddresses/>
   <SentToMe/>
   <SentToOrCcMe/>
   <Sensitivity/>
   <WithinDateRange/>
   <WithinSizeRange/>
</Conditions>
```

 **RulePredicatesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |Contains the categories that must be applied to an incoming message in order for the condition or exception to apply.  <br/> |
|[ContainsBodyStrings](containsbodystrings.md) <br/> |Indicates the strings that must appear in the body of incoming messages in order for the condition or exception to apply.  <br/> |
|[ContainsHeaderStrings](containsheaderstrings.md) <br/> |Indicaqtes the strings that must appear in the headers of incoming messages in order for the condition or exception to apply.  <br/> |
|[ContainsRecipientStrings](containsrecipientstrings.md) <br/> |Indicates the strings that must appear in either the **ToRecipients** or **CcRecipients** properties of incoming messages in order for the condition or exception to apply.  <br/> |
|[ContainsSenderStrings](containssenderstrings.md) <br/> |Indicates the strings that must appear in the **From** property of incoming messages in order for the condition or exception to apply.  <br/> |
|[ContainsSubjectOrBodyStrings](containssubjectorbodystrings.md) <br/> |Indicates the strings that must appear in either the body or the subject of incoming messages in order for the condition or exception to apply.  <br/> |
|[ContainsSubjectStrings](containssubjectstrings.md) <br/> |Indicates the strings that must appear in the subject of incoming messages in order for the condition or exception to apply.  <br/> |
|[FlaggedForAction](flaggedforaction.md) <br/> |Specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.  <br/> |
|[FromAddresses](fromaddresses.md) <br/> |Indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply.  <br/> |
|[FromConnectedAccounts](fromconnectedaccounts.md) <br/> |Represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Indicates whether incoming messages have to have attachments in order for the condition or exception to apply.  <br/> |
|[Importance](importance.md) <br/> |Specifies the importance that is stamped on incoming messages in order for the condition or exception to apply.  <br/> |
|[IsApprovalRequest](isapprovalrequest.md) <br/> |Indicates whether incoming messages must be approval requests in order for the condition or exception to apply.  <br/> |
|[IsAutomaticForward](isautomaticforward.md) <br/> |Indicates whether incoming messages must be automatic forwards in order for the condition or exception to apply.  <br/> |
|[IsAutomaticReply](isautomaticreply.md) <br/> |Indicates whether incoming messages must be automatic replies in order for the condition or exception to apply.  <br/> |
|[IsEncrypted](isencrypted.md) <br/> |Indicates whether incoming messages must be S/MIME encrypted in order for the condition or exception to apply.  <br/> |
|[IsMeetingRequest](ismeetingrequest.md) <br/> |Indicates whether incoming messages must be meeting requests in order for the condition or exception to apply.  <br/> |
|[IsMeetingResponse](ismeetingresponse.md) <br/> |Indicates whether incoming messages must be meeting responses in order for the condition or exception to apply.  <br/> |
|[IsNDR](isndr.md) <br/> |Indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.  <br/> |
|[IsPermissionControlled](ispermissioncontrolled.md) <br/> |Indicates whether incoming messages must be permission controlled (RMS protected) in order for the condition or exception to apply  <br/> |
|[IsReadReceipt](isreadreceipt.md) <br/> |Indicates whether incoming messages must be read receipts in order for the condition or exception to apply.  <br/> |
|[IsSigned](issigned.md) <br/> |Indicates whether incoming messages must be S/MIME signed in order for the condition or exception to apply.  <br/> |
|[IsVoicemail](isvoicemail.md) <br/> |Indicates whether incoming messages must be voice mail messages in order for the condition or exception to apply.  <br/> |
|[ItemClasses](itemclasses.md) <br/> |Represents the item classes that must be stamped on incoming messages in order for the condition or exception to apply.  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |Represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply.  <br/> |
|[NotSentToMe](notsenttome.md) <br/> |Indicates whether the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.  <br/> |
|[SentCcMe](sentccme.md) <br/> |Indicates whether the owner of the mailbox has to be in the **CcRecipients** property of incoming messages in order for the condition or exception to apply.  <br/> |
|[SentOnlyToMe](sentonlytome.md) <br/> |Indicates whether the owner of the mailbox has to be the only one in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.  <br/> |
|[SentToAddresses](senttoaddresses.md) <br/> |Indicates the e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.  <br/> |
|[SentToMe](senttome.md) <br/> |Indicates whether the owner of the mailbox has to be in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.  <br/> |
|[SentToOrCcMe](senttoorccme.md) <br/> |Indicates whether the owner of the mailbox has to be in either a **ToRecipients** or **CcRecipients** property of incoming messages in order for the condition or exception to apply.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Indicates the sensitivity that must be stamped on incoming messages in order for the condition or exception to apply.  <br/> |
|[WithinDateRange](withindaterange.md) <br/> |Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.  <br/> |
|[WithinSizeRange](withinsizerange.md) <br/> |Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Rule (RuleType)](rule-ruletype.md) <br/> |Contains a single rule and represents a rule in a user's mailbox.  <br/> |
   
## Text value

None.
  
## Remarks

The rule predicates are used as rule conditions or exceptions.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[Conditions](conditions.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

