---
title: "FieldURIOrConstant"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FieldURIOrConstant
api_type:
- schema
ms.assetid: 89d7a87e-7c93-49b8-83ec-8798e08c1052
description: "The FieldURIOrConstant element represents either a property or a constant value to be used when comparing with another property."
---

# FieldURIOrConstant

The **FieldURIOrConstant** element represents either a property or a constant value to be used when comparing with another property. 
  
```xml
<FieldURIOrConstant>
   <Constant/>
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
    <IndexedFieldURI/> 
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
   <FieldURI/>
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
   <ExtendedFieldURI/> 
</FieldURIOrConstant>
```

**FieldURIOrConstantType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Constant](constant.md) <br/> |Identifies a constant value in a restriction.  <br/> |
|[FieldURI](fielduri.md) <br/> |Identifies frequently referenced properties by URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifies individual members of a dictionary.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifies MAPI properties.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[IsEqualTo](isequalto.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and evaluates to true if they are equal.  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater.  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater than or equal to the second value or property.  <br/> |
|[IsLessThan](islessthan.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than the second value or property.  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than or equal to the second value or property.  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns true if the values are not the same.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Example

The following XML example shows the FieldURIOrConstant element used with both a constant and field URI.
  
```xml
<Restriction>
  <Or xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
    <IsEqualTo>
      <FieldURI FieldURI="item:DateTimeCreated"/>
      <FieldURIOrConstant>
        <FieldURI FieldURI="item:DateTimeReceived"/>
      </FieldURIOrConstant>
    </IsEqualTo>
    <IsEqualTo>
      <FieldURI FieldURI="item:Subject"/>
      <FieldURIOrConstant>
        <Constant Value="Here is a test message"/>
      </FieldURIOrConstant>
    </IsEqualTo>
  </Or>
</Restriction>
```

## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

