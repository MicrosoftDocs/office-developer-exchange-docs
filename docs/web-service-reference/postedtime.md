---
title: "PostedTime"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- PostedTime
api_type:
- schema
ms.assetid: e8b3813c-fc7e-4674-a4c6-6818c13d2bcf
description: "The PostedTime element represents the time at which a PostItem was posted. This element is read-only. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# PostedTime

The **PostedTime** element represents the time at which a [PostItem](postitem.md) was posted. This element is read-only. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<PostedTime/>
```

 **dateTime**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[PostItem](postitem.md) <br/> |Represents a PostItem in the Exchange store. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Text value

The text value is a dateTime that represents when a **PostItem** was posted. This property is read-only. 
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
