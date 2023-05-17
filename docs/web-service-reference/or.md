---
title: "Or" 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Or
api_type:
- schema
ms.assetid: 4876d83a-73a3-4953-9d95-3048e6b76ccb
description: "The Or element represents a search expression that performs a logical OR on the search expression that it contains. Or will return true if any of its children return true. Or must have two or more children."
---

# Or

The **Or** element represents a search expression that performs a logical **OR** on the search expression that it contains. **Or** will return **true** if any of its children return **true**. **Or** must have two or more children. 
  
```xml
<Or>
   <SearchExpression/>
   <SearchExpression/>
</Or>
```

 **OrType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> | Represents the base class for expressions within a restriction. <br/><br/>One of the following elements must be substituted for the **SearchExpression** element: <br/> <br/>- [Exists](exists.md) <br/>- [Excludes](excludes.md) <br/>- [IsEqualTo](isequalto.md) <br/>- [IsNotEqualTo](isnotequalto.md) <br/>- [IsGreaterThan](isgreaterthan.md) <br/>- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/>- [IsLessThan](islessthan.md) <br/>- [IsLessThanOrEqualTo](islessthanorequalto.md) <br/>- [Contains](contains.md) <br/>- [Not](not.md) <br/>- [And](and.md) <br/>- **Or** <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.  <br/> |
|[Not](not.md) <br/> |Represents a search expression that negates the Boolean value of the search expression that it contains.  <br/> |
|[And](and.md) <br/> |Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions. The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.  <br/> |
|**Or** <br/> |Represents a search expression that performs a logical **OR** operation on the search expression that it contains. **Or** will return **true** if any of its children return **true**. **Or** must have two or more children.  <br/> |
   
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
