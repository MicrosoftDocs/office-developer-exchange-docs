---
title: "Mailbox (Availability)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Mailbox
api_type:
- schema
ms.assetid: affd192e-8914-473f-9098-d9bdf898de2c
description: "The Mailbox element represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request."
---

# Mailbox (Availability)

The **Mailbox** element represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request. 
  
```xml
<Mailbox>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Mailbox>
```

**EmailAddressType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Name (EmailAddress)](name-emailaddress.md) <br/> |Represents the display name of the mailbox user. This element is optional in the SetUserOofSettingsRequest. The GetUserOofSettingsRequest will return this element.  <br/> |
|[Address (string)](address-string.md) <br/> |Represents the e-mail address of the mailbox user. This element is required.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Represents the routing protocol for the message. This element is optional in the SetUserOofSettingsRequest. The GetUserOofSettingsRequest will return this element.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetUserOofSettingsRequest](getuseroofsettingsrequest.md) <br/> |Used to get a mailbox user's Out of Office (OOF) settings and messages.  <br/> The following is the XPath expression to this element:  <br/>  `/GetUserOofSettingsRequest` <br/> |
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |Used to set a mailbox user's OOF settings and messages.  <br/> The following is the XPath expression to this element:  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## Remarks

The e-mail address is used to identify the calendar folder that contains the OOF settings. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetUserOofSettings operation](getuseroofsettings-operation.md)
- [SetUserOofSettings operation](setuseroofsettings-operation.md)

