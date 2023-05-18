---
title: "SyncFolderItemsResponseMessage"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SyncFolderItemsResponseMessage
api_type:
- schema
ms.assetid: f58e773f-94a7-4729-90f0-ac4c71b4ba59
description: "The SyncFolderItemsResponseMessage element contains the status and result of a single SyncFolderItems operation request."
---

# SyncFolderItemsResponseMessage

The **SyncFolderItemsResponseMessage** element contains the status and result of a single [SyncFolderItems operation](syncfolderitems-operation.md) request. 
  
- [SyncFolderItemsResponse](syncfolderitemsresponse.md) 
- [ResponseMessages](responsemessages.md)
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
  
```xml
<SyncFolderItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SyncState/>
   <IncludesLastItemInRange/>
   <Changes/>
</SyncFolderItemsResponseMessage>
```

 **SyncFolderItemsResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ResponseClass** <br/> | Describes the status of a [SyncFolderItems operation](syncfolderitems-operation.md) response. <br/><br/>The following values are valid for this attribute: <br/> <br/>- Success  <br/>- Warning  <br/>- Error  <br/> |
   
#### ResponseClass Attribute

|**Value**|**Description**|
|:-----|:-----|
|**Success** <br/> |Describes a request that is fulfilled.  <br/> |
|**Warning** <br/> | Describes a request that was not processed. A warning may be returned if an error occurred while processing an item in the request and subsequent items cannot be processed. <br/><br/>The following are examples of sources of warnings:  <br/><br/>- The Exchange store is offline during the batch.  <br/>- Active Directory Domain Services (AD DS) is offline.  <br/>- Mailboxes were moved.  <br/>- The message database (MDB) is offline.  <br/>- A password has expired.  <br/>- A quota was exceeded.  <br/> |
|**Error** <br/> | Describes a request that cannot be fulfilled. <br/><br/>The following are examples of sources of errors:  <br/><br/>- Invalid attributes or elements  <br/>- Attributes or elements that are out of range  <br/>- An unknown tag  <br/>- An attribute or element that is not valid in the context  <br/>- Any unauthorized access attempt by any client  <br/>- Any server-side failure in response to a valid client-side call  <br/>  <br/>Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides an error code that identifies the specific error that the request encountered.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and is reserved for future use. It contains the value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
|[SyncState](syncstate-ex15websvcsotherref.md) <br/> |Contains a base64-encoded form of the synchronization data that is updated after each successful request. This is used to identify the synchronization state.  <br/> |
|[IncludesLastItemInRange](includeslastiteminrange.md) <br/> |Indicates whether the last item to synchronize has been included in the response.  <br/> |
|[Changes (Items)](changes-items.md) <br/> |Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [SyncFolderItems operation](syncfolderitems-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
