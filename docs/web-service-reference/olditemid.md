---
title: "OldItemId"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- OldItemId
api_type:
- schema
ms.assetid: fb57deee-9cc3-4730-9805-ff34f39e3ab7
description: "The OldItemId element contains the unique identifier of the item that was copied or moved."
---

# OldItemId

The **OldItemId** element contains the unique identifier of the item that was copied or moved. 
  
```xml
<OldItemId Id="" ChangeKey=""/>
```

 **ItemIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Id** <br/> |Contains a string that identifies an item in the Exchange store. This attribute is required.  <br/> |
|**ChangeKey** <br/> |Contains a string that identifies a version of an item that is identified by the Id attribute. This attribute is optional. Use this attribute to make sure that the correct version of an item is used.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CopiedEvent](copiedevent.md) <br/> |Represents an event in which an item or folder is copied.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Represents an event in which an item or folder is moved from one parent folder to another parent folder.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[Subscribe operation](subscribe-operation.md)
  
[GetEvents operation](getevents-operation.md)
  
[Unsubscribe operation](unsubscribe-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

