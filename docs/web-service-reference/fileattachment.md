---
title: "FileAttachment"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FileAttachment
api_type:
- schema
ms.assetid: 3ecea174-73d1-47fd-8917-6065cef1d565
description: "The FileAttachment element represents a file that is attached to an item in the Exchange store."
---

# FileAttachment

The **FileAttachment** element represents a file that is attached to an item in the Exchange store. 
  
```XML
<FileAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <IsContactPhoto/>
   <Content/>
</FileAttachment>
```

 **FileAttachmentType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AttachmentId](attachmentid.md) <br/> |Identifies the file attachment.  <br/> |
|[Name (AttachmentType)](name-attachmenttype.md) <br/> |Represents the name of the attachment.  <br/> |
|[ContentType](contenttype.md) <br/> |Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.  <br/> |
|[ContentId](contentid.md) <br/> |Represents an identifier for the contents of an attachment. [ContentId](contentid.md) can be set to any string value. Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.  <br/> |
|[ContentLocation](contentlocation.md) <br/> |Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.  <br/> |
|[Size](size.md) <br/> |Represents the size in bytes of the file attachment.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Represents when the file attachment was last modified.  <br/> |
|[IsInline](isinline.md) <br/> |Represents whether the attachment appears inline within an item.  <br/> |
|[IsContactPhoto](iscontactphoto.md) <br/> |Indicates whether the file attachment is a contact picture.  <br/> |
|[Content](content.md) <br/> |Contains the Base64-encoded contents of the file attachment.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Attachments](attachments-ex15websvcsotherref.md) <br/> |Contains the items or files that are attached to an item in the Exchange store.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

