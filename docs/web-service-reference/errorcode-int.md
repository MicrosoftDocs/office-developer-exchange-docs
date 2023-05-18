---
title: "ErrorCode (int)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 65537d96-edf9-41ee-9ad5-91ffe37e2269
description: "The ErrorCode element specifies the error code of a failed search performed against a mailbox."
---

# ErrorCode (int)

The **ErrorCode** element specifies the error code of a failed search performed against a mailbox. 
  
```XML
<ErrorCode></ErrorCode>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FailedMailbox](failedmailbox.md) <br/> |Specifies the hold status of the mailbox.  <br/> |
   
## Text value

The text value of the **ErrorCode** element is the error code returned for a failed search performed against a mailbox. 
  
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

