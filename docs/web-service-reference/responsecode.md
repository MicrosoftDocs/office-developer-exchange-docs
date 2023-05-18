---
title: "ResponseCode"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 4b84d670-74c9-4d6d-84e7-f0a9f76f0d93
description: "The ResponseCode element provides status information about the request."
---

# ResponseCode

The **ResponseCode** element provides status information about the request.
  
- [ResponseMessage](responsemessage.md)
- [ResponseCode](responsecode.md)
  
```XML
<ResponseCode/>
```

**ResponseCodeType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|Element|Description|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) Provides descriptive information about the response status. The following are the possible XPath expressions to this element: <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/> `/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/> `/SetUserOofSettingsResponse/ResponseMessage` <br/> `/GetUserOofSettingsResponse/ResponseMessage`
|[DeleteItemResponseMessage](deleteitemresponsemessage.md)Contains the status and result of a single [DeleteItem operation](deleteitem-operation.md) request. |
|[SendItemResponseMessage](senditemresponsemessage.md)Contains the status and result of a single [SendItem operation](senditem-operation.md) request. |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md)Contains the status and result of a single [DeleteFolder operation](deletefolder-operation.md) request. |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md)Contains the status and result of a single [DeleteAttachment operation](deleteattachment-operation.md) request. |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md)Contains the status and result of a single [Unsubscribe operation](unsubscribe-operation.md) request. |
|[CreateFolderResponseMessage](createfolderresponsemessage.md)Contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request. |
|[GetFolderResponseMessage](getfolderresponsemessage.md)Contains the status and result of a single [GetFolder operation](getfolder-operation.md) request. |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md)Contains the status and result of a single [UpdateFolder operation](updatefolder-operation.md) request. |
|[MoveFolderResponseMessage](movefolderresponsemessage.md)Contains the status and result of a single [MoveFolder operation](movefolder-operation.md) request. |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md)Contains the status and result of a single [CopyFolder operation](copyfolder-operation.md)request. |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)Contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request. |
|[FindFolderResponseMessage](findfolderresponsemessage.md)Contains the status and result of a single [FindFolder operation](findfolder-operation.md) request. |
|[CreateItemResponseMessage](createitemresponsemessage.md)Contains the status and result of a single [CreateItem operation](createitem-operation.md) request. |
|[GetItemResponseMessage](getitemresponsemessage.md)Contains the status and result of a single [GetItem operation](getitem-operation.md) request. |
|[UpdateItemResponseMessage](updateitemresponsemessage.md)Contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request. |
|[MoveItemResponseMessage](moveitemresponsemessage.md)Contains the status and result of a single [MoveItem operation](moveitem-operation.md) request. |
|[CopyItemResponseMessage](copyitemresponsemessage.md)Contains the status and result of a single [CopyItem operation](copyitem-operation.md) request. |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md)Contains the status and result of a single [CreateAttachment operation](createattachment-operation.md) request. |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md)Contains the status and result of a single [GetAttachment operation](getattachment-operation.md) request. |
|[FindItemResponseMessage](finditemresponsemessage.md)Contains the status and result of a single [FindItem operation](finditem-operation.md) request. |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md)Contains the status and result of a [ResolveNames operation](resolvenames-operation.md) request. |
|[ExpandDLResponseMessage](expanddlresponsemessage.md)Contains the status and result of a single [ExpandDL operation](expanddl-operation.md) request. |
|[SubscribeResponseMessage](subscriberesponsemessage.md)Contains the status and result of a single [Subscribe operation](subscribe-operation.md) request. |
|[GetEventsResponseMessage](geteventsresponsemessage.md)Contains the status and result of a single [GetEvents operation](getevents-operation.md) request. |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md)Contains the status and result of a single SendNotification operation request. |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)Contains the status and result of a [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) request. |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)Contains the status and result of a [SyncFolderItems operation](syncfolderitems-operation.md) request. |
|[ConvertIdResponseMessage](convertidresponsemessage.md)Contains the status and result of a [ConvertId operation](convertid-operation.md) request. |
|[AddDelegateResponse](adddelegateresponse.md)Contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request. |
|[GetDelegateResponse](getdelegateresponse.md)Contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request. |
|[RemoveDelegateResponse](removedelegateresponse.md)Contains the status and result of a [RemoveDelegate operation](removedelegate-operation.md) request. |
|[UpdateDelegateResponse](updatedelegateresponse.md)Contains the status and result of an [UpdateDelegate operation](updatedelegate-operation.md) request. |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md)Contains the status and result of a [GetServerTimeZones operation](getservertimezones-operation.md) request. |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md)Contains the status and result of a [GetSharingFolder operation](getsharingfolder-operation.md) request. |
|[GetSharingFolderResponse](getsharingfolderresponse.md)Defines a response to a [GetSharingFolder operation](getsharingfolder-operation.md) request. |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md)Contains the status and result of a [GetSharingMetadata operation](getsharingmetadata-operation.md) request. |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md)Defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request. |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md)Contains the status and result of a [RefreshSharingFolder operation](refreshsharingfolder-operation.md) request. |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md)Defines a response to a [RefreshSharingFolder operation](refreshsharingfolder-operation.md) request. |
|[FindConversationResponse](findconversationresponse.md)Contains the status and results of a [FindConversation operation](findconversation-operation.md) response. |
|[ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md)Contains the status and results of an [ApplyConversationAction operation](applyconversationaction-operation.md) request. |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md)Contains the status and result of a single [EmptyFolder operation](emptyfolder-operation.md) request. |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md)Contains a status and result of an [UpdateInboxRules operation](updateinboxrules-operation.md) request. |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md)Contains a status and result of an [UploadItems operation](uploaditems-operation.md) request. |
|[GetInboxRulesResponse](getinboxrulesresponse.md)Contains a response to a [GetInboxRules operation](getinboxrules-operation.md) **** request. |
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md)Contains a response to a [GetServiceConfiguration operation](getserviceconfiguration-operation.md) request. |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md)Contains service configuration settings. |

## Text value

A text value is required if this element is used. The following table describes the values that are returned with this element.
  
|Value|Description|
|:-----|:-----|
|NoError |No error occurred for the request. |
|ErrorAccessDenied |This error occurs when the calling account does not have the rights to perform the requested action. |
|ErrorAccessModeSpecified |This error is for internal use only. This error is not returned. |
|ErrorAccountDisabled |This error occurs when the account in question has been disabled. |
|ErrorAddDelegatesFailed |This error occurs when a list with added delegates cannot be saved. |
|ErrorAddressSpaceNotFound |This error occurs when the address space record, or Domain Name System (DNS) domain name, for cross-forest availability could not be found in the Active Directory database. |
|ErrorADOperation |This error occurs when the operation failed because of communication problems with Active Directory Domain Services (AD DS). |
|ErrorADSessionFilter |This error is returned when a **ResolveNames** operation request specifies a name that is not valid. |
|ErrorADUnavailable |This error occurs when AD DS is unavailable. Try your request again later. |
|ErrorAffectedTaskOccurrencesRequired |This error indicates that the **AffectedTaskOccurrences** attribute was not specified. When the [DeleteItem](deleteitem.md) element is used to delete at least one item that is a task, and regardless of whether that task is recurring or not, the **AffectedTaskOccurrences** attribute has to be specified so that **DeleteItem** can determine whether to delete the current occurrence or the entire series. |
|ErrorArchiveFolderPathCreation |Indicates an error in archive folder path creation. |
|ErrorArchiveMailboxNotEnabled |Indicates that the archive mailbox was not enabled. |
|ErrorArchiveMailboxServiceDiscoveryFailed |Indicates that archive mailbox service discovery failed. |
|ErrorAttachmentNestLevelLimitExceeded |Specifies that an attempt was made to create an item with more than 10 nested attachments. This value was introduced in Exchange Server 2010 Service Pack 2 (SP2). |
|ErrorAttachmentSizeLimitExceeded |The [CreateAttachment](createattachment.md) element returns this error if an attempt is made to create an attachment with size exceeding Int32.MaxValue, in bytes. The [GetAttachment](getattachment.md) element returns this error if an attempt to retrieve an existing attachment with size exceeding Int32.MaxValue, in bytes. |
|ErrorAutoDiscoverFailed |This error indicates that Exchange Web Services tried to determine the location of a cross-forest computer that is running Exchange 2010 that has the Client Access server role installed by using the Autodiscover service, but the call to the Autodiscover service failed. |
|ErrorAvailabilityConfigNotFound |This error indicates that the availability configuration information for the local forest is missing from AD DS. |
|ErrorBatchProcessingStopped |This error indicates that an exception occurred while processing an item and that exception is likely to occur for the items that follow. Requests may include multiple items; for example, a GetItem operation request might include multiple identifiers. In general, items are processed one at a time. If an exception occurs while processing an item and that exception is likely to occur for the items that follow, items that follow will not be processed. The following are examples of errors that will stop processing for items that follow: <br/> - ErrorAccessDenied <br/> - ErrorAccountDisabled <br/> - ErrorADUnavailable <br/> - ErrorADOperation <br/> - ErrorConnectionFailed <br/> - ErrorMailboxStoreUnavailable <br/> - ErrorMailboxMoveInProgress <br/> - ErrorPasswordChangeRequired <br/> - ErrorPasswordExpired <br/> - ErrorQuotaExceeded <br/> - ErrorInsufficientResources |
|ErrorCalendarCannotMoveOrCopyOccurrence |This error occurs when an attempt is made to move or copy an occurrence of a recurring calendar item. |
|ErrorCalendarCannotUpdateDeletedItem |This error occurs when an attempt is made to update a calendar item that is located in the Deleted Items folder and when meeting updates or cancellations are to be sent according to the value of the **SendMeetingInvitationsOrCancellations** attribute. The following are the possible values for this attribute: <br/> - SendToAllAndSaveCopy <br/> - SendToChangedAndSaveCopy <br/> - SendOnlyToAll <br/> - SendOnlyToChanged <br/> However, such an update is allowed only when the value of this attribute is set to SendToNone. |
|ErrorCalendarCannotUseIdForOccurrenceId |This error occurs when the UpdateItem, GetItem, DeleteItem, MoveItem, CopyItem, or SendItem operation is called and the ID that was specified is not an occurrence ID of any recurring calendar item. |
|ErrorCalendarCannotUseIdForRecurringMasterId |This error occurs when the **UpdateItem**, **GetItem**, **DeleteItem**, **MoveItem**, **CopyItem**, or **SendItem** operation is called and the ID that was specified is not an ID of any recurring master item. |
|ErrorCalendarDurationIsTooLong |This error occurs during a **CreateItem** or **UpdateItem** operation when a calendar item duration is longer than the maximum allowed, which is currently 5 years. |
|ErrorCalendarEndDateIsEarlierThanStartDate |This error occurs when a calendar End time is set to the same time or after the Start time. |
|ErrorCalendarFolderIsInvalidForCalendarView |This error occurs when the specified folder for a **FindItem** operation with a [CalendarView](calendarview.md) element is not of calendar folder type. |
|ErrorCalendarInvalidAttributeValue |This response code is not used. |
|ErrorCalendarInvalidDayForTimeChangePattern |This error occurs during a **CreateItem** or **UpdateItem** operation when invalid values of Day, WeekendDay, and Weekday are used to define the time change pattern. |
|ErrorCalendarInvalidDayForWeeklyRecurrence |This error occurs during a **CreateItem** or **UpdateItem** operation when invalid values of Day, WeekDay, and WeekendDay are used to specify the weekly recurrence. |
|ErrorCalendarInvalidPropertyState |This error occurs when the state of a calendar item recurrence binary large object (BLOB) in the Exchange store is invalid. |
|ErrorCalendarInvalidPropertyValue |This response code is not used. |
|ErrorCalendarInvalidRecurrence |This error occurs when the specified recurrence cannot be created. |
|ErrorCalendarInvalidTimeZone |This error occurs when an invalid time zone is encountered. |
|ErrorCalendarIsCancelledForAccept |This error Indicates that a calendar item has been canceled. |
|ErrorCalendarIsCancelledForDecline |This error indicates that a calendar item has been canceled. |
|ErrorCalendarIsCancelledForRemove |This error indicates that a calendar item has been canceled. |
|ErrorCalendarIsCancelledForTentative |This error indicates that a calendar item has been canceled. |
|ErrorCalendarIsDelegatedForAccept |This error indicates that the [AcceptItem](acceptitem.md) element is invalid for a calendar item or meeting request in a delegated scenario. |
|ErrorCalendarIsDelegatedForDecline |This error indicates that the [DeclineItem](declineitem.md) element is invalid for a calendar item or meeting request in a delegated scenario. |
|ErrorCalendarIsDelegatedForRemove |This error indicates that the [RemoveItem](removeitem.md) element is invalid for a meeting cancellation in a delegated scenario. |
|ErrorCalendarIsDelegatedForTentative |This error indicates that the [TentativelyAcceptItem](tentativelyacceptitem.md) element is invalid for a calendar item or meeting request in a delegated scenario. |
|ErrorCalendarIsNotOrganizer |This error indicates that the operation (currently CancelItem) on the calendar item is not valid for an attendee. Only the meeting organizer can cancel the meeting. |
|ErrorCalendarIsOrganizerForAccept |This error indicates that [AcceptItem](acceptitem.md) is invalid for the organizer's calendar item. |
|ErrorCalendarIsOrganizerForDecline |This error indicates that [DeclineItem](declineitem.md) is invalid for the organizer's calendar item. |
|ErrorCalendarIsOrganizerForRemove |This error indicates that [RemoveItem](removeitem.md) is invalid for the organizer's calendar item. To remove a meeting from the calendar, the organizer must use CancelCalendarItem. |
|ErrorCalendarIsOrganizerForTentative |This error indicates that [TentativelyAcceptItem](tentativelyacceptitem.md) is invalid for the organizer's calendar item. |
|ErrorCalendarMeetingRequestIsOutOfDate |This error indicates that a meeting request is out-of-date and cannot be updated. |
|ErrorCalendarOccurrenceIndexIsOutOfRecurrenceRange |This error indicates that the occurrence index does not point to an occurrence within the current recurrence. For example, if your recurrence pattern defines a set of three meeting occurrences and you try to access the fifth occurrence, this response code will result. |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence |This error indicates that any operation on a deleted occurrence (addressed via recurring master ID and occurrence index) is invalid. |
|ErrorCalendarOutOfRange |This error is reported on CreateItem and UpdateItem operations for calendar items or task recurrence properties when the property value is out of range. For example, specifying the fifteenth week of the month will result in this response code. |
|ErrorCalendarViewRangeTooBig |This error occurs when Start to End range for the [CalendarView](calendarview.md) element is more than the maximum allowed, currently 2 years. |
|ErrorCallerIsInvalidADAccount |This error indicates that the requesting account is not a valid account in the directory database. |
|ErrorCannotArchiveCalendarContactTaskFolderException |Indicates that an attempt was made to archive a calendar contact task folder. |
|ErrorCannotArchiveItemsInPublicFolders |Indicates that an attempt was made to archive items in public folders. |
|ErrorCannotArchiveItemsInArchiveMailbox |Indicates that attempt was made to archive items in the archive mailbox. |
|ErrorCannotCreateCalendarItemInNonCalendarFolder |This error occurs when a calendar item is being created and the **SavedItemFolderId** attribute refers to a non-calendar folder. |
|ErrorCannotCreateContactInNonContactFolder |This error occurs when a contact is being created and the **SavedItemFolderId** attribute refers to a non-contact folder. |
|ErrorCannotCreatePostItemInNonMailFolder |This error indicates that a post item cannot be created in a folder other than a mail folder, such as Calendar, Contact, Tasks, Notes, and so on. |
|ErrorCannotCreateTaskInNonTaskFolder |This error occurs when a task is being created and the **SavedItemFolderId** attribute refers to a non-task folder. |
|ErrorCannotDeleteObject |This error occurs when the item or folder to delete cannot be deleted. |
|ErrorCannotDeleteTaskOccurrence |The [DeleteItem operation](deleteitem-operation.md) returns this error when it fails to delete the current occurrence of a recurring task. This can only happen if the **AffectedTaskOccurrences** attribute has been set to SpecifiedOccurrenceOnly. |
|ErrorCannotDisableMandatoryExtension |Indicates that an attempt was made to disable a mandatorty extension. |
|ErrorCannotEmptyFolder |This error must be returned when the server cannot empty a folder. |
|ErrorCannotGetSourceFolderPath |Indicates that the source folder path could not be retrieved. |
|ErrorCannotGetExternalEcpUrl |Specifies that the server could not retrieve the external URL for Outlook Web App Options. |
|ErrorCannotOpenFileAttachment |The **GetAttachment** operation returns this error if it cannot retrieve the body of a file attachment. |
|ErrorCannotSetCalendarPermissionOnNonCalendarFolder |This error indicates that the caller tried to set calendar permissions on a non-calendar folder. |
|ErrorCannotSetNonCalendarPermissionOnCalendarFolder |This error indicates that the caller tried to set non-calendar permissions on a calendar folder. |
|ErrorCannotSetPermissionUnknownEntries |This error indicates that you cannot set unknown permissions in a permissions set. |
|ErrorCannotSpecifySearchFolderAsSourceFolder |Indicates that an attempt was made to specify the search folder as the source folder. |
|ErrorCannotUseFolderIdForItemId |This error occurs when a request that requires an item identifier is given a folder identifier. |
|ErrorCannotUseItemIdForFolderId |This error occurs when a request that requires a folder identifier is given an item identifier. |
|ErrorChangeKeyRequired |This response code has been replaced by **ErrorChangeKeyRequiredForWriteOperations**
|ErrorChangeKeyRequiredForWriteOperations |This error is returned when the change key for an item is missing or stale. For SendItem, UpdateItem, and UpdateFolder operations, the caller must pass in a correct and current change key for the item. Note that this is the case with UpdateItem even when conflict resolution is set to always overwrite. |
|ErrorClientDisconnected |Specifies that the client was disconnected. |
|ErrorClientIntentInvalidStateDefinition |This error is intended for internal use only. |
|ErrorClientIntentNotFound |This error is intended for internal use only. |
|ErrorConnectionFailed |This error occurs when Exchange Web Services cannot connect to the mailbox. |
|ErrorContainsFilterWrongType |This error indicates that the property that was inspected for a Contains filter is not a string type. |
|ErrorContentConversionFailed |The **GetItem** operation returns this error when Exchange Web Services is unable to retrieve the MIME content for the item requested. The **CreateItem** operation returns this error when Exchange Web Services is unable to create the item from the supplied MIME content. Usually this is an indication that the item property is corrupted or truncated. |
|ErrorContentIndexingNotEnabled |This error occurs when a search request is made using the QueryString option and content indexing is not enabled for the target mailbox. |
|ErrorCorruptData |This error occurs when the data is corrupted and cannot be processed. |
|ErrorCreateItemAccessDenied |This error occurs when the caller does not have permission to create the item. |
|ErrorCreateManagedFolderPartialCompletion |This error occurs when one or more of the managed folders that were specified in the CreateManagedFolder operation request failed to be created. Search for each folder to determine which folders were created and which folders do not exist. |
|ErrorCreateSubfolderAccessDenied |This error occurs when the calling account does not have the permissions required to create the subfolder. |
|ErrorCrossMailboxMoveCopy |This error occurs when an attempt is made to move an item or folder from one mailbox to another. If the source mailbox and destination mailbox are different, you will get this error. |
|ErrorCrossSiteRequest |This error indicates that the request is not allowed because the Client Access server that should service the request is in a different site. |
|ErrorDataSizeLimitExceeded |This error can occur in the following scenarios: <br/> - An attempt is made to access or write a property on an item and the property value is too large. <br/> - The base64 encoded MIME content length within the request XML exceeds the limit. <br/> - The size of the body of an existing item body exceeds the limit. <br/> - The consumer tries to set an HTML or text body whose length (or combined length in the case of append) exceeds the limit. |
|ErrorDataSourceOperation |This error occurs when the underlying data provider fails to complete the operation. |
|ErrorDelegateAlreadyExists |This error occurs in an **AddDelegate** operation when the specified user already exists in the list of delegates. |
|ErrorDelegateCannotAddOwner |This error occurs in an **AddDelegate** operation when the specified user to be added is the owner of the mailbox. |
|ErrorDelegateMissingConfiguration |This error occurs in a **GetDelegate** operation when either there is no delegate information on the local FreeBusy message or no Active Directory public delegate (no "public delegate" or no "Send On Behalf" entry in AD DS). |
|ErrorDelegateNoUser |This error occurs when a specified user cannot be mapped to a user in AD DS. |
|ErrorDelegateValidationFailed |This error occurs in the **AddDelegate** operation when an added delegate user is not valid. |
|ErrorDeleteDistinguishedFolder |This error occurs when an attempt is made to delete a distinguished folder. |
|ErrorDeleteItemsFailed |This response code is not used. |
|ErrorDeleteUnifiedMessagingPromptFailed |This error is intended for internal use only. |
|ErrorDistinguishedUserNotSupported |This error indicates that a distinguished user ID is not valid for the operation. **DistinguishedUserType** should not be present in the request. |
|ErrorDistributionListMemberNotExist |This error indicates that a request distribution list member does not exist in the distribution list. |
|ErrorDuplicateInputFolderNames |This error occurs when duplicate folder names are specified within the [FolderNames](foldernames.md) element of the **CreateManagedFolder** operation request. |
|ErrorDuplicateSOAPHeader |This error indicates that there are duplicate SOAP headers. |
|ErrorDuplicateUserIdsSpecified |This error indicates that a duplicate user ID has been found in a permission set, either Default or Anonymous are set more than once, or there are duplicate SIDs or recipients. |
|ErrorEmailAddressMismatch |This error occurs when a request attempts to create/update the search parameters of a search folder. For example, this can occur when a search folder is created in the mailbox but the search folder is directed to look in another mailbox. |
|ErrorEventNotFound |This error occurs when the event that is associated with a watermark is deleted before the event is returned. When this error is returned, the subscription is also deleted. |
|ErrorExceededConnectionCount |This error -iIndicates that there are more concurrent requests against the server than are allowed by a user's policy. |
|ErrorExceededSubscriptionCount |This error indicates that a user's throttling policy maximum subscription count has been exceeded. |
|ErrorExceededFindCountLimit |This error indicates that a search operation call has exceeded the total number of items that can be returned. |
|ErrorExpiredSubscription |This error occurs if the [GetEvents operation](getevents-operation.md) is called as a subscription is being deleted because it has expired. |
|ErrorExtensionNotFound |Indicates that the extension was not found. |
|ErrorFolderCorrupt |This error occurs when the folder is corrupted and cannot be saved. |
|ErrorFolderExists |This error occurs when an attempt is made to create a folder that has the same name as another folder in the same parent. Duplicate folder names are not allowed. |
|ErrorFolderNotFound |This error indicates that the folder ID that was specified does not correspond to a valid folder, or that the delegate does not have permission to access the folder. |
|ErrorFolderPropertRequestFailed |This error indicates that the requested property could not be retrieved. This does not indicate that the property does not exist, but that the property was corrupted in some way so that the retrieval failed. |
|ErrorFolderSave |This error indicates that the folder could not be created or updated because of an invalid state. |
|ErrorFolderSaveFailed |This error indicates that the folder could not be created or updated because of an invalid state. |
|ErrorFolderSavePropertyError |This error indicates that the folder could not be created or updated because of invalid property values. The response code lists which properties caused the problem. |
|ErrorFreeBusyDLLimitReached |This error indicates that the maximum group member count has been reached for obtaining free/busy information for a distribution list. |
|ErrorFreeBusyGenerationFailed |This error is returned when free/busy information cannot be retrieved because of an intervening failure. |
|ErrorGetServerSecurityDescriptorFailed |This response code is not used. |
|ErrorImContactLimitReached |This error is returned when new instant messaging (IM) contacts cannot be added because the maximum number of contacts has been reached. This error was introduced in Exchange Server 2013. |
|ErrorImGroupDisplayNameAlreadyExists |This error is returned when an attempt is made to add a group display name when an existing group already has the same display name. This error was introduced in Exchange 2013. |
|ErrorImGroupLimitReached |This error is returned when new IM groups cannot be added because the maximum number of groups has been reached. This error was introduced in Exchange 2013. |
|ErrorImpersonateUserDenied |The error is returned in the server-to-server authorization case for Exchange Impersonation when the caller does not have the proper rights to impersonate the specific user in question. This error maps to the ms-Exch-EPI-May-Impersonate extended Active Directory right. |
|ErrorImpersonationDenied |This error is returned in the server-to-server authorization for Exchange Impersonation when the caller does not have the proper rights to impersonate through the Client Access server that they are making the request against. This maps to the ms-Exch-EPI-Impersonation extended Active Directory right. |
|ErrorImpersonationFailed |This error indicates that there was an unexpected error when an attempt was made to perform server-to-server authentication. This response code typically indicates either that the service account that is running the Exchange Web Services application pool is configured incorrectly, that Exchange Web Services cannot talk to the directory, or that a trust between forests is not correctly configured. |
|ErrorIncorrectSchemaVersion |This error indicates that the request was valid for the current Exchange Server version but was invalid for the request server version that was specified. |
|ErrorIncorrectUpdatePropertyCount |This error indicates that each change description in the [UpdateItem](updateitem.md) or [UpdateFolder](updatefolder.md) elements must list only one property to update. |
|ErrorIndividualMailboxLimitReached |This error occurs when the request contains too many attendees to resolve. By default, the maximum number of attendees to resolve is 100. |
|ErrorInsufficientResources |This error occurs when the mailbox server is overloaded. Try your request again later. |
|ErrorInternalServerError |This error indicates that Exchange Web Services encountered an error that it could not recover from, and a more specific response code that is associated with the error that occurred does not exist. |
|ErrorInternalServerTransientError |This error indicates that an internal server error occurred and that you should try your request again later. |
|ErrorInvalidAccessLevel |This error indicates that the level of access that the caller has on the free/busy data is invalid. |
|ErrorInvalidArgument |This error indicates an error caused by all invalid arguments passed to the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md). This error is returned in the following scenarios: <br/> - The user specified in the _sending-as_ parameter does not exist in the directory. <br/> - The user specified in the _sending-as_ parameter is not unique in the directory. <br/> - The _sending-as_ address is empty. <br/> - The _sending-as_ address is not a valid e-mail address. |
|ErrorInvalidAttachmentId |This error is returned by the [GetAttachment operation](getattachment-operation.md) or the [DeleteAttachment operation](deleteattachment-operation.md) when an attachment that corresponds to the specified ID is not found. |
|ErrorInvalidAttachmentSubfilter |This error occurs when you try to bind to an existing search folder by using a complex attachment table restriction. Exchange Web Services only supports simple contains filters against the attachment table. If you try to bind to an existing search folder that has a more complex attachment table restriction (a subfilter), Exchange Web Services cannot render the XML for that filter and returns this response code. <br/> Note that you can still call the GetFolder operation on the folder, but do not request the [SearchParameters](searchparameters.md) element. |
|ErrorInvalidAttachmentSubfilterTextFilter |This error occurs when you try to bind to an existing search folder by using a complex attachment table restriction. Exchange Web Services only supports simple contains filters against the attachment table. <br/> If you try to bind to an existing search folder that has a more complex attachment table restriction, Exchange Web Services cannot render the XML for that filter. In this case, the attachment subfilter contains a text filter, but it is not looking at the attachment display name. <br/> Note that you can still call the GetFolder operation on the folder, but do not request the [SearchParameters](searchparameters.md) element. |
|ErrorInvalidAuthorizationContext |This error indicates that the authorization procedure for the requestor failed. |
|ErrorInvalidChangeKey |This error occurs when a consumer passes in a folder or item identifier with a change key that cannot be parsed. For example, this could be invalid base64 content or an empty string. |
|ErrorInvalidClientSecurityContext |This error indicates that there was an internal error when an attempt was made to resolve the identity of the caller. |
|ErrorInvalidCompleteDate |This error is returned when an attempt is made to set the [CompleteDate](completedate.md) element value of a task to a time in the future. When it is converted to the local time of the Client Access server, the [CompleteDate](completedate.md) of a task cannot be set to a value that is later than the local time on the Client Access server. |
|ErrorInvalidContactEmailAddress |This error indicates that an invalid e-mail address was provided for a contact. |
|ErrorInvalidContactEmailIndex |This error indicates that an invalid e-mail index value was provided for an e-mail entry. |
|ErrorInvalidCrossForestCredentials |This error occurs when the credentials that are used to proxy a request to a different directory service forest fail authentication. |
|ErrorInvalidDelegatePermission |This error indicates that the specified folder permissions are invalid. |
|ErrorInvalidDelegateUserId |This error indicates that the specified delegate user ID is invalid. |
|ErrorInvalidExchangeImpersonationHeaderData |This error occurs during Exchange Impersonation when a caller does not specify a UPN, an e-mail address, or a user SID. This will also occur if the caller specifies one or more of those and the values are empty. |
|ErrorInvalidExcludesRestriction |This error occurs when the bitmask that was passed into an [Excludes](excludes.md) element restriction is unable to be parsed. |
|ErrorInvalidExpressionTypeForSubFilter |This response code is not used. |
|ErrorInvalidExtendedProperty |This error occurs when the following events take place: <br/> - The caller tries to use an extended property that is not supported by Exchange Web Services. <br/> - The caller passes in an invalid combination of attribute values for an extended property. This also occurs if no attributes are passed. Only certain combinations are allowed. |
|ErrorInvalidExtendedPropertyValue |This error occurs when the value section of an extended property does not match the type of the property. <br/> For example, setting an extended property that has PropertyType="String" to an array of integers will result in this error. Any string representation that is not coercible into the type that is specified for the extended property will give this error. |
|ErrorInvalidExternalSharingInitiator |This error indicates that the sharing invitation sender did not create the sharing invitation metadata. |
|ErrorInvalidExternalSharingSubscriber |This error indicates that a sharing message is not intended for the caller. |
|ErrorInvalidFederatedOrganizationId |This error indicates that the requestor's organization federation objects are not correctly configured. |
|ErrorInvalidFolderId |This error occurs when the folder ID is corrupt. |
|ErrorInvalidFolderTypeForOperation |This error indicates that the specified folder type is invalid for the current operation. For example, you cannot create a Search folder in a public folder. |
|ErrorInvalidFractionalPagingParameters |This error occurs in fractional paging when the user has specified one of the following: <br/> - A numerator that is greater than the denominator <br/> - A numerator that is less than zero <br/> - A denominator that is less than or equal to zero. |
|ErrorInvalidGetSharingFolderRequest |This error indicates that the [DataType](datatype.md) and ShareFolderId elements are both present in a request. |
|ErrorInvalidFreeBusyViewType |This error occurs when the [GetUserAvailability operation](getuseravailability-operation.md) is called with a [FreeBusyViewType](freebusyviewtype.md) of None. |
|ErrorInvalidId |This error indicates that the ID and/or change key is malformed. |
|ErrorInvalidIdEmpty |This error occurs when the caller specifies an **Id** attribute that is empty. |
|ErrorInvalidLikeRequest |This error occurs when the item can't be liked. Versions of Exchange starting with build number 15.00.0913.09 include this value. |
|ErrorInvalidIdMalformed |This error occurs when the caller specifies an **Id** attribute that is malformed. |
|ErrorInvalidIdMalformedEwsLegacyIdFormat |This error indicates that a folder or item ID that is using the Exchange 2007 format was specified for a request with a version of Exchange 2007 SP1 or later. You cannot use Exchange 2007 IDs in Exchange 2007 SP1 or later requests. You have to use the [ConvertId operation](convertid-operation.md) to convert them first. |
|ErrorInvalidIdMonikerTooLong |This error occurs when the caller specifies an **Id** attribute that is too long. |
|ErrorInvalidIdNotAnItemAttachmentId |This error is returned whenever an ID that is not an item attachment ID is passed to a Web service method that expects an attachment ID. |
|ErrorInvalidIdReturnedByResolveNames |This error occurs when a contact in your mailbox is corrupt. |
|ErrorInvalidIdStoreObjectIdTooLong |This error occurs when the caller specifies an **Id** attribute that is too long. |
|ErrorInvalidIdTooManyAttachmentLevels |This error is returned when the attachment hierarchy on an item exceeds the maximum of 255 levels deep. |
|ErrorInvalidIdXml |This response code is not used. |
|ErrorInvalidImContactId |This error is returned when the specified IM contact identifier does not represent a valid identifier. This error was introduced in Exchange 2013. |
|ErrorInvalidImDistributionGroupSmtpAddress |This error is returned when the specified IM distribution group SMTP address identifier does not represent a valid identifier. This error was introduced in Exchange 2013. |
|ErrorInvalidImGroupId |This error is returned when the specified IM group identifier does not represent a valid identifier. This error was introduced in Exchange 2013. |
|ErrorInvalidIndexedPagingParameters |This error occurs if the offset for indexed paging is negative. |
|ErrorInvalidInternetHeaderChildNodes |This response code is not used. |
|ErrorInvalidItemForOperationArchiveItem |Indicates that the item was invalid for an **ArchiveItem** operation. |
|ErrorInvalidItemForOperationAcceptItem |This error occurs when an attempt is made to use an AcceptItem response object for an item type other than a meeting request or a calendar item, or when an attempt is made to accept a calendar item occurrence that is in the Deleted Items folder. |
|ErrorInvalidItemForOperationCancelItem |This error occurs when an attempt is made to use a CancelItem response object on an item type other than a calendar item. |
|ErrorInvalidItemForOperationCreateItemAttachment |This error is returned when an attempt is made to create an item attachment of an unsupported type. Supported item types for item attachments include the following objects: <br/> - [Item](item.md) <br/> - [Message](message-ex15websvcsotherref.md) <br/> - [CalendarItem](calendaritem.md) <br/> - [Task](task.md) <br/> - [Contact](contact.md) <br/> For example, if you try to create a [MeetingMessage](meetingmessage.md) attachment, you'll encounter this response code. |
|ErrorInvalidItemForOperationCreateItem |This error is returned from a [CreateItem operation](createitem-operation.md) if the request contains an unsupported item type. <br/> Supported items include the following objects: <br/> - [Item](item.md) <br/> - [Message](message-ex15websvcsotherref.md) <br/> - [CalendarItem](calendaritem.md) <br/> - [Task](task.md) <br/> - [Contact](contact.md) <br/> Certain types are created as a side effect of doing something else. Meeting messages, for example, are created when you send a calendar item to attendees; they are not explicitly created. |
|ErrorInvalidItemForOperationDeclineItem |This error occurs when an attempt is made to use a DeclineItem response object for an item type other than a meeting request or a calendar item, or when an attempt is made to decline a calendar item occurrence that is in the Deleted Items folder. |
|ErrorInvalidItemForOperationExpandDL |This error indicates that the [ExpandDL operation](expanddl-operation.md) is valid only for private distribution lists. |
|ErrorInvalidItemForOperationRemoveItem |This error is returned from a RemoveItem response object if the request specifies an item that is not a meeting cancellation item. |
|ErrorInvalidItemForOperationSendItem |This error is returned from a [SendItem operation](senditem-operation.md) if the request specifies an item that is not a message item. |
|ErrorInvalidItemForOperationTentative |This error occurs when an attempt is made to use [TentativelyAcceptItem](tentativelyacceptitem.md) for an item type other than a meeting request or a calendar item, or when an attempt is made to tentatively accept a calendar item occurrence that is in the Deleted Items folder. |
|ErrorInvalidLogonType |This error is for internal use only. This error is not returned. |
|ErrorInvalidMailbox |This error indicates that the [CreateItem operation](createitem-operation.md) or the [UpdateItem operation](updateitem-operation.md) failed while creating or updating a personal distribution list. |
|ErrorInvalidManagedFolderProperty |This error occurs when the structure of the managed folder is corrupted and cannot be rendered. |
|ErrorInvalidManagedFolderQuota |This error occurs when the quota that is set on the managed folder is less than zero, which indicates a corrupted managed folder. |
|ErrorInvalidManagedFolderSize |This error occurs when the size that is set on the managed folder is less than zero, which indicates a corrupted managed folder. |
|ErrorInvalidMergedFreeBusyInterval |This error occurs when the supplied merged free/busy internal value is invalid. The default minimum value is 5 minutes. The default maximum value is 1440 minutes. |
|ErrorInvalidNameForNameResolution |This error occurs when the name is invalid for the [ResolveNames operation](resolvenames-operation.md). For example, a zero length string, a single space, a comma, and a dash are all invalid names. |
|ErrorInvalidNetworkServiceContext |This error indicates an error in the Network Service account on the Client Access server. |
|ErrorInvalidOofParameter |This response code is not used. |
|ErrorInvalidOperation |This is a general error that is used when the requested operation is invalid. <br/> For example, you cannot do the following: <br/> - Perform a "Deep" traversal by using the [FindFolder operation](findfolder-operation.md) on a public folder. <br/> - Move or copy the public folder root. <br/> - Delete an associated item by using any mode except "Hard" delete. <br/> - Move or copy an associated item. |
|ErrorInvalidOrganizationRelationshipForFreeBusy |This error indicates that a caller requested free/busy information for a user in another organization but the organizational relationship does not have free/busy enabled. |
|ErrorInvalidPagingMaxRows |This error occurs when a consumer passes in a zero or a negative value for the maximum rows to be returned. |
|ErrorInvalidParentFolder |This error occurs when a consumer passes in an invalid parent folder for an operation. For example, this error is returned if you try to create a folder within a search folder. |
|ErrorInvalidPercentCompleteValue |This error is returned when an attempt is made to set a task completion percentage to an invalid value. The value must be between 0 and 100 (inclusive). |
|ErrorInvalidPermissionSettings |This error indicates that the permission level is inconsistent with the permission settings. |
|ErrorInvalidPhoneCallId |This error indicates that the caller identifier is not valid. |
|ErrorInvalidPhoneNumber |This error indicates that the telephone number is not correct or does not fit the dial plan rules. |
|ErrorInvalidPropertyAppend |This error occurs when the property that you are trying to append to does not support appending. The following are the only properties that support appending: <br/> - Recipient collections (ToRecipients, CcRecipients, BccRecipients) <br/> - Attendee collections (RequiredAttendees, OptionalAttendees, Resources) <br/> - Body <br/> - ReplyTo <br/> In addition, this error occurs when a message body is appended if the format specified in the request does not match the format of the item in the store. |
|ErrorInvalidPropertyDelete |This error occurs if the delete operation is specified in an [UpdateItem operation](updateitem-operation.md) or [UpdateFolder operation](updatefolder-operation.md) call for a property that does not support the delete operation. For example, you cannot delete the [ItemId](itemid.md) element of the [Item](item.md) object. |
|ErrorInvalidPropertyForExists |This error occurs if the consumer passes in one of the flag properties in an [Exists](exists.md) filter. For example, this error occurs if the [IsRead](isread.md) or [IsFromMe](isfromme.md) flags are specified in the [Exists](exists.md) element. The request should use the [IsEqualTo](isequalto.md) element instead for these as they are flags and therefore part of a single property. |
|ErrorInvalidPropertyForOperation |This error occurs when the property that you are trying to manipulate does not support the operation that is being performed on it. |
|ErrorInvalidPropertyRequest |This error occurs if a property that is specified in the request is not available for the item type. For example, this error is returned if a property that is only available on calendar items is requested in a [GetItem operation](getitem-operation.md) call for a message or is updated in an [UpdateItem operation](updateitem-operation.md) call for a message. This occurs in the following operations: <br/> - [GetItem operation](getitem-operation.md) <br/> - [GetFolder operation](getfolder-operation.md) <br/> - [UpdateItem operation](updateitem-operation.md) <br/> - [UpdateFolder operation](updatefolder-operation.md)
|ErrorInvalidPropertySet |This error indicates that the property that you are trying to manipulate does not support the operation that is being performed on it. For example, this error is returned if the property that you are trying to set is read-only. |
|ErrorInvalidPropertyUpdateSentMessage |This error occurs during an [UpdateItem operation](updateitem-operation.md) when a client tries to update certain properties of a message that has already been sent. <br/> For example, the following properties cannot be updated on a sent message: <br/> - [IsReadReceiptRequested](isreadreceiptrequested.md) <br/> - [IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md)
|ErrorInvalidProxySecurityContext |This response code is not used. |
|ErrorInvalidPullSubscriptionId |This error occurs if you call the [GetEvents operation](getevents-operation.md) or the [Unsubscribe operation](unsubscribe-operation.md) by using a push subscription ID. To unsubscribe from a push subscription, you must respond to a push request with an unsubscribe response, or disconnect your Web service and wait for the push notifications to time out. |
|ErrorInvalidPushSubscriptionUrl |This error is returned by the [Subscribe operation](subscribe-operation.md) when it creates a "push" subscription and indicates that the URL that is included in the request is invalid. The following conditions must be met for Exchange Web Services to accept the URL: <br/> - String length \> 0 and \< 2083. <br/> - Protocol is http or https. <br/> - The URL can be parsed by the URI Microsoft .NET Framework class. |
|ErrorInvalidRecipients |This error indicates that the recipient collection on your message or the attendee collection on your calendar item is invalid. For example, this error will be returned when an attempt is made to send an item that has no recipients. |
|ErrorInvalidRecipientSubfilter |This error indicates that the search folder has a recipient table filter that Exchange Web Services cannot represent. To get around this error, retrieve the folder without requesting the search parameters. |
|ErrorInvalidRecipientSubfilterComparison |This error indicates that the search folder has a recipient table filter that Exchange Web Services cannot represent. To get around this error, retrieve the folder without requesting the search parameters. |
|ErrorInvalidRecipientSubfilterOrder |This error indicates that the search folder has a recipient table filter that Exchange Web Services cannot represent. To get around this error, retrieve the folder without requesting the search parameters. |
|ErrorInvalidRecipientSubfilterTextFilter |This error indicates that the search folder has a recipient table filter that Exchange Web Services cannot represent. To get around this error, retrieve the folder without requesting the search parameters. |
|ErrorInvalidReferenceItem |This error is returned from the [CreateItem operation](createitem-operation.md) for Forward and Reply response objects in the following scenarios: <br/> - The referenced item identifier is not a [Message](message-ex15websvcsotherref.md), a [CalendarItem](calendaritem.md), or a descendant of a **Message** or **CalendarItem**. <br/> - The reference item identifier is for a **CalendarItem** and the organizer is trying to Reply or ReplyAll to himself. <br/> - The message is a draft and Reply or ReplyAll is selected. <br/> - The reference item, for [SuppressReadReceipt](suppressreadreceipt.md), is not a **Message** or a descendant of a **Message**. |
|ErrorInvalidRequest |This error occurs when the SOAP request has a SOAP action header, but nothing in the SOAP body. Note that the SOAP Action header is not required as Exchange Web Services can determine the method to call from the local name of the root element in the SOAP body. |
|ErrorInvalidRestriction |This response code is not used. |
|ErrorInvalidRetentionTagTypeMismatch |This error is returned when the specified retention tag has an incorrect action associated with it. This error was introduced in Exchange 2013. |
|ErrorInvalidRetentionTagInvisible |This error is returned when an attempt is made to set a nonexistent or invisible tag on a **PolicyTag** property. This error was introduced in Exchange 2013. |
|ErrorInvalidRetentionTagInheritance |This error is returned when an attempt is made to set an implicit tag on the **PolicyTag** property. This error was introduced in Exchange 2013. |
|ErrorInvalidRetentionTagIdGuid |Indicates that the retention tag GUID was invalid. |
|ErrorInvalidRoutingType |This error occurs if the routing type that is passed for a [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) element is invalid. Typically, the routing type is set to Simple Mail Transfer Protocol (SMTP). |
|ErrorInvalidScheduledOofDuration |This error occurs if the specified duration end time is not greater than the start time, or if the end time does not occur in the future. |
|ErrorInvalidSchemaVersionForMailboxVersion |This error indicates that a proxy request that was sent to another server is not able to service the request due to a versioning mismatch. |
|ErrorInvalidSecurityDescriptor |This error indicates that the Exchange security descriptor on the Calendar folder in the store is corrupted. |
|ErrorInvalidSendItemSaveSettings |This error occurs during an attempt to send an item where the [SavedItemFolderId](saveditemfolderid.md) is specified in the request but the **SaveItemToFolder** property is set to **false**. |
|ErrorInvalidSerializedAccessToken |This error indicates that the token that was passed in the header is malformed, does not refer to a valid account in the directory, or is missing the primary group **ConnectingSID**. |
|ErrorInvalidSharingData |This error indicates that the sharing metadata is not valid. This can be caused by invalid XML. |
|ErrorInvalidSharingMessage |This error indicates that the sharing message is not valid. This can be caused by a missing property. |
|ErrorInvalidSid |This error occurs when an invalid SID is passed in a request. |
|ErrorInvalidSIPUri |This error indicates that the SIP name, dial plan, or the phone number are invalid SIP URIs. |
|ErrorInvalidServerVersion |This error indicates that an invalid request server version was specified in the request. |
|ErrorInvalidSmtpAddress |This error occurs when the SMTP address cannot be parsed. |
|ErrorInvalidSubfilterType |This response code is not used. |
|ErrorInvalidSubfilterTypeNotAttendeeType |This response code is not used. |
|ErrorInvalidSubfilterTypeNotRecipientType |This response code is not used. |
|ErrorInvalidSubscription |This error indicates that the subscription is no longer valid. This could be because the Client Access server is restarting or because the subscription is expired. |
|ErrorInvalidSubscriptionRequest |This error indicates that the subscribe request included multiple public folder IDs. A subscription can include multiple folders from the same mailbox or one public folder ID. |
|ErrorInvalidSyncStateData |This error is returned by [SyncFolderItems](syncfolderitems.md) or [SyncFolderHierarchy](syncfolderhierarchy.md) if the [SyncState](syncstate-ex15websvcsotherref.md) data that is passed is invalid. To fix this error, you must resynchronize without the sync state. Make sure that if you are persisting sync state BLOBs, you are not accidentally truncating the BLOB. |
|ErrorInvalidTimeInterval |This error indicates that the specified time interval is invalid. The start time must be greater than or equal to the end time. |
|ErrorInvalidUserInfo |This error indicates that an internally inconsistent [UserId](userid.md) was specified for a permissions operation. For example, if a distinguished user ID is specified (Default or Anonymous), this error is returned if you also try to specify a SID, or primary SMTP address or display name for this user. |
|ErrorInvalidUserOofSettings |This error indicates that the user Out of Office (OOF) settings are invalid because of a missing internal or external reply. |
|ErrorInvalidUserPrincipalName |This error occurs during Exchange Impersonation. The caller passed in an invalid UPN in the SOAP header that was not accessible in the directory. |
|ErrorInvalidUserSid |This error occurs when an invalid SID is passed in a request. |
|ErrorInvalidUserSidMissingUPN |This response code is not used. |
|ErrorInvalidValueForProperty |This error indicates that the comparison value in the restriction is invalid for the property you are comparing against. For example, the comparison value of [DateTimeCreated](datetimecreated.md) > **true** would return this response code. This response code is also returned if you specify an enumeration property in the comparison, but the value that you are comparing against is not a valid value for that enumeration. |
|ErrorInvalidWatermark |This error is caused by an invalid watermark. |
|ErrorIPGatewayNotFound |This error indicates that a valid VoIP gateway is not available. |
|ErrorIrresolvableConflict |This error indicates that conflict resolution was unable to resolve changes for the properties. The items in the store may have been changed and have to be updated. Retrieve the updated change key and try again. |
|ErrorItemCorrupt |This error indicates that the state of the object is corrupted and cannot be retrieved. When you are retrieving an item, only certain elements will be in this state, such as [Body](body.md) and [MimeContent](mimecontent.md). Omit these elements and retry the operation. |
|ErrorItemNotFound |This error occurs when the item was not found or you do not have permission to access the item. |
|ErrorItemPropertyRequestFailed |This error occurs if a property request on an item fails. The property may exist, but it could not be retrieved. |
|ErrorItemSave |This error occurs when attempts to save the item or folder fail. |
|ErrorItemSavePropertyError |This error occurs when attempts to save the item or folder fail because of invalid property values. The response code includes the path of the invalid properties. |
|ErrorLegacyMailboxFreeBusyViewTypeNotMerged |This response code is not used. |
|ErrorLocalServerObjectNotFound |This response code is not used. |
|ErrorLogonAsNetworkServiceFailed |This error indicates that the Availability service was unable to log on as the network service to proxy requests to the appropriate sites or forests. This response typically indicates a configuration error. |
|ErrorMailboxConfiguration |This error indicates that the mailbox information in AD DS is configured incorrectly. |
|ErrorMailboxDataArrayEmpty |This error indicates that the [MailboxDataArray](mailboxdataarray.md) element in the request is empty. You must supply at least one mailbox identifier. |
|ErrorMailboxDataArrayTooBig |This error occurs when more than 100 entries are supplied in a [MailboxDataArray](mailboxdataarray.md) element.. |
|ErrorMailboxFailover |This error indicates that an attempt to access a mailbox failed because the mailbox is in a failover process. |
|ErrorMailboxHoldNotFound |Indicates that the mailbox hold was not found. |
|ErrorMailboxLogonFailed |This error occurs when the connection to the mailbox to get the calendar view information failed. |
|ErrorMailboxMoveInProgress |This error indicates that the mailbox is being moved to a different mailbox store or server. This error can also indicate that the mailbox is on another server or mailbox database. |
|ErrorMailboxStoreUnavailable |This error indicates that one of the following error conditions occurred: <br/> - The mailbox store is corrupt. <br/> - The mailbox store is being stopped. <br/> - The mailbox store is offline. <br/> - A network error occurred when an attempt was made to access the mailbox store. <br/> - The mailbox store is overloaded and cannot accept any more connections. <br/> - The mailbox store has been paused. |
|ErrorMailRecipientNotFound |This error occurs if the [MailboxData](mailboxdata.md) element information cannot be mapped to a valid mailbox account. |
|ErrorMailTipsDisabled |This error indicates that mail tips are disabled. |
|ErrorManagedFolderAlreadyExists |This error occurs if the managed folder that you are trying to create already exists in a mailbox. |
|ErrorManagedFolderNotFound |This error occurs when the folder name that was specified in the request does not map to a managed folder definition in AD DS. You can only create instances of managed folders for folders that are defined in AD DS. Check the name and try again. |
|ErrorManagedFoldersRootFailure |This error indicates that the managed folders root was deleted from the mailbox or that a folder exists in the same parent folder that has the name of the managed folder root. This will also occur if the attempt to create the root managed folder fails. |
|ErrorMeetingSuggestionGenerationFailed |This error indicates that the suggestions engine encountered a problem when it was trying to generate the suggestions. |
|ErrorMessageDispositionRequired |This error occurs if the **MessageDisposition** attribute is not set. This attribute is required for the following: <br/> - The [CreateItem operation](createitem-operation.md) and the [UpdateItem operation](updateitem-operation.md) when the item being created or updated is a [Message](message-ex15websvcsotherref.md). <br/> - [CancelCalendarItem](cancelcalendaritem.md), [AcceptItem](acceptitem.md), [DeclineItem](declineitem.md), or [TentativelyAcceptItem](tentativelyacceptitem.md) response objects. |
|ErrorMessageSizeExceeded |This error indicates that the message that you are trying to send exceeds the allowed limits. |
|ErrorMessageTrackingNoSuchDomain |This error indicates that the given domain cannot be found. |
|ErrorMessageTrackingPermanentError |This error indicates that the message tracking service cannot track the message. |
| ErrorMessageTrackingTransientError |This error indicates that the message tracking service is either down or busy. This error code indicates a transient error. Clients can retry to connect to the server when this error is received. |
|ErrorMimeContentConversionFailed |This error occurs when the MIME content is not a valid iCal for a [CreateItem operation](createitem-operation.md). For a [GetItem operation](getitem-operation.md), this response indicates that the MIME content could not be generated. |
|ErrorMimeContentInvalid |This error occurs when the MIME content is invalid. |
|ErrorMimeContentInvalidBase64String |This error occurs when the MIME content in the request is not a valid base 64 string. |
|ErrorMissingArgument |This error indicates that a required argument was missing from the request. The response message text indicates which argument to check. |
|ErrorMissingEmailAddress |This error indicates that you specified a distinguished folder ID in the request, but the account that made the request does not have a mailbox on the system. In that case, you must supply a [Mailbox](mailbox.md) sub-element under [DistinguishedFolderId](distinguishedfolderid.md). |
|ErrorMissingEmailAddressForManagedFolder |This error indicates that you specified a distinguished folder ID in the request, but the account that made the request does not have a mailbox on the system. In that case, you must supply a [Mailbox](mailbox.md) sub-element under [DistinguishedFolderId](distinguishedfolderid.md). This response is returned from the [CreateManagedFolder operation](createmanagedfolder-operation.md). |
|ErrorMissingInformationEmailAddress |This error occurs if the [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element is missing. |
|ErrorMissingInformationReferenceItemId |This error occurs if the [ReferenceItemId](referenceitemid.md) is missing. |
|ErrorMissingInformationSharingFolderId |This error code is never returned. |
|ErrorMissingItemForCreateItemAttachment |This error is returned when an attempt is made to not include the item element in the **ItemAttachment** element of a [CreateAttachment operation](createattachment-operation.md) request. |
|ErrorMissingManagedFolderId |This error occurs when the policy IDs property, property tag 0x6732, for the folder is missing. You should consider this a corrupted folder. |
|ErrorMissingRecipients |This error indicates that you tried to send an item without including recipients. Note that if you call the [CreateItem operation](createitem-operation.md) with a message disposition that causes the message to be sent, you will get the following response code: **ErrorInvalidRecipients**. |
|ErrorMissingUserIdInformation |This error indicates that a [UserId](userid.md) has not been fully specified in a permissions set. |
|ErrorMoreThanOneAccessModeSpecified |This error indicates that you have specified more than one [ExchangeImpersonation](exchangeimpersonation.md) element value within a request. |
|ErrorMoveCopyFailed |This error indicates that the move or copy operation failed. Moving occurs in the [CreateItem operation](createitem-operation.md) when you accept a meeting request that is in the Deleted Items folder. In addition, if you decline a meeting request, cancel a calendar item, or remove a meeting from your calendar, it is moved to the Deleted Items folder. |
|ErrorMoveDistinguishedFolder |This error occurs if you try to move a distinguished folder. |
|ErrorMultiLegacyMailboxAccess |This error occurs when a request attempts to access multiple mailbox servers. This error was introduced in Exchange 2013. |
|ErrorNameResolutionMultipleResults |This error occurs if the [ResolveNames operation](resolvenames-operation.md) returns more than one result or the ambiguous name that you specified matches more than one object in the directory. The response code includes the matched names in the response data. |
|ErrorNameResolutionNoMailbox |This error indicates that the caller does not have a mailbox on the system. The [ResolveNames operation](resolvenames-operation.md) or [ExpandDL operation](expanddl-operation.md) is invalid for connecting a user without a mailbox. |
|ErrorNameResolutionNoResults |This error indicates that the [ResolveNames operation](resolvenames-operation.md) returns no results. |
|ErrorNoApplicableProxyCASServersAvailable |This error code MUST be returned when the Web service cannot find a server to handle the request. |
|ErrorNoCalendar |This error occurs if there is no Calendar folder for the mailbox. |
|ErrorNoDestinationCASDueToKerberosRequirements |This error indicates that the request referred to a mailbox in another Active Directory site, but no Client Access servers in the destination site were configured for Windows Authentication, and therefore the request could not be proxied. |
|ErrorNoDestinationCASDueToSSLRequirements |This error indicates that the request referred to a mailbox in another Active Directory site, but no Client Access servers in the destination site were configured for SSL connections, and therefore the request could not be proxied. |
|ErrorNoDestinationCASDueToVersionMismatch |This error indicates that the request referred to a mailbox in another Active Directory site, but no Client Access servers in the destination site were of an acceptable product version to receive the request, and therefore the request could not be proxied. |
|ErrorNoFolderClassOverride |This error occurs if you set the [FolderClass](folderclass.md) element when you are creating an item other than a generic folder. For typed folders such as [CalendarFolder](calendarfolder.md) and [TasksFolder](tasksfolder.md), the folder class is implied. Setting the folder class to a different folder type by using the [UpdateFolder operation](updatefolder-operation.md) results in the **ErrorObjectTypeChanged** response. Instead, use a generic folder type but set the folder class to the value that you require. Exchange Web Services will create the correct strongly typed folder. |
|ErrorNoFreeBusyAccess |This error indicates that the caller does not have free/busy viewing rights on the Calendar folder in question. |
|ErrorNonExistentMailbox |This error occurs in the following scenarios: <br/> - The e-mail address is empty in [CreateManagedFolder](createmanagedfolder.md). <br/> - The e-mail address does not refer to a valid account in a request that takes an e-mail address in the body or in the SOAP header, such as in an Exchange Impersonation call. |
|ErrorNonPrimarySmtpAddress |This error occurs when a caller passes in a non-primary SMTP address. The response includes the correct SMTP address to use. |
|ErrorNoPropertyTagForCustomProperties |This error indicates that MAPI properties in the custom range, 0x8000 and greater, cannot be referenced by property tags. You must use the EWS Managed API [PropertySetId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition.propertysetid%28v=exchg.80%29.aspx)property or the EWS [ExtendedFieldURI](extendedfielduri.md) element with the PropertySetId attribute. |
|ErrorNoPublicFolderReplicaAvailable |This response code is not used. |
|ErrorNoPublicFolderServerAvailable |This error code MUST be returned if no public folder server is available or if the caller does not have a home public server. |
|ErrorNoRespondingCASInDestinationSite |This error indicates that the request referred to a mailbox in another Active Directory site, but none of the Client Access servers in that site responded, and therefore the request could not be proxied. |
|ErrorNotAllowedExternalSharingByPolicy |This error indicates that the caller tried to grant permissions in its calendar or contacts folder to a user in another organization, and the attempt failed. |
|ErrorNotDelegate |This error indicates that the user is not a delegate for the mailbox. It is returned by the [GetDelegate operation](getdelegate-operation.md), the [RemoveDelegate operation](removedelegate-operation.md), and the [UpdateDelegate operation](updatedelegate-operation.md) when the specified delegate user is not found in the list of delegates. |
|ErrorNotEnoughMemory |This error indicates that the operation could not be completed because of insufficient memory. |
|ErrorNotSupportedSharingMessage |This error indicates that the sharing message is not supported. |
|ErrorObjectTypeChanged |This error occurs if the object type changed. |
|ErrorOccurrenceCrossingBoundary |This error occurs when the [Start](start.md) or [End](end-ex15websvcsotherref.md) time of an occurrence is updated so that the occurrence is scheduled to happen earlier or later than the corresponding previous or next occurrence. |
|ErrorOccurrenceTimeSpanTooBig |This error indicates that the time allotment for a given occurrence overlaps with another occurrence of the same recurring item. This response also occurs when the length in minutes of a given occurrence is larger than Int32.MaxValue. |
|ErrorOperationNotAllowedWithPublicFolderRoot |This error indicates that the current operation is not valid for the public folder root. |
|ErrorOrganizationNotFederated |This error indicates that the requester's organization is not federated so the requester cannot create sharing messages to send to an external user or cannot accept sharing messages received from an external user. |
|ErrorParentFolderIdRequired |This response code is not used. |
|ErrorParentFolderNotFound |This error occurs in the [CreateFolder operation](createfolder-operation.md) when the parent folder is not found. |
|ErrorPasswordChangeRequired |This error indicates that you must change your password before you can access this mailbox. This occurs when a new account has been created and the administrator indicated that the user must change the password at first logon. You cannot update the password by using Exchange Web Services. You must use a tool such as Microsoft Office Outlook Web App to change your password. |
|ErrorPasswordExpired |This error indicates that the password has expired. You cannot change the password by using Exchange Web Services. You must use a tool such as Outlook Web App to change your password. |
|ErrorPermissionNotAllowedByPolicy |This error indicates that the requester tried to grant permissions in its calendar or contacts folder to an external user but the sharing policy assigned to the requester indicates that the requested permission level is higher than what the sharing policy allows. |
|ErrorPhoneNumberNotDialable |This error indicates that the telephone number was not in the correct form. |
|ErrorPropertyUpdate |This error indicates that the update failed because of invalid property values. The response message includes the invalid property paths. |
|ErrorPromptPublishingOperationFailed |This error is intended for internal use only. This error was introduced in Exchange 2013. |
|ErrorPropertyValidationFailure |This response code is not used. |
|ErrorProxiedSubscriptionCallFailure |This error indicates that the request referred to a subscription that exists on another Client Access server, but an attempt to proxy the request to that Client Access server failed. |
|ErrorProxyCallFailed |This response code is not used. |
|ErrorProxyGroupSidLimitExceeded |This error indicates that the request referred to a mailbox in another Active Directory site, and the original caller is a member of more than 3,000 groups. |
|ErrorProxyRequestNotAllowed |This error indicates that the request that Exchange Web Services sent to another Client Access server when trying to fulfill a [GetUserAvailabilityRequest](getuseravailabilityrequest.md) request was invalid. This response code typically indicates that a configuration or rights error has occurred, or that someone tried unsuccessfully to mimic an availability proxy request. |
|ErrorProxyRequestProcessingFailed |This error indicates that Exchange Web Services tried to proxy an availability request to another Client Access server for fulfillment, but the request failed. This response can be caused by network connectivity issues or request timeout issues. |
|ErrorProxyServiceDiscoveryFailed |This error code must be returned if the Web service cannot determine whether the request is to run on the target server or will be proxied to another server. |
|ErrorProxyTokenExpired |This response code is not used. |
|ErrorPublicFolderMailboxDiscoveryFailed |This error occurs when the public folder mailbox URL cannot be found. This error is intended for internal use only. This error was introduced in Exchange 2013. |
|ErrorPublicFolderOperationFailed |This error occurs when an attempt is made to access a public folder and the attempt is unsuccessful. This error was introduced in Exchange 2013Exchange Server 2013. |
|ErrorPublicFolderRequestProcessingFailed |This error occurs when the recipient that was passed to the [GetUserAvailability operation](getuseravailability-operation.md) is located on a computer that is running a version of Exchange Server that is earlier than Exchange 2007, and the request to retrieve free/busy information for the recipient from the public folder server failed. |
|ErrorPublicFolderServerNotFound |This error occurs when the recipient that was passed to the [GetUserAvailability operation](getuseravailability-operation.md) is located on a computer that is running a version of Exchange Server that is earlier than Exchange 2007, and the request to retrieve free/busy information for the recipient from the public folder server failed because the organizational unit did not have an associated public folder server. |
|ErrorPublicFolderSyncException |This error occurs when a synchronization operation succeeds against the primary public folder mailbox but does not succeed against the secondary public folder mailbox. This error was introduced in Exchange 2013. |
|ErrorQueryFilterTooLong |This error indicates that the search folder restriction may be valid, but it is not supported by EWS. Exchange Web Services limits restrictions to contain a maximum of 255 filter expressions. If you try to bind to an existing search folder that exceeds 255, this response code is returned. |
|ErrorQuotaExceeded |This error occurs when the mailbox quota is exceeded. |
|ErrorReadEventsFailed |This error is returned by the [GetEvents operation](getevents-operation.md) or push notifications when a failure occurs while retrieving event information. When this error is returned, the subscription is deleted. Re-create the event synchronization based on a last known watermark. |
|ErrorReadReceiptNotPending |This error is returned by the [CreateItem operation](createitem-operation.md) if an attempt was made to suppress a read receipt when the message sender did not request a read receipt on the message or if the message is in the Junk E-mail folder. |
|ErrorRecurrenceEndDateTooBig |This error occurs when the end date for the recurrence is after 9/1/4500. |
|ErrorRecurrenceHasNoOccurrence |This error occurs when the specified recurrence does not have any occurrence instances in the specified range. |
|ErrorRemoveDelegatesFailed |This error indicates that the delegate list failed to be saved after delegates were removed. |
|ErrorRequestAborted |This response code is not used. |
|ErrorRequestStreamTooBig |This error occurs when the request stream is larger than 400 KB. |
|ErrorRequiredPropertyMissing |This error is returned when a required property is missing in a [CreateAttachment operation](createattachment-operation.md) request. The missing property URI is included in the response. |
|ErrorResolveNamesInvalidFolderType |This error indicates that the caller has specified a folder that is not a contacts folder to the [ResolveNames operation](resolvenames-operation.md). |
|ErrorResolveNamesOnlyOneContactsFolderAllowed |This error indicates that the caller has specified more than one contacts folder to the [ResolveNames operation](resolvenames-operation.md). |
|ErrorResponseSchemaValidation |This response code is not used. |
|ErrorRestrictionTooLong |This error occurs if the restriction contains more than 255 nodes. |
|ErrorRestrictionTooComplex |This error occurs when the restriction cannot be evaluated by Exchange Web Services. |
|ErrorResultSetTooBig |This error indicates that the number of calendar entries for a given recipient exceeds the allowed limit of 1000. Reduce the window and try again. |
|ErrorSavedItemFolderNotFound |This error occurs when the [SavedItemFolderId](saveditemfolderid.md) is not found. |
|ErrorSchemaValidation |This error occurs when the request cannot be validated against the schema. |
|ErrorSearchFolderNotInitialized |This error indicates that the search folder was created, but the search criteria were never set on the folder. This only occurs when you access corrupted search folders that were created by using another API or client. To fix this error, use the [UpdateFolder operation](updatefolder-operation.md) to set the [SearchParameters](searchparameters.md) element to include the restriction that should be on the folder. |
|ErrorSendAsDenied |This error occurs when both of the following conditions occur: <br/> - A user has been granted CanActAsOwner permissions but is not granted delegate rights on the principal's mailbox. <br/> - The same user tries to create and send an e-mail message in the principal's mailbox by using the SendAndSaveCopy option. <br/> The result is an ErrorSendAsDenied error and the creation of the e-mail message in the principal's Drafts folder. |
|ErrorSendMeetingCancellationsRequired |This error is returned by the [DeleteItem operation](deleteitem-operation.md) if the **SendMeetingCancellations** attribute is missing from the request and the item to delete is a calendar item. |
|ErrorSendMeetingInvitationsOrCancellationsRequired |This error is returned by the [UpdateItem operation](updateitem-operation.md) if the **SendMeetingInvitationsOrCancellations** attribute is missing from the request and the item to update is a calendar item. |
|ErrorSendMeetingInvitationsRequired |This error is returned by the [CreateItem operation](createitem-operation.md) if the **SendMeetingInvitations** attribute is missing from the request and the item to create is a calendar item. |
|ErrorSentMeetingRequestUpdate |This error indicates that after the organizer sends a meeting request, the request cannot be updated. To modify the meeting, modify the calendar item, not the meeting request. |
|ErrorSentTaskRequestUpdate |This error indicates that after the task initiator sends a task request, that request cannot be updated. |
|ErrorServerBusy |This error occurs when the server is busy. |
|ErrorServiceDiscoveryFailed |This error indicates that Exchange Web Services tried to proxy a user availability request to the appropriate forest for the recipient, but it could not determine where to send the request because of a service discovery failure. |
|ErrorSharingNoExternalEwsAvailable |This error indicates that the external URL property has not been set in the Active Directory database. |
|ErrorSharingSynchronizationFailed |This error indicates that an attempt at synchronizing a sharing folder failed. This error code is returned when the following occurs: <br/> - The subscription for a sharing folder is not found. <br/> - The sharing folder is not found. <br/> - The corresponding directory user is not found. <br/> - The user no longer exists. <br/> - The appointment is invalid. <br/> - The contact item is invalid. <br/> - There is a communication failure with the remote server. |
|ErrorStaleObject |This error occurs in an [UpdateItem operation](updateitem-operation.md) or a [SendItem operation](senditem-operation.md) when the change key is not up-to-date or was not supplied. Call the [GetItem operation](getitem-operation.md) to retrieve an updated change key and then try the operation again. |
|ErrorSubmissionQuotaExceeded |This error Indicates that a user cannot immediately send more requests because the submission quota has been reached. |
|ErrorSubscriptionAccessDenied |This error occurs when you try to access a subscription by using an account that did not create that subscription. Each subscription can only be accessed by the creator of the subscription. |
|ErrorSubscriptionDelegateAccessNotSupported |This error indicates that you cannot create a subscription if you are not the owner or do not have owner access to the mailbox. |
|ErrorSubscriptionNotFound |This error occurs if the subscription that corresponds to the specified [SubscriptionId (GetEvents)](subscriptionid-getevents.md) is not found. The subscription may have expired, the Exchange Web Services process may have been restarted, or an invalid subscription was passed in. If the subscription was valid, re-create the subscription with the latest watermark. This is returned by the [Unsubscribe operation](unsubscribe-operation.md) or the [GetEvents operation](getevents-operation.md) responses. |
|ErrorSubscriptionUnsubsribed |This error code must be returned when a request is made for a subscription that has been unsubscribed. |
|ErrorSyncFolderNotFound |This error is returned by the [SyncFolderItems operation](syncfolderitems-operation.md) if the parent folder that is specified cannot be found. |
|ErrorTeamMailboxNotFound |This error indicates that a team mailbox was not found. This error was introduced in Exchange 2013. |
|ErrorTeamMailboxNotLinkedToSharePoint |This error indicates that a team mailbox was found but that it is not linked to a SharePoint Server. This error was introduced in Exchange 2013. |
|ErrorTeamMailboxUrlValidationFailed |This error indicates that a team mailbox was found but that the link to the SharePoint Server is not valid. This error was introduced in Exchange 2013. |
|ErrorTeamMailboxNotAuthorizedOwner |This error code is not used. This error was introduced in Exchange 2013. |
|ErrorTeamMailboxActiveToPendingDelete |This error code is not used. This error was introduced in Exchange 2013. |
|ErrorTeamMailboxFailedSendingNotifications |This error indicates that an attempt to send a notification to the team mailbox owners was unsuccessful. This error was introduced in Exchange 2013. |
|ErrorTeamMailboxErrorUnknown |This error indicates a general error that can occur when trying to access a team mailbox. Try submitting the request at a later time. This error was introduced in Exchange 2013. |
|ErrorTimeIntervalTooBig |This error indicates that the time window that was specified is larger than the allowed limit. By default, the allowed limit is 42. |
|ErrorTimeoutExpired |This error occurs when there is not enough time to complete the processing of the request. |
|ErrorTimeZone |This error indicates that there is a time zone error. |
|ErrorToFolderNotFound |This error indicates that the destination folder does not exist. |
|ErrorTokenSerializationDenied |This error occurs if the caller tries to do a Token serialization request but does not have the ms-Exch-EPI-TokenSerialization right on the Client Access server. |
|ErrorTooManyObjectsOpened |This error occurs when the internal limit on open objects has been exceeded. |
|ErrorUnifiedMessagingDialPlanNotFound |This error indicates that a user's dial plan is not available. |
|ErrorUnifiedMessagingReportDataNotFound |This error is intended for internal use only. This error was introduced in Exchange 2013. |
|ErrorUnifiedMessagingPromptNotFound |This error is intended for internal use only. This error was introduced in Exchange 2013. |
|ErrorUnifiedMessagingRequestFailed |This error indicates that the user could not be found. |
|ErrorUnifiedMessagingServerNotFound |This error indicates that a valid server for the dial plan can be found to handle the request. |
|ErrorUnableToGetUserOofSettings |This response code is not used. |
|ErrorUnableToRemoveImContactFromGroup |This error occurs when an unsuccessful attempt is made to remove an IM contact from a group. This error was introduced in Exchange 2013. |
|ErrorUnsupportedCulture |This error occurs when you try to set the **Culture** property to a value that is not parsable by the **System.Globalization.CultureInfo** class. |
|ErrorUnsupportedMapiPropertyType |This error occurs when a caller tries to use extended properties of types object, object array, error, or null. |
|ErrorUnsupportedMimeConversion |This error occurs when you are trying to retrieve or set MIME content for an item other than a [PostItem](postitem.md), [Message](message-ex15websvcsotherref.md), or [CalendarItem](calendaritem.md) object. |
|ErrorUnsupportedPathForQuery |This error occurs when the caller passes a property that is invalid for a query. This can occur when calculated properties are used. |
|ErrorUnsupportedPathForSortGroup |This error occurs when the caller passes a property that is invalid for a sort or group by property. This can occur when calculated properties are used. |
|ErrorUnsupportedPropertyDefinition |This response code is not used. |
|ErrorUnsupportedQueryFilter |This error indicates that the search folder restriction may be valid, but it is not supported by EWS. |
|ErrorUnsupportedRecurrence |This error indicates that the specified recurrence is not supported for tasks. |
|ErrorUnsupportedSubFilter |This response code is not used. |
|ErrorUnsupportedTypeForConversion |This error indicates that Exchange Web Services found a property type in the store but it cannot generate XML for the property type. |
|ErrorUpdateDelegatesFailed |This error indicates that the delegate list failed to be saved after delegates were updated. |
|ErrorUpdatePropertyMismatch |This error occurs when the single property path that is listed in a change description does not match the single property that is being set within the actual [Item](item.md) or [Folder](folder.md) object. |
|ErrorUserNotUnifiedMessagingEnabled |This error indicates that the requester is not enabled. |
|ErrorUserNotAllowedByPolicy |This error indicates that the requester tried to grant permissions in its calendar or contacts folder to an external user but the sharing policy assigned to the requester indicates that the domain of the external user is not listed in the policy. |
|ErrorUserWithoutFederatedProxyAddress |Indicates that the requester's organization has a set of federated domains but the requester's organization does not have any SMTP proxy addresses with one of the federated domains. |
|ErrorValueOutOfRange |This error indicates that a calendar view start date or end date was set to 1/1/0001 12:00:00 AM or 12/31/9999 11:59:59 PM. |
|ErrorVirusDetected |This error indicates that the Exchange store detected a virus in the message. |
|ErrorVirusMessageDeleted |This error indicates that the Exchange store detected a virus in the message and deleted it. |
|ErrorVoiceMailNotImplemented |This response code is not used. |
|ErrorWebRequestInInvalidState |This response code is not used. |
|ErrorWin32InteropError |This error indicates that there was an internal failure during communication with unmanaged code. |
|ErrorWorkingHoursSaveFailed |This response code is not used. |
|ErrorWorkingHoursXmlMalformed |This response code is not used. |
|ErrorWrongServerVersion |This error indicates that a request can only be made to a server that is the same version as the mailbox server. |
|ErrorWrongServerVersionDelegate |This error indicates that a request was made by a delegate that has a different server version than the principal's mailbox server. |
|ErrorMissingInformationSharingFolderId |This error code is never returned. |
|ErrorDuplicateSOAPHeader |Specifies that there are duplicate SOAP headers. |
|ErrorSharingSynchronizationFailed | Specifies that an attempt at synchronizing a sharing folder failed. This error code MUST be returned when: <br/> - The subscription for a sharing folder is not found. <br/> - The sharing folder was not found. <br/> - The corresponding directory user was not found. <br/> - The user no longer exists. <br/> - The appointment is invalid. <br/> - The contact item is invalid. <br/> - There was a communication failure with the remote server. |
|ErrorSharingNoExternalEwsAvailable |Specifies that the external URL property has not been set in the Active Directory database. This error code MUST be returned if the external URL property has not been set in the Active Directory database. |
|ErrorFreeBusyDLLimitReached |Specifies that the maximum group member count has been reached for obtaining free/busy information for a distribution list. This error MUST be returned when the maximum group member count has been reached for obtaining free/busy information for a distribution list. |
|ErrorInvalidGetSharingFolderRequest |Specifies that the DataType and ShareFolderId element are both present in a request. This error code MUST be returned if the DataType and ShareFolderId element are both present in a request. |
|ErrorNotAllowedExternalSharingByPolicy |Specifies that the caller attempted to grant permissions in its calendar or contacts folder to a user in another organization and the attempt failed. This error code MUST be returned when the sharing policy is disabled for the caller or when the sharing policy assigned to the caller disallows sharing for the requested level or the requested folder type. |
|ErrorUserNotAllowedByPolicy |Specifies that the requestor attempted to grant permissions in its calendar or contacts folder to an external user but the sharing policy assigned to the requestor specifies that the domain of the external user is not listed in the policy. |
|ErrorPermissionNotAllowedByPolicy |Specifies that the requestor attempted to grant permissions in its calendar or contacts folder to an external user but the sharing policy assigned to the requestor specifies that the requested permission level is higher is than what the sharing policy allows. |
|ErrorOrganizationNotFederated |Specifies that the requestor's organization is not federated so the requestor cannot create sharing messages to send to an external user or cannot accept sharing messages received from an external user. This error code MUST be returned if the requestor's organization is not federated. |
|ErrorMailboxFailover |Specifies that an attempt to access a mailbox failed because the mailbox is in a failover process. |
|ErrorInvalidExternalSharingInitiator |Specifies that the sharing invitation sender did not create the sharing invitation metadata. This error code MUST be returned if the sharing invitation sender did not create the sharing invitation metadata. |
|ErrorMessageTrackingPermanentError |Specifies that the message tracking service cannot track the message. |
|ErrorMessageTrackingTransientError |Specifies that either the message tracking service is down or busy. This error code specifies a transient error. Clients can retry to connect to the server when this error is received. |
|ErrorMessageTrackingNoSuchDomain |Specifies that the given domain cannot be found. |
|ErrorUserWithoutFederatedProxyAddress |Specifies that the requestor's organization has a set of federated domains but the requestor's organization does not have any SMTP proxy addresses with one of the federated domains. |
|ErrorInvalidOrganizationRelationshipForFreeBusy |Specifies that a caller requested free/busy information for a user in another organization but the organizational relationship does not have free/busy enabled. |
|ErrorInvalidFederatedOrganizationId |Specifies that the requestor's organization federation objects are not properly configured. |
|ErrorInvalidExternalSharingSubscriber |Specifies that a sharing message is not intended for the caller. |
|ErrorInvalidSharingData |Specifies that the sharing metadata is not valid. This can be caused by invalid XML. |
|ErrorInvalidSharingMessage |Specifies that the sharing message is not valid. This can be caused by a missing property. |
|ErrorNotSupportedSharingMessage |Specifies that the sharing message is not supported. |
|ErrorApplyConversationActionFailed |This error MUST be returned if an action cannot be applied to one or more items in the conversation. |
|ErrorInboxRulesValidationError |This error MUST be returned if any rule does not validate. |
|ErrorOutlookRuleBlobExists |This error MUST be returned when an attempt to manage Inbox rules occurs after another client has accessed the Inbox rules. |
|ErrorRulesOverQuota |This error MUST be returned when a user's rule quota has been exceeded. |
|ErrorNewEventStreamConnectionOpened |This error MUST be returned to the first subscription connection if a second subscription connection is opened. |
|ErrorMissedNotificationEvents |This error MUST be returned when event notifications are missed. |
|ErrorDuplicateLegacyDistinguishedName |This error is returned when there are duplicate legacy distinguished names in Active Directory Domain Services (AD DS). This error was introduced in Exchange 2013. |
|ErrorInvalidClientAccessTokenRequest |This error indicates that a request to get a client access token was not valid. This error was introduced in Exchange 2013. |
|ErrorNoSpeechDetected |This error is intended for internal use only. This error was introduced in Exchange 2013. |
|ErrorUMServerUnavailable |This error is intended for internal use only. This error was introduced in Exchange 2013. |
|ErrorRecipientNotFound |This error is intended for internal use only. This error was introduced in Exchange 2013. |
|ErrorRecognizerNotInstalled |This error is intended for internal use only. This error was introduced in Exchange 2013. |
|ErrorSpeechGrammarError |This error is intended for internal use only. This error was introduced in Exchange 2013. |
|ErrorInvalidManagementRoleHeader |This error is returned if the [ManagementRole](managementrole.md) header in the SOAP header is incorrect. This error was introduced in Exchange 2013. |
|ErrorLocationServicesDisabled |This error is intended for internal use only. This error was introduced in Exchange 2013. |
|ErrorLocationServicesRequestTimedOut |This error is intended for internal use only. This error was introduced in Exchange 2013. |
|ErrorLocationServicesRequestFailed |This error is intended for internal use only. This error was introduced in Exchange 2013. |
|ErrorLocationServicesInvalidRequest |This error is intended for internal use only. This error was introduced in Exchange 2013. |
|ErrorWeatherServiceDisabled |This error is intended for internal use only. |
|ErrorMailboxScopeNotAllowedWithoutQueryString |This error is returned when a scoped search attempt is performed without using a [QueryString (String)](querystring-string.md) element for a content indexing search. This is applicable to the **SearchMailboxes** and **FindConversation** operations. This error was introduced in Exchange 2013. |
|ErrorArchiveMailboxSearchFailed |This error is returned when an archive mailbox search is unsuccessful. This error was introduced in Exchange 2013. |
|ErrorArchiveMailboxServiceDiscoveryFailed |This error is returned when the URL of an archive mailbox is not discoverable. This error was introduced in Exchange 2013. |
|ErrorGetRemoteArchiveFolderFailed |This error occurs when the operation to get the remote archive mailbox folder failed. |
|ErrorFindRemoteArchiveFolderFailed |This error occurs when the operation to find the remote archive mailbox folder failed. |
|ErrorGetRemoteArchiveItemFailed |This error occurs when the operation to get the remote archive mailbox item failed. |
|ErrorExportRemoteArchiveItemsFailed |This error occurs when the operation to export remote archive mailbox items failed. |
|ErrorInvalidPhotoSize |This error is returned if an invalid photo size is requested from the server. This error was introduced in Exchange 2013. |
|ErrorSearchQueryHasTooManyKeywords |This error is returned when an unexpected photo size is requested in a **GetUserPhoto** operation request. This error was introduced in Exchange 2013. |
|ErrorSearchTooManyMailboxes |This error is returned when a **SearchMailboxes** operation request contains too many mailboxes to search. This error was introduced in Exchange 2013. |
|ErrorInvalidRetentionTagNone |This error indicates that no retention tags were found for this user. This error was introduced in Exchange 2013. |
|ErrorDiscoverySearchesDisabled |This error is returned when discovery searches are disabled on a tenant or server. This error was introduced in Exchange 2013. |
|ErrorCalendarSeekToConditionNotSupported |This error occurs when attempting to invoke the [FindItem operation](finditem-operation.md) with a [SeekToConditionPageItemView](seektoconditionpageitemview.md) for fetching calendar items, which is not supported. |
|ErrorCalendarIsGroupMailboxForAccept |This error is intended for internal use only. |
|ErrorCalendarIsGroupMailboxForDecline |This error is intended for internal use only. |
|ErrorCalendarIsGroupMailboxForTentative |This error is intended for internal use only. |
|ErrorCalendarIsGroupMailboxForSuppressReadReceipt |This error is intended for internal use only. |
|ErrorOrganizationAccessBlocked |The tenant is marked for removal. |
|ErrorInvalidLicense |The user doesn't have a valid license. |
|ErrorMessagePerFolderCountReceiveQuotaExceeded |The message per folder receive quota has been exceeded. |

## Remarks

This element is not required and is not included in all responses.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace | https://schemas.microsoft.com/exchange/services/2006/messages |
|Schema Name | Messages schema |
|Validation File | Messages.xsd |
|Can be Empty | False |

## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
