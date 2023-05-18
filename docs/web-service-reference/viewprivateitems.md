---
title: "ViewPrivateItems"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ViewPrivateItems
api_type:
- schema
ms.assetid: 80b949ac-440c-4a01-b428-ebafb5b1b802
description: "The ViewPrivateItems element indicates whether a delegate user or client application has permission to view private items in the principal's mailbox."
---

# ViewPrivateItems

The **ViewPrivateItems** element indicates whether a delegate user or client application has permission to view private items in the principal's mailbox. 
  
```XML
<ViewPrivateItems>true | false</ViewPrivateItems>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DelegateUser](delegateuser.md) <br/> |Identifies a single delegate to add or update in a mailbox.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contains the client's rights based on the permission settings for the item or folder. This element is read-only.  <br/> |
   
## Text value

A value of **true** indicates that the delegate or client can view private items in the principal's mailbox. A value of **false** indicates that private items are not visible to a delegate or client. 
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [AddDelegate operation](adddelegate-operation.md)
  
- [UpdateDelegate operation](updatedelegate-operation.md)

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

- [Adding Delegates](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)
