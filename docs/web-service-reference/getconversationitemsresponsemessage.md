---
title: "GetConversationItemsResponseMessage"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 2e930650-7848-4bf2-a975-026309b3ea02
description: "The GetConversationItemsResponseMessage element specifies the response message for a GetConversationItems request."
---

# GetConversationItemsResponseMessage

The **GetConversationItemsResponseMessage** element specifies the response message for a **GetConversationItems** request. 
  
```XML
<GetConversationItemsResponseMessage ResponseClass="Success | Warning | Error">
    <Conversation/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetConversationItemsResponseMessage>
```

 **GetConversationItemsResponseMessageType**
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
|[Conversation (ConversationResponseType)](conversation-conversationresponsetype.md) <br/> |Represents a single conversation returned in a **GetConversationItems** response.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and reserved for future use.  <br/> |
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides status information about the request.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services (EWS) request.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |messages.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

