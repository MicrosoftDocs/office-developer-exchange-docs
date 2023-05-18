---
title: "ResponseCode (InvalidRecipientResponseCodeType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 582e9caa-d2bc-4be1-a460-739294f9ef18
description: "The ResponseCode element provides information about why the recipient is invalid."
---

# ResponseCode (InvalidRecipientResponseCodeType)

The **ResponseCode** element provides information about why the recipient is invalid. 
  
```XML
<ResponseCode>OtherError or RecipientOrganizationNotFederated or CannotObtainTokenFromSTS or SystemPolicyBlocksSharingWithThisRecipient or RecipientOrganizationFederatedWithUnknownTokenIssuer</ResponseCode>
```

 **InvalidRecipientResponseCodeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[InvalidRecipient](invalidrecipient.md) <br/> |Contains the SMTP address of the invalid recipient and information about why the recipient is invalid.  <br/> |
   
## Text value

The following table lists the possible values for the **ResponseCode** element. 
  
|**Code**|**Description**|
|:-----|:-----|
|OtherError  <br/> |Indicates that the error is not specified by another error response code.  <br/> |
|RecipientOrganizationNotFederated  <br/> |Indicates that a sharing relationship is not available with the organization specified in the recipient's SMTP e-mail address.  <br/> |
|CannotObtainTokenFromSTS  <br/> |Indicates that there was a problem obtaining a security token from the token server.  <br/> |
|SystemPolicyBlocksSharingWithThisRecipient  <br/> |Indicates that the system administrator has set a system policy that blocks sharing with the specified recipient.  <br/> |
|RecipientOrganizationFederatedWithUnknownTokenIssuer  <br/> |Indicates that the secure token service that is used by the specified recipient is unknown.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetSharingMetadata operation](getsharingmetadata-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

