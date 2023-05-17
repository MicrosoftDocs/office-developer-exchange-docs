---
title: "DelegateUser"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DelegateUser
api_type:
- schema
ms.assetid: aac4e74e-f69b-4c41-a0c9-489610330fbf
description: "The DelegateUser element identifies a single delegate to add or update in a mailbox or a delegate returned in a delegate management response. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# DelegateUser

The **DelegateUser** element identifies a single delegate to add or update in a mailbox or a delegate returned in a delegate management response. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<DelegateUser>
   <UserId/>
   <DelegatePermissions/>
   <ReceiveCopiesOfMeetingMessages/>
   <ViewPrivateItems/>
</DelegateUser>
```

**DelegateUserType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[UserId](userid.md) <br/> |Identifies the delegate. This element was introduced in Exchange 2007 SP1.  <br/> |
|[DelegatePermissions](delegatepermissions.md) <br/> |Contains the delegate permission level settings. This element was introduced in Exchange 2007 SP1.  <br/> |
|[ReceiveCopiesOfMeetingMessages](receivecopiesofmeetingmessages.md) <br/> |Indicates whether a delegate receives copies of meeting-related messages that are addressed to the principal. This element was introduced in Exchange 2007 SP1.  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |Indicates whether a delegate has permission to view private calendar items in the principal's mailbox. This element was introduced in Exchange 2007 SP1.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DelegateUsers](delegateusers.md) <br/> |Contains the identities of delegates to add or update in a mailbox.  <br/> |
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |Contains response messages for delegate management operations. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [AddDelegate operation](adddelegate-operation.md) 
- [UpdateDelegate operation](updatedelegate-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
- [Adding Delegates](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

