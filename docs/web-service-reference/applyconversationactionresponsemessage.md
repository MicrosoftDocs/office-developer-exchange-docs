---
title: "ApplyConversationActionResponseMessage"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ApplyConversationActionResponseMessage
api_type:
- schema
ms.assetid: a09edc89-7f2f-4846-a3a5-06694c97b9f6
description: "The ApplyConversationActionResponseMessage element contains the status and results of an ApplyConversationAction operation request."
---

# ApplyConversationActionResponseMessage

The **ApplyConversationActionResponseMessage** element contains the status and results of an [ApplyConversationAction operation](applyconversationaction-operation.md) request.  
  
- [ApplyConversationActionResponse](applyconversationactionresponse.md)
- [ResponseMessages](responsemessages.md)
- [ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md)
  
```XML
<ApplyConversationActionResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ApplyConversationActionResponseMessage>
```

 **ApplyConversationActionResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ResponseClass** <br/> | Describes the status of the response.<br/><br/>The following values are valid for this attribute:<ul><li>Success</li><li>Warning</li><li>Error</li></ul> |
   
#### ResponseClass attribute values

|**Value**|**Description**|
|:-----|:-----|
|**Success** <br/> |Describes a request that is fulfilled.  <br/> |
|**Warning** <br/> | Describes a request that was not processed. A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.<br/><br/>The following are examples of sources of warnings:<ul><li>The Exchange store is offline during the batch.</li><li>Active Directory Domain Services (AD DS) is offline.</li><li>Mailboxes were moved.</li><li>The message database (MDB) is offline.</li><li>A password is expired.</li><li>A quota has been exceeded.</li></ul> |
|**Error** <br/> | Describes a request that cannot be fulfilled.<br/><br/>The following are examples of sources of errors:  <ul><li>Invalid attributes or elements</li><li>Attributes or elements that are out of range</li><li>An unknown tag  </li><li>An attribute or element that is not valid in the context</li><li>An unauthorized access attempt by any client</li><li>A server-side failure in response to a valid client-side call</li></ul>Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides an error code that identifies the specific error that the request encountered.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and reserved for future use. This element contains a value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services request.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).
  
### Version differences

In versions of Exchange starting with build 15.00.0986.00, the **ApplyConversationActionResponseMessage** element is of type **ApplyConversationActionResponseMessageType**. In previous versions, the element is of type **ResponseMessageType**.
  
## Element information

|**Element**|**Example**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [ApplyConversationAction operation](applyconversationaction-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

