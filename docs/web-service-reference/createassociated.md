---
title: "CreateAssociated"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CreateAssociated
api_type:
- schema
ms.assetid: 742a6136-6015-4924-bae4-f3868127e966
description: "The CreateAssociated element indicates whether a client can create an associated contents table. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# CreateAssociated

The **CreateAssociated** element indicates whether a client can create an associated contents table. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<CreateAssociated>true or false</CreateAssociated>
```

 **boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[EffectiveRights](effectiverights.md) <br/> |Contains the rights of the client based on the permission settings for the item or folder. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Text value

A text value of **true** indicates that a client can create an associated contents table. 
  
## Remarks

This property is only used on folder objects.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

