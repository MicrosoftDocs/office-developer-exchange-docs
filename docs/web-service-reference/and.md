---
title: "And"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- And
api_type:
- schema
ms.assetid: 790246c2-37ad-49a8-91b9-6186d743b011
description: "The And element represents a search expression that allows you to perform a Boolean AND operation between two or more search expressions. The result of the AND operation is true if all the search expressions contained within the And element are true."
---

# And

The **And** element represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions. The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.
  
```xml
<And>
   <SearchExpression/>
   <SearchExpression/>
</And>
```

 **AndType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> | Represents the base class for expressions within a restriction. There must be two or more search expressions in an And operation.<br/><br/>  One of the following elements must be substituted for the **SearchExpression** element:<ul><li> [Exists](exists.md)</li><li>[Excludes](excludes.md)</li><li>[IsEqualTo](isequalto.md)</li><li>[IsNotEqualTo](isnotequalto.md)</li><li>[IsGreaterThan](isgreaterthan.md)</li><li>[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</li><li>[IsLessThan](islessthan.md)</li><li>[IsLessThanOrEqualTo](islessthanorequalto.md)</li><li>[Contains](contains.md)</li><li>[Not](not.md)</li><li>**And**</li><li>[Or](or.md) </li></ul> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.  <br/> |
|[Not](not.md) <br/> |Represents a search expression that negates the Boolean value of the search expression that it contains.  <br/> |
|**And** <br/> |Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions. The result of the **AND** operation is **true** if all of the search expressions contained within the **And** element are **true**.  <br/> |
|[Or](or.md) <br/> |Represents a search expression that performs a logical **OR** operation on the search expression that it contains. **Or** will return **true** if any of its children return **true**. **Or** must have two or more children.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

