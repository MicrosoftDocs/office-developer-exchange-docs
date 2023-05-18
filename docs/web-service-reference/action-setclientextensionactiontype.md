---
title: "Action (SetClientExtensionActionType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: c5624a87-3436-40ce-8d6b-cc01eecab64d
description: "The Action element contains the action that the Exchange server should take on an app."
---

# Action (SetClientExtensionActionType)

The **Action** element contains the action that the Exchange server should take on an app. 
  
```XML
<Action ActionId="" ExtensionId="">
   <ClientExtension/>
</Action>
```

 **SetClientExtensionActionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|ActionId  <br/> |Specifies the identifier of the action. This attribute is required.  <br/> |
|ExtensionId  <br/> |Specifies the identifier of the extension. This attribute is optional.  <br/> |
   
#### ActionId

|**Value**|**Description**|
|:-----|:-----|
|Configure  <br/> |Indicates a configuration action.  <br/> |
|Install  <br/> |Indicates an installation action.  <br/> |
|Uninstall  <br/> |Indicates an uninstallation action.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ClientExtension](clientextension.md) <br/> |Contains user and configuration information about an app.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Actions (ArrayOfSetClientExtensionActionsType)](actions-arrayofsetclientextensionactionstype.md) <br/> |Specifies an array of **Action** elements.  <br/> |
   
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

