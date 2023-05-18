---
title: "RemoveOutlookRuleBlob"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RemoveOutlookRuleBlob
api_type:
- schema
ms.assetid: 69614475-8bd3-4475-b988-614fe9cad8ef
description: "The RemoveOutlookRuleBlob element indicates whether to remove the Microsoft Outlook rule blob."
---

# RemoveOutlookRuleBlob

The **RemoveOutlookRuleBlob** element indicates whether to remove the Microsoft Outlook rule blob. 
  
[UpdateInboxRules](updateinboxrules.md)
  
[RemoveOutlookRuleBlob](removeoutlookruleblob.md)
  
```XML
<RemoveOutlookRuleBlob>true | false</RemoveOutlookRuleBlob>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[UpdateInboxRules](updateinboxrules.md) <br/> |Defines a request to update the Inbox rules in a mailbox in the server store.  <br/> |
   
## Text value

A text value of **true** indicates that the Outlook rule blob should be removed. A text value of **false** indicates that the Outlook rule blob should not be removed. 
  
## Remarks

Set this element to **true** to allow for an Inbox rule update. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also



[UpdateInboxRules operation](updateinboxrules-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

