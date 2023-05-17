---
title: "LobbyBypass"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: e05ed6eb-00ae-49c8-8341-43f6e0d728ff
description: "The LobbyBypass element specifies the online meeting setting to bypass the virtual lobby."
---

# LobbyBypass

The **LobbyBypass** element specifies the online meeting setting to bypass the virtual lobby. 
  
```XML
<LobbyBypass> Disabled | EnabledForGatewayParticipants </LobbyBypass>
```

 **LobbyBypassType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[OnlineMeetingSettings](onlinemeetingsettings.md)
  
## Text value

The text value of the **LobbyBypass** element can be either **Disabled** or **EnabledForGatewayParticipants**. The **Disabled** value indicates that the lobby bypass is disabled so all meeting attendees must access through the virtual lobby. The **EnabledForGatewayParticipants** value indicates that the lobby bypass is enabled for telephone participants. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  

