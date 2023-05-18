---
title: "Contact (ContactType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 7f7119b7-f5b4-484d-a7de-fa74836d9aee
description: "The Contact element specifies a contact in the Unified Contact Store."
---

# Contact (ContactType)

The **Contact** element specifies a contact in the Unified Contact Store. 
  
```XML
<Contact>
    <PersonName></PersonName>
    <BusinessName></BusinessName>
    <PhoneNumbers></PhoneNumbers>
    <Urls></Urls>
    <EmailAddresses></EmailAddresses>
    <Addresses></Addesses>    <ContactString></ContactString
</Contact>
```

 **ContactType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[PersonName](personname.md) <br/> |Specifies the name of an individual.  <br/> |
|[BusinessName](businessname.md) <br/> |Specifies the name of a business.  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |Represents a collection of telephone numbers for a contact.  <br/> |
|[Urls](urls.md) <br/> |Specifies an array of URLs for a persona.  <br/> |
|[EmailAddresses (ArrayOfExtractedEmailAddresses)](emailaddresses-arrayofextractedemailaddresses.md) <br/> |Specifies an array of extracted email addresses.  <br/> |
|[Addresses (ArrayOfAddressesType)](addresses-arrayofaddressestype.md) <br/> |Specifies an array of **Address** elements.  <br/> |
|[ContactString](contactstring.md) <br/> |Specifies the display name of a contact.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Contacts (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |Specifies an array of contacts.  <br/> |
   
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

