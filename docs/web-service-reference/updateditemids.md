---
title: "UpdatedItemIds"
 
 
manager: sethgros
ms.date: 3/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9199aeb2-abdf-40c5-8743-40b61853c951
description: "The UpdatedItemIds element specifies the identifiers of updated reminder items."
---

# UpdatedItemIds

The **UpdatedItemIds** element specifies the identifiers of updated reminder items. 
  
```XML
<UpdatedItemIds>
   <ItemId></ItemId>
</UpdatedItemIds>

```

 **NonEmptyArrayOfItemIdsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[ItemId](itemid.md)
  
#### Parent elements

[PerformReminderActionResponse](performreminderactionresponse.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
If the [PerformReminderAction](performreminderaction-operation.md) operation did not complete successfully, or no changes were made on the server, the **UpdatedItemIds** element is returned as an empty value. 
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

#### Reference

[PerformReminderActionResponse](performreminderactionresponse.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

