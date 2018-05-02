---
title: "FilterHtmlContent"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FilterHtmlContent
api_type:
- schema
ms.assetid: 2f9358a0-de1d-4544-9aa0-d9f6519f3b5f
description: "The FilterHtmlContent element specifies whether potentially unsafe HTML content is filtered from an item or attachment."
---

# FilterHtmlContent

The **FilterHtmlContent** element specifies whether potentially unsafe HTML content is filtered from an item or attachment. 
  
```
<FilterHtmlContent>true or false</FilterHtmlContent>
```

 **boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AttachmentShape](attachmentshape.md) <br/> | Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.  <br/>  The following is the XPath expression to this element:  <br/>  `/GetAttachment/AttachmentShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.  <br/>  The following are the XPath expressions to this element:  <br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## Text value

This element can be either **true** or **false**. The default value is **false**. This is a Boolean data type.
  
## Remarks

This element is optional.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

