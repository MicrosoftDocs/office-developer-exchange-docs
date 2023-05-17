---
title: "GetUserOofSettingsResponse"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GetUserOofSettingsResponse
api_type:
- schema
ms.assetid: 011cb38b-da3c-4b1b-8836-a6b212b511f6
description: "The GetUserOofSettingsResponse element contains the response message and the Out of Office (OOF) settings for a user."
---

# GetUserOofSettingsResponse

The **GetUserOofSettingsResponse** element contains the response message and the Out of Office (OOF) settings for a user. 
  
```xml
<GetUserOofSettingsResponse>
   <ResponseMessage>...</ResponseMessage>
   <OofSettings>...</OofSettings>
   <AllowExternalOof>...</AllowExternalOof>
</GetUserOofSettingsResponse>
```

 **GetUserOofSettingsResponse**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> |Provides descriptive information about the response status.  <br/> |
|[OofSettings](oofsettings.md) <br/> |Contains the OOF settings.  <br/> |
|[AllowExternalOof](allowexternaloof.md) <br/> |Contains a value that identifies to whom external OOF messages are sent.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetUserOofSettings operation](getuseroofsettings-operation.md)
  
[SetUserOofSettings operation](setuseroofsettings-operation.md)

