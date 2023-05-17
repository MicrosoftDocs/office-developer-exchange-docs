---
title: "GetSharingMetadataResponse"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GetSharingMetadataResponse
api_type:
- schema
ms.assetid: 1acc2d8f-7104-4b36-9c04-dd4fc4f571bb
description: "The GetSharingMetadataResponse element defines a response to a GetSharingMetadata operation request."
---

# GetSharingMetadataResponse

The **GetSharingMetadataResponse** element defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request. 
  
```xml
<GetSharingMetadataResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <EncryptedSharedFolderDataCollection/>   <InvalidRecipients/>
</GetSharingMetadataResponse>
```

 **GetSharingMetadataResponseMessageType**
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
|**Warning** <br/> | Describes a request that was not processed. A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed. <br/><br/>The following are examples of sources of warnings:  <br/><br/>- The Exchange store is offline during the batch.  <br/>- The Active Directory directory service is offline.  <br/>- Mailboxes were moved.  <br/>- The message database (MDB) is offline.  <br/>- A password is expired.  <br/>- A quota has been exceeded.  <br/> |
|**Error** <br/> | Describes a request that cannot be fulfilled. <br/><br/>The following are examples of sources of errors:  <br/><br/>- Invalid attributes or elements  <br/>- Attributes or elements out of range  <br/>- Unknown tag  <br/>- Attribute or element not valid in the context  <br/>- Unauthorized access attempt by any client  <br/>- Server-side failure in response to a valid client-side call  <br/>  <br/>Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides an error code that identifies the specific error that the request encountered.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and reserved for future use. This element contains a value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
|[EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md) <br/> |Contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.  <br/> |
|[InvalidRecipients](invalidrecipients.md) <br/> |Represents recipients of the folder sharing request that are invalid.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetSharingMetadata operation](getsharingmetadata-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

