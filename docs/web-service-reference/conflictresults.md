---
title: "ConflictResults"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ConflictResults
api_type:
- schema
ms.assetid: 08cdd547-4de7-4c7a-b60f-e618dc217d20
description: "The ConflictResults element contains the number of conflicts in an UpdateItem operation response."
---

# ConflictResults

The [ConflictResults](conflictresults.md) element contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response. 
  
[UpdateItemResponse](updateitemresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[UpdateItemResponseMessage](updateitemresponsemessage.md)
  
[ConflictResults](conflictresults.md)
  
```xml
<ConflictResults>
   <Count/>
</ConflictResults>
```

 **ConflictResultsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Count](count.md) <br/> |Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[UpdateItem operation](updateitem-operation.md)
  
 **ConflictResultsType**

