---
title: "Message (Availability)"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Message
api_type:
- schema
ms.assetid: 1eec24dd-c981-41f4-a2f0-c51d43f1d7c0
description: "The Message element contains the out of Office (OOF) response."
---

# Message (Availability)

The **Message** element contains the out of Office (OOF) response. 
  
```
<Message/> 
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[InternalReply](internalreply.md) <br/> | Contains the OOF message sent to other users in the sender's domain.  <br/>  The following are the possible XPath expressions to this element:  <br/>  `/SetUserOofSettingsRequest/UserOofSettings/InternalReply` <br/>  `/GetUserOofSettingsResponse/OofSettings/InternalReply` <br/> |
|[ExternalReply](externalreply.md) <br/> | Contains the OOF message that is sent to addresses outside the sender's domain.  <br/>  The following are the possible XPath expressions to this element:  <br/>  `/SetUserOofSettingsRequest/UserOofSettings/ExternalReply` <br/>  `/GetUserOofSettingsResponse/OofSettings/ExternalReply` <br/> |
|[ReplyBody](replybody.md) <br/> |Contains an OOF message and the language used for the message.  <br/> |
   
## Text value

A text value is required to set the OOF message.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Example

The following example of a [SetUserOofSettings operation](setuseroofsettings-operation.md) request sets the [OofState](oofstate.md) to **Enabled**, sets the duration of OOF to 10 days, and sets the internal and external OOF messages.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[SetUserOofSettings operation](setuseroofsettings-operation.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

