---
title: "SearchDumpster"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: ddb62dce-c87a-4714-8023-a6b697a29699
description: "The SearchDumpster element specifies whether to search in the Exchange Dumpster."
---

# SearchDumpster

The **SearchDumpster** element specifies whether to search in the Exchange Dumpster. 
  
```XML
<SearchDumpster> true | false </SearchDumpster>
```

 ****
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[FindMailboxStatisticsByKeywords](findmailboxstatisticsbykeywords.md)
  
## Text value

A text value of **true** for the **SearchDumpster** element indicates that the mailbox statistics search includes the Exchange Dumpster. A value of **false** indicates that the Exchange Dumpster is not searched. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

