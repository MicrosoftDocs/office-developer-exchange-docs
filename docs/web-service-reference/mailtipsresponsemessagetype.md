---
title: "MailTipsResponseMessageType"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MailTipsResponseMessageType
api_type:
- schema
ms.assetid: 532cb9d9-1232-4e88-80aa-4cf163eb05da
description: "The MailTipsResponseMessageType element represents mail tips settings."
---

# MailTipsResponseMessageType

The **MailTipsResponseMessageType** element represents mail tips settings. 
  
```XML
<MailTipsResponseMessageType ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailTips/>
</MailTipsResponseMessageType>
```

 **MailTipsResponseMessageType**
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
|**Warning** <br/> | Describes a request that was not processed. A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed. <br/><br/>The following are examples of sources of warnings: <br/> <br/>- The Exchange store is offline during the batch.  <br/>- Active Directory Domain Services (AD DS) is offline.  <br/>- Mailboxes were moved.  <br/>- The message database (MDB) is offline.  <br/>- A password is expired.  <br/>- A quota has been exceeded.  <br/> |
|**Error** <br/> | Describes a request that cannot be fulfilled. <br/><br/>The following are examples of sources of errors:  <br/><br/>- Invalid attributes or elements  <br/>- Attributes or elements that are out of range  <br/>- An unknown tag  <br/>- An attribute or element that is not valid in the context  <br/>- An unauthorized access attempt by any client  <br/>- A server-side failure in response to a valid client-side call  <br/><br/>  Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides an error code that identifies the specific error that the request encountered.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and reserved for future use. This element contains a value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
|[MailTips](mailtips.md) <br/> |Represents values for various types of mail tips.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages (ArrayOfMailTipsResponseMessageType)](responsemessages-arrayofmailtipsresponsemessagetype.md) <br/> |Represents a list of mail tips response messages.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

