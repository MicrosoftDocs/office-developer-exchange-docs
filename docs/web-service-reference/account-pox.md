---
title: "Account (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 488fdbdc-e9d9-4301-91ab-e22eb42e549e
description: "The Account element specifies account settings for the user or contains error responses."
---

# Account (POX)

The **Account** element specifies account settings for the user or contains error responses. 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
- [Response (POX)](response-pox.md)
- [Account (POX)](account-pox.md)
  
```XML
<Account>
   <AccountType/>
   <Action/>
   <MicrosoftOnline/>
   <RedirectURL/>
   <RedirectAddr/>
   <Image/>
   <ServiceHome/>
   <Protocol/>
   <PublicFolderInformation/>
</Account>
```

<br/>

```XML
<Account> 
    <Error/> 
</Account>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[AccountType (POX)](accounttype-pox.md) <br/> |Represents the account type.  <br/> |
|[Action (POX)](action-pox.md) <br/> |Provides information that is used to determine whether another Autodiscover request is required to return the user configuration information.  <br/> |
|[MicrosoftOnline (POX)](microsoftonline-pox.md) <br/> |Contains a value that indicates whether the user's mailbox is hosted in Exchange Online or Exchange Online as part of Office 365.  <br/> |
|[RedirectUrl (POX)](redirecturl-pox.md) <br/> |Contains the URL of the computer that is running Exchange Server that has the Client Access server role installed that should be used to obtain Autodiscover settings.  <br/> |
|[RedirectAddr (POX)](redirectaddr-pox.md) <br/> |Specifies the email address that should be used for a subsequent Autodiscover request.  <br/> |
|[Image (POX)](image-pox.md) <br/> |Contains the path of an image that is used to brand the configuration experience.  <br/> |
|[ServiceHome (POX)](servicehome-pox.md) <br/> |Contains the URL of the home page of the Internet service provider (ISP).  <br/> |
|[Protocol (POX)](protocol-pox.md) <br/> |Contains the specifications for connecting a client to the Client Access server.  <br/> |
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.  <br/> |
|[Error (POX)](error-pox.md) <br/> |Contains an Autodiscover error response.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Response (POX)](response-pox.md) <br/> |Contains the response from the Autodiscover service.  <br/> |
   
## See also

- [POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

