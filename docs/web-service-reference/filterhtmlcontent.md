---
title: "FilterHtmlContent"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FilterHtmlContent
api_type:
- schema
ms.assetid: 2f9358a0-de1d-4544-9aa0-d9f6519f3b5f
description: "The FilterHtmlContent element specifies whether potentially unsafe HTML content is filtered from an item or attachment."
---

# FilterHtmlContent

The **FilterHtmlContent** element specifies whether potentially unsafe HTML content is filtered from an item or attachment. 
  
```xml
<FilterHtmlContent>true or false</FilterHtmlContent>
```

 **boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[AttachmentShape](attachmentshape.md) <br/> | Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.  <br/><br/>  The following is the XPath expression to this element: <br/> <br/>  `/GetAttachment/AttachmentShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.  <br/> <br/> The following are the XPath expressions to this element: <br/> <br/>  `/GetItem/ItemShape`<br/> <br/>  `/FindItem/ItemShape`<br/> <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## Text value

This element can be either **true** or **false**. The default value is **false**. This is a Boolean data type.
  
## Remarks

This element is optional.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.
  
## Element information

|Element|Type|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

