---
title: "UpdateDelegate"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- UpdateDelegate
api_type:
- schema
ms.assetid: c6ae99c4-18b0-4136-90ab-12cf15e15f91
description: "The UpdateDelegate element defines a request to update delegates in a mailbox. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# UpdateDelegate

The **UpdateDelegate** element defines a request to update delegates in a mailbox. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<UpdateDelegate>
      <DelegateUsers/>
   <DeliverMeetingRequests/>
      <Mailbox/>
</UpdateDelegate>
```

 **UpdateDelegateType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[DelegateUsers](delegateusers.md) <br/> |Contains an array of [DelegateUser](delegateuser.md) elements that identify the delegates and the updates to apply to the delegates. This element was introduced in Exchange 2007 SP1.  <br/> |
|[DeliverMeetingRequests](delivermeetingrequests.md) <br/> |Defines how meeting requests are handled between the delegate and the principal. This element was introduced in Exchange 2007 SP1.  <br/> |
|[Mailbox](mailbox.md) <br/> |Identifies a mail-enabled Active Directory directory service object.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [UpdateDelegate operation](updatedelegate-operation.md)

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
