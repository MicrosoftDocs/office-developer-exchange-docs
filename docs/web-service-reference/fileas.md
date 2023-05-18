---
title: "FileAs"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FileAs
api_type:
- schema
ms.assetid: df50524e-471c-49d2-89fe-b2d0f61a1365
description: "The FileAs element represents how a contact or distribution list is filed in the Contacts folder."
---

# FileAs

The **FileAs** element represents how a contact or distribution list is filed in the Contacts folder. 
  
```xml
<FileAs/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
   
## Text value

A text value that represents a string is required if this element is used.
  
## Remarks

The **FileAs** element is used to sort contacts and distribution lists by a name other than a full name or company name. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

