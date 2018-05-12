---
title: "ImAddresses"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ImAddresses
api_type:
- schema
ms.assetid: 29f614a7-7fe6-47fa-b5f2-8feff106aa99
description: "The ImAddresses element represents a collection of instant messaging addresses for a contact."
---

# ImAddresses

The **ImAddresses** element represents a collection of instant messaging addresses for a contact. 
  
```
<ImAddresses>
   <Entry/>
</ImAddresses>
```

 **ImAddressDictionaryType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Entry (IMAddress)](entry-imaddress.md) <br/> |Represents an instant messaging address for a contact.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
   
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



[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

