---
title: "DirectoryId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 4958764f-64dd-4ae7-ade1-0255cb414fcc
description: "The DirectoryId element contains the directory ID of a contact."
---

# DirectoryId

The **DirectoryId** element contains the directory ID of a contact. 
  
```XML
<DirectoryId/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element name**|**Description**|
|:-----|:-----|
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
   
## Text value

The text value is a string that represents the directory ID of the contact.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
- [Creating Contacts (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

