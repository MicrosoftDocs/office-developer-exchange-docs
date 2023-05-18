---
title: "InvalidRecipient"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- InvalidRecipient
api_type:
- schema
ms.assetid: 9e2d3433-22d7-444b-9883-e5649297d8fe
description: "The InvalidRecipient element contains the SMTP address of the invalid recipient and information about why the recipient is invalid."
---

# InvalidRecipient

The **InvalidRecipient** element contains the SMTP address of the invalid recipient and information about why the recipient is invalid. 
  
```XML
<InvalidRecipient>
   <SmtpAddress/>
   <ResponseCode/>
   <MessageText/>
</InvalidRecipient>

```

 **InvalidRecipientType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SmtpAddress](smtpaddress.md) <br/> |Contains the SMTP address of the invalid recipient. This element is required.  <br/> |
|[ResponseCode (InvalidRecipientResponseCodeType)](responsecode-invalidrecipientresponsecodetype.md) <br/> |Provides an error code that identifies the specific error that the request encountered. This element is required.  <br/> |
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response. This element is optional.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[InvalidRecipients](invalidrecipients.md) <br/> |Represents the recipients of a folder sharing request that are invalid.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

-[GetSharingMetadata operation](getsharingmetadata-operation.md)

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)