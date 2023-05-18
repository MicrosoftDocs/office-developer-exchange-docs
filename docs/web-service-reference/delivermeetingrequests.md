---
title: "DeliverMeetingRequests"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DeliverMeetingRequests
api_type:
- schema
ms.assetid: 04b999af-0b27-4e6d-a8b1-400955a1afaa
description: "The DeliverMeetingRequests element defines how meeting requests are handled between the delegate and the principal. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# DeliverMeetingRequests

The **DeliverMeetingRequests** element defines how meeting requests are handled between the delegate and the principal. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```XML
<DeliverMeetingRequests>DelegatesOnly or DelegatesAndMe or DelegatesAndSendInformationToMe or NoForward</DeliverMeetingRequests>
```

 **DeliverMeetingRequestsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AddDelegate](adddelegate.md) <br/> |Defines a request to add delegates to a mailbox. This element was introduced in Exchange 2007 SP1.  <br/> |
|[UpdateDelegate](updatedelegate.md) <br/> |Defines a request to update delegates in a mailbox. This element was introduced in Exchange 2007 SP1.  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Contains the status and result of a GetDelegate request. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Text value

The following table lists the possible values for the **DeliverMeetingRequests** element. 
  
**DeliverMeetingRequests element values**

|**Value**|**Description**|
|:-----|:-----|
|DelegatesOnly  <br/> |Meeting requests are forwarded to the delegate and moved to the Deleted Items folder in the principal's mailbox.  <br/> |
|DelegatesAndMe  <br/> |Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox.  <br/> |
|DelegatesAndSendInformationToMe  <br/> |Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox, but the Accept, Tentative, and Decline buttons do not appear in the Microsoft Office Outlook reading pane.  <br/> |
|NoForward  <br/> |Meeting requests are not forwarded to the delegate.  <br/> |
   
## Remarks

The **DeliverMeetingRequests** setting affects all delegates in a principal's mailbox. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [AddDelegate operation](adddelegate-operation.md)  
- [UpdateDelegate operation](updatedelegate-operation.md)  
- [GetDelegate operation](getdelegate-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
- [Adding Delegates](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

