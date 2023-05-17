---
title: "DelegationState"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DelegationState
api_type:
- schema
ms.assetid: 9dbb83ed-1ded-48f3-8e06-2489fc8b28d5
description: "The DelegationState element represents the status of a delegated task."
---

# DelegationState

The **DelegationState** element represents the status of a delegated task. 
  
```xml
<DelegationState/>
```

**TaskDelegateStateType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
   
## Text value

This is a read-only property. The following are the possible values:
  
- NoMatch
    
- OwnNew
    
- Owned
    
- Accepted
    
- Declined
    
- Max
    
## Remarks

Exchange Web Services in Microsoft Exchange Server 2007 does not support task assignments.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

