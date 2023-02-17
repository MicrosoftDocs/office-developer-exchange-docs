---
title: "Setting (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 43db26e1-f7be-49fd-b26b-fc1b10bd3458
description: "The Setting element represents a configuration setting to be returned."
 
 
---

# Setting (SOAP)

The **Setting** element represents a configuration setting to be returned.
  
```XML
<Setting/>
```

 **string**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Contains the names of the requested configuration settings.  <br/> |

## Text value

The text value for this element is the configuration setting. The following table lists the possible configuration settings.
  
|**Configuration setting**|**Description**|
|:-----|:-----|
|UserDisplayName  <br/> |The display name of the user.  <br/> |
|UserDN  <br/> |The legacy distinguished name of the user.  <br/> |
|UserDeploymentId  <br/> |The deployment identifier of the user.  <br/> |
|InternalMailboxServer  <br/> |The fully qualified domain name (FQDN) of the mailbox server.  <br/> |
|InternalRpcClientServer  <br/> |The fully qualified domain name of the RPC client server.  <br/> |
|InternalMailboxServerDN  <br/> |The legacy distinguished name of the mailbox server.  <br/> |
|InternalEcpUrl  <br/> |The internal URL of the Exchange Control Panel.  <br/> |
|InternalEcpVoicemailUrl  <br/> |The internal URL of the Exchange Control Panel for VoiceMail Customization.  <br/> |
|InternalEcpEmailSubscriptionsUrl  <br/> |The internal URL of the Exchange Control Panel for Email Subscriptions.  <br/> |
|InternalEcpTextMessagingUrl  <br/> |The internal URL of the Exchange Control Panel for Text Messaging.  <br/> |
|InternalEcpDeliveryReportUrl  <br/> |The internal URL of the Exchange Control Panel for Delivery Reports.  <br/> |
|InternalEcpRetentionPolicyTagsUrl  <br/> |The internal URL of the Exchange Control Panel for RetentionPolicy Tags.  <br/> |
|InternalEcpPublishingUrl  <br/> |The internal URL of the Exchange Control Panel for Publishing.  <br/> |
|InternalEwsUrl  <br/> |The internal URL of Exchange Web Services.  <br/> |
|InternalOABUrl  <br/> |The internal URL of the offline address book (OAB).  <br/> |
|InternalUMUrl  <br/> |The internal URL of the Unified Messaging services.  <br/> |
|InternalWebClientUrls  <br/> |The internal URLs of the Exchange Web client.  <br/> |
|MailboxDN  <br/> |The distinguished name of the mailbox database of the user's mailbox.  <br/> |
|PublicFolderServer  <br/> |The name of the public folders server.  <br/> |
|ActiveDirectoryServer  <br/> |The name of the Active Directory server.  <br/> |
|ExternalMailboxServer  <br/> |The name of the RPC over HTTP server.  <br/> |
|ExternalMailboxServerRequiresSSL  <br/> |The indicator for whether the RPC over HTTP server requires SSL.  <br/> |
|ExternalMailboxServerAuthenticationMethods  <br/> |The authentication methods that are supported by the RPC over HTTP server.  <br/> |
|EcpVoicemailUrlFragment, <br/> |The URL fragment of the Exchange Control Panel for VoiceMail Customization.  <br/> |
|EcpEmailSubscriptionsUrlFragment  <br/> |The URL fragment of the Exchange Control Panel for Email Subscriptions.  <br/> |
|EcpTextMessagingUrlFragment  <br/> |The URL fragment of the Exchange Control Panel for Text Messaging.  <br/> |
|EcpDeliveryReportUrlFragment  <br/> |The URL fragment of the Exchange Control Panel for Delivery Reports.  <br/> |
|EcpRetentionPolicyTagsUrlFragment  <br/> |The URL fragment of the Exchange Control Panel for RetentionPolicy Tags.  <br/> |
|EcpPublishingUrlFragment  <br/> |The URL fragment of the Exchange Control Panel for Publishing.  <br/> |
|ExternalEcpUrl  <br/> |The external URL of the Exchange Control Panel.  <br/> |
|ExternalEcpVoicemailUrl  <br/> |The external URL of the Exchange Control Panel for VoiceMail Customization.  <br/> |
|ExternalEcpEmailSubscriptionsUrl  <br/> |The external URL of the Exchange Control Panel for Email Subscriptions.  <br/> |
|ExternalEcpTextMessagingUrl  <br/> |The external URL of the Exchange Control Panel for Text Messaging.  <br/> |
|ExternalEcpDeliveryReportUrl  <br/> |The external URL of the Exchange Control Panel for Delivery Reports.  <br/> |
|ExternalEcpRetentionPolicyTagsUrl  <br/> |The external URL of the Exchange Control Panel for RetentionPolicy Tags.  <br/> |
|ExternalEcpPublishingUrl  <br/> |The external URL of the Exchange Control Panel for Publishing.  <br/> |
|ExternalEwsUrl  <br/> |The external URL of the Exchange Web Services.  <br/> |
|ExternalOABUrl  <br/> |The external URL of the OAB.  <br/> |
|ExternalUMUrl  <br/> |The external URL of the Unified Messaging services.  <br/> |
|ExternalWebClientUrls  <br/> |The external URLs of the Exchange Web client.  <br/> |
|CrossOrganizationSharingEnabled  <br/> |Indicates that cross-organization sharing is enabled.  <br/> |
|AlternateMailboxes  <br/> |Collection of alternate mailboxes.  <br/> |
|CasVersion  <br/> |The version of the Client Access server that is serving the request (for example, 14.XX.YYYY.ZZZ)  <br/> |
|EwsSupportedSchemas  <br/> |A comma-separated list of schema versions supported by Exchange Web Services. The schema version values will be the same as the values of the **ExchangeServerVersion** enumeration.  <br/> |
|InternalPop3Connections  <br/> |The internal connection settings list for POP3 protocol connections.  <br/> |
|ExternalPop3Connections  <br/> |The external connection settings list for POP3 protocol connections.  <br/> |
|InternalImap4Connections  <br/> |The internal connection settings list for IMAP4 protocol connections.  <br/> |
|ExternalImap4Connections  <br/> |The external connection settings list for IMAP4 protocol connections.  <br/> |
|InternalSmtpConnections  <br/> |The internal connection settings list for SMTP connections.  <br/> |
|ExternalSmtpConnections  <br/> |The external connection settings list for SMTP connections.  <br/> |
|InternalServerExclusiveConnect  <br/> |The internal server exclusive connect flag. If set to "Off" then clients SHOULD not connect via this protocol.  <br/> |
|ExternalServerExclusiveConnect  <br/> |The external server exclusive connect flag. If set to "On" then clients SHOULD connect via this protocol.  <br/> |
|ExchangeRpcUrl  <br/> |The URL that used for Remote Procedure Calls. This URL is internal to the server and is not to be used by clients.  <br/> |
|ShowGalAsDefaultView  <br/> |Specifies a Boolean value that indicates whether the GAL should be shown as the address book. A text value of "true" indicates that the GAL is to be shown by default. A text value of "false" indicates that the contact list is to be shown.  <br/> |
|AutoDiscoverSMTPAddress  <br/> |The AutoDiscover Primary SMTP Address for the user. This is the proxy address in lieu of the e-mail address of the user, if a proxy address exists.  <br/> |
|InteropExternalEwsUrl  <br/> |The external URL of the server's Web service endpoint. This is the URL to a server that can serve mailboxes hosted on a server that does not have the Web services.  <br/> |
|ExternalEwsVersion  <br/> |The version of the Web services server that is delivering the specified request.  <br/> |
|InteropExternalEwsVersion  <br/> |The version of the server InteropExternalEwsUrl is pointing to.  <br/> |
|MobileMailboxPolicyInterop  <br/> |The mobile mailbox policy settings.  <br/> |
|GroupingInformation  <br/> |A value used in conjunction with the ExternalEwsUrl setting to group multiple mailboxes together to [maintain affinity](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) when subscribing to notifications.  <br/> |
|UserMSOnline  <br/> |A Boolean value that indicates whether the user's mailbox is hosted in Exchange Online or Exchange Online as part of Office 365.  <br/> |
|MapiHttpEnabled  <br/> |A Boolean value that indicates whether the user's mailbox is accessible via the MAPI/HTTP protocol.  <br/> |

## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |<https://schemas.microsoft.com/exchange/2010/Autodiscover>  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |

## See also

[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)
