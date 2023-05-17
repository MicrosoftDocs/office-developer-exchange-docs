---
title: "ArchiveItemResponse"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 68109a92-c49e-4c0e-b6ec-e90d38d4be4d
description: "The ArchiveItemResponse element specifies the response to an ArchiveItem request."
---

# ArchiveItemResponse

The **ArchiveItemResponse** element specifies the response to an **ArchiveItem** request. 
  
```XML
<ArchiveItemResponse>
    <ResponseMessages></ResponseMessages>
</ArchiveItemResponse>
```

 **ArchiveItemResponseType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages to an Exchange Web Services request.  <br/> |
   
### Parent elements

None.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |messages.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

