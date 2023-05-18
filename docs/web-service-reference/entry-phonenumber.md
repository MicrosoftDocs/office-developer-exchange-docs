---
title: "Entry (PhoneNumber)"
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
ms.assetid: e3d0a4d5-8af8-4607-aa2e-ef3111b63b55
description: "The Entry element represents a telephone number for a contact."
---

# Entry (PhoneNumber)

The **Entry** element represents a telephone number for a contact. 
  
```xml
<Entry Key=""/>
```

 **PhoneNumberDictionaryEntryType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Key** <br/> | Identifies the telephone number. The Key attribute is of type **PhoneNumberKeyType**.<br/><br/> The following are the possible values for this attribute:<br/><br/>- AssistantPhone  <br/>- BusinessFax  <br/>- BusinessPhone  <br/>- BusinessPhone2  <br/>- Callback  <br/>- CarPhone  <br/>- CompanyMainPhone  <br/>- HomeFax  <br/>- HomePhone  <br/>- HomePhone2  <br/>- Isdn  <br/>- MobilePhone  <br/>- OtherFax  <br/>- OtherTelephone  <br/>- Pager  <br/>- PrimaryPhone  <br/>- RadioPhone  <br/>- Telex  <br/>- TtyTddPhone  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[PhoneNumbers](phonenumbers.md) <br/> |Represents a collection of telephone numbers for a contact.  <br/> |
   
## Text value

A text value that represents a telephone number is required if this element is used.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
- [Creating Contacts (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [Updating Contacts](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [Deleting Contacts](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

