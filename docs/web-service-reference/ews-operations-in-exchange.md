---
title: "EWS operations in Exchange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
api_name:
- Exchange
api_type:
- schema
ms.assetid: cf6fd871-9a65-4f34-8557-c8c71dd7ce09
description: "Find information about the EWS operations that are available in Exchange."
localization_priority: Priority
---

# EWS operations in Exchange

Find information about the EWS operations that are available in Exchange.
  
Exchange Web Services (EWS) provides many operations that enable you to access information from the Exchange store. The articles in this section provide information about the overall structure of the requests, responses, and error response messages for EWS operations, as well as XML examples for each operation. They provide an overview of the message structures that are sent between the client and the server. You can use this information to debug message structures and to find information about what you can do in an EWS request. For more information about what the XML structure represents, see - [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md).
  
All EWS functionality is associated with a version of the schema. New EWS schema versions are introduced in new releases of Exchange Server or Exchange Online. The [RequestServerVersion](requestserverversion.md) element contains a **Version** attribute that maps the server version to the schema version. This article provides information about when each operation was introduced. Specific functionality within an operation might require a later version of the service. The versioned schemas are implemented so that clients that are designed against an older version of EWS will work with a newer version of EWS. 
  
These operations can target the EWS endpoint that services your mailbox. You can browse to the EWS endpoint by using a URL that is similar in structure to http://\<***clientaccessserver***\>.com/ews/exchange.asmx, where \<***clientaccessserver***\> is the Exchange Client Access server that services your mailbox. You can use Autodiscover to get the URL to the Client Access server that services your mailbox. For more information about Autodiscover, see [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md).
  
## eDiscovery operations
<a name="bk_eDiscovery"> </a>

The eDiscovery operations provide search operations for legal holds and identify mailbox data that cannot be indexed and returned in discovery search results.
  
The following table lists the eDiscovery operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[GetDiscoverySearchConfiguration operation](getdiscoverysearchconfiguration-operation.md) <br/> |Exchange 2013  <br/> |
|[GetHoldOnMailboxes operation](getholdonmailboxes-operation.md) <br/> |Exchange 2013  <br/> |
|[GetNonIndexableItemDetails operation](getnonindexableitemdetails-operation.md) <br/> |Exchange 2013  <br/> |
|[GetNonIndexableItemStatistics operation](getnonindexableitemstatistics-operation.md) <br/> |Exchange 2013  <br/> |
|[GetSearchableMailboxes operation](getsearchablemailboxes-operation.md) <br/> |Exchange 2013  <br/> |
|[SearchMailboxes operation](searchmailboxes-operation.md) <br/> |Exchange 2013  <br/> |
|[SetHoldOnMailboxes operation](setholdonmailboxes-operation.md) <br/> |Exchange 2013  <br/> |
   
## Exchange mailbox data operations
<a name="bk_Exchange_mailbox_data"> </a>

The Exchange mailbox data operations enable clients to handle and organize items, folders, and attachments, as well as ambiguous name resolution and distribution list expansion. Exchange mailbox data operations include item, folder, attachment, and utilities operations.
  
The following table lists the Exchange mailbox data operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[ArchiveItem operation](archiveitem-operation.md) <br/> |Exchange 2013  <br/> |
|[CreateItem operation](createitem-operation.md) <br/> |Exchange 2007  <br/> |
|[CopyItem operation](copyitem-operation.md) <br/> |Exchange 2007  <br/> |
|[DeleteItem operation](deleteitem-operation.md) <br/> |Exchange 2007  <br/> |
|[FindItem operation](finditem-operation.md) <br/> |Exchange 2007  <br/> |
|[GetItem operation](getitem-operation.md) <br/> |Exchange 2007  <br/> |
|[MarkAllItemsAsRead operation](markallitemsasread-operation.md) <br/> |Exchange 2013  <br/> |
|[MoveItem operation](moveitem-operation.md) <br/> |Exchange 2007  <br/> |
|[SendItem operation](senditem-operation.md) <br/> |Exchange 2007  <br/> |
|[UpdateItem operation](updateitem-operation.md) <br/> |Exchange 2007  <br/> |
   
