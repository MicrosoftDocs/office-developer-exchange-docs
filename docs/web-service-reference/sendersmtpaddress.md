---
title: "SenderSmtpAddress"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SenderSmtpAddress
api_type:
- schema
ms.assetid: e39c7df7-4bfa-455f-b4bb-1f1d05398eec
description: "The SenderSmtpAddress element represents the SMTP e-mail address corresponding to the mailbox that contains the folder that will be shared."
---

# SenderSmtpAddress

The **SenderSmtpAddress** element represents the SMTP e-mail address corresponding to the mailbox that contains the folder that will be shared. 
  
```xml
<SenderSmtpAddress/>
```

 **NonEmptyStringType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetSharingMetadata](getsharingmetadata.md) <br/> |Defines a request to get an opaque authentication token that identifies the sharing invitation.  <br/> |
   
## Text value

A text value that represents an SMTP address is required.
  
## Remarks

The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetSharingMetadata operation](getsharingmetadata-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

