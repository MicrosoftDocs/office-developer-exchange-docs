---
title: "BodyType"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- BodyType
api_type:
- schema
ms.assetid: d42ec77b-fb9f-404a-9bf2-1801e8744676
description: "The BodyType element identifies how the body text is formatted in the response."
---

# BodyType

The **BodyType** element identifies how the body text is formatted in the response. 
  
```xml
<BodyType>Best or HTML or Text</BodyType>
```

**BodyTypeResponseType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> | Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.  <br/><br/>The following are the XPath expressions to this element:<br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request.  <br/><br/>The following is the XPath expression to this element:<br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## Text value

The following table lists the possible values for the **BodyType** element. 
  
|**Value**|**Description**|
|:-----|:-----|
|Best  <br/> |The response will return the richest available content of body text. This is useful if it is unknown whether the content is text or HTML.<br/><br/> The returned body will be text if the stored body is plain text. Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.<br/><br/> This is the default value.  <br/> |
|HTML  <br/> |The response will return an item body as HTML.  <br/> |
|Text  <br/> |The response will return an item body as plain text.  <br/> |
   
## Remarks

You can identify the type of body returned in the response by checking the **BodyType** attribute of the [Body](body.md) element. The **BodyType** attribute will identify the body as either HTML or text. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Example

The following example of a request shows where a **BodyType** element is used. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape>
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

The Id attribute has been shortened to preserve readability.
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   

