---
title: "RetentionPolicyType"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: abce5b3e-971d-42fc-aeea-caa7202214de
description: "The RetentionPolicyType element specifies the retention policy type applied to items in a conversation."
---

# RetentionPolicyType

The **RetentionPolicyType** element specifies the retention policy type applied to items in a conversation. 
  
```XML
<RetentionPolicyType> Delete | Archive </RetentionPolicyType>
```

 **RetentionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[ConversationAction](conversationaction.md)
  
## Text value

The text value of the **RetentionPolicyType** element is the retention type applied to items in a conversation. The text value of **Delete** indicates that the items in the conversation are deleted when the retention hold expires. The text value of **Archive** indicates that the items in the conversation are moved to the archive mailbox when the retention hold expires. 
  
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
   