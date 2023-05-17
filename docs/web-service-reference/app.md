---
title: "App"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 92b776b5-fec6-4443-a606-51ccb06f7afd
description: "The App element contains information about an XML manifest file for a mail app that is installed in a mailbox."
---

# App

The **App** element contains information about an XML manifest file for a mail app that is installed in a mailbox. 
  
```XML
<App>
    <Metadata/>
    <Manifest/>
</App>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[Metadata](metadata-ex15websvcsotherref.md) | [Manifest](manifest.md)
  
### Parent elements

[Apps](apps.md)
  
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Not applicable  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [Apps](apps.md)
- [Metadata](metadata-ex15websvcsotherref.md)
- [Manifest](manifest.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

