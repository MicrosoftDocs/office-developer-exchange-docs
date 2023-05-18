---
title: "Body"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 7851ea9b-9f87-4adc-a26f-7a27df4a9bca
description: "The Body element specifies the body of an item."
---

# Body

The **Body** element specifies the body of an item. 
  
```XML
<Body> BodyType="" IsTruncated="" </Body>
```

 **BodyType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|BodyType  <br/> |Specifies the type of the body.  <br/> |
|IsTruncated  <br/> |Boolean value that indicates whether the body is truncated.  <br/> |
   
#### BodyType

|**Value**|**Description**|
|:-----|:-----|
|HTML  <br/> |Indicates that the body is in HTML.  <br/> |
|Text  <br/> |Indicates that the body is in text.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[Contact](contact.md) <br/> |Represents a contact item in the Exchange store.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[Item](item.md) <br/> |Represents a generic item in the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents a Microsoft Exchange email message.  <br/> |
|[PostItem](postitem.md) <br/> |Represents a post item in the Exchange store.  <br/> |
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
   
## Text value

The text value of the **Body** element is the body content of the item. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

