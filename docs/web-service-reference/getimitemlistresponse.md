---
title: "GetImItemListResponse"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 00422885-0e7b-4b50-a9ca-01f24ff9858f
description: "The GetImItemListResponse element defines a response to a GetImItemList request."
---

# GetImItemListResponse

The **GetImItemListResponse** element defines a response to a **GetImItemList** request. 
  
```XML
<GetImItemListResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ImItemList/>
</GetImItemListResponse>
```

 **GetImItemListResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [ImItemList](imitemlist.md)
  
### Parent elements

None.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |messages.xsd  <br/> |
|Can be empty  <br/> ||
