---
title: "DistinguishedUser"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DistinguishedUser
api_type:
- schema
ms.assetid: 9362699d-666a-4acf-8fa1-c6669f0a2ae5
description: "The DistinguishedUser element identifies Anonymous and Default user accounts for delegate access. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# DistinguishedUser

The **DistinguishedUser** element identifies Anonymous and Default user accounts for delegate access. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<DistinguishedUser>Default or Anonymous</DistinguishedUser>
```

 **DistinguishedUserType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[UserId](userid.md) <br/> |Identifies a delegate user or a user who has folder access permissions. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Text value

A text value of **Default** describes the default setting for delegate users who are added to the principal's mailbox. A text value of **Anonymous** describes the delegate access settings that anonymous users have on the principal's mailbox. 
  
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

