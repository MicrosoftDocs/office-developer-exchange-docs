---
title: "ParentItemId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ParentItemId
api_type:
- schema
ms.assetid: 72dc4391-72db-44d2-85d9-4718d59886a7
description: "The ParentItemId element identifies the parent item that links to an associated attachment."
---

# ParentItemId

The **ParentItemId** element identifies the parent item that links to an associated attachment. 
  
- [CreateAttachment](createattachment.md)
  
- [ParentItemId](parentitemid.md)
  
```xml
<ParentItemId Id="" ChangeKey="" />
```

**ItemIdType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Id** <br/> |Identifies a single item in the Exchange store to associate with an attachment. This value is a string. This attribute is required.  <br/> |
|**ChangeKey** <br/> |Identifies an unspecified version of an item that is identified by the **Id** attribute in the Exchange store. This is used to make sure that a current item is used when it is updated with an attachment. This value is a string. This attribute is optional.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CreateAttachment](createattachment.md) <br/> |Defines a request to create an attachment to an item in a mailbox.  <br/> The following is the XPath expression to this element:  <br/>  `/CreateAttachment` <br/> |
   
## Remarks

This element is required in the [CreateAttachment operation](createattachment-operation.md). This element is basically the same as the [ItemId](itemid.md) element. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |[https://schemas.microsoft.com/exchange/services/2006/messages](https://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [CreateAttachment operation](createattachment-operation.md)

