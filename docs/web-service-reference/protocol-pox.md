---
title: "Protocol (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: f77e4d66-6fdd-4999-9339-f7d7f9c86f44
description: "The Protocol element contains the specifications for connecting a client to the computer that is running Exchange Server that has the Client Access server role installed."
 
 
---

# Protocol (POX)

The **Protocol** element contains the specifications for connecting a client to the computer that is running Exchange Server that has the Client Access server role installed. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
```xml
<Protocol>
   <Type/>
   <Internal/>
   <External/>
   <TTL/>
   <Server/>
   <ServerDN/>
   <ServerVersion/>
   <MdbDN/>
   <PublicFolderServer/>
   <Port/>
   <DirectoryPort/>
   <ReferralPort/>
   <ASUrl/>
   <EwsUrl/>
   <EmwsUrl/>
   <SharingUrl/>
   <EcpUrl/>
   <EcpUrl-um/>
   <EcpUrl-aggr/>
   <EcpUrl-mt/>
   <EcpUrl-ret/>
   <EcpUrl-sms/>
   <EcpUrl-publish/>
   <EcpUrl-photo/>
   <EcpUrl-tm/>
   <EcpUrl-tmCreating/>
   <EcpUrl-tmHiding/>
   <EcpUrl-tmEditing/>
   <EcpUrl-extinstall/>
   <OOFUrl/>
   <OABUrl/>
   <UMUrl/>
   <EwsPartnerUrl/>
   <LoginName/>
   <DomainRequired/>
   <DomainName/>
   <SPA/>
   <AuthPackage/>
   <CertPrincipalName/>
   <SSL/>
   <AuthRequired/>
   <UsePOPAuth/>
   <SMTPLast/>
   <NetworkRequirements/>
   <AddressBook/>
   <MailStore/>
</Protocol>
```

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Type  <br/> |Indicates the type of protocol described by this **Protocol** element. The only valid value for this attribute is "mapiHttp". This attribute is only present if the Autodiscover request that corresponds to this response [included an X-MapiHttpCapability header](pox-autodiscover-request-for-exchange.md). This attribute is applicable to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, or on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).  <br/> |
|Version  <br/> |Indicates the version of the protocol described by this **Protocol** element. The only valid value for this attribute is "1". This attribute is only present if the Autodiscover request that corresponds to this response included an **X-MapiHttpCapability** header. This attribute is applicable to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, or on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Type (POX)](type-pox.md) <br/> |Identifies the type of the configured mail account.  <br/> |
|[Internal (POX)](internal-pox.md) <br/> |Contains a collection of URLs that a client can use to connect to Exchange from inside the organization's network.  <br/> |
|[External (POX)](external-pox.md) <br/> |Contains a collection of URLs that a client can use to connect to Exchange from outside of the organization's network.  <br/> |
|[TTL (POX)](ttl-pox.md) <br/> |Specifies the Time to Live, in hours, during which the settings remain valid.  <br/> |
|[Server (POX)](server-pox.md) <br/> |Specifies the name of the mail server.  <br/> |
|[ServerDN (POX)](serverdn-pox.md) <br/> |Specifies the Exchange Server distinguished name.  <br/> |
|[ServerVersion (POX)](serverversion-pox.md) <br/> |Represents the Exchange Server version number.  <br/> |
|[MdbDN (POX)](mdbdn-pox.md) <br/> |Represents the distinguished name of the mailbox database.  <br/> |
|[PublicFolderServer (POX)](publicfolderserver-pox.md) <br/> |Contains the fully-qualified domain name (FQDN) of the public folder server for the user.  <br/> |
|[Port (POX)](port-pox.md) <br/> |Specifies the port that is used to connect to the store.  <br/> |
|[DirectoryPort (POX)](directoryport-pox.md) <br/> |Specifies the port that is used to connect to the directory when the Name Service Provider Interface (NSPI) protocol is used.  <br/> |
|[ReferralPort (POX)](referralport-pox.md) <br/> |Specifies the port that is used to get a referral to a directory.  <br/> |
|[ASUrl (POX)](asurl-pox.md) <br/> |Specifies the URL of the best instance of the Exchange Web Services for a mail-enabled user.  <br/> |
|[EwsUrl (POX)](ewsurl-pox.md) <br/> |Specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.  <br/> |
|[EmwsUrl (POX)](emwsurl-pox.md) <br/> |Specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.  <br/> |
|[SharingUrl (POX)](sharingurl-pox.md) <br/> |Contains the URL of the sharing server used for cross-organization sharing of calendars and contacts.  <br/> |
|[EcpUrl (POX)](ecpurl-pox.md) <br/> |Specifies the URL of the Exchange Control Panel for a mail-enabled user.  <br/> |
|[EcpUrl-um (POX)](ecpurl-um-pox.md) <br/> |Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access voice mail settings for a mail-enabled user.  <br/> |
|[EcpUrl-aggr (POX)](ecpurl-aggr-pox.md) <br/> |Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email aggregation settings for a mail-enabled user.  <br/> |
|[EcpUrl-mt (POX)](ecpurl-mt-pox.md) <br/> |Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email message tracking settings for a mail-enabled user.  <br/> |
|[EcpUrl-ret (POX)](ecpurl-ret-pox.md) <br/> |Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access retention tag settings for a mail-enabled user.  <br/> |
|[EcpUrl-sms (POX)](ecpurl-sms-pox.md) <br/> |Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access Short Message Service (SMS) settings for a mail-enabled user.  <br/> |
|[EcpUrl-publish (POX)](ecpurl-publish-pox.md) <br/> |Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access calendar publishing settings for a mail-enabled user.  <br/> |
|[EcpUrl-photo (POX)](ecpurl-photo-pox.md) <br/> |Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change a mail-enabled user's current photo.  <br/> |
|[EcpUrl-tm (POX)](ecpurl-tm-pox.md) <br/> |Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access a list of all site mailboxes of which a mail-enabled user is currently a member.  <br/> |
|[EcpUrl-tmCreating (POX)](ecpurl-tmcreating-pox.md) <br/> |Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to create a new site mailbox.  <br/> |
|[EcpUrl-tmHiding (POX)](ecpurl-tmhiding-pox.md) <br/> |Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to unsubscribe the user from a site mailbox.  <br/> |
|[EcpUrl-tmEditing (POX)](ecpurl-tmediting-pox.md) <br/> |Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox.  <br/> |
|[EcpUrl-extinstall (POX)](ecpurl-extinstall-pox.md) <br/> |Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change the mail apps currently installed in the user's mailbox.  <br/> |
|[OOFUrl (POX)](oofurl-pox.md) <br/> |Specifies the URL of the best instance of the Availability service for a mail-enabled user.  <br/> |
|[OABUrl (POX)](oaburl-pox.md) <br/> |Specifies the Offline Address Book configuration server URL for an Exchange topology.  <br/> |
|[UMUrl (POX)](umurl-pox.md) <br/> |Specifies the URL of the best instance of the Unified Messaging Web service for a mail-enabled user.  <br/> |
|[EwsPartnerUrl (POX)](ewspartnerurl-pox.md) <br/> |Specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.  <br/> |
|[LoginName (POX)](loginname-pox.md) <br/> |Specifies the user's logon name.  <br/> |
|[DomainRequired (POX)](domainrequired-pox.md) <br/> |Indicates whether the domain is required for authentication.  <br/> |
|[DomainName (POX)](domainname-pox.md) <br/> |Specifies the user's domain.  <br/> |
|[SPA (POX)](spa-pox.md) <br/> |Indicates whether secure password authentication is required.  <br/> |
|[AuthPackage (POX)](authpackage-pox.md) <br/> |Specifies the authentication scheme that is used when authenticating against the Exchange 2007 computer that has the Mailbox server role installed.  <br/> |
|[CertPrincipalName (POX)](certprincipalname-pox.md) <br/> |Specifies the Secure Sockets Layer (SSL) certificate principal name that is required to connect to the Microsoft Exchange organization by using SSL.  <br/> |
|[SSL (POX)](ssl-pox.md) <br/> |Specifies whether secure logon is needed.  <br/> |
|[AuthRequired (POX)](authrequired-pox.md) <br/> |Specifies whether authentication is required.  <br/> |
|[UsePOPAuth (POX)](usepopauth-pox.md) <br/> |Indicates whether the authentication information that is provided for a POP3 type of account is also used for Simple Mail Transfer Protocol (SMTP).  <br/> |
|[SMTPLast (POX)](smtplast-pox.md) <br/> |Specifies whether the SMTP server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.  <br/> |
|[NetworkRequirements (POX)](networkrequirements-pox.md) <br/> |Contains the criteria that are used to determine whether the client computer is on a network that meets the Internet Service Provider's requirements to connect to the server.  <br/> |
|[AddressBook (POX)](addressbook-pox.md) <br/> |Contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol. This element is only present if the **Type** attribute on the **Protocol** element is present and set to "mapiHttp". The **AddressBook** element is applicable to clients that implement the MAPI/HTTP protocol and target Exchange Online and versions of Exchange starting with 15.00.0847.032.  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |Contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol. This element is only present if the **Type** attribute on the **Protocol** element is present and set to "mapiHttp". The **MailStore** element is applicable to clients that implement the MAPI/HTTP protocol and target Exchange Online and versions of Exchange starting with 15.00.0847.032.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Account (POX)](account-pox.md) <br/> |Specifies account settings for the user.  <br/> |
   
## Remarks

The **Protocol** element is present in a response that has an [Action (POX)](action-pox.md) value that is equal to **settings**.
  
## See also



[POX Autodiscover XML elements for Exchange](pox-autodiscover-xml-elements-for-exchange.md)

