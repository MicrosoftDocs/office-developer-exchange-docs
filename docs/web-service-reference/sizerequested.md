---
title: "SizeRequested"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: e86f98b6-83b5-4530-80eb-dc5df42e2c62
description: "The SizeRequested element contains the requested photo size for a GetUserPhoto operation."
---

# SizeRequested

The **SizeRequested** element contains the requested photo size for a **GetUserPhoto** operation. 
  
```XML
<SizeRequested>HR48x48 | HR64x64 | HR96X96 | HR120X120 | HR240X240 | HR360X360 | HR432X432 | HR504X504 | HR648X648</SizeRequested>
```

 **UserPhotoSizeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[GetUserPhoto](getuserphoto.md)
  
## Text value

The text value of the **SizeRequested** element is the requested photo size of a digital image returned from the server. The following table identifies the text values for the **SizeRequested** element. 
  
|**Value**|**Meaning**|
|:-----|:-----|
|HR48x48  <br/> |The image is 48 pixels high and 48 pixels wide.  <br/> |
|HR64x64  <br/> |The image is 64 pixels high and 64 pixels wide.  <br/> |
|HR96x96  <br/> |The image is 96 pixels high and 96 pixels wide.  <br/> |
|HR120x120  <br/> |The image is 120 pixels high and 120 pixels wide.  <br/> |
|HR240x240  <br/> |The image is 240 pixels high and 240 pixels wide.  <br/> |
|HR360x360  <br/> |The image is 360 pixels high and 360 pixels wide.  <br/> |
|HR432x432  <br/> |The image is 432 pixels high and 432 pixels wide.  <br/> |
|HR504x504  <br/> |The image is 504 pixels high and 504 pixels wide.  <br/> |
|HR648x648  <br/> |The image is 648 pixels high and 648 pixels wide.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> ||
   

