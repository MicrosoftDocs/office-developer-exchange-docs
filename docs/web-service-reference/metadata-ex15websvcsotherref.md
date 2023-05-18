---
title: "Metadata"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: c1cc609b-65ff-4998-8d2b-545f0fdcb54c
description: "The Metadata element contains metadata about the mail app."
---

# Metadata

The **Metadata** element contains metadata about the mail app. 
  
```XML
<Metadata>
    <EndNodeUrl/>
    <AppStatus/>
    <ActionUrl/>
</Metadata>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[EndNodeUrl](endnodeurl.md) | [AppStatus](appstatus-ex15websvcsotherref.md) | [ActionUrl](actionurl.md)
  
### Parent elements

[App](app.md)
  
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> | https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Not applicable  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[App](app.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

