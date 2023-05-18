---
title: "Recipients (ArrayOfSmtpAddressType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Recipients
api_type:
- schema
ms.assetid: cf68417d-85cf-49e0-857a-f987d3675344
description: "The Recipients element specifies an array of recipients of a message."
---

# Recipients (ArrayOfSmtpAddressType)

The **Recipients** element specifies an array of recipients of a message. 
  
```xml
<Recipients>   <SmtpAddress/></Recipients>
```

 **ArrayOfSmtpAddressType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SmtpAddress](smtpaddress.md) <br/> |Represents the Simple Mail Transfer Protocol (SMTP) recipient address of a calendar or contact sharing request.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetSharingMetadata](getsharingmetadata.md) <br/> |Defines a request to get an opaque authentication token that identifies the sharing invitation.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetSharingMetadata operation](getsharingmetadata-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

