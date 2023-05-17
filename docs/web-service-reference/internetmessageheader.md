---
title: "InternetMessageHeader"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- InternetMessageHeader
api_type:
- schema
ms.assetid: c70675f8-6feb-4c89-ba48-bce0479b308b
description: "The InternetMessageHeader element represents the Internet message header for a given header within the headers collection. To get the entire collection of Internet message headers, use the PR_TRANSPORT_MESSAGE_HEADERS property. For more information about EWS and Internet message headers, seeGetting Internet message headers in EWS, MIME, and the missing Internet message headers."
---

# InternetMessageHeader

The **InternetMessageHeader** element represents the Internet message header for a given header within the headers collection. To get the entire collection of Internet message headers, use the **PR_TRANSPORT_MESSAGE_HEADERS** property. For more information about EWS and Internet message headers, see "Getting Internet message headers in [EWS, MIME, and the missing Internet message headers](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx).
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 **InternetHeaderType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**HeaderName** <br/> |Identifies the header name.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Represents the collection of all Internet message headers that are contained in an item in a mailbox.  <br/> |
   
## Text value

The text value represents the value for the header.
  
## Remarks

The following is the EWS Managed API extended property definition for the **PR_TRANSPORT_MESSAGE_HEADERS** property. 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[EWS, MIME, and the missing Internet message headers](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)

