---
title: "CreateFolderResponseMessage"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CreateFolderResponseMessage
api_type:
- schema
ms.assetid: 1301dd15-b008-4fd9-8c89-b15a20b186e2
description: "The CreateFolderResponseMessage element contains the status and result of a single CreateFolder operation request."
---

# CreateFolderResponseMessage

The **CreateFolderResponseMessage** element contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request. 
  
```xml
<CreateFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CreateFolderResponseMessage>
```

**FolderInfoResponseMessageType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ResponseClass** <br/> | Describes the status of a [CreateFolder operation](createfolder-operation.md) response.<br/><br/>The following values are valid for this attribute:<br/><br/>- Success  <br/>- Warning  <br/>- Error  <br/> |
   
#### ResponseClass attribute values

|**Value**|**Description**|
|:-----|:-----|
|**Success** <br/> |Describes a request that is fulfilled.  <br/> |
|**Warning** <br/> | Describes a request that was not processed. A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.<br/><br/>The following are examples of sources of warnings:<br/><br/>- The Exchange store is offline during the batch.  <br/>- Active Directory Domain Services (AD DS) is offline.  <br/>- Mailboxes are moved.  <br/>- The message database (MDB) is offline.  <br/>- A password is expired.  <br/>- A quota is exceeded.  <br/> |
|**Error** <br/> | Describes a request that cannot be fulfilled.<br/><br/>The following are examples of sources of errors:  <br/><br/>- Invalid attributes or elements  <br/>- Attributes or elements out of range  <br/>- Unknown tag  <br/>- Attribute or element not valid in the context  <br/>- Unauthorized access attempt by any client  <br/>- Server-side failure in response to a valid client-side call<br/><br/>  Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides an error code that identifies the specific error that the request encountered.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and is reserved for future use. It contains a value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
|[Folders](folders-ex15websvcsotherref.md) <br/> |Contains an array of created folders.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [CreateFolder operation](createfolder-operation.md)
- [EWS reference for Exchange](ews-reference-for-exchange.md) 
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

