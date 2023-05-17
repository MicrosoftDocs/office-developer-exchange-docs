---
title: "SyncScope"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SyncScope
api_type:
- schema
ms.assetid: e0ca231f-0374-4844-8d4c-ada8da167920
description: "The SyncScope element specifies whether just items or items and folder associated information are returned in a synchronization response."
---

# SyncScope

The **SyncScope** element specifies whether just items or items and folder associated information are returned in a synchronization response. 
  
```xml
<SyncScope>NormalItems or NormalAndAssociatedItems</SyncScope>
```

 **SyncFolderItemsScopeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SyncFolderItems](syncfolderitems.md) <br/> |The element that defines a request to synchronize items in an Exchange store folder.  <br/> The following is the XPath expression to this element:  <br/> /SyncFolderItems  <br/> |
   
## Text value

The following table lists the possible values for the **SyncScope** element. 
  
**SyncScope element values**

|**Value**|**Description**|
|:-----|:-----|
|NormalItems  <br/> |Specifies that only items in the folder are returned in a synchronization response.  <br/> |
|NormalAndAssociatedItems  <br/> |Specifies that both items in the folder and folder associated information are returned in a synchronization response.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[SyncFolderItems operation](syncfolderitems-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

