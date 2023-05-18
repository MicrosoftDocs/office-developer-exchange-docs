---
title: "ExtendedProperty (PathToExtendedFieldType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: fa620b48-2ce3-437d-b51e-541247eea1d9
description: "The ExtendedProperty element specifies an extended property for the Unified Contact Store."
---

# ExtendedProperty (PathToExtendedFieldType)

The **ExtendedProperty** element specifies an extended property for the Unified Contact Store. 
  
```xml
<ExtendedProperty DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" FieldURI="">
</ExtendedProperty>
```

**PathToExtendedFieldType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|DistinguishedPropertySetId  <br/> |Indicates the distinguished property set identifier. This attribute is optional.  <br/> |
|PropertySetId  <br/> |Indicates the GUID property set identifier. This attribute is optional.  <br/> |
|PropertyTag  <br/> | Represents the property tag minus the type part.<br/><br/>There are two options for representation:  <br/><br/>- Hexadecimal: 0x3fa4  <br/>- Decimal: 0-65535<br/><br/>  This attribute is optional.  <br/> |
|PropertyName  <br/> |String that indicates the property name. This attribute is optional.  <br/> |
|PropertyId  <br/> |Integer that indicates the property identifier. This attribute is optional.  <br/> |
|PropertyType  <br/> |Indicates the property type. This attribute is required.  <br/> |
|FieldURI  <br/> |Indicates the field Uniform Resource Identifier (URI). This attribute is required. For possible values, see the [FieldURI](fielduri.md) element.  <br/> |
   
#### DistinguishedPropertySetId

|**Value**|**Description**|
|:-----|:-----|
|Meeting  <br/> |Indicates a meeting.  <br/> |
|Appointment  <br/> |Indicates an appointment.  <br/> |
|Common  <br/> |Indicates the common property set.  <br/> |
|PublicStrings  <br/> |Indicates public strings.  <br/> |
|Address  <br/> |Indicates an address.  <br/> |
|InternetHeaders  <br/> |Indicates Internet headers.  <br/> |
|CalendarAssistant  <br/> |Indicates the Calendar Assistant.  <br/> |
|UnifiedMessaging  <br/> |Indicates Unified Messaging.  <br/> |
|Task  <br/> |Indicates a task.  <br/> |
   
#### PropertyType

|**Value**|**Description**|
|:-----|:-----|
|ApplicationTime  <br/> |Indicates the application time.  <br/> |
|ApplicationTimeArray  <br/> |Indicates an array of application times.  <br/> |
|Binary  <br/> |Indicates a binary value.  <br/> |
|BinaryArray  <br/> |Indicates an array of binary values.  <br/> |
|Boolean  <br/> |Indicates a Boolean value.  <br/> |
|CLSID  <br/> |Indicates a CLSID.  <br/> |
|CLSIDArray  <br/> |Indicates an array of CLSIDs.  <br/> |
|Currency  <br/> |Indicates a currency value.  <br/> |
|CurrencyArray  <br/> |Indicates an array of currency values.  <br/> |
|Double  <br/> |Indicates a **double**.  <br/> |
|DoubleArray  <br/> |Indicates an array of **double** values.  <br/> |
|Error  <br/> |Indicates an error. This is for error-reporting purposes. It cannot be used in restrictions or for getting or setting values.  <br/> |
|Float  <br/> |Indicates a **float**.  <br/> |
|FloatArray  <br/> |Indicates an array of **float** values.  <br/> |
|Integer  <br/> |Indicates an integer.  <br/> |
|IntegerArray  <br/> |Indicates an array of integers.  <br/> |
|Long  <br/> |Indicates a **long**.  <br/> |
|LongArray  <br/> |Indicates an array of **long** values.  <br/> |
|Null  <br/> |Indicates a null value. This is for error-reporting purposes. It cannot be used in restrictions or for getting or setting values.  <br/> |
|Object  <br/> |Indicates an object. This is for error-reporting purposes. It cannot be used in restrictions or for getting or setting values.  <br/> |
|ObjectArray  <br/> |Indicates an array of objects. This is for error-reporting purposes. It cannot be used in restrictions or for getting or setting values.  <br/> |
|Short  <br/> |Indicates a **short**.  <br/> |
|ShortArray  <br/> |Indicates an array of **short** values.  <br/> |
|SystemTime  <br/> |Indicates a system time value.  <br/> |
|SystemTimeArray  <br/> |Indicates an array of system time values.  <br/> |
|String  <br/> |Indicates a string.  <br/> |
|StringArray  <br/> |Indicates an array of strings.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifies an extended MAPI property.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

