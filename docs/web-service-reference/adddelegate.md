---
title: "AddDelegate"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AddDelegate
api_type:
- schema
ms.assetid: 646fb994-229e-4d90-8b95-6541191cb3ae
description: "The AddDelegate element defines a request to add delegates to a mailbox. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# AddDelegate

The **AddDelegate** element defines a request to add delegates to a mailbox. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```
<AddDelegate>
   <DelegateUsers/>
   <DeliverMeetingRequests/>
   <Mailbox/>
</AddDelegate>
```

 **AddDelegateType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[DelegateUsers](delegateusers.md) <br/> |Contains the identities of delegates to add to or update in a mailbox. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|[DeliverMeetingRequests](delivermeetingrequests.md) <br/> |Defines how meeting requests are handled between the delegate and the principal. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|[Mailbox](mailbox.md) <br/> |Identifies a mail-enabled Active Directory directory service object.  <br/> |
   
#### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[AddDelegate operation](adddelegate-operation.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
#### Other resources

[Adding Delegates](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

