---
title: "Status (MemberStatusType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Status
api_type:
- schema
ms.assetid: 4f8a860b-0a48-4a0d-9a7a-69a0304aa747
description: "The Status element provides information about the status of a distribution list member on the server."
---

# Status (MemberStatusType)

The **Status** element provides information about the status of a distribution list member on the server. 
  
```
<Status>Unrecognized or Normal or Demoted</Status>
```

 **MemberStatusType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Member](member-ex15websvcsotherref.md) <br/> |Represents a member of a distribution list.  <br/> |
   
## Text value

The following table lists the possible values for the **Status** element. 
  
**Status element values**

|**Value**|**Description**|
|:-----|:-----|
|Unrecognized  <br/> |Member information is invalid or unrecognized.  <br/> |
|Normal  <br/> |Member information in a distribution list is in sync with the referenced object.  <br/> |
|Demoted  <br/> |Referenced object is not available.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

