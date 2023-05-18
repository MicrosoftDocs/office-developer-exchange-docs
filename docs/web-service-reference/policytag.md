---
title: "PolicyTag"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: "The PolicyTag element specifies the retention identifier on an item or folder."
---

# PolicyTag

The **PolicyTag** element specifies the retention identifier on an item or folder. 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 **RetentionTagType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|IsExplicit  <br/> |Indicates whether a policy tag was explicitly set on an item or folder.  <br/> A text value of **true** for the **IsExplicit** attribute indicates that the policy tag was explicitly set on the item or folder. A text value of **false** indicates that the policy tag was implicitly set on the item or folder based on the parent folder policy tag.  <br/> |
   
### Child elements

None.
  
### Parent elements

[SearchPreviewItem](searchpreviewitem.md) | [Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)
  
## Text value

The text value of the **PolicyTag** element is the policy tag identifier. The policy tag identifier is a GUID. 
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> ||
   

