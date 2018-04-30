---
title: "MaxChangesReturned"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
api_name:
- MaxChangesReturned
api_type:
- schema
ms.assetid: f471db84-a666-4dfa-9993-8ca9113a0384
description: "The MaxChangesReturned element describes the maximum number of changes that can be returned in a synchronization response."
---

# MaxChangesReturned

The **MaxChangesReturned** element describes the maximum number of changes that can be returned in a synchronization response. 
  
[SyncFolderItems](syncfolderitems.md)
  
[MaxChangesReturned](maxchangesreturned.md)
  
```
<MaxChangesReturned/>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SyncFolderItems](syncfolderitems.md) <br/> |Defines a request to synchronize items in an Exchange store folder.  <br/> |
   
## Text value

The text value represents an integer that describes the maximum number of items that are returned in a single synchronization call. The value must be between 1 and 512, inclusive.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

#### Reference

[SyncFolderItems operation](syncfolderitems-operation.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

