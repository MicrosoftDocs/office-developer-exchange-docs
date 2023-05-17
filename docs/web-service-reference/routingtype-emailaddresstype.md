---
title: "RoutingType (EmailAddressType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 683216be-9972-4f48-a148-c34bfe7f53e5
description: "The RoutingType element defines the address type for the mailbox."
---

# RoutingType (EmailAddressType)

The **RoutingType** element defines the address type for the mailbox. 
  
```XML
<RoutingType/>
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
|[ActingAs](actingas.md) <br/> |Identifies who the caller is sending as.  <br/> |
|[Mailbox](mailbox.md) <br/> |Identifies a fully resolved e-mail address.  <br/> |
|[RoomList](roomlist.md) <br/> |Identifies a list of meeting rooms.  <br/> |
   
## Text value

The text value represents a routing type. SMTP is the typical text value for this element.
  
## Remarks

This element is optional in the [Mailbox](mailbox.md) element. Another [RoutingType (EmailAddress)](routingtype-emailaddress.md) element is used for Availability operations. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

