---
title: "TextBody"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: "The TextBody element specifies the text body."
---

# TextBody

The **TextBody** element specifies the text body. 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 **BodyType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|BodyTypeType  <br/> |Indicates the body type. The value of **Text** for the **BodyTypeType** attribute indicates that the body is in plain text form. The value of **HTML** for the **BodyTypeType** attribute indicates that the body is in HTML form. The **BodyTypeType** attribute is required.  <br/> |
|IsTruncated  <br/> |Indicates that the body contents have been truncated. A text value of **false** for the **IsTruncated** attribute indicates that the body contents have not been truncated. The normalized body will be truncated if the text body length is longer than the value set in the [MaximumBodySize](maximumbodysize.md) element.  <br/> |
   
### Child elements

None.
  
### Parent elements

[Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)
  
## Text value

The text value of the **TextBody** element is the text body of the item. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

