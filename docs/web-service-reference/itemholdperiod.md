---
title: "ItemHoldPeriod"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 30369db5-4d45-40e8-bc83-3236667fc404
description: "The ItemHoldPeriod element specifies the amount of time to hold content that matches the mailbox query."
---

# ItemHoldPeriod

The **ItemHoldPeriod** element specifies the amount of time to hold content that matches the mailbox query. 
  
```XML
<ItemHoldPeriod/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[SetHoldOnMailboxes](setholdonmailboxes.md)
  
## Text value

The text value can be "Unlimited" or the string value of any [Timespan](https://msdn.microsoft.com/library/1ecy8h51%28v=vs.110%29.aspx) value. 
  
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

- [SetHoldOnMailboxes](setholdonmailboxes.md)

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
