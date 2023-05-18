---
title: "Attribution (PersonaAttributionType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: "The Attribution element specifies an instance in an array of attributes for a PersonaType element."
---

# Attribution (PersonaAttributionType)

The **Attribution** element specifies an instance in an array of attributes for a **PersonaType** element. 
  
```XML
<Attribution>
    <Id></Id>
    <SourceId></SourceId>
    <DisplayName></DisplayName>
    <IsWritable></IsWritable>
    <IsQuickContact></IsQuickContact>
    <IsHidden></IsHidden>
    <FolderId></FolderId>
</Attribution>
```

 **PersonaAttributionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ID (String)](id-string.md) <br/> |Specifies a string that uniquely identifies an app or an attribution in a persona.  <br/> |
|[SourceId](sourceid.md) <br/> |Specifies the identifier of the contact or Active Directory recipient.  <br/> |
|[DisplayName (string)](displayname-string.md) <br/> |Defines the display name of a folder, contact, distribution list, delegate user, or rule.  <br/> |
|[IsWritable](iswritable.md) <br/> |Specifies whether the underlying contact or Active Directory recipient can be written to.  <br/> |
|[IsQuickContact](isquickcontact.md) <br/> |Specifies a Boolean value that indicates whether the underlying contact or Active Directory recipient is a quick contact.  <br/> |
|[IsHidden](ishidden.md) <br/> |Contains a Boolean value that indicates whether the underlying contact or Active Directory recipient should be hidden or displayed as part of the persona.  <br/> |
|[FolderId](folderid.md) <br/> |Contains the identifier and change key of a folder.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Attributions (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md) <br/> |Specifies an array of attribution information for one or more of the contacts or active directory (AD) recipients aggregated into the associated persona.  <br/> |
   
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

