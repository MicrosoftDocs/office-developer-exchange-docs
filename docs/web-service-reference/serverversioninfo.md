---
title: "ServerVersionInfo"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ServerVersionInfo
api_type:
- schema
ms.assetid: c04a6872-ca27-432b-aac2-36b023d0afc6
description: "The ServerVersionInfo element represents the Microsoft Exchange Server version number."
---

# ServerVersionInfo

The **ServerVersionInfo** element represents the Microsoft Exchange Server version number. 
  
```xml
<ServerVersionInfo MajorVersion="" MinorVersion="" MajorBuildNumber="" MinorBuildNumber="" Version="" />
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|MajorVersion  <br/> |Describes the major version number.  <br/> |
|MinorVersion  <br/> |Describes the minor version number.  <br/> |
|MajorBuildNumber  <br/> |Describes the major build number.  <br/> |
|MinorBuildNumber  <br/> |Describes the minor build number.  <br/> |
|Version  <br/> |Describes the Exchange Web Services (EWS) schema version.  <br/> |
   
### Child elements

None.
  
### Parent elements

None.
  
## Remarks

This element is returned in the SOAP header of an Exchange Web Services response message.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed. 
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can Be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

