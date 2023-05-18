---
title: "AttachmentShape"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AttachmentShape
api_type:
- schema
ms.assetid: 734914b5-3a16-4744-90a5-741fd30c4676
description: "The AttachmentShape element identifies additional properties to return in a response to a GetAttachment request."
---

# AttachmentShape

The **AttachmentShape** element identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request. 
  
- [GetAttachment](getattachment.md)
  
- [AttachmentShape](attachmentshape.md)
  
```xml
<AttachmentShape>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <AdditionalProperties/>
</AttachmentShape>
```

 **AttachmentResponseShapeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[IncludeMimeContent](includemimecontent.md) <br/> |Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item or attachment is returned in the response. This element is optional.  <br/> |
|[BodyType](bodytype.md) <br/> |Identifies how the body text is formatted in the response. This element is optional.  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |Specifies whether potentially unsafe HTML content is filtered from an attachment. This element is optional.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifies additional properties to return in a response. This element is optional.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetAttachment](getattachment.md) <br/> |The element that defines a request to get an attachment from a mailbox in the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/GetAttachment` <br/> |
   
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

- [GetAttachment operation](getattachment-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

