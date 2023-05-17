---
title: "IsEqualTo"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- IsEqualTo
api_type:
- schema
ms.assetid: 48e7e067-049c-4184-8026-071e6f558e8a
description: "The IsEqualTo element represents a search expression that compares a property with either a constant value or another property and evaluates to true if they are equal."
---

# IsEqualTo

The **IsEqualTo** element represents a search expression that compares a property with either a constant value or another property and evaluates to true if they are equal. 
  
```xml
<IsEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsEqualTo>
```

```xml
<IsEqualTo>
   <ExtendedFieldURI/>
   <FieldURIOrConstant/>
</IsEqualTo>
```

```xml
<IsEqualTo>
   <IndexedFieldURI/> 
   <FieldURIOrConstant/>
</IsEqualTo>
```

**IsEqualToType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifies frequently referenced properties by URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifies individual members of a dictionary.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifies MAPI properties.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Represents either a property or a constant value to be used when comparing with another property.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.  <br/> |
|[Not](not.md) <br/> |Represents a search expression that negates the Boolean value of the search expression that it contains.  <br/> |
|[And](and.md) <br/> |Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions. The result of the And operation is **true** if all of the search expressions contained within the And are **true**.  <br/> |
|[Or](or.md) <br/> |Represents a search expression that performs a logical OR on the search expression that it contains. [Or](or.md) will return true if any of its children return true. **Or** must have two or more children.  <br/> |
   
## Remarks

To perform string comparisons, consider using the [Contains](contains.md) element, as it provides options for matching parameters, such as case and white space. Use the [Not](not.md) element in conjunction with the [Contains](contains.md) element to negate the result. 
  
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

