---
title: "AdditionalInfo"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 50bebbab-2fef-4a27-a5a9-32d7200820b6
description: "The AdditionalInfo element specifies additional information about the hold status of a mailbox."
---

# AdditionalInfo

The **AdditionalInfo** element specifies additional information about the hold status of a mailbox. 
  
```XML
<AdditionalInfo></AdditionalInfo>
```

 **xs:string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[MailboxHoldStatus](mailboxholdstatus.md) <br/> |Specifies the hold status of the mailbox.  <br/> |
|[NonIndexableItemDetail](nonindexableitemdetail.md) <br/> |Specifies detail for an item that cannot be indexed.  <br/> |
   
## Text value

The text value of the AdditionalInfo element is additional information about the hold status of a mailbox.
  
## Remarks

This element is optional.
  
This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

