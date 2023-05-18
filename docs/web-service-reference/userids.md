---
title: "UserIds"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- UserIds
api_type:
- schema
ms.assetid: 78a09c3a-1646-4c55-95a2-1109fb11e1c6
description: "The UserIds element contains an array of delegate users to get or remove from a principal's mailbox. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# UserIds

The **UserIds** element contains an array of delegate users to get or remove from a principal's mailbox. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<UserIds>
   <UserId/>
</UserIds>
```

 **ArrayOfUserIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[UserId](userid.md) <br/> |Identifies a delegate to get or remove from a principal's mailbox. This element was introduced in Exchange 2007 SP1.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetDelegate](getdelegate.md) <br/> |Defines a request to get information about delegates to a mailbox. This element was introduced in Exchange 2007 SP1.  <br/> |
|[RemoveDelegate](removedelegate.md) <br/> |Defines a request to remove delegates from a mailbox. This element was introduced in Exchange 2007 SP1.  <br/> |
   
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



[GetDelegate operation](getdelegate-operation.md)
  
[RemoveDelegate operation](removedelegate-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

