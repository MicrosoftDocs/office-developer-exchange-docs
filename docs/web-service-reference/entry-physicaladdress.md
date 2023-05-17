---
title: "Entry (PhysicalAddress)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Entry
api_type:
- schema
ms.assetid: 9e5b6515-453e-4f4c-b55e-6ffefe23c31b
description: "The Entry element describes a single physical address for a contact item."
---

# Entry (PhysicalAddress)

The **Entry** element describes a single physical address for a contact item. 
  
```xml
<Entry Key="">
   <Street/>
   <City/>
   <State/>
   <Country/>
   <PostalCode/>
</Entry>
```

 **PhysicalAddressDictionaryEntryType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Key** <br/> | Identifies a physical address.<br/><br/> The following are the possible values for this attribute:<br/>  <br/>- Business  <br/>- Home  <br/>- Other  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Street](street.md) <br/> |Represents a street address for a contact item.  <br/> |
|[City](city.md) <br/> |Represents the city name that is associated with a contact.  <br/> |
|[State](state-ex15websvcsotherref.md) <br/> |Represents the state of residence for a contact item.  <br/> |
|[CountryOrRegion](countryorregion.md) <br/> |Represents the country or region for a given physical address.  <br/> |
|[PostalCode](postalcode.md) <br/> |Represents the postal code for a contact item.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[PhysicalAddresses](physicaladdresses.md) <br/> |Contains a collection of physical addresses that are associated with a contact.  <br/> |
   
## Remarks

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
- [Creating Contacts (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [Updating Contacts](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [Deleting Contacts](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

