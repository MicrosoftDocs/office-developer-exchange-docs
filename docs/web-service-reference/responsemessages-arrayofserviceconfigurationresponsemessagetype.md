---
title: "ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: c7cfa0d1-fcb2-441f-8489-3a549da33b34
description: "The ResponseMessages element contains an array of service configuration response messages."
---

# ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)

The **ResponseMessages** element contains an array of service configuration response messages. 
  
```XML
<ResponseMessages>
   <ServiceConfigurationResponseMessageType/>
</ResponseMessages>
```

 **ArrayOfServiceConfigurationResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contains service configuration settings. This element is required.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md) <br/> |Defines a response to a GetServiceConfiguration request.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

