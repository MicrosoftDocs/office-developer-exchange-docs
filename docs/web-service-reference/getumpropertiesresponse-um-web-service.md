---
title: "GetUMPropertiesResponse (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- GetUMPropertiesResponse
api_type:
- schema
ms.assetid: fcd93ce5-7403-46a9-b46e-56d2ebdd2f79
description: "The GetUMPropertiesResponse element defines a response to a GetUMProperties operation (UM web service) request."
 
 
---

# GetUMPropertiesResponse (UM web service)

The **GetUMPropertiesResponse** element defines a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request. 
  
[GetUMPropertiesResponse (UM web service)](getumpropertiesresponse-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
  <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 **UMProperties**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MissedCallNotificationEnabled (UM web service)](missedcallnotificationenabled-um-web-service.md) <br/> |Indicates whether missed call notifications are enabled.  <br/> |
|[PlayOnPhoneDialString (UM web service)](playonphonedialstring-um-web-service.md) <br/> |Contains the default dial string to use for the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).  <br/> |
|[TelephoneAccessNumbers (UM web service)](telephoneaccessnumbers-um-web-service.md) <br/> |Contains the list of telephone numbers the user can use to access Unified Messaging via a telephone.  <br/> |
|[TelephoneAccessFolderEmail (UM web service)](telephoneaccessfolderemail-um-web-service.md) <br/> |Contains the identifier for the e-mail folder from which Unified Messaging will read messages over the telephone.  <br/> |
   
### Parent elements

None.
  
## Text value

None.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md)

