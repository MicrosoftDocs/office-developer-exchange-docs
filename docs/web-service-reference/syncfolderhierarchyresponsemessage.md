---
title: "SyncFolderHierarchyResponseMessage"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchyResponseMessage
api_type:
- schema
ms.assetid: ab96c649-1005-401c-9d1c-9917f0b19a60
description: "The SyncFolderHierarchyResponseMessage element contains the status and result of a single SyncFolderHierarchy operation request."
---

# SyncFolderHierarchyResponseMessage

The **SyncFolderHierarchyResponseMessage** element contains the status and result of a single [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) request. 
  
[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
  
```
<SyncFolderHierarchyResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SyncState/>
   <IncludesLastFolderInRange/>
   <Changes/>
</SyncFolderHierarchyResponseMessage>
```

 **SyncFolderHierarchyResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ResponseClass** <br/> | Describes the status of a [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) response. The following values are valid for this attribute:  <br/>  Success  <br/>  Warning  <br/>  Error  <br/> |
   
#### ResponseClass Attribute Values

|**Value**|**Description**|
|:-----|:-----|
|**Success** <br/> |Describes a request that is fulfilled.  <br/> |
|**Warning** <br/> | Describes a request that was not processed. A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed. The following are examples of sources of warnings:  <br/>  The Exchange store is offline during the batch.  <br/>  Active Directory Domain Services (AD DS) is offline.  <br/>  Mailboxes were moved.  <br/>  The message database (MDB) is offline.  <br/>  A password has expired.  <br/>  A quota has been exceeded.  <br/> |
|**Error** <br/> | Describes a request that cannot be fulfilled. The following are examples of sources of errors:  <br/>  Invalid attributes or elements  <br/>  Attributes or elements that are out of range  <br/>  An unknown tag  <br/>  An attribute or element that is not valid in the context  <br/>  An unauthorized access attempt by any client  <br/>  A server-side failure in response to a valid client-side call  <br/>  Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.  <br/> |
   
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides an error code that identifies the specific error that the request encountered.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and is reserved for future use. It contains a value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
|[SyncState](syncstate-ex15websvcsotherref.md) <br/> |Contains a base64-encoded form of the synchronization data that is updated after each successful request. This is used to identify the synchronization state.  <br/> |
|[IncludesLastFolderInRange](includeslastfolderinrange.md) <br/> |Indicates whether the last item to synchronize has been included in the response.  <br/> |
|[Changes (Hierarchy)](changes-hierarchy.md) <br/> |Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services request.  <br/> |
   
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

[SyncFolderHierarchy operation](syncfolderhierarchy-operation.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

