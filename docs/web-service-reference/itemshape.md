---
title: "ItemShape"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ItemShape
api_type:
- schema
ms.assetid: c5604161-bbc0-40bc-ad75-ff7e837d745f
description: "The ItemShape element identifies a set of properties to return in a GetItem operation, FindItem operation, or SyncFolderItems operation response."
---

# ItemShape

The **ItemShape** element identifies a set of properties to return in a [GetItem operation](getitem-operation.md), [FindItem operation](finditem-operation.md), or [SyncFolderItems operation](syncfolderitems-operation.md) response. 
  
```XML
<ItemShape>
   <BaseShape/>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <ConvertHtmlCodePageToUTF8/>
   <AdditionalProperties/>
</ItemShape>
```

 **ItemResponseShapeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[BaseShape](baseshape.md) <br/> |Identifies the basic configuration of properties to return in an item or folder response.  <br/> |
|[IncludeMimeContent](includemimecontent.md) <br/> |Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item is returned in the response.  <br/> |
|[BodyType](bodytype.md) <br/> |Identifies how the body text is formatted in the response.  <br/> |
|[ConvertHtmlCodePageToUTF8](converthtmlcodepagetoutf8.md) <br/> |Indicates whether the item HTML body is converted to UTF8.  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |Specifies whether HTML content filtering is enabled.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifies additional properties to return in a response.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetItem](getitem.md) <br/> |Defines a request to retrieve items from a mailbox in the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/GetItem` <br/> |
|[FindItem](finditem.md) <br/> |Defines a request to find all items that are contained in a folder.  <br/> The following is the XPath expression to this element:  <br/>  `/FindItem` <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |Defines a request to synchronize items in an Exchange store folder.  <br/> The following is the XPath expression to this element:  <br/>  `/SyncFolderItems` <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetItem operation](getitem-operation.md)
  
[FindItem operation](finditem-operation.md)
  
[SyncFolderItems operation](syncfolderitems-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

