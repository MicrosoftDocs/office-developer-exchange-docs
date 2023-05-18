---
title: "RemoveDelegate"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RemoveDelegate
api_type:
- schema
ms.assetid: f21c5171-62e7-47c8-99b1-22e1ff5883bb
description: "The RemoveDelegate element defines a request to remove delegates from a mailbox. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# RemoveDelegate

The **RemoveDelegate** element defines a request to remove delegates from a mailbox. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<RemoveDelegate>
      <Mailbox/>
   <UserIds/>
</RemoveDelegate>
```

 **RemoveDelegateType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |Identifies the principal's mailbox.  <br/> |
|[UserIds](userids.md) <br/> |Contains an array of delegate users to remove from a principal's mailbox. This element was introduced in Exchange 2007 SP1.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[RemoveDelegate operation](removedelegate-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

