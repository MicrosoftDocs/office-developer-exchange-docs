---
title: "UpdateInboxRules"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- UpdateInboxRules
api_type:
- schema
ms.assetid: d220064f-ff4d-4537-8077-adf94f2cbdbd
description: "The UpdateInboxRules element defines a request to update the Inbox rules in a mailbox in the server store."
---

# UpdateInboxRules

The **UpdateInboxRules** element defines a request to update the Inbox rules in a mailbox in the server store. 
  
```XML
<UpdateInboxRules>
   <MailboxSmtpAddress/>
   <RemoveOutlookRuleBlob/>
   <Operations/>
</UpdateInboxRules>
```

 **UpdateInboxRulesRequestType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MailboxSmtpAddress](mailboxsmtpaddress.md) <br/> |Represents the SMTP address of the user whose Inbox rules are to be created, modified, or deleted.  <br/> |
|[RemoveOutlookRuleBlob](removeoutlookruleblob.md) <br/> |Indicates whether to remove the Microsoft Outlook rule blob.  <br/> |
|[Operations](operations.md) <br/> |Contains an array of rule operations that can be performed on an Inbox.  <br/> |
   
### Parent elements

None.
  
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[UpdateInboxRules operation](updateinboxrules-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

