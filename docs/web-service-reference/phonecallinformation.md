---
title: "PhoneCallInformation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- PhoneCallInformation
api_type:
- schema
ms.assetid: a0363c42-6d35-4074-bc17-946eb12736ff
description: "The PhoneCallInformation element specifies the state information for a phone call."
---

# PhoneCallInformation

The **PhoneCallInformation** element specifies the state information for a phone call. 
  
```XML
<PhoneCallInformation>
   <PhoneCallState/>
   <ConnectionFailureCause/>
   <SIPResponseText/>
   <SIPResponseCode/>
</PhoneCallInformation>
```

 **PhoneCallInformationType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[PhoneCallState](phonecallstate.md) <br/> |Specifies the state for a phone call. This element is required.  <br/> |
|[ConnectionFailureCause](connectionfailurecause.md) <br/> |Specifies the cause of a connection failure. This element is required.  <br/> |
|[SIPResponseText](sipresponsetext.md) <br/> |Specifies the SIP response text. This element is optional.  <br/> |
|[SIPResponseCode](sipresponsecode.md) <br/> |Specifies the SIP response code. This element is optional.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetPhoneCallInformationResponse](getphonecallinformationresponse.md) <br/> |Defines a response to a [GetPhoneCallInformation operation](getphonecallinformation-operation.md) request.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

