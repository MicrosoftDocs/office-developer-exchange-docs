---
title: "UserConfigurationProperties"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- UserConfigurationProperties
api_type:
- schema
ms.assetid: c143a6ec-62ad-4d48-b844-b1ad88054bc1
description: "The UserConfigurationProperties element specifies the property types to get in a GetUserConfiguration operation."
---

# UserConfigurationProperties

The **UserConfigurationProperties** element specifies the property types to get in a GetUserConfiguration operation. 
  
```xml
<UserConfigurationProperties>Id | Dictionary | XmlData | BinaryData | All</UserConfigurationProperties>
```

 **UserConfigurationPropertyType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetUserConfiguration](getuserconfiguration.md) <br/> |Specifies a request to get a user configuration object.  <br/> |
   
## Text value

The following table lists the possible values for the **UserConfigurationProperties** element. 
  
|**Value**|**Description**|
|:-----|:-----|
|Id  <br/> |Specifies the identifier property.  <br/> |
|Dictionary  <br/> |Specifies dictionary property types.  <br/> |
|XmlData  <br/> |Specifies XML data property types.  <br/> |
|BinaryData  <br/> |Specifies binary data property types.  <br/> |
|All  <br/> |Specifies the identifier, dictionary, XML data, and binary data property types.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

