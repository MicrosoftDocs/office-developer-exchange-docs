---
title: "ContactId"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 86f66275-1e39-48ed-bd89-ac3bffc465a7
description: "The ContactId element uniquely identifies a contact."
---

# ContactId

The **ContactId** element uniquely identifies a contact. 
  
```XML
<ContactId Id="" ChangeKey=""/>
```

 **ItemIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |The text value of the **Id** attribute is the identifier of the contact item.  <br/> |
|ChangeKey  <br/> |The text value of the **ChangeKey** attribute is the change key of the contact item.  <br/> |
   
### Child elements

None.
  
### Parent elements

[AddImContactToGroup](addimcontacttogroup.md) | [RemoveContactFromImList](removecontactfromimlist.md) | [RemoveImContactFromGroup](removeimcontactfromgroup.md)
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |types.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

