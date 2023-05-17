---
title: "OofSettings"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- OofSettings
api_type:
- schema
ms.assetid: 8f37d174-db11-427c-bbed-fdde754a60c7
description: "The OofSettings element contains the Out of Office (OOF) settings."
---

# OofSettings

The **OofSettings** element contains the Out of Office (OOF) settings. 
  
[GetUserOofSettingsResponse](getuseroofsettingsresponse.md)
  
[OofSettings](oofsettings.md)
  
```xml
<OofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</OofSettings>
```

 **UserOofSettings**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |Contains the user's OOF state.  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |Contains a value that determines to whom external OOF messages are sent.  <br/> |
|[Duration (UserOofSettings)](duration-useroofsettings.md) <br/> |Contains the duration for which the OOF status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**. If the [OofState](oofstate.md) element is set to **Enabled** or **Disabled**, the value of this element is ignored.  <br/> |
|[InternalReply](internalreply.md) <br/> |Contains the OOF response sent to other users in the user's domain or trusted domain.  <br/> |
|[ExternalReply](externalreply.md) <br/> |Contains the OOF response sent to addresses outside the recipient's domain or trusted domains.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Contains the response results and the OOF settings for a user.  <br/> The following is the XPath expression to this element:  <br/>  `/GetUserOofSettingsResponse` <br/> |
   
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

