---
title: "ActionUrl"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 9697f2e5-a5f7-471a-a052-ae79e06eb09d
description: "The ActionUrl element identifies the URL that the user should navigate to, in order to fix an issue indicated by the AppStatus element."
---

# ActionUrl

The **ActionUrl** element identifies the URL that the user should navigate to, in order to fix an issue indicated by the [AppStatus](appstatus-ex15websvcsotherref.md) element. 
  
```XML
<ActionUrl/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[Metadata](metadata-ex15websvcsotherref.md)
  
## Text value

The text value of the **ActionUrl** element identifies the URL that the user should navigate to, in order to fix an issue indicated by the **AppStatus** element. 
  
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> | https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Not applicable  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [Metadata](metadata-ex15websvcsotherref.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

