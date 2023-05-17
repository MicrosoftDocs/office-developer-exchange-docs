---
title: "ConnectionFailureCause"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ConnectionFailureCause
api_type:
- schema
ms.assetid: d2160c8a-015c-4964-b7f7-93478764a173
description: "The ConnectionFailureCause element specifies the reason for a disconnection from a telephone call."
---

# ConnectionFailureCause

The **ConnectionFailureCause** element specifies the reason for a disconnection from a telephone call. 
  
```xml
<ConnectionFailureCause>None or UserBusy or NoAnswer or Unavailable or Other</ConnectionFailureCause>
```

 **ConnectionFailureCauseType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[PhoneCallInformation](phonecallinformation.md) <br/> |Specifies the state information for a telephone call.  <br/> |
   
## Text value

The following table lists the possible values for the **ConnectionFailureCause** element. 
  
**ConnectionFailureCause element values**

|**Value**|**Description**|
|:-----|:-----|
|None  <br/> |Call state is not disconnected or the disconnect reason is not known.  <br/> |
|UserBusy  <br/> |The called party line was busy.  <br/> |
|NoAnswer  <br/> |The called party did not answer.  <br/> |
|Unavailable  <br/> |The called party number was not available.  <br/> |
|Other  <br/> |Catch-all for other disconnect reasons.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

