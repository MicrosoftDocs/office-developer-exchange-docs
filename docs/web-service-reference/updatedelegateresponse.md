---
title: "UpdateDelegateResponse"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateDelegateResponse
api_type:
- schema
ms.assetid: cd336add-fbcc-4f61-9867-d4c08a60e142
description: "The UpdateDelegateResponse element contains the status and result of an UpdateDelegate operation request."
---

# UpdateDelegateResponse

The **UpdateDelegateResponse** element contains the status and result of an [UpdateDelegate operation](updatedelegate-operation.md) request. 
  
```
<UpdateDelegateResponseMessage>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UpdateDelegateResponseMessage>
```

 **UpdateDelegateResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages (ArrayOfDelegateUserResponseMessageType)](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |Contains the response messages for an Exchange Web Services delegate management request.  <br/> |
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides an error code that identifies the specific error that the request encountered.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and is reserved for future use. It contains a value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
   
#### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[UpdateDelegate operation](updatedelegate-operation.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

