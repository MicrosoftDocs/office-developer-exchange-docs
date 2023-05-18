---
title: "Nickname"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Nickname
api_type:
- schema
ms.assetid: 3d35b207-d28c-4f3f-8b00-55339d30d19a
description: "The Nickname element represents the nickname of a contact."
---

# Nickname

The **Nickname** element represents the nickname of a contact. 
  
```xml
<Nickname/>
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
|[CompleteName](completename.md) <br/> |Represents the complete name of a contact.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
   
## Text value

The **Nickname** element takes a string value. 
  
## Remarks

This element is optional.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
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

