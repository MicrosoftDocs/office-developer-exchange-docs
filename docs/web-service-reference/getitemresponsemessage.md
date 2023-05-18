---
title: "GetItemResponseMessage"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GetItemResponseMessage
api_type:
- schema
ms.assetid: cc583723-54d1-4a17-8c1f-6586f70fdefd
description: "The GetItemResponseMessage element contains the status and result of a single GetItem operation request."
---

# GetItemResponseMessage

The **GetItemResponseMessage** element contains the status and result of a single [GetItem operation](getitem-operation.md) request. 
  
- [GetItemResponse](getitemresponse.md) 
- [ResponseMessages](responsemessages.md)
- [GetItemResponseMessage](getitemresponsemessage.md)
  
```xml
<GetItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</GetItemResponseMessage>
```

**ItemInfoResponseMessageType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ResponseClass** <br/> | Describes the status of a [GetItem operation](getitem-operation.md) response. <br/><br/>The following values are valid for this attribute:<br/><br/>- Success<br/>- Warning<br/>- Error |
   
#### ResponseClass attribute values

|**Value**|**Description**|
|:-----|:-----|
|**Success** <br/> |Describes a request that is fulfilled.  <br/> |
|**Warning** <br/> | Describes a request that was not processed. A warning may be returned if an error occurred while an item in the request was processed and subsequent items could not be processed.<br/><br/>The following are examples of sources for warnings:<br/><br/>- The Exchange store is offline during the batch.<br/>- Active Directory Domain Services (AD DS) is offline.<br/>- Mailboxes are moved.<br/>- MDB is offline.<br/>- Password is expired.  <br/>- Quota is exceeded. |
|**Error** <br/> | Describes a request that cannot be fulfilled.<br/><br/>The following are examples of sources for errors:<br/><br/>- Invalid attributes or elements<br/>- Attributes or elements out of range<br/>- Unknown tag<br/>- Attribute or element not valid in the context<br/>- Unauthorized access attempted by any client<br/>- Server-side failure in response to a valid client-side call<br/><br/>Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements. |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides an error code that identifies the specific error that the request encountered.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and is reserved for future use. It contains a value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
|[Items](items.md) <br/> |Contains an array of returned items.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

|Element|Type|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetItem](getitem.md)
- [GetItem operation](getitem-operation.md)

