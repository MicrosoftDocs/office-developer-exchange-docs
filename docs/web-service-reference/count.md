---
title: "Count"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Count
api_type:
- schema
ms.assetid: 68314b4a-1e17-4e21-9c2e-224d70ef7a32
description: "The Count element contains the number of conflicts in an UpdateItem operation response."
---

# Count

The [Count](count.md) element contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response. 
  
[UpdateItemResponse](updateitemresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[UpdateItemResponseMessage](updateitemresponsemessage.md)
  
[ConflictResults](conflictresults.md)
  
[Count](count.md)
  
```
<Count/>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ConflictResults](conflictresults.md) <br/> |Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.  <br/> |
   
## Text value

The text value is an integer that represents the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response. 
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[UpdateItem operation](updateitem-operation.md)
  
 **ConflictResultsType**

