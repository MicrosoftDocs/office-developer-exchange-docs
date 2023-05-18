---
title: "GetPasswordExpirationDateResponse"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 3d3fff1f-ef13-46d5-bd7f-ef535eb80c72
description: "The GetPasswordExpirationDateResponse element defines the response to a GetPasswordExpirationDate operation operation request."
---

# GetPasswordExpirationDateResponse

The **GetPasswordExpirationDateResponse** element defines the response to a [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) operation request. 
  
- [ResponseMessages](responsemessages.md)
- [GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md)
  
```XML
<GetPasswordExpirationDateResponse>
    <PasswordExpirationDate />
</GetPasswordExpirationDateResponse>
```

 **GetPasswordExpirationDateResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ResponseClass** <br/> | Describes the status of the response. <br/><br/>The following values are valid for this attribute:  <br/><br/>- Success  <br/>- Warning  <br/>- Error  <br/> |
   
#### ResponseClass attribute values

|**Value**|**Description**|
|:-----|:-----|
|**Success** <br/> |Describes a request that is fulfilled.  <br/> |
|**Warning** <br/> | Describes a request that was not processed. A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.<br/><br/> The following are examples of sources of warnings:  <br/><br/>- The Exchange store is offline during the batch.  <br/>- Active Directory Domain Services (AD DS) is offline.  <br/>- Mailboxes were moved.  <br/>- The message database (MDB) is offline.  <br/>- A password is expired.  <br/>- A quota has been exceeded.  <br/> |
|**Error** <br/> | Describes a request that cannot be fulfilled. <br/><br/>The following are examples of sources of errors:  <br/><br/>- Invalid attributes or elements.  <br/>- Attributes or elements that are out of range.  <br/>- An unknown tag.  <br/>- An attribute or element that is not valid in the context.  <br/>- An unauthorized access attempt by any client.  <br/>- A server-side failure in response to a valid client-side call.  <br/><br/>  Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.  <br/> |
   
### Child elements

|**Element name**|**Description**|
|:-----|:-----|
|[PasswordExpirationDate](passwordexpirationdate.md) <br/> |Provides the password expiration date for the email account specified in the request.  <br/> |
   
### Parent elements

|**Element name**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services (EWS) request.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

