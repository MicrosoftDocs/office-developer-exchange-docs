---
title: "Apps"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f6f0a2ca-22dd-4789-9eed-f0c1ec9036c4
description: "The Apps element contains information about all the XML manifest files for apps installed in a mailbox."
---

# Apps

The **Apps** element contains information about all the XML manifest files for apps installed in a mailbox. 
  
```XML
<Apps>
    <App/>
</Apps>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[App](app.md)
  
### Parent elements

[GetAppManifestsResponse](getappmanifestsresponse.md)
  
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Not applicable  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [App](app.md)
- [GetAppManifestsResponse](getappmanifestsresponse.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

