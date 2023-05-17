---
title: "EmptyFolderResponse"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: c900be49-3c90-41aa-aba5-bcf1116ec2aa
description: "The EmptyFolderResponse element defines a response to an EmptyFolder operation request."
---

# EmptyFolderResponse

The **EmptyFolderResponse** element defines a response to an [EmptyFolder operation](emptyfolder-operation.md) request. 
  
```XML
<EmptyFolderResponse>
   <ResponseMessages/>
</EmptyFolderResponse>
```

 **EmptyFolderResponseType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services request.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[EmptyFolder operation](emptyfolder-operation.md)
  
[EmptyFolder](emptyfolder.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

