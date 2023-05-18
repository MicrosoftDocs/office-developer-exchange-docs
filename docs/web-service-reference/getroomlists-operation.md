---
title: "GetRoomLists operation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GetRoomLists
api_type:
- schema
ms.assetid: 55d451f9-547f-44ac-872e-9cb220ea7b7c
description: "The GetRoomLists operation gets the room lists that are available within the Exchange organization."
---

# GetRoomLists operation

The **GetRoomLists** operation gets the room lists that are available within the Exchange organization. 
  
## SOAP Headers

The **GetRoomLists** operation can use the SOAP headers that are listed and described in the following table. 
  
|**Header**|**Element**|**Description**|
|:-----|:-----|:-----|
|Impersonation  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifies the user whom the client application is impersonating.  <br/> |
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifies the RFC3066 culture to be used to access the mailbox.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifies the schema version for the operation request.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifies the version of the server that responded to the request.  <br/> |
   
## GetRoomLists request example

### Description

The following is an example of a **GetRoomLists** request that returns the room lists that are available on the server. 
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
    <m:GetRoomLists />
  </soap:Body>
</soap:Envelope>

```

### Request elements

The following element is used in the request:
  
- [GetRoomLists](getroomlists.md)
    
## Successful GetRoomLists response example

### Description

The following is an example of a response to a **GetRoomLists** request. This response shows one room list on the server. 
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomListsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:RoomLists xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
        <t:Address xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
          <t:Name>Room List</t:Name>
          <t:EmailAddress>RoomList@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
      </m:RoomLists>
    </GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

### Successful GetRoomLists response elements

The following elements are used in the response:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetRoomListsResponse](getroomlistsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [RoomLists](roomlists.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddress)](routingtype-emailaddress.md)
    
- [MailboxType](mailboxtype.md)
    
### GetRoomLists Error response example

#### Description

The following example shows the response to an attempt to get room lists from a server that does not have any room lists defined.
  
#### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomListsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:RoomLists xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"/>
    </GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

#### GetRoomLists Error response elements

The following elements are used in the error response:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetRoomListsResponse](getroomlistsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [RoomLists](roomlists.md)
    
## See also



[EWS operations in Exchange](ews-operations-in-exchange.md)
  
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

