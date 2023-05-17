---
title: "GetNonIndexableItemDetailsResponseMessage"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 00566965-6cbd-4f31-9fa9-85b3e5559c0c
description: "The GetNonIndexableItemDetailsResponseMessage element specifies the response message for a GetNonIndexableItemDetails request."
---

# GetNonIndexableItemDetailsResponseMessage

The **GetNonIndexableItemDetailsResponseMessage** element specifies the response message for a **GetNonIndexableItemDetails** request. 

```XML
<GetNonIndexableItemDetailsResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <NonIndexableItemDetailsResult/>
</GetNonIndexableItemDetailsResponseMessage>
```

 **GetNonIndexableItemDetailsResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.

### Attributes

None.

### Child elements

[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [NonIndexableItemDetailsResult](nonindexableitemdetailsresult.md)

### Parent elements

[ResponseMessages](responsemessages.md)

## Remarks

This element was introduced in Exchange Server 2013.

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.

## Element information

|**Element**|**Type**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |  
