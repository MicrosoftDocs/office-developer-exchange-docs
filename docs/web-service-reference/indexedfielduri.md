---
title: "IndexedFieldURI"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- IndexedFieldURI
api_type:
- schema
ms.assetid: 5c9cd0b5-7eca-480a-8730-fe98b1779afa
description: "The IndexedFieldURI element identifies individual members of a dictionary."
---

# IndexedFieldURI

The **IndexedFieldURI** element identifies individual members of a dictionary. 
  
```xml
<IndexedFieldURI FieldURI="" FieldIndex="" />
```

 **PathToIndexedFieldType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**FieldURI** <br/> |Identifies the dictionary that contains the member to return. This attribute is required.  <br/> |
|**FieldIndex** <br/> |Identifies the member of the dictionary to return. This attribute is required.  <br/> |
   
#### FieldURI Attribute

|**Value**|**Description**|
|:-----|:-----|
|item:InternetMessageHeader  <br/> |Represents the message header of an item.  <br/> |
|contacts:ImAddress  <br/> |Represents the instant messaging address of a contact.  <br/> |
|contacts:PhysicalAddress:Street  <br/> |Represents the street address of a contact.  <br/> |
|contacts:PhysicalAddress:City  <br/> |Represents the city of a contact.  <br/> |
|contacts:PhysicalAddress:State  <br/> |Represents the state of a contact.  <br/> |
|contacts:PhysicalAddress:Country  <br/> |Represents the country/region of a contact.  <br/> |
|contacts:PhysicalAddress:PostalCode  <br/> |Represents the postal code of a contact.  <br/> |
|contacts:PhoneNumber  <br/> |Represents the phone number of a contact.  <br/> |
|contacts:EmailAddress  <br/> |Represents the e-mail address of a contact.  <br/> |
|distributionlist:Members:Member  <br/> |Represents a member of a distribution list.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AdditionalProperties](additionalproperties.md) <br/> |Identifies additional properties to get, set, or create.  <br/> |
|[AggregateOn](aggregateon.md) <br/> |Represents the property that is used to determine the order of grouped items for a grouped FindItem result set.  <br/> |
|[GroupBy](groupby.md) <br/> |Specifies an arbitrary grouping for FindItem queries.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

