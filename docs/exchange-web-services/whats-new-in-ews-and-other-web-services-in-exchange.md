---
title: "What's new in EWS and other web services in Exchange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: aff6328f-cff1-42a6-9a4d-ea4d2d0461cf
description: "Find out what's new in EWS and web services in Exchange and the EWS Managed API."
localization_priority: Priority
---

# What's new in EWS and other web services in Exchange

Find out what's new in EWS and web services in Exchange and the EWS Managed API.
  
Web services in Exchange have been updated to include new features. 
  
**Table 1. New web service features in Exchange Online, Exchange 2013, and the EWS Managed API**

|Feature|Implemented in Exchange Online|Implemented in Exchange 2013|Implemented in the EWS Managed API|
|:-----|:-----:|:-----:|:-----:|
|[eDiscovery](#eDisc) <br/> |Yes  <br/> |Yes  <br/> |Yes  <br/> |
|[Archiving](#arch) <br/> |Yes  <br/> |Yes  <br/> |Yes  <br/> |
|[Personas](#personas) <br/> |Yes  <br/> |Yes  <br/> |No  <br/> |
|[Unified Contact Store](#unified) <br/> |Yes  <br/> |Yes  <br/> |No  <br/> |
|[Retention policies](#retentionpolicy) <br/> |Yes  <br/> |Yes  <br/> |Yes  <br/> |
|[User photos](#userphoto) <br/> |Yes  <br/> |Yes  <br/> |No  <br/> |
|[Mail apps for Outlook management](#ewsmailapps) <br/> |Yes  <br/> |Yes  <br/> |Yes  <br/> |
|[Propose new meeting time](#propose) <br/> |Yes  <br/> |No  <br/> |No  <br/> |

<a name="eDisc"> </a>

## eDiscovery in EWS

eDiscovery is a federated query web service that enables external applications, such as SharePoint 2013, to perform queries of Exchange data. Discovery consists of several phases, including identifying and preserving key data, culling down and reviewing the data, and producing data in court. eDiscovery queries facilitate the discovery process by providing a single discovery workflow across Exchange and SharePoint.
  
**Table 2. EWS operations and EWS Managed API methods for working with eDiscovery**

|**Operation name**|**EWS Managed API method**|**Description**|
|:-----|:-----|:-----|
|[GetDiscoverySearchConfiguration operation](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |[ExchangeService.GetDiscoverySearchConfiguration()](https://msdn.microsoft.com/library/jj670206%28v=exchg.80%29.aspx) <br/> |Gets configuration information for in-place holds, saved discovery searches, and the mailboxes that are enabled for discovery search.  <br/> |
|[GetHoldOnMailboxes operation](https://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |[ExchangeService.GetHoldOnMailboxes()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getholdonmailboxes%28v=exchg.80%29.aspx) <br/> |Gets the status of a query-based hold, which is set by using the **SetHoldOnMailboxes** operation.  <br/> |
|[GetNonIndexableItemDetails operation](https://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |[ExchangeService.GetNonIndexableItemDetails()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemdetails%28v=exchg.80%29.aspx) <br/> |Gets details about items that cannot be indexed. This includes, but is not limited to, the item identifier, an error code, an error description, when an attempt was made to index the item, and additional information about the item.  <br/> |
|[GetNonIndexableItemStatistics operation](https://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |[ExchangeService.GetNonIndexableItemStatistics()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemstatistics%28v=exchg.80%29.aspx) <br/> |Gets the count of items that cannot be indexed in a mailbox.  <br/> |
|[GetSearchableMailboxes operation](https://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |[ExchangeService.GetSearchableMailboxes()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getsearchablemailboxes%28v=exchg.80%29.aspx) <br/> |Gets a list of mailboxes that the client has permission to search or perform eDiscovery on.  <br/> |
|[SearchMailboxes operation](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[ExchangeService.SearchMailboxes()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> |Searches for items in specific mailboxes that match query keywords.  <br/> |
|[SetHoldOnMailboxes operation](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |[ExchangeService.SetHoldOnMailboxes()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) <br/> |Sets a query-based hold on items.  <br/> |

<a name="arch"> </a>

## Archiving in EWS

Archive mailboxes are secondary mailboxes that are associated with a user. Archive mailboxes are typically used to manage email storage limits. For example, older email items might periodically be moved from the Inbox to the archive mailbox. 
  
Exchange introduces two new EWS operations that you can use to archive a set of mail items from a primary mailbox. Archiving Inbox items in this way preserves the folder hierarchy of the items. In addition, archive mailboxes can now be stored either locally on a client, or remotely, in a way that is mostly opaque to a user, by using a folder path to point to the contents of the archive.
  
**Table 3. EWS operations and EWS Managed API methods for working with archiving**

|**Operation name**|**EWS Managed API method**|**Description**|
|:-----|:-----|:-----|
|[ArchiveItem operation](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |[ExchangeService.ArchiveItems()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.archiveitems%28v=exchg.80%29.aspx) <br/> |Moves an item from the primary mailbox to the archive mailbox.  <br/> |
|[CreateFolderPath operation](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |Not implemented.  <br/> |Creates a folder hierarchy in a primary or archive mailbox.  <br/> |

<a name="personas"> </a>

## Personas in EWS

A *persona* is a collection of data that is associated with an individual. The data can come from one or more sources and is associated with the persona by means of a common link ID. Personas in EWS enable you to link, search, browse, and retrieve information about a person from multiple sources and organize that information into a single logical entity. Personas differ from contacts in that a contact is a collection of data from a single source that is associated with an individual; for example, a personal Outlook contact or an entry in a global address list (GAL). 
  
The EWS Managed API does not implement this functionality.
  
> [!NOTE]
> The Unified Contact Store also exposes persona functionality by means of the operations that support that feature. 
  
**Table 4. EWS operations for working with personas**

|**Operation name**|**Description**|
|:-----|:-----|
|[FindPeople operation](https://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |Returns all persona objects from a specified contact folder or retrieves all contacts that match a specified query string.  <br/> |
|[GetPersona operation](https://msdn.microsoft.com/library/e2146df0-53d0-4caf-9758-b600bbc14b6a%28Office.15%29.aspx) <br/> |Retrieves a persona.  <br/> |

<a name="unified"> </a>

## Unified Contact Store in EWS

The Unified Contact Store is a feature that provides a consistent contact experience across Office products and acts as an integration point for third-party applications to use the same contact store. It allows users and applications to store, manage, and access contact information and make it available globally among Lync, Exchange 2013, Outlook, Outlook Web App and any other application that implements access to the Unified Contact Store. Exchange is the contact store for the Unified Contact Store experience. 
  
The EWS Managed API does not implement this functionality.
  
**Table 5. EWS operations for working with the Unified Contact Store**

|**Operation name**|**Description**|
|:-----|:-----|
|[AddNewImContactToGroup operation](https://msdn.microsoft.com/library/0cb5525f-faa3-48f1-9551-df55ffc26f46%28Office.15%29.aspx) <br/> |Adds a new IM contact to a group. The Unified Contact Store can contain a maximum of 1000 contacts.  <br/> |
|[AddImContactToGroup operation](https://msdn.microsoft.com/library/376acc42-2684-4596-aca1-82a4a10865c9%28Office.15%29.aspx) <br/> |Adds an existing IM contact to a group. The Unified Contact Store can contain a maximum of 1000 contacts.  <br/> |
|[AddImGroup operation](https://msdn.microsoft.com/library/6df6e504-b7c8-4773-b10f-ffa5defac229%28Office.15%29.aspx) <br/> |Adds a new IM group. The Unified Contact Store can contain a maximum of 64 groups.  <br/> |
|[AddNewTelUriContactToGroup operation](https://msdn.microsoft.com/library/c9688ce8-2465-45bb-8bd2-94b32ed4885c%28Office.15%29.aspx) <br/> |Adds a new contact to a group based on a contact's phone number.  <br/> |
|[AddDistributionGroupToImList operation](https://msdn.microsoft.com/library/5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a%28Office.15%29.aspx) <br/> |Adds a new distribution list group. The Unified Contact Store can contain a maximum of 64 groups.  <br/> |
|[GetImItemList operation](https://msdn.microsoft.com/library/e31d14e1-0c1f-4b69-98b7-157d59c13698%28Office.15%29.aspx) <br/> |Retrieves a list of IM groups and IM contact personas.  <br/> |
|[GetImItems operation](https://msdn.microsoft.com/library/51186691-46d2-4d5c-b8bc-4ee2bb20fbe7%28Office.15%29.aspx) <br/> |Retrieves information about the specified IM groups and IM contact personas.  <br/> |
|[RemoveContactFromImList operation](https://msdn.microsoft.com/library/28ec96c3-45af-48ff-9f17-718a527dc0ad%28Office.15%29.aspx) <br/> |Removes the specified contact from all IM groups.  <br/> |
|[RemoveImContactFromGroup operation](https://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx) <br/> |Removes an IM contact from a group.  <br/> |
|[RemoveDistributionGroupFromImList operation](https://msdn.microsoft.com/library/252bddf2-98b6-4824-b548-2fba2bda5384%28Office.15%29.aspx) <br/> |Removes the specified IM distribution list group.  <br/> |
|[RemoveImGroup operation](https://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx) <br/> |Removes the specified IM group.  <br/> |
|[SetImGroup operation](https://msdn.microsoft.com/library/2d48aa07-8152-4c3d-a519-061253e80174%28Office.15%29.aspx) <br/> |Changes the display name of a group.  <br/> |

<a name="retentionpolicy"> </a>
  
## Retention policies in EWS

Retention policies are policies that are used in Exchange to group one or more retention tags, to apply retention settings to folders or individual items such as email and voice mail messages, and to apply retention settings to a mailbox.
  
Exchange includes three types of retention tags:
  
- Default policy tags that apply to mailbox items that have no other type of retention tag applied.
    
- System folder policy tags that are applied to default folders such as the Inbox.
    
- Personal tags that a user can apply to folders they create or to individual items.
    
Only one retention policy can be assigned to a mailbox, but the policy can have one or more retention tags of various types linked to it. Retention tags can be linked to or unlinked from a retention policy at any time. EWS in Exchange exposes a new operation, [GetUserRetentionPolicyTags](https://msdn.microsoft.com/library/57c6ff23-5c2c-42ee-824b-5a1b6dafab8c%28Office.15%29.aspx), and the EWS Managed API implements a new method, [ExchangeService.GetUserRetentionPolicyTags()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getuserretentionpolicytags%28v=exchg.80%29.aspx), that provides a list of all the tags that are linked to a retention policy. You can set and retrieve retention policy tags for items and folders by using the **CreateItem**, **CreateFolder**, **UpdateItem**, **UpdateFolder**, **GetItem**, and **GetFolder** operations. 

<a name="userphoto"> </a>

## Requesting user photos

You can request user photos from the Exchange server by using one of the two implementations of the [GetUserPhoto operation](https://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx): [REST](how-to-get-user-photos-by-using-ews-in-exchange.md) or SOAP. The REST endpoint uses a standard HTTPS **GET** request to get the user photo. The service will either return a user photo stored in Exchange or a photo from Active Directory Domain Services (AD DS). 
  
The EWS Managed API does not implement this functionality. You can, however, use the EWS Managed API to return user photos that are stored in a mailbox by getting the photo that is attached to a contact.

<a name="blocksender"> </a>

## Block senders and mark email as junk in EWS

You can now block senders and mark email as junk by using the new [MarkAsJunk operation](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) in EWS or the [ExchangeService.MarkAsJunk()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) method in the EWS Managed API. 

<a name="ewsmailapps"> </a>

## Mail apps for Outlook

EWS now includes support for managing mail apps for Outlook. 
  
**Table 6. EWS operations and EWS Managed API methods for working with mail apps for Outlook**

|**Operation name**|**EWS Managed API method**|**Description**|
|:-----|:-----|:-----|
|[DisableApp operation](https://msdn.microsoft.com/library/211731a3-2470-49af-bda3-1ddfc15a8e46%28Office.15%29.aspx) <br/> |[ExchangeService.DisableApp()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.disableapp%28v=exchg.80%29.aspx) <br/> |Disables an installed app.  <br/> |
|[GetAppManifests operation](https://msdn.microsoft.com/library/21a4987c-c24d-4a6e-ace4-e81edcda6303%28Office.15%29.aspx) <br/> |[ExchangeService.GetAppManifests()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getappmanifests%28v=exchg.80%29.aspx) <br/> |Gets the app manifests for a mailbox.  <br/> |
|[GetAppMarketplaceUrl operation](https://msdn.microsoft.com/library/2c016fc3-0e13-4624-9a5b-d3e84577a860%28Office.15%29.aspx) <br/> |[ExchangeService.GetAppMarketplaceUrl()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getappmarketplaceurl%28v=exchg.80%29.aspx) <br/> |Gets the app marketplace URL.  <br/> |
|[GetClientAccessToken operation](https://msdn.microsoft.com/library/086876cc-e22c-4e89-89f9-19e78af51217%28Office.15%29.aspx) <br/> |[ExchangeService.GetClientAccessToken()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getclientaccesstoken%28v=exchg.80%29.aspx) <br/> |Gets client access tokens.  <br/> |
|[InstallApp operation](https://msdn.microsoft.com/library/596eae95-3e78-489a-8bb2-d2dd4a026405%28Office.15%29.aspx) <br/> |[ExchangeService.InstallApp()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.installapp%28v=exchg.80%29.aspx) <br/> |Installs an app for a mailbox.  <br/> |
|[UninstallApp operation](https://msdn.microsoft.com/library/7707aa6a-381d-43f7-a454-54f6343ed127%28Office.15%29.aspx) <br/> |[ExchangeService.UninstallApp](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.uninstallapp%28v=exchg.80%29.aspx) <br/> |Uninstalls an app from a mailbox.  <br/> |

<a name="propose"> </a>

## Propose new meeting time

The propose new time feature was introduced in version 15.00.0800.007 of Exchange. This allows meeting attendees to [propose new meeting times](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md) to the meeting organizer. 
  
The EWS Managed API does not implement this functionality.
  
## See also

- [Explore the EWS Managed API, EWS, and web services in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [EWS client design overview for Exchange](ews-client-design-overview-for-exchange.md)
- [Mail apps for Outlook and EWS in Exchange](mail-apps-for-outlook-and-ews-in-exchange.md)
- [Archiving in EWS in Exchange](archiving-in-ews-in-exchange.md)
- [eDiscovery in EWS in Exchange](ediscovery-in-ews-in-exchange.md)
- [People and contacts in EWS in Exchange](people-and-contacts-in-ews-in-exchange.md)
    

