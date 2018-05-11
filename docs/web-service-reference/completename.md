---
title: "CompleteName"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CompleteName
api_type:
- schema
ms.assetid: 22d30d1f-a84d-48bb-ad8f-ce13f8e76604
description: "The CompleteName element represents the complete name of a contact."
---

# CompleteName

The **CompleteName** element represents the complete name of a contact. 
  
```
<CompleteName>
   <Title/>
   <FirstName/>
   <MiddleName/>
   <LastName/>
   <Suffix/>
   <Initials/>
   <FullName/>
   <Nickname/>
   <YomiFirstName/>
   <YomiLastName/>
</CompleteName>
```

 **CompleteNameType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Title](title.md) <br/> |Represents the title of a contact.  <br/> |
|[FirstName](firstname.md) <br/> |Represents the first name of contact.  <br/> |
|[MiddleName](middlename.md) <br/> |Represents the middle name of a contact.  <br/> |
|[LastName](lastname.md) <br/> |Represents the last name of a contact.  <br/> |
|[Suffix](suffix.md) <br/> |Represents a suffix to a contact's name.  <br/> |
|[Initials](initials.md) <br/> |Represents the initials of a contact.  <br/> |
|[FullName](fullname.md) <br/> |Represents the full name of a contact.  <br/> |
|[Nickname](nickname.md) <br/> |Represents the nickname of a contact.  <br/> |
|[YomiFirstName](yomifirstname.md) <br/> |Represents the name used in Japan for the searchable or phonetic spelling of a Japanese first name.  <br/> |
|[YomiLastName](yomilastname.md) <br/> |Represents the name used in Japan for the searchable or phonetic spelling of a Japanese last name.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
   
## Remarks

The [CompleteName](completename.md) property is part of the [Default](https://msdn.microsoft.com/library/ExchangeWebServices.DefaultShapeNamesType.Default.aspx) shape. In the initial release version of Microsoft Exchange Server 2007, the [CompleteName](completename.md) property is returned by the [GetItem operation](getitem-operation.md), but not the [FindItem operation](finditem-operation.md). Starting with Exchange Server 2007 Service Pack 1 (SP1), the [FindItem operation](finditem-operation.md) also returns the [CompleteName](completename.md) property with the [Default](https://msdn.microsoft.com/library/ExchangeWebServices.DefaultShapeNamesType.Default.aspx) shape. This change does not affect the schema. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

#### Reference

[CompleteNameType](https://msdn.microsoft.com/library/ExchangeWebServices.CompleteNameType.aspx)
  
[CompleteName](https://msdn.microsoft.com/library/ExchangeWebServices.ContactItemType.CompleteName.aspx)
  
[contactsCompleteName](https://msdn.microsoft.com/library/ExchangeWebServices.UnindexedFieldURIType.contactsCompleteName.aspx)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
#### Other resources

[Creating Contacts (Exchange Web Services)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

