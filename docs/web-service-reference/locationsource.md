---
title: "LocationSource"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: fc4d77d5-6200-4cf3-848a-1088fec0e0d6
description: "The LocationSource element specifies information about the origin of the associated postal address, for example, a contact or a telephone book."
---

# LocationSource

The **LocationSource** element specifies information about the origin of the associated postal address, for example, a contact or a telephone book. 
  
```XML
<LocationSource> None | LocationServices | PhonebookServices | Device | Contact | Resource </LocationSource>
```

 **LocationSourceType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[Value (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)
  
## Text value

The text values for the **LocationSource** element are listed in the following table: 
  
**LocationSource element text values**

|**Value**|**Description**|
|:-----|:-----|
|None  <br/> |There is no location source.  <br/> |
|LocationServices  <br/> |The information was obtained from location services.  <br/> |
|PhonebookServices  <br/> |The information was obtained from phonebook services.  <br/> |
|Device  <br/> |The information was obtained from the device.  <br/> |
|Contact  <br/> |The information was obtained from a contact.  <br/> |
|Resource  <br/> |The information was obtained from a resource.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  

