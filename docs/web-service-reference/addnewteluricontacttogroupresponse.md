---
title: "AddNewTelUriContactToGroupResponse"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: abff2306-a3a7-489a-b548-2edbc1eb5cc4
description: "The AddNewTelUriContactToGroupResponse element specifies the result data for the AddNewTelUriContactToGroup WSDL operation."
---

# AddNewTelUriContactToGroupResponse

The **AddNewTelUriContactToGroupResponse** element specifies the result data for the **AddNewTelUriContactToGroup** WSDL operation. 
  
```XML
<AddNewTelUriContactToGroupResponse>
   <Persona/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
</AddNewTelUriContactToGroupResponse>
```

 **AddNewTelUriContactToGroupResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

[Persona](persona.md) | [MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md)
  
### Parent elements

None.
  
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [AddNewTelUriContactToGroup operation](addnewteluricontacttogroup-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

