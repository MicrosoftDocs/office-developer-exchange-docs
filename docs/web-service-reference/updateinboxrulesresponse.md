---
title: "UpdateInboxRulesResponse"
description: "The UpdateInboxRulesResponse element defines a response to an UpdateInboxRules request."
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- UpdateInboxRulesResponse
api_type:
- schema
ms.assetid: 0947b6aa-0d95-421b-aebb-d03021ecc110
---

# UpdateInboxRulesResponse

The **UpdateInboxRulesResponse** element defines a response to an UpdateInboxRules request. 
  
```XML
<UpdateInboxRulesResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RuleOperationErrors/>
</UpdateInboxRulesResponse>
```

**UpdateInboxRulesResponseType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ResponseClass** <br/> | Describes the status of an [Unsubscribe operation](unsubscribe-operation.md) response.<br/><br/> The following values are valid for this attribute:  <br/><br/>- Success  <br/>- Warning  <br/>- Error  <br/> |
   
#### ResponseClass attribute values

|**Value**|**Description**|
|:-----|:-----|
|**Success** <br/> |Describes a request that is fulfilled.  <br/> |
|**Warning** <br/> | Describes a request that was not processed. A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed. <br/><br/>The following are examples of sources of warnings:  <br/><br/>- The Exchange store is offline during the batch.  <br/>- Active Directory Domain Services (AD DS) is offline.  <br/>- Mailboxes are moved.  <br/>- The message database (MDB) is offline.  <br/>- A password is expired.  <br/>- A quota is exceeded.  <br/> |
|**Error** <br/> | Describes a request that cannot be fulfilled. <br/><br/>The following are examples of sources of errors:  <br/><br/>- Invalid attributes or elements  <br/>- Attributes or elements that are out of range  <br/>- An unknown tag  <br/>- An attribute or element that is not valid in the context  <br/>- An unauthorized access attempt by any client  <br/>- A server-side failure in response to a valid client-side call  <br/> <br/> Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides status information about the request.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and is reserved for future use. It contains a value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
|[RuleOperationErrors](ruleoperationerrors.md) <br/> |Represents an array of rule validation errors on each rule field that has an error.  <br/> |
   
### Parent elements

None.
  
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element info|value|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [UpdateInboxRules](updateinboxrules.md)
- [UpdateInboxRules operation](updateinboxrules-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
