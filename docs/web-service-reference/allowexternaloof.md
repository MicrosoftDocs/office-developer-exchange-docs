---
title: "AllowExternalOof"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AllowExternalOof
api_type:
- schema
ms.assetid: e5387172-5b92-4bb1-8394-180e9c7ff771
description: "The AllowExternalOof element contains a value that identifies to whom external Out of Office (OOF) messages are sent."
---

# AllowExternalOof

The **AllowExternalOof** element contains a value that identifies to whom external Out of Office (OOF) messages are sent. 
  
- [GetUserOofSettingsResponse](getuseroofsettingsresponse.md)
  
- [AllowExternalOof](allowexternaloof.md)
  
```xml
<AllowExternalOof>None or Known or All</AllowExternalOof>
```

 **ExternalAudience**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Contains the response results and the OOF settings for a user.  <br/> |
   
## Text value

A text value is required for this element. The following table lists the possible values for this element.
  
|**Value**|**Description**|
|:-----|:-----|
|**None** <br/> |E-mail senders outside the mailbox user's organization who send messages to the user will not receive an external OOF message response.  <br/> |
|**Known** <br/> |E-mail senders outside the mailbox user's organization who send messages to the user will only receive an external OOF message response if the sender is in the user's Exchange store contact list.  <br/> |
|**All** <br/> |E-mail senders outside the mailbox user's organization who send messages to the user will receive an external OOF message response.  <br/> |
   
## Remarks

This element shares the same type as the [ExternalAudience](externalaudience.md) element. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetUserOofSettings operation](getuseroofsettings-operation.md) 
- [SetUserOofSettings operation](setuseroofsettings-operation.md)

