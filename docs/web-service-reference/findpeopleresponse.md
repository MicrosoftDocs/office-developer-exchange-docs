---
title: "FindPeopleResponse"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 95f016a9-002f-4be3-abd6-f5e3528afd44
description: "The FindPeopleResponse element specifies the response to a FindPeople request."
---

# FindPeopleResponse

The **FindPeopleResponse** element specifies the response to a **FindPeople** request. 
  
```XML
<FindPeopleResponse ResponseClass=" Success | Warning | Error ">
    <People/>
    <TotalNumberOfPeopleInView/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</FindPeopleResponse>
```

 **FindPeopleResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|ResponseClass  <br/> |Specifies the response class.  <br/> |
   
#### ResponseClass

|**Value**|**Description**|
|:-----|:-----|
|Success  <br/> |Indicates success.  <br/> |
|Warning  <br/> |Indicates a warning.  <br/> |
|Error  <br/> |Indicates an error.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[People](people.md) <br/> |Specifies an array of persona data returned as the result of a **FindPeople** request.  <br/> |
|[TotalNumberOfPeopleInView](totalnumberofpeopleinview.md) <br/> |Specifies the total number of personas stored on a server that are returned by a **FindPeople** request.  <br/> |
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides status information about the request.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and reserved for future use.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Specifies an array of response messages.  <br/> |
   
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

