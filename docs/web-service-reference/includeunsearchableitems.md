---
title: "IncludeUnsearchableItems"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 9a9bd2dc-f5b9-4b82-a6a0-f643d2951080
description: "The IncludeUnsearchableItems element specifies whether to include items that cannot be searched."
---

# IncludeUnsearchableItems

The **IncludeUnsearchableItems** element specifies whether to include items that cannot be searched. 
  
```XML
<IncludeUnsearchableItems>true | false</IncludeUnsearchableItems>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindMailboxStatisticsByKeywords](findmailboxstatisticsbykeywords.md) <br/> |Specifies a request to search for mailbox statistics by keyword.  <br/> |
   
## Text value

A text value of **true** for the **IncludeUnsearchableItems** element indicates that statistics are not included for items that are not searchable. A value of **false** indicates that statistics are included for items that are not searchable. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |messages.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

