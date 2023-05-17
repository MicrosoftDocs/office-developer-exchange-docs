---
title: "DeleteFolderResponseMessage"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DeleteFolderResponseMessage
api_type:
- schema
ms.assetid: de4c63ff-80b2-40c2-bc06-ef0c23beacd4
description: "The DeleteFolderResponseMessage element contains the status and result of a single DeleteFolder operation request."
---

# DeleteFolderResponseMessage

The **DeleteFolderResponseMessage** element contains the status and result of a single [DeleteFolder operation](deletefolder-operation.md) request. 
  
- [DeleteFolderResponse](deletefolderresponse.md)  
- [ResponseMessages](responsemessages.md)  
- [DeleteFolderResponseMessage](deletefolderresponsemessage.md)
  
```xml
<DeleteFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteFolderResponseMessage>
```

 **ResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ResponseClass** <br/> | Describes the status of a [DeleteFolder operation](deletefolder-operation.md) response.<br/><br/>The following values are valid for this attribute:<br/><br/>- Success  <br/>- Warning  <br/>- Error  <br/> |
   
#### ResponseClass attribute values

|**Value**|**Description**|
|:-----|:-----|
|**Success** <br/> |Describes a request that is fulfilled.  <br/> |
|**Warning** <br/> | Describes a request that was not processed. A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.<br/><br/>The following are examples of sources of warnings:<br/><br/>- The Exchange store goes offline during the batch.<br/>- Active Directory Domain Services (AD DS) goes offline.<br/>- Mailboxes are moved.<br/>- The message database (MDB) goes offline.<br/>- A password is expired.<br/>- A quota is exceeded.  <br/> |
|**Error** <br/> | Describes a request that cannot be fulfilled.<br/><br/>The following are examples of sources of errors:<br/><br/>- Invalid attributes or elements<br/>- Attributes or elements out of range<br/>- Unknown tag<br/>- Attribute or element not valid in the context<br/>- Unauthorized access attempt by any client<br/>- Server-side failure in response to a valid client-side call  <br/><br/>  Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |A text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides an error code that identifies the specific error that the request encountered.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and is reserved for future use. It contains the value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [DeleteFolder operation](deletefolder-operation.md)
- [EWS reference for Exchange](ews-reference-for-exchange.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
- [Deleting Folders](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

