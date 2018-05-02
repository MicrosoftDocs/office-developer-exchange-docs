---
title: "IsUMEnabled (UM web service)"
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: 33810bbd-837f-4a71-9ed9-cb4b8c52186d
description: "The IsUMEnabled element indicates whether a mailbox is enabled for Unified Messaging."
 
 
---

# IsUMEnabled (UM web service)

The **IsUMEnabled** element indicates whether a mailbox is enabled for Unified Messaging. 
  
```
<IsUMEnabled/>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

None.
  
## Text value

A text value that represents a Boolean value is required if this element is included. A value of **true** indicates that the mailbox is enabled for Unified Messaging. A value of **false** means that the mailbox is not enabled for Unified Messaging. 
  
## Remarks

To determine whether a mailbox is enabled for Unified Messaging, use the [IsUMEnabled operation (UM web service)](isumenabled-operation-um-web-service.md).
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[IsUMEnabled operation (UM web service)](isumenabled-operation-um-web-service.md)
#### Concepts

[Unified Messaging web service XML elements for Exchange](unified-messaging-web-service-xml-elements-for-exchange.md)

