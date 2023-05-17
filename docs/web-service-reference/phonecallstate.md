---
title: "PhoneCallState"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- PhoneCallState
api_type:
- schema
ms.assetid: ac009eb3-6334-49ce-82be-48fe83577f9c
description: "The PhoneCallState element specifies the current state for a phone call."
---

# PhoneCallState

The **PhoneCallState** element specifies the current state for a phone call. 
  
```xml
<PhoneCallState>Idle or Connecting or Alerted or Connected or Disconnected or Incoming or Transferring or Forwarding</PhoneCallState>
```

 **PhoneCallStateType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[PhoneCallInformation](phonecallinformation.md) <br/> |Specifies the state information for a phone call.  <br/> |
   
## Text value

The following table lists the possible values for the **PhoneCallState** element. 
  
**PhoneCallState element values**

|**Value**|**Description**|
|:-----|:-----|
|Idle  <br/> |Initial call state.  <br/> |
|Connecting  <br/> |The system is dialing this call.  <br/> |
|Alerted  <br/> |The call is in alerting state (phone is ringing).  <br/> |
|Connected  <br/> |The call is in the connected state.  <br/> |
|Disconnected  <br/> |The call is disconnected.  <br/> |
|Incoming  <br/> |The call is inbound.  <br/> |
|Transferring  <br/> |The call is being transferred to another destination.  <br/> |
|Forwarding  <br/> |The call is being forwarded to another destination.  <br/> |
   
## Remarks

The schema that describes this element is located in the /ews/ directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

