---
title: "UserConfigurationName"
description: "The UserConfigurationName element represents the name of a user configuration object. The user configuration object name is the identifier for a user configuration object."
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- UserConfigurationName
api_type:
- schema
ms.assetid: 6947dd03-9727-4379-9b9d-42373fa120c7
---

# UserConfigurationName

The **UserConfigurationName** element represents the name of a user configuration object. The user configuration object name is the identifier for a user configuration object. 
  
```XML
<UserConfigurationName Name="">
   <FolderId/>
</UserConfigurationName>
```

```XML
<UserConfigurationName Name="">
   <DistinguishedFolderId/> 
</UserConfigurationName>
```

**UserConfigurationNameType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Name** <br/> |Contains a string value that represents the name of a user configuration object. This attribute is required.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Represents the folder identifier of the folder that contains the user configuration object.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Represents a distinguished folder name of the folder that contains the user configuration object.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DeleteUserConfiguration](deleteuserconfiguration.md) <br/> |Represents a request to delete a user configuration object.  <br/> |
|[GetUserConfiguration](getuserconfiguration.md) <br/> |Represents a request to get a user configuration object.  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |Defines a single user configuration object.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element info|value|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