The following table lists the Exchange mailbox data folder operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[CreateFolder operation](createfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[CreateFolderPath operation](createfolderpath-operation.md) <br/> |Exchange 2013  <br/> |
|[CreateManagedFolder operation](createmanagedfolder-operation.md) <br/> |Exchange 2007. This functionality has been deemphasized in versions of Exchange starting with Exchange 2010. For more information about how to migrate to using retention tags and policies for messaging records management, see [Migrate from Managed Folders](https://technet.microsoft.com/library/dd298032%28v=exchg.141%29.aspx).  <br/> |
|[CopyFolder operation](copyfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[DeleteFolder operation](deletefolder-operation.md) <br/> |Exchange 2007  <br/> |
|[EmptyFolder operation](emptyfolder-operation.md) <br/> |Exchange 2010  <br/> |
|[FindFolder operation](findfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[GetFolder operation](getfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[MoveFolder operation](movefolder-operation.md) <br/> |Exchange 2007  <br/> |
|[UpdateFolder operation](updatefolder-operation.md) <br/> |Exchange 2007  <br/> |
   
The following table lists the Exchange mailbox data attachment operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[CreateAttachment operation](createattachment-operation.md) <br/> |Exchange 2007  <br/> |
|[GetAttachment operation](getattachment-operation.md) <br/> |Exchange 2007  <br/> |
|[DeleteAttachment operation](deleteattachment-operation.md) <br/> |Exchange 2007  <br/> |
   
The following table lists the Exchange mailbox reminder operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[GetReminders operation](getreminders-operation.md) <br/> |Exchange 2013  <br/> |
|[PerformReminderAction operation](performreminderaction-operation.md) <br/> |Exchange 2013  <br/> |
   
The following table lists the Exchange mailbox data conversation operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[ApplyConversationAction operation](applyconversationaction-operation.md) <br/> |Exchange 2010 Service Pack 1 (SP1)  <br/> |
|[FindConversation operation](findconversation-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[GetConversationItems operation](getconversationitems-operation.md) <br/> |Exchange 2013  <br/> |
   
The following table lists the Exchange mailbox data utilities operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[ConvertId operation](convertid-operation.md) <br/> |Exchange 2007 Service Pack 1  <br/> |
|[ExpandDL operation](expanddl-operation.md) <br/> |Exchange 2007  <br/> |
|[GetUserPhoto operation](getuserphoto-operation.md) <br/> |Exchange 2013. This operation has both a REST and a SOAP implementation.  <br/> |
|[MarkAsJunk operation](markasjunk-operation.md) <br/> |Exchange 2013  <br/> |
|[ResolveNames operation](resolvenames-operation.md) <br/> |Exchange 2007  <br/> |
|[GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## Availability operations
<a name="bk_Availability"> </a>

The availability operations improve the calendar and free/busy sharing experience by providing more secure, up-to-date, and rich free/busy information. Free/busy data is a critical component of scheduling meetings. The availability operations provide a reliable foundation for effective scheduling. 
  
The following table lists the availability operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[GetUserAvailability operation](getuseravailability-operation.md) <br/> |Exchange 2007  <br/> |
|[GetRoomLists operation](getroomlists-operation.md) <br/> |Exchange 2010  <br/> |
|[GetRooms operation](getrooms-operation.md) <br/> |Exchange 2010  <br/> |
|[GetUserOofSettings operation](getuseroofsettings-operation.md) <br/> |Exchange 2007  <br/> |
|[SetUserOofSettings operation](setuseroofsettings-operation.md) <br/> |Exchange 2007  <br/> |
   
## Bulk transfer operations
<a name="bk_bulk_transfer"> </a>

The bulk transfer operations enable clients to stream items into and out of a mailbox. 
  
The following table lists the bulk transfer operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[UploadItems operation](uploaditems-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[ExportItems operation](exportitems-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## Delegate management operations
<a name="bk_delegate_management"> </a>

The delegate management operations enable clients to add, get, update, and remove delegates from their mailboxes. 
  
The following table lists the delegate management operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[AddDelegate operation](adddelegate-operation.md) <br/> |Exchange 2007 Service Pack 1 (SP1)  <br/> |
|[GetDelegate operation](getdelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
|[UpdateDelegate operation](updatedelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
|[RemoveDelegate operation](removedelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
   
## Inbox rules operations
<a name="bk_inbox_rules"> </a>

The Inbox rules operations enable clients to get Inbox rules and update them for messages on the server. Inbox rules are sets of conditions and associated actions that enable clients to automatically organize, categorize, and act on messages as the messages are delivered to a folder. 
  
The following table lists the Inbox rules operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[GetInboxRules operation](getinboxrules-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[UpdateInboxRules operation](updateinboxrules-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## Mail app management operations
<a name="bk_mail_apps"> </a>

The mail app management operations enable you to manage mail apps for Outlook. You can use these operations to install, uninstall, disable, and get information about mail apps that are available for Outlook Web App and Outlook 2013.
  
The following table lists the mail app management operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[DisableApp operation](disableapp-operation.md) <br/> |Exchange 2013  <br/> |
|[GetAppManifests operation](getappmanifests-operation.md) <br/> |Exchange 2013  <br/> |
|[GetAppMarketplaceUrl operation](getappmarketplaceurl-operation.md) <br/> |Exchange 2013  <br/> |
|[GetClientAccessToken operation](getclientaccesstoken-operation.md) <br/> |Exchange 2013  <br/> |
|[InstallApp operation](installapp-operation.md) <br/> |Exchange 2013  <br/> |
|[UninstallApp operation](uninstallapp-operation.md) <br/> |Exchange 2013  <br/> |
   
## Mail tips operation
<a name="bk_mail_tips"> </a>

The mail tips operation enables clients to request information from the server about recipient mailboxes when an author is composing a message. The following table lists the mail tips operation.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[GetMailTips operation](getmailtips-operation.md) <br/> |Exchange 2010  <br/> |
   
## Message tracking operations
<a name="bk_message_tracking"> </a>

The message tracking operations enable clients to find messages that meet specified criteria and to get detailed tracking information about each message in a message tracking report. 
  
The following table lists the message tracking operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) <br/> |Exchange 2010  <br/> |
|[GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) <br/> |Exchange 2010  <br/> |
   
## Notification operations
<a name="bk_notification"> </a>

The notification operations notify the client application of events that are associated with items and folders a specified mailbox. The subscription model can be push-based, pull-based, or streaming-based. 
  
The following table lists the notification operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[GetEvents operation](getevents-operation.md) <br/> |Exchange 2007  <br/> |
|[GetStreamingEvents operation](getstreamingevents-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[Subscribe operation](subscribe-operation.md) <br/> |Exchange 2007  <br/> |
|[Unsubscribe operation](unsubscribe-operation.md) <br/> |Exchange 2007  <br/> |
   
## Persona operations
<a name="bk_personas"> </a>

The persona operations provide an interface to find and get information about a linked contact. The following table lists the persona operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[FindPeople operation](findpeople-operation.md) <br/> |Exchange 2013  <br/> |
|[GetPersona operation](getpersona-operation.md) <br/> |Exchange 2013  <br/> |
   
## Retention policy operation
<a name="bk_retention_policy"> </a>

The retention policy operation provides a list of all the retention tags that are linked to a user's retention policy. 
  
The following table lists the retention policy operation.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[GetUserRetentionPolicyTags operation](getuserretentionpolicytags-operation.md) <br/> |Exchange 2013  <br/> |
   
## Service configuration operation
<a name="bk_service_config"> </a>

The service configuration operation enables clients to get configuration information for the Unified Messaging, Protection Rules, Policy Tips, and Mail Tips services. 
  
The following table lists the service configuration operation.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[GetServiceConfiguration operation](getserviceconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
   
## Sharing operations
<a name="bk_sharing"> </a>

The sharing operations enable clients to share calendar data and contacts data. 
  
The following table lists the sharing operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[CreateItem (AcceptSharingInvitation)](createitem-acceptsharinginvitation.md) <br/> |Exchange 2010. Although the **CreateItem** operation is applicable to all versions of EWS, the **AcceptSharingInvitation** response object is only applicable to EWS in versions of Exchange starting with Exchange 2010.  <br/> |
|[GetSharingFolder operation](getsharingfolder-operation.md) <br/> |Exchange 2010  <br/> |
|[GetSharingMetadata operation](getsharingmetadata-operation.md) <br/> |Exchange 2010  <br/> |
|[RefreshSharingFolder operation](refreshsharingfolder-operation.md) <br/> |Exchange 2010  <br/> |
   
## Synchronization operations
<a name="bk_synchronization"> </a>

The synchronization operations provide a one-way synchronized cached copy of a user's folders and items. 
  
The following table lists the synchronization operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) <br/> |Exchange 2007  <br/> |
|[SyncFolderItems operation](syncfolderitems-operation.md) <br/> |Exchange 2007  <br/> |
   
## Time zone operation
<a name="bk_timezone"> </a>

The time zone operation enables clients to get a list of time zone definitions that are supported by the server. 
  
The following table lists the time zone operation.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[GetServerTimeZones operation](getservertimezones-operation.md) <br/> |Exchange 2010  <br/> |
   
## Unified Messaging operations
<a name="bk_um"> </a>

The Unified Messaging operations enable clients to read information about Unified Messaging properties and to play voice mail messages over the phone. 
  
The following table lists the Unified Messaging operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[DisconnectPhoneCall operation](disconnectphonecall-operation.md) <br/> |Exchange 2010  <br/> |
|[GetPhoneCallInformation operation](getphonecallinformation-operation.md) <br/> |Exchange 2010  <br/> |
|[PlayOnPhone operation (EWS)](playonphone-operation-ews.md) <br/> |Exchange 2010  <br/> |
   
Use the [GetServiceConfiguration operation](getserviceconfiguration-operation.md) to get the Unified Messaging configuration information for a mailbox. Use the Unified Messaging web service for Unified Messaging applications that target Exchange 2007. For more information, see [Unified Messaging web service reference for Exchange](unified-messaging-web-service-reference-for-exchange.md).
  
## Unified Contact Store operations
<a name="bk_ucs"> </a>

The Unified Contact Store provides a consistent contact experience across Office products and acts as an integration point for third-party applications to use the same contact store. It enables users and applications to store, manage, and access contact information and make it available globally among Lync, Exchange 2013, Outlook, Outlook Web App, and any other application that implements access to the Unified Contact Store. Exchange is the content store for the Unified Contact Store experience.
  
The following table lists the Unified Contact Store operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[AddNewImContactToGroup operation](addnewimcontacttogroup-operation.md) <br/> |Exchange 2013  <br/> |
|[AddImContactToGroup operation](addimcontacttogroup-operation.md) <br/> |Exchange 2013  <br/> |
|[AddImGroup operation](addimgroup-operation.md) <br/> |Exchange 2013  <br/> |
|[AddNewTelUriContactToGroup operation](addnewteluricontacttogroup-operation.md) <br/> |Exchange 2013  <br/> |
|[AddDistributionGroupToImList operation](adddistributiongrouptoimlist-operation.md) <br/> |Exchange 2013  <br/> |
|[GetImItemList operation](getimitemlist-operation.md) <br/> |Exchange 2013  <br/> |
|[GetImItems operation](getimitems-operation.md) <br/> |Exchange 2013  <br/> |
|[RemoveContactFromImList operation](removecontactfromimlist-operation.md) <br/> |Exchange 2013  <br/> |
|[RemoveImContactFromGroup operation](removeimcontactfromgroup-operation.md) <br/> |Exchange 2013  <br/> |
|[RemoveDistributionGroupFromImList operation](removedistributiongroupfromimlist-operation.md) <br/> |Exchange 2013  <br/> |
|[RemoveImGroup operation](removeimgroup-operation.md) <br/> |Exchange 2013  <br/> |
|[SetImGroup operation](setimgroup-operation.md) <br/> |Exchange 2013  <br/> |
   
## User configuration operations
<a name="bk_user_config"> </a>

The user configuration operations enable clients to create, delete, get, and update user configuration information. 
  
The following table lists the user configuration operations.
  
|**Operation name**|**Introduced in**|
|:-----|:-----|
|[CreateUserConfiguration operation](createuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[DeleteUserConfiguration operation](deleteuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[GetUserConfiguration operation](getuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[UpdateUserConfiguration operation](updateuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
   
## See also

- [Explore the EWS Managed API, EWS, and web services in Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md)
    

