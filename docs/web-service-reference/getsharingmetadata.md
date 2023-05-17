---
title: "GetSharingMetadata"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GetSharingMetadata
api_type:
- schema
ms.assetid: b609ee26-6d28-4559-81b6-b8e8d4759a23
description: "The GetSharingMetadata element defines a request to get an opaque authentication token that identifies the sharing invitation. This element is the base element for the GetSharingMetadata operation."
---

# GetSharingMetadata

The **GetSharingMetadata** element defines a request to get an opaque authentication token that identifies the sharing invitation. This element is the base element for the [GetSharingMetadata operation](getsharingmetadata-operation.md).
  
```XML
<GetSharingMetadata>
   <IdOfFolderToShare/>
   <SenderSmtpAddress/>
   <Recipients/>
</GetSharingMetadata>
```

 **GetSharingMetadataType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[IdOfFolderToShare](idoffoldertoshare.md) <br/> |Represents the identifier of the folder on the server that will be shared. This element is required.  <br/> |
|[SenderSmtpAddress](sendersmtpaddress.md) <br/> |Represents the SMTP email address that corresponds to the mailbox that contains the folder that is identified by the [IdOfFolderToShare](idoffoldertoshare.md) element. This element is required.  <br/> |
|[Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Represents the SMTP email addresses of one or more entities that will be granted access to the data in the folder that is identified by the [IdOfFolderToShare](idoffoldertoshare.md) element. This element is required.  <br/> |
   
### Parent elements

None.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetSharingMetadata operation](getsharingmetadata-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

