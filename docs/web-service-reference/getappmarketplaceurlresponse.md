---
title: "GetAppMarketplaceUrlResponse"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: dc3368ec-78c2-4f8d-8394-4891e90dafd2
description: "The GetAppMarketplaceUrlResponse element specifies the response to a GetAppMarketplaceUrl request."
---

# GetAppMarketplaceUrlResponse

The **GetAppMarketplaceUrlResponse** element specifies the response to a **GetAppMarketplaceUrl** request. 
  
```XML
<GetAppMarketplaceUrlResponse ResponseClass=" Success | Warning | Error ">
    <AppMarketplaceUrl/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppMarketplaceUrlResponse>
```

 **GetAppMarketplaceUrlResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|ResponseClass  <br/> |Indicates the class of the response.  <br/> |
   
#### ResponseClass

|**Value**|**Description**|
|:-----|:-----|
|Success  <br/> |Indicates success.  <br/> |
|Warning  <br/> |Indicates a warning.  <br/> |
|Error  <br/> |Indicates an error.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AppMarketplaceUrl](appmarketplaceurl.md) <br/> |Specifies the URL for the app.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and reserved for future use.  <br/> |
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides status information about the request.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services request.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |messages.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
