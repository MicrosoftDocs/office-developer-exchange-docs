---
title: "UnresolvedEntry"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- UnresolvedEntry
api_type:
- schema
ms.assetid: 5ac6116a-3b24-40f8-a877-dbe9a6935919
description: "The UnresolvedEntry element contains the name of a contact or distribution list to resolve."
---

# UnresolvedEntry

The **UnresolvedEntry** element contains the name of a contact or distribution list to resolve. 
  
[ResolveNames](resolvenames.md)
  
[UnresolvedEntry](unresolvedentry.md)
  
```xml
<UnresolvedEntry/>
```

 **NonEmptyStringType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResolveNames](resolvenames.md) <br/> |Defines a request to resolve ambiguous names.  <br/> |
   
## Text value

The text value represents the name of a public contact or distribution list. The minimum length of the string is one character.
  
## Remarks

The text value of this element is used to resolve names against the following fields:
  
- First name
    
- Last name
    
- Display name
    
- Full name
    
- Office
    
- Alias
    
- SMTP address
    
Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array. The [ResolveNames operation](resolvenames-operation.md) performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com". If you don't specify a routing type, the **ResolveNames** operation will default to the routing type of smtp, match it to a primary SMTP address property, and not search the multivalue array. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[ResolveNames operation](resolvenames-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

