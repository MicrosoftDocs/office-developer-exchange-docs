---
title: "Recipients (ArrayOfRecipientsType)"
 
 
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
ms.assetid: f4b71403-cbae-4176-8b2e-3597048c057b
description: "The Recipients element represents a collection of recipients that receive a copy of the message."
---

# Recipients (ArrayOfRecipientsType)

The **Recipients** element represents a collection of recipients that receive a copy of the message. 
  
```XML
<Recipients>
   <Mailbox/>
</Recipients>
```

 **ArrayOfRecipientsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |Identifies a mail-enabled Active Directory object.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetMailTips](getmailtips.md) <br/> |Contains the recipients and types of mail tips to retrieve.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

