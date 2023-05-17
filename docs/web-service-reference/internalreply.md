---
title: "InternalReply"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- InternalReply
api_type:
- schema
ms.assetid: 1d784ded-b874-4eb1-8f6d-2e0e03330e1e
description: "The InternalReply element contains the out of office (OOF) response sent to other users in the user's domain or trusted domains."
---

# InternalReply

The **InternalReply** element contains the out of office (OOF) response sent to other users in the user's domain or trusted domains. 
  
```XML
<InternalReply>
   <Message/> 
</InternalReply>
```

 **ReplyBody**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|xml:lang  <br/> |Specifies the language used in the **InternalReply** message. The possible values of this attribute are defined by IETF RFC 3066.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Message (Availability)](message-availability.md) <br/> |Contains the OOF response.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[UserOofSettings](useroofsettings.md) <br/> |Specifies the OOF settings.  <br/> The following is the XPath expression to this element:  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |Contains the OOF settings.  <br/> The following is the XPath expression to this element:  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Example

The following example of a SetUserOofSettings request sets the [OofState](oofstate.md) to **Enabled**, sets the duration of OOF for 10 days, and sets the internal and external OOF messages.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2005-10-05T00:00:00</StartTime>
          <EndTime>2005-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## Element information

|Element|Type|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetUserOofSettings operation](getuseroofsettings-operation.md)
  
[SetUserOofSettings operation](setuseroofsettings-operation.md)

