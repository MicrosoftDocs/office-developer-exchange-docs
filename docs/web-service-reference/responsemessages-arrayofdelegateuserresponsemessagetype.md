---
title: "ResponseMessages (ArrayOfDelegateUserResponseMessageType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: 14819975-ce54-4f0e-9f90-d4b275895ea0
description: "The ResponseMessages element contains the response messages for an Exchange Web Services delegate management request."
---

# ResponseMessages (ArrayOfDelegateUserResponseMessageType)

The **ResponseMessages** element contains the response messages for an Exchange Web Services delegate management request. 
  
```
<ResponseMessages>
   <DelegateUserResponseMessageType/>
</ResponseMessages>
```

 **ArrayOfDelegateUserResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |Contains response messages for delegate management operations.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request.  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request.  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |Contains the status and result of an [UpdateDelegate operation](updatedelegate-operation.md) request.  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |Contains the status and result of a [RemoveDelegate operation](removedelegate-operation.md) request.  <br/> |
   
## Remarks

This element is used in the [AddDelegate operation](adddelegate-operation.md), the [GetDelegate operation](getdelegate-operation.md), the [UpdateDelegate operation](updatedelegate-operation.md), and the [RemoveDelegate operation](removedelegate-operation.md). The delegate management operation responses are structured differently than other responses. The delegate management response messages are strongly typed.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[AddDelegate operation](adddelegate-operation.md)
  
[GetDelegate operation](getdelegate-operation.md)
  
[UpdateDelegate operation](updatedelegate-operation.md)
  
[RemoveDelegate operation](removedelegate-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

