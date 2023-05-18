---
title: "MessageText"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MessageText
api_type:
- schema
ms.assetid: 59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1
description: "The MessageText element provides a text description of the status of the response."
---

# MessageText

The **MessageText** element provides a text description of the status of the response. 
  
```XML
<MessageText/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> | Provides descriptive information about the response status.  <br/> <br/> The following are some of the possible XPath expressions to this element: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/> <br/> `/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>  `/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>  `/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |Contains the status and result of a single DeleteItem request.  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |Contains the status and result of a single SendItem request.  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |Contains the status and result of a single DeleteFolder request.  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Contains the status and result of a single DeleteAttachment request.  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |Contains the status and result of a single Unsubscribe request.  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Contains the status and result of a single CreateFolder request.  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Contains the status and result of a single GetFolder request.  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Contains the status and result of a single UpdateFolder request.  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Contains the status and result of a single MoveFolder request.  <br/> |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Contains the status and result of a single CopyFolder request.  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Contains the status and result of a single CreateManagedFolder request.  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Contains the status and result of a single FindFolder request.  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Contains the status and result of a single CreateItem request.  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Contains the status and result of a single GetItem request.  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Contains the status and result of a single UpdateItem request.  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Contains the status and result of a single MoveItem request.  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Contains the status and result of a single CopyItem request.  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |Contains the status and result of a single CreateAttachment request.  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |Contains the status and result of a single GetAttachment request.  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Contains the status and result of a single FindItem request.  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Contains the status and result of a ResolveNames request.  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Contains the status and result of a single ExpandDL request.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contains the status and result of a single Subscribe request.  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Contains the status and result of a single GetEvents request.  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Contains the status and result of a single SendNotification request.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contains the status and result of a SyncFolderHierarchy request.  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Contains the status and result of a SyncFolderItems request.  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Contains the status and result of a ConvertId request.  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Contains the status and result of an AddDelegate request.  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |Contains the status and result of a GetServerTimeZones request.  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Contains the status and result of a GetSharingFolder request.  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |Defines a response to a GetSharingFolder request.  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Contains the status and result of a GetSharingMetadata request.  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Defines a response to a GetSharingMetadata request.  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |Contains the status and result of a RefreshSharingFolder request.  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |Defines a response to a RefreshSharingFolder request.  <br/> |
|[InvalidRecipient](invalidrecipient.md) <br/> |Represents an invalid recipient for a GetSharingMetadata request.  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |Contains the status and results of a **FindConversation** response.  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |Contains the status and result of a single **EmptyFolder** request.  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Contains a response to an **UpdateInboxRules** request.  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Contains a response to a **GetInboxRules** request.  <br/> |
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md) <br/> |Contains a response to a **GetServiceConfiguration** request.  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contains service configuration settings.  <br/> |
   
## Remarks

This element is not required and is not included in all responses. This element is included when error messages are returned. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)