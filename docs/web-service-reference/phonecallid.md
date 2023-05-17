---
title: "PhoneCallId"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- PhoneCallId
api_type:
- schema
ms.assetid: 79e31a4c-fc84-4802-8761-470df8d63694
description: "The PhoneCallId element specifies the identifier of a phone call. This element is required."
---

# PhoneCallId

The **PhoneCallId** element specifies the identifier of a phone call. This element is required. 
  
```xml
<PhoneCallId Id="" />
```

 **PhoneCallIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |Identifies the phone call to disconnect. This attribute is required.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DisconnectPhoneCall](disconnectphonecall.md) <br/> |Represents a request to disconnect a call.  <br/> |
|[GetPhoneCallInformation](getphonecallinformation.md) <br/> |Represents a request to get telephone call information.  <br/> |
|[PlayOnPhoneResponse (Exchange Web Services)](playonphoneresponse-exchange-web-services.md) <br/> |Defines a response to a PlayOnPhone request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

