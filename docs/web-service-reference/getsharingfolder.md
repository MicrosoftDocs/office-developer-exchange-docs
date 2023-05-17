---
title: "GetSharingFolder"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GetSharingFolder
api_type:
- schema
ms.assetid: ed5bb61f-89c7-4baa-83ee-30f06a49ff9b
description: "The GetSharingFolder element defines a request to get the local folder identifier of a specified shared folder. It is the base element for the GetSharingFolder operation."
---

# GetSharingFolder

The **GetSharingFolder** element defines a request to get the local folder identifier of a specified shared folder. It is the base element for the [GetSharingFolder operation](getsharingfolder-operation.md).
  
```xml
<GetSharingFolder>   <SmtpAddress/>   <DataType/>   <SharedFolderId/></GetSharingFolder>
```

 **GetSharingFolderType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SmtpAddress](smtpaddress.md) <br/> |Represents the SMTP e-mail address of the other party in the sharing relationship. This element is required.  <br/> |
|[DataType](datatype.md) <br/> |Describes the type of data that is shared by a shared folder. This element is optional.  <br/> |
|[SharedFolderId](sharedfolderid.md) <br/> |Represents the identifier of the shared folder whose local folder identifier should be returned. This element is optional.  <br/> |
   
### Parent elements

None.
  
## Remarks

A GetSharingFolder element must contain an [SmtpAddress](smtpaddress.md) element. A GetSharingFolder element must also contain either a [DataType](datatype.md) element or a [SharedFolderId](sharedfolderid.md) element, but cannot contain both. 
  
The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetSharingFolder operation](getsharingfolder-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

