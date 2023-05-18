---
title: "Restriction"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Restriction
api_type:
- schema
ms.assetid: 77f19014-d112-4999-8e83-ecc32a117a73
description: "The Restriction element represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations."
---

# Restriction

The **Restriction** element represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations. 
  
```xml
<Restriction>
   <SearchExpression/>
</Restriction>
```

 **RestrictionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[And](and.md) <br/> |Represents a search expression that enables you to perform a Boolean **AND** operation between two or more search expressions.  <br/> |
|[Contains](contains.md) <br/> |Represents a search expression that determines whether a given property contains the supplied constant string value.  <br/> |
|[Excludes](excludes.md) <br/> |Performs a bitwise mask of the properties.  <br/> |
|[Exists](exists.md) <br/> |Represents a search expression that returns **true** if the supplied property exists on an item.  <br/> |
|[IsEqualTo](isequalto.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and evaluates to **true** if they are equal.  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than the value or property.  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than or equal to the value or property.  <br/> |
|[IsLessThan](islessthan.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than the value or property.  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than or equal to the value or property.  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns **true** if the values are not the same.  <br/> |
|[Not](not.md) <br/> |Represents a search expression that negates the Boolean value of the search expression it contains.  <br/> |
|[Or](or.md) <br/> |Represents a search expression that performs a logical **OR** operation on the search expression it contains. The **Or** element will return **true** if any of its children return **true**.  <br/> |
|[SearchExpression](searchexpression.md) <br/> |Represents the substituted element within a restriction. This element is not used in an XML instance document.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Defines a request to identify folders in a mailbox.  <br/> |
|[FindItem](finditem.md) <br/> |Defines a request to find items in a mailbox.  <br/> |
|[SearchParameters](searchparameters.md) <br/> |Represents the parameters that define a search folder.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

