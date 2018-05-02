---
title: "UploadItemsResponseMessage"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UploadItemsResponseMessage
api_type:
- schema
ms.assetid: 03febd08-c015-4009-b291-1b4296182ffe
description: "The UploadItemsResponseMessage element contains the status and results of a request to upload a single mailbox item."
---

# UploadItemsResponseMessage

The **UploadItemsResponseMessage** element contains the status and results of a request to upload a single mailbox item. 
  
[UploadItemsResponse](uploaditemsresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[UploadItemsResponseMessage](uploaditemsresponsemessage.md)
  
```XML
<UploadItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ItemId/>
</UploadItemsResponseMessage>
```

 **UploadItemsResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ResponseClass** <br/> | Describes the status of the response. The following values are valid for this attribute:  <br/>  Success  <br/>  Warning  <br/>  Error  <br/> |
   
#### ResponseClass Attribute Values

|**Value**|**Description**|
|:-----|:-----|
|**Success** <br/> |Describes a request that is fulfilled.  <br/> |
|**Warning** <br/> | Describes a request that was not processed. A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed. The following are examples of sources of warnings:  <br/>  The Exchange store is offline during the batch.  <br/>  Active Directory Domain Services (AD DS) is offline.  <br/>  Mailboxes were moved.  <br/>  The message database (MDB) is offline.  <br/>  A password is expired.  <br/>  A quota has been exceeded.  <br/> |
|**Error** <br/> | Describes a request that cannot be fulfilled. The following are examples of sources of errors:  <br/>  Invalid attributes or elements  <br/>  Attributes or elements that are out of range  <br/>  An unknown tag  <br/>  An attribute or element that is not valid in the context  <br/>  An unauthorized access attempt by any client  <br/>  A server-side failure in response to a valid client-side call  <br/>  Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.  <br/> |
   
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides an error code that identifies the specific error that the request encountered.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and reserved for future use. This element contains a value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
|[ItemId](itemid.md) <br/> |Contains the item identifier of an uploaded item.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services request.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[ExportItems operation](exportitems-operation.md)
  
[UploadItems operation](uploaditems-operation.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

