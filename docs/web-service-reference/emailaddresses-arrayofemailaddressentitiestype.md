---
title: "EmailAddresses (ArrayOfEmailAddressEntitiesType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 2fc4a8e8-5377-4059-8fb4-3fdabfd30fe3
description: "The EmailAddresses element specifies an array of email address entities."
---

# EmailAddresses (ArrayOfEmailAddressEntitiesType)

The **EmailAddresses** element specifies an array of email address entities. 
  
```XML
<EmailAddresses>
    <EmailAddressEntity></EmailAddressEntity>
</EmailAddresses>
```

 **ArrayOfEmailAddressEntitiesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[EmailAddressEntity](emailaddressentity.md) <br/> |Specifies a single email address entity.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[EntityExtractionResult](entityextractionresult.md) <br/> |Specifies the **EntityExtractionResult** property of an item.  <br/> |
   
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

