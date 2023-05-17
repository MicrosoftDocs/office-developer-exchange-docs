---
title: "ExchangeStoreId"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 5acceb42-a757-4c74-ab1c-b1abf7bf1e0a
description: "The ExchangeStoreId element specifies the instant messaging (IM) group identifier."
---

# ExchangeStoreId

The **ExchangeStoreId** element specifies the instant messaging (IM) group identifier. 
  
```XML
<ExchangeStoreId Id="" ChangeKey=""/>
```

 **ItemIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |The text value of the **Id** attribute is the identifier of the group.  <br/> |
|ChangeKey  <br/> |The text value of the **ChangeKey** attribute is the change key of the group.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ImGroup](imgroup.md) <br/> |Represents an instant messaging group.  <br/> |
   
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

