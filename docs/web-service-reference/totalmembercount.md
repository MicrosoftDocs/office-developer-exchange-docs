---
title: "TotalMemberCount"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- TotalMemberCount
api_type:
- schema
ms.assetid: fa86bfa6-10aa-4736-938c-9a23525aef8d
description: "The TotalMemberCount element represents the count of all members in a group."
---

# TotalMemberCount

The **TotalMemberCount** element represents the count of all members in a group. 
  
```XML
<TotalMemberCount/>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MailTips](mailtips.md) <br/> |Represents values for various types of mail tips.  <br/> |
   
## Text value

The text value is an integer that represents the number of members in a group.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
