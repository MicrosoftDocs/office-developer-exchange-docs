---
title: "Contains"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Contains
api_type:
- schema
ms.assetid: 476d059d-c243-43e9-b475-319fc413ade2
description: "The Contains element represents a search expression that determines whether a given property contains the supplied constant string value."
---

# Contains

The **Contains** element represents a search expression that determines whether a given property contains the supplied constant string value. 
  
```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <FieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <ExtendedFieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <IndexedFieldURI/>
   <Constant/>
</Contains>
```


**ContainsExpressionType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ContainmentMode** <br/> |Identifies the boundaries of a search.  <br/> |
|**ContainmentComparison** <br/> |Determines whether the search ignores cases and spaces.  <br/> |
   
#### ContainmentMode attribute values

|**Value**|**Description**|
|:-----|:-----|
|FullString  <br/> |The comparison is between the full string and the constant. The property value and the supplied constant are precisely the same.  <br/> |
|Prefixed  <br/> |The comparison is between the string prefix and the constant.  <br/> |
|Substring  <br/> |The comparison is between a substring of the string and the constant.  <br/> |
|PrefixOnWords  <br/> |The comparison is between a prefix on individual words in the string and the constant.  <br/> |
|ExactPhrase  <br/> |The comparison is between an exact phrase in the string and the constant.  <br/> |
   
#### ContainmentComparison attribute values

|**Value**|**Description**|
|:-----|:-----|
|Exact  <br/> |The comparison must be exact.  <br/> |
|IgnoreCase  <br/> |The comparison ignores casing.  <br/> |
|IgnoreNonSpacingCharacters  <br/> |The comparison ignores non-spacing characters.  <br/> |
|Loose  <br/> |To be removed.  <br/> |
|IgnoreCaseAndNonSpacingCharacters  <br/> |The comparison ignores casing and non-spacing characters.  <br/> |
|LooseAndIgnoreCase  <br/> |To be removed.  <br/> |
|LooseAndIgnoreNonSpace  <br/> |To be removed.  <br/> |
|LooseAndIgnoreCaseAndIgnoreNonSpace  <br/> |To be removed.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifies frequently referenced properties by URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifies individual members of a dictionary.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifies MAPI properties.  <br/> |
|[Constant](constant.md) <br/> |Identifies a constant value in a restriction.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.  <br/> |
|[Not](not.md) <br/> |Represents a search expression that negates the Boolean value of the search expression it contains.  <br/> |
|[And](and.md) <br/> |Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions. The result of the And operation is **true** if all of the search expressions contained within the And are **true**.  <br/> |
|[Or](or.md) <br/> |Represents a search expression that performs a logical OR on the search expression it contains. The [Or](or.md) element will return **true** if any of its children return **true**.  <br/> |
   
## Remarks

The attributes are used to determine how the elements are matched.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

