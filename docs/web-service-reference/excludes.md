---
title: "Excludes"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Excludes
api_type:
- schema
ms.assetid: bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1
description: "The Excludes element performs a bitwise mask of the specified property and a supplied value."
---

# Excludes

The **Excludes** element performs a bitwise mask of the specified property and a supplied value. 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <ExtendedFieldURI/> 
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <IndexedFieldURI/> 
   <Bitmask/>
</Excludes>
```

**ExcludesType**

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
|[Bitmask](bitmask.md) <br/> |Represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation. If the bitmask represents a hexadecimal number, it must be prefixed by 0x or 0X. Otherwise, it will be considered a decimal number.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.  <br/> |
|[Not](not.md) <br/> |Represents a search expression that negates the Boolean value of the search expression that it contains.  <br/> |
|[And](and.md) <br/> |Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions. The result of the And operation is **true** if all of the search expressions contained within the And are **true**.  <br/> |
|[Or](or.md) <br/> |Represents a search expression that performs a logical OR on the search expression it contains. The [Or](or.md) element will return **true** if any of its children return **true**.  <br/> |
   
## Remarks

**Excludes** will resolve to **true** if an AND operation performed on the following resolves to 0: 
  
1. The bitwise value for the property
    
2. The bitmask value for the property
    
**Excludes** can only be applied to a property that has an integer value. If the property type is anything other than an integer, an error code of **ErrorUnsupportedPathForQuery** is returned in the response. 
  
You can perform the reverse operation by calling Not(Excludes).
  
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

