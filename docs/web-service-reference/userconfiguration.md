---
title: "UserConfiguration"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- UserConfiguration
api_type:
- schema
ms.assetid: 1811df99-ca5b-48a3-b160-b3fd70320c34
description: "The UserConfiguration element defines a single user configuration object."
---

# UserConfiguration

The **UserConfiguration** element defines a single user configuration object. 
  
```XML
<UserConfiguration>
   <UserConfigurationName/>
   <ItemId/>
   <Dictionary/>
   <XmlData/>
  <BinaryData/>
</UserConfiguration>
```

 **UserConfigurationType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[UserConfigurationName](userconfigurationname.md) <br/> |Represents the name of a user configuration object. This element must be used when you create a user configuration object.  <br/> |
|[ItemId](itemid.md) <br/> |Defines the user configuration object item identifier.  <br/> |
|[Dictionary](dictionary.md) <br/> |Defines a set of dictionary property entries for a user configuration object.  <br/> |
|[XmlData](xmldata.md) <br/> |Contains XML data property content for a user configuration object.  <br/> |
|[BinaryData](binarydata.md) <br/> |Contains binary data property content for a user configuration object.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CreateUserConfiguration](createuserconfiguration.md) <br/> |Represents a request to create a user configuration object.  <br/> |
|[GetUserConfigurationResponseMessage](getuserconfigurationresponsemessage.md) <br/> |Represents a response that returns a user configuration object.  <br/> |
|[UpdateUserConfiguration](updateuserconfiguration.md) <br/> |Represents a request to update a user configuration object.  <br/> |
   
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
