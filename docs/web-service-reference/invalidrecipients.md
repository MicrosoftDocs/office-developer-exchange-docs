---
title: "InvalidRecipients"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- InvalidRecipients
api_type:
- schema
ms.assetid: e4e7b50e-2fa9-4649-94a6-6002f341ecc4
description: "The InvalidRecipients element represents the recipients of a folder sharing request that are invalid."
---

# InvalidRecipients

The **InvalidRecipients** element represents the recipients of a folder sharing request that are invalid. 
  
```XML
<InvalidRecipients>
   <InvalidRecipient/>
</InvalidRecipients>
```

 **ArrayOfInvalidRecipientsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[InvalidRecipient](invalidrecipient.md) <br/> |Contains the SMTP address of the invalid recipient and information about why the recipient is invalid.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetSharingMetadata operation](getsharingmetadata-operation.md)

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
