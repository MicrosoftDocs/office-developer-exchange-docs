---
title: "ResponseCode"
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
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
|[ResponseMessage](responsemessage.md) <br/> | Provides descriptive information about the response status.<br/><br/>  The following are the possible XPath expressions to this element:<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/><br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>  `/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>  `/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |Contains the status and result of a single [DeleteItem operation](deleteitem-operation.md) request.  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |Contains the status and result of a single [SendItem operation](senditem-operation.md) request.  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |Contains the status and result of a single [DeleteFolder operation](deletefolder-operation.md) request.  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Contains the status and result of a single [DeleteAttachment operation](deleteattachment-operation.md) request.  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |Contains the status and result of a single [Unsubscribe operation](unsubscribe-operation.md) request.  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Contains the status and result of a single [GetFolder operation](getfolder-operation.md) request.  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Contains the status and result of a single [UpdateFolder operation](updatefolder-operation.md) request.  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Contains the status and result of a single [MoveFolder operation](movefolder-operation.md) request.  <br/> |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Contains the status and result of a single [CopyFolder operation](copyfolder-operation.md)request.  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request.  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Contains the status and result of a single [FindFolder operation](findfolder-operation.md) request.  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Contains the status and result of a single [CreateItem operation](createitem-operation.md) request.  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Contains the status and result of a single [GetItem operation](getitem-operation.md) request.  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request.  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Contains the status and result of a single [MoveItem operation](moveitem-operation.md) request.  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Contains the status and result of a single [CopyItem operation](copyitem-operation.md) request.  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |Contains the status and result of a single [CreateAttachment operation](createattachment-operation.md) request.  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |Contains the status and result of a single [GetAttachment operation](getattachment-operation.md) request.  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Contains the status and result of a single [FindItem operation](finditem-operation.md) request.  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Contains the status and result of a [ResolveNames operation](resolvenames-operation.md) request.  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Contains the status and result of a single [ExpandDL operation](expanddl-operation.md) request.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contains the status and result of a single [Subscribe operation](subscribe-operation.md) request.  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Contains the status and result of a single [GetEvents operation](getevents-operation.md) request.  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Contains the status and result of a single SendNotification operation request.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contains the status and result of a [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) request.  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Contains the status and result of a [SyncFolderItems operation](syncfolderitems-operation.md) request.  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Contains the status and result of a [ConvertId operation](convertid-operation.md) request.  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request.  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request.  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |Contains the status and result of a [RemoveDelegate operation](removedelegate-operation.md) request.  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |Contains the status and result of an [UpdateDelegate operation](updatedelegate-operation.md) request.  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |Contains the status and result of a [GetServerTimeZones operation](getservertimezones-operation.md) request.  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Contains the status and result of a [GetSharingFolder operation](getsharingfolder-operation.md) request.  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |Defines a response to a [GetSharingFolder operation](getsharingfolder-operation.md) request.  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Contains the status and result of a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |Contains the status and result of a [RefreshSharingFolder operation](refreshsharingfolder-operation.md) request.  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |Defines a response to a [RefreshSharingFolder operation](refreshsharingfolder-operation.md) request.  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |Contains the status and results of a [FindConversation operation](findconversation-operation.md) response.  <br/> |
|[ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md) <br/> |Contains the status and results of an [ApplyConversationAction operation](applyconversationaction-operation.md) request.  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |Contains the status and result of a single [EmptyFolder operation](emptyfolder-operation.md) request.  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Contains a status and result of an [UpdateInboxRules operation](updateinboxrules-operation.md) request.  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Contains a status and result of an [UploadItems operation](uploaditems-operation.md) request.  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Contains a response to a [GetInboxRules operation](getinboxrules-operation.md) **** request.  <br/> |
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md) <br/> |Contains a response to a [GetServiceConfiguration operation](getserviceconfiguration-operation.md) request.  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contains service configuration settings.  <br/> |
   
## Text value

A text value is required if this element is used. The following table describes the values that are returned with this element.
  
|Value|Description|
|:-----|:-----|
|NoError  <br/> |No error occurred for the request.  <br/> |
|ErrorAccessDenied  <br/> |This error occurs when the calling account does not have the rights to perform the requested action.  <br/> |
|ErrorAccessModeSpecified  <br/> |This error is for internal use only. This error is not returned.  <br/> |
|ErrorAccountDisabled  <br/> |This error occurs when the account in question has been disabled.  <br/> |
|ErrorAddDelegatesFailed  <br/> |This error occurs when a list with added delegates cannot be saved.  <br/> |
|ErrorAddressSpaceNotFound  <br/> |This error occurs when the address space record, or Domain Name System (DNS) domain name, for cross-forest availability could not be found in the Active Directory database.  <br/> |
|ErrorADOperation  <br/> |This error occurs when the operation failed because of communication problems with Active Directory Domain Services (AD DS).  <br/> |
|ErrorADSessionFilter  <br/> |This error is returned when a **ResolveNames** operation request specifies a name that is not valid.  <br/> |
|ErrorADUnavailable  <br/> |This error occurs when AD DS is unavailable. Try your request again later.  <br/> |
|ErrorAffectedTaskOccurrencesRequired  <br/> |This error indicates that the **AffectedTaskOccurrences** attribute was not specified. When the [DeleteItem](deleteitem.md) element is used to delete at least one item that is a task, and regardless of whether that task is recurring or not, the **AffectedTaskOccurrences** attribute has to be specified so that **DeleteItem** can determine whether to delete the current occurrence or the entire series.  <br/> |
|ErrorArchiveFolderPathCreation  <br/> |Indicates an error in archive folder path creation.  <br/> |
|ErrorArchiveMailboxNotEnabled  <br/> |Indicates that the archive mailbox was not enabled.  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |Indicates that archive mailbox service discovery failed.  <br/> |
|ErrorAttachmentNestLevelLimitExceeded  <br/> |Specifies that an attempt was made to create an item with more than 10 nested attachments. This value was introduced in Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
|ErrorAttachmentSizeLimitExceeded  <br/> |The [CreateAttachment](createattachment.md) element returns this error if an attempt is made to create an attachment with size exceeding Int32.MaxValue, in bytes.  <br/> The [GetAttachment](getattachment.md) element returns this error if an attempt to retrieve an existing attachment with size exceeding Int32.MaxValue, in bytes.  <br/> |
|ErrorAutoDiscoverFailed  <br/> |This error indicates that Exchange Web Services tried to determine the location of a cross-forest computer that is running Exchange 2010 that has the Client Access server role installed by using the Autodiscover service, but the call to the Autodiscover service failed.  <br/> |
|ErrorAvailabilityConfigNotFound  <br/> |This error indicates that the availability configuration information for the local forest is missing from AD DS.  <br/> |
|ErrorBatchProcessingStopped  <br/> | This error indicates that an exception occurred while processing an item and that exception is likely to occur for the items that follow. Requests may include multiple items; for example, a GetItem operation request might include multiple identifiers. In general, items are processed one at a time. If an exception occurs while processing an item and that exception is likely to occur for the items that follow, items that follow will not be processed.  <br/><br/>  The following are examples of errors that will stop processing for items that follow:<br/>  <br/>-  ErrorAccessDenied  <br/>-  ErrorAccountDisabled  <br/>-  ErrorADUnavailable  <br/>-  ErrorADOperation  <br/>-  ErrorConnectionFailed  <br/>-  ErrorMailboxStoreUnavailable  <br/>-  ErrorMailboxMoveInProgress  <br/>-  ErrorPasswordChangeRequired  <br/>-  ErrorPasswordExpired  <br/>-  ErrorQuotaExceeded  <br/>-  ErrorInsufficientResources  <br/> |
|ErrorCalendarCannotMoveOrCopyOccurrence  <br/> |This error occurs when an attempt is made to move or copy an occurrence of a recurring calendar item.  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> | This error occurs when an attempt is made to update a calendar item that is located in the Deleted Items folder and when meeting updates or cancellations are to be sent according to the value of the **SendMeetingInvitationsOrCancellations** attribute. <br/><br/>The following are the possible values for this attribute:  <br/><br/>-  SendToAllAndSaveCopy  <br/>-  SendToChangedAndSaveCopy  <br/>-  SendOnlyToAll  <br/>-  SendOnlyToChanged  <br/>  <br/>However, such an update is allowed only when the value of this attribute is set to SendToNone.  <br/> |
|ErrorCalendarCannotUseIdForOccurrenceId  <br/> |This error occurs when the UpdateItem, GetItem, DeleteItem, MoveItem, CopyItem, or SendItem operation is called and the ID that was specified is not an occurrence ID of any recurring calendar item.  <br/> |
|ErrorCalendarCannotUseIdForRecurringMasterId  <br/> |This error occurs when the **UpdateItem**, **GetItem**, **DeleteItem**, **MoveItem**, **CopyItem**, or **SendItem** operation is called and the ID that was specified is not an ID of any recurring master item.  <br/> |
|ErrorCalendarDurationIsTooLong  <br/> |This error occurs during a **CreateItem** or **UpdateItem** operation when a calendar item duration is longer than the maximum allowed, which is currently 5 years.  <br/> |
|ErrorCalendarEndDateIsEarlierThanStartDate  <br/> |This error occurs when a calendar End time is set to the same time or after the Start time.  <br/> |
|ErrorCalendarFolderIsInvalidForCalendarView  <br/> |This error occurs when the specified folder for a **FindItem** operation with a [CalendarView](calendarview.md) element is not of calendar folder type.  <br/> |
|ErrorCalendarInvalidAttributeValue  <br/> |This response code is not used.  <br/> |
|ErrorCalendarInvalidDayForTimeChangePattern  <br/> |This error occurs during a **CreateItem** or **UpdateItem** operation when invalid values of Day, WeekendDay, and Weekday are used to define the time change pattern.  <br/> |
|ErrorCalendarInvalidDayForWeeklyRecurrence  <br/> |This error occurs during a **CreateItem** or **UpdateItem** operation when invalid values of Day, WeekDay, and WeekendDay are used to specify the weekly recurrence.  <br/> |
|ErrorCalendarInvalidPropertyState  <br/> |This error occurs when the state of a calendar item recurrence binary large object (BLOB) in the Exchange store is invalid.  <br/> |
|ErrorCalendarInvalidPropertyValue  <br/> |This response code is not used.  <br/> |
|ErrorCalendarInvalidRecurrence  <br/> |This error occurs when the specified recurrence cannot be created.  <br/> |
|ErrorCalendarInvalidTimeZone  <br/> |This error occurs when an invalid time zone is encountered.  <br/> |
|ErrorCalendarIsCancelledForAccept  <br/> |This error Indicates that a calendar item has been canceled.  <br/> |
|ErrorCalendarIsCancelledForDecline  <br/> |This error indicates that a calendar item has been canceled.  <br/> |
|ErrorCalendarIsCancelledForRemove  <br/> |This error indicates that a calendar item has been canceled.  <br/> |
|ErrorCalendarIsCancelledForTentative  <br/> |This error indicates that a calendar item has been canceled.  <br/> |
|ErrorCalendarIsDelegatedForAccept  <br/> |This error indicates that the [AcceptItem](acceptitem.md) element is invalid for a calendar item or meeting request in a delegated scenario.  <br/> |
|ErrorCalendarIsDelegatedForDecline  <br/> |This error indicates that the [DeclineItem](declineitem.md) element is invalid for a calendar item or meeting request in a delegated scenario.  <br/> |
|ErrorCalendarIsDelegatedForRemove  <br/> |This error indicates that the [RemoveItem](removeitem.md) element is invalid for a meeting cancellation in a delegated scenario.  <br/> |
|ErrorCalendarIsDelegatedForTentative  <br/> |This error indicates that the [TentativelyAcceptItem](tentativelyacceptitem.md) element is invalid for a calendar item or meeting request in a delegated scenario.  <br/> |
|ErrorCalendarIsNotOrganizer  <br/> |This error indicates that the operation (currently CancelItem) on the calendar item is not valid for an attendee. Only the meeting organizer can cancel the meeting.  <br/> |
|ErrorCalendarIsOrganizerForAccept  <br/> |This error indicates that [AcceptItem](acceptitem.md) is invalid for the organizer's calendar item.  <br/> |
|ErrorCalendarIsOrganizerForDecline  <br/> |This error indicates that [DeclineItem](declineitem.md) is invalid for the organizer's calendar item.  <br/> |
|ErrorCalendarIsOrganizerForRemove  <br/> |This error indicates that [RemoveItem](removeitem.md) is invalid for the organizer's calendar item. To remove a meeting from the calendar, the organizer must use CancelCalendarItem.  <br/> |
|ErrorCalendarIsOrganizerForTentative  <br/> |This error indicates that [TentativelyAcceptItem](tentativelyacceptitem.md) is invalid for the organizer's calendar item.  <br/> |
|ErrorCalendarMeetingRequestIsOutOfDate  <br/> |This error indicates that a meeting request is out-of-date and cannot be updated.  <br/> |
|ErrorCalendarOccurrenceIndexIsOutOfRecurrenceRange  <br/> |This error indicates that the occurrence index does not point to an occurrence within the current recurrence. For example, if your recurrence pattern defines a set of three meeting occurrences and you try to access the fifth occurrence, this response code will result.  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |This error indicates that any operation on a deleted occurrence (addressed via recurring master ID and occurrence index) is invalid.  <br/> |
|ErrorCalendarOutOfRange  <br/> |This error is reported on CreateItem and UpdateItem operations for calendar items or task recurrence properties when the property value is out of range. For example, specifying the fifteenth week of the month will result in this response code.  <br/> |
|ErrorCalendarViewRangeTooBig  <br/> |This error occurs when Start to End range for the [CalendarView](calendarview.md) element is more than the maximum allowed, currently 2 years.  <br/> |
|ErrorCallerIsInvalidADAccount  <br/> |This error indicates that the requesting account is not a valid account in the directory database.  <br/> |
|ErrorCannotArchiveCalendarContactTaskFolderException  <br/> |Indicates that an attempt was made to archive a calendar contact task folder.  <br/> |
|ErrorCannotArchiveItemsInPublicFolders  <br/> |Indicates that an attempt was made to archive items in public folders.  <br/> |
|ErrorCannotArchiveItemsInArchiveMailbox  <br/> |Indicates that attempt was made to archive items in the archive mailbox.  <br/> |
|ErrorCannotCreateCalendarItemInNonCalendarFolder  <br/> |This error occurs when a calendar item is being created and the **SavedItemFolderId** attribute refers to a non-calendar folder.  <br/> |
|ErrorCannotCreateContactInNonContactFolder  <br/> |This error occurs when a contact is being created and the **SavedItemFolderId** attribute refers to a non-contact folder.  <br/> |
|ErrorCannotCreatePostItemInNonMailFolder  <br/> |This error indicates that a post item cannot be created in a folder other than a mail folder, such as Calendar, Contact, Tasks, Notes, and so on.  <br/> |
|ErrorCannotCreateTaskInNonTaskFolder  <br/> |This error occurs when a task is being created and the **SavedItemFolderId** attribute refers to a non-task folder.  <br/> |
|ErrorCannotDeleteObject  <br/> |This error occurs when the item or folder to delete cannot be deleted.  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |The [DeleteItem operation](deleteitem-operation.md) returns this error when it fails to delete the current occurrence of a recurring task. This can only happen if the **AffectedTaskOccurrences** attribute has been set to SpecifiedOccurrenceOnly.  <br/> |
|ErrorCannotDisableMandatoryExtension  <br/> |Indicates that an attempt was made to disable a mandatorty extension.  <br/> |
|ErrorCannotEmptyFolder  <br/> |This error must be returned when the server cannot empty a folder.  <br/> |
|ErrorCannotGetSourceFolderPath  <br/> |Indicates that the source folder path could not be retrieved.  <br/> |
|ErrorCannotGetExternalEcpUrl  <br/> |Specifies that the server could not retrieve the external URL for Outlook Web App Options.  <br/> |
|ErrorCannotOpenFileAttachment  <br/> |The **GetAttachment** operation returns this error if it cannot retrieve the body of a file attachment.  <br/> |
|ErrorCannotSetCalendarPermissionOnNonCalendarFolder  <br/> |This error indicates that the caller tried to set calendar permissions on a non-calendar folder.  <br/> |
|ErrorCannotSetNonCalendarPermissionOnCalendarFolder  <br/> |This error indicates that the caller tried to set non-calendar permissions on a calendar folder.  <br/> |
|ErrorCannotSetPermissionUnknownEntries  <br/> |This error indicates that you cannot set unknown permissions in a permissions set.  <br/> |
|ErrorCannotSpecifySearchFolderAsSourceFolder  <br/> |Indicates that an attempt was made to specify the search folder as the source folder.  <br/> |
|ErrorCannotUseFolderIdForItemId  <br/> |This error occurs when a request that requires an item identifier is given a folder identifier.  <br/> |
|ErrorCannotUseItemIdForFolderId  <br/> |This error occurs when a request that requires a folder identifier is given an item identifier.  <br/> |
|ErrorChangeKeyRequired  <br/> |This response code has been replaced by **ErrorChangeKeyRequiredForWriteOperations** <br/> |
|ErrorChangeKeyRequiredForWriteOperations  <br/> |This error is returned when the change key for an item is missing or stale. <br/><br/>For SendItem, UpdateItem, and UpdateFolder operations, the caller must pass in a correct and current change key for the item. Note that this is the case with UpdateItem even when conflict resolution is set to always overwrite.  <br/> |
|ErrorClientDisconnected  <br/> |Specifies that the client was disconnected.  <br/> |
|ErrorClientIntentInvalidStateDefinition  <br/> |This error is intended for internal use only.  <br/> |
|ErrorClientIntentNotFound  <br/> |This error is intended for internal use only.  <br/> |
|ErrorConnectionFailed  <br/> |This error occurs when Exchange Web Services cannot connect to the mailbox.  <br/> |
|ErrorContainsFilterWrongType  <br/> |This error indicates that the property that was inspected for a Contains filter is not a string type.  <br/> |
|ErrorContentConversionFailed  <br/> |The **GetItem** operation returns this error when Exchange Web Services is unable to retrieve the MIME content for the item requested. <br/><br/>The **CreateItem** operation returns this error when Exchange Web Services is unable to create the item from the supplied MIME content. Usually this is an indication that the item property is corrupted or truncated.  <br/> |
|ErrorContentIndexingNotEnabled  <br/> |This error occurs when a search request is made using the QueryString option and content indexing is not enabled for the target mailbox.  <br/> |
|ErrorCorruptData  <br/> |This error occurs when the data is corrupted and cannot be processed.  <br/> |
|ErrorCreateItemAccessDenied  <br/> |This error occurs when the caller does not have permission to create the item.  <br/> |
|ErrorCreateManagedFolderPartialCompletion  <br/> |This error occurs when one or more of the managed folders that were specified in the CreateManagedFolder operation request failed to be created. Search for each folder to determine which folders were created and which folders do not exist.  <br/> |
|ErrorCreateSubfolderAccessDenied  <br/> |This error occurs when the calling account does not have the permissions required to create the subfolder.  <br/> |
|ErrorCrossMailboxMoveCopy  <br/> |This error occurs when an attempt is made to move an item or folder from one mailbox to another. If the source mailbox and destination mailbox are different, you will get this error.  <br/> |
|ErrorCrossSiteRequest  <br/> |This error indicates that the request is not allowed because the Client Access server that should service the request is in a different site.  <br/> |
|ErrorDataSizeLimitExceeded  <br/> |This error can occur in the following scenarios:<br/>  <br/>- An attempt is made to access or write a property on an item and the property value is too large.<br/>- The base64 encoded MIME content length within the request XML exceeds the limit.<br/>- The size of the body of an existing item body exceeds the limit.<br/>- The consumer tries to set an HTML or text body whose length (or combined length in the case of append) exceeds the limit. |
|ErrorDataSourceOperation  <br/> |This error occurs when the underlying data provider fails to complete the operation.  <br/> |
|ErrorDelegateAlreadyExists  <br/> |This error occurs in an **AddDelegate** operation when the specified user already exists in the list of delegates.  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |This error occurs in an **AddDelegate** operation when the specified user to be added is the owner of the mailbox.  <br/> |
|ErrorDelegateMissingConfiguration  <br/> |This error occurs in a **GetDelegate** operation when either there is no delegate information on the local FreeBusy message or no Active Directory public delegate (no "public delegate" or no "Send On Behalf" entry in AD DS).  <br/> |
|ErrorDelegateNoUser  <br/> |This error occurs when a specified user cannot be mapped to a user in AD DS.  <br/> |
|ErrorDelegateValidationFailed  <br/> |This error occurs in the **AddDelegate** operation when an added delegate user is not valid.  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |This error occurs when an attempt is made to delete a distinguished folder.  <br/> |
|ErrorDeleteItemsFailed  <br/> |This response code is not used.  <br/> |
|ErrorDeleteUnifiedMessagingPromptFailed  <br/> |This error is intended for internal use only.  <br/> |
|ErrorDistinguishedUserNotSupported  <br/> |This error indicates that a distinguished user ID is not valid for the operation. **DistinguishedUserType** should not be present in the request.  <br/> |
|ErrorDistributionListMemberNotExist  <br/> |This error indicates that a request distribution list member does not exist in the distribution list.  <br/> |
|ErrorDuplicateInputFolderNames  <br/> |This error occurs when duplicate folder names are specified within the [FolderNames](foldernames.md) element of the **CreateManagedFolder** operation request.  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |This error indicates that there are duplicate SOAP headers.  <br/> |
|ErrorDuplicateUserIdsSpecified  <br/> |This error indicates that a duplicate user ID has been found in a permission set, either Default or Anonymous are set more than once, or there are duplicate SIDs or recipients.  <br/> |
|ErrorEmailAddressMismatch  <br/> |This error occurs when a request attempts to create/update the search parameters of a search folder. For example, this can occur when a search folder is created in the mailbox but the search folder is directed to look in another mailbox.  <br/> |
|ErrorEventNotFound  <br/> |This error occurs when the event that is associated with a watermark is deleted before the event is returned. When this error is returned, the subscription is also deleted.  <br/> |
|ErrorExceededConnectionCount  <br/> |This error -iIndicates that there are more concurrent requests against the server than are allowed by a user's policy.  <br/> |
|ErrorExceededSubscriptionCount  <br/> |This error indicates that a user's throttling policy maximum subscription count has been exceeded.  <br/> |
|ErrorExceededFindCountLimit  <br/> |This error indicates that a search operation call has exceeded the total number of items that can be returned.  <br/> |
|ErrorExpiredSubscription  <br/> |This error occurs if the [GetEvents operation](getevents-operation.md) is called as a subscription is being deleted because it has expired.  <br/> |
|ErrorExtensionNotFound  <br/> |Indicates that the extension was not found.  <br/> |
|ErrorFolderCorrupt  <br/> |This error occurs when the folder is corrupted and cannot be saved.  <br/> |
|ErrorFolderExists  <br/> |This error occurs when an attempt is made to create a folder that has the same name as another folder in the same parent. Duplicate folder names are not allowed.  <br/> |
|ErrorFolderNotFound  <br/> |This error indicates that the folder ID that was specified does not correspond to a valid folder, or that the delegate does not have permission to access the folder.  <br/> |
|ErrorFolderPropertRequestFailed  <br/> |This error indicates that the requested property could not be retrieved. This does not indicate that the property does not exist, but that the property was corrupted in some way so that the retrieval failed.  <br/> |
|ErrorFolderSave  <br/> |This error indicates that the folder could not be created or updated because of an invalid state.  <br/> |
|ErrorFolderSaveFailed  <br/> |This error indicates that the folder could not be created or updated because of an invalid state.  <br/> |
|ErrorFolderSavePropertyError  <br/> |This error indicates that the folder could not be created or updated because of invalid property values. The response code lists which properties caused the problem.  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |This error indicates that the maximum group member count has been reached for obtaining free/busy information for a distribution list.  <br/> |
|ErrorFreeBusyGenerationFailed  <br/> |This error is returned when free/busy information cannot be retrieved because of an intervening failure.  <br/> |
|ErrorGetServerSecurityDescriptorFailed  <br/> |This response code is not used.  <br/> |
|ErrorImContactLimitReached  <br/> |This error is returned when new instant messaging (IM) contacts cannot be added because the maximum number of contacts has been reached. This error was introduced in Exchange Server 2013.  <br/> |
|ErrorImGroupDisplayNameAlreadyExists  <br/> |This error is returned when an attempt is made to add a group display name when an existing group already has the same display name. This error was introduced in Exchange 2013.  <br/> |
|ErrorImGroupLimitReached  <br/> |This error is returned when new IM groups cannot be added because the maximum number of groups has been reached. This error was introduced in Exchange 2013.  <br/> |
|ErrorImpersonateUserDenied  <br/> |The error is returned in the server-to-server authorization case for Exchange Impersonation when the caller does not have the proper rights to impersonate the specific user in question. This error maps to the ms-Exch-EPI-May-Impersonate extended Active Directory right.  <br/> |
|ErrorImpersonationDenied  <br/> |This error is returned in the server-to-server authorization for Exchange Impersonation when the caller does not have the proper rights to impersonate through the Client Access server that they are making the request against. This maps to the ms-Exch-EPI-Impersonation extended Active Directory right.  <br/> |
|ErrorImpersonationFailed  <br/> |This error indicates that there was an unexpected error when an attempt was made to perform server-to-server authentication. This response code typically indicates either that the service account that is running the Exchange Web Services application pool is configured incorrectly, that Exchange Web Services cannot talk to the directory, or that a trust between forests is not correctly configured.  <br/> |
|ErrorIncorrectSchemaVersion  <br/> |This error indicates that the request was valid for the current Exchange Server version but was invalid for the request server version that was specified.  <br/> |
|ErrorIncorrectUpdatePropertyCount  <br/> |This error indicates that each change description in the [UpdateItem](updateitem.md) or [UpdateFolder](updatefolder.md) elements must list only one property to update.  <br/> |
|ErrorIndividualMailboxLimitReached  <br/> |This error occurs when the request contains too many attendees to resolve. By default, the maximum number of attendees to resolve is 100.  <br/> |
|ErrorInsufficientResources  <br/> |This error occurs when the mailbox server is overloaded. Try your request again later.  <br/> |
|ErrorInternalServerError  <br/> |This error indicates that Exchange Web Services encountered an error that it could not recover from, and a more specific response code that is associated with the error that occurred does not exist.  <br/> |
|ErrorInternalServerTransientError  <br/> |This error indicates that an internal server error occurred and that you should try your request again later.  <br/> |
|ErrorInvalidAccessLevel  <br/> |This error indicates that the level of access that the caller has on the free/busy data is invalid.  <br/> |
|ErrorInvalidArgument  <br/> |This error indicates an error caused by all invalid arguments passed to the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).<br/><br/> This error is returned in the following scenarios: <br/><br/>- The user specified in the  _sending-as_ parameter does not exist in the directory. <br/>- The user specified in the  _sending-as_ parameter is not unique in the directory. <br/>- The  _sending-as_ address is empty.<br/>- The  _sending-as_ address is not a valid e-mail address.  <br/> |
|ErrorInvalidAttachmentId  <br/> |This error is returned by the [GetAttachment operation](getattachment-operation.md) or the [DeleteAttachment operation](deleteattachment-operation.md) when an attachment that corresponds to the specified ID is not found.  <br/> |
|ErrorInvalidAttachmentSubfilter  <br/> |This error occurs when you try to bind to an existing search folder by using a complex attachment table restriction. Exchange Web Services only supports simple contains filters against the attachment table. If you try to bind to an existing search folder that has a more complex attachment table restriction (a subfilter), Exchange Web Services cannot render the XML for that filter and returns this response code. <br/><br/>Note that you can still call the GetFolder operation on the folder, but do not request the [SearchParameters](searchparameters.md) element.  <br/> |
|ErrorInvalidAttachmentSubfilterTextFilter  <br/> |This error occurs when you try to bind to an existing search folder by using a complex attachment table restriction. Exchange Web Services only supports simple contains filters against the attachment table. <br/><br/>If you try to bind to an existing search folder that has a more complex attachment table restriction, Exchange Web Services cannot render the XML for that filter. In this case, the attachment subfilter contains a text filter, but it is not looking at the attachment display name.<br/><br/> Note that you can still call the GetFolder operation on the folder, but do not request the [SearchParameters](searchparameters.md) element.  <br/> |
|ErrorInvalidAuthorizationContext  <br/> | This error indicates that the authorization procedure for the requestor failed.  <br/> |
|ErrorInvalidChangeKey  <br/> |This error occurs when a consumer passes in a folder or item identifier with a change key that cannot be parsed. For example, this could be invalid base64 content or an empty string.  <br/> |
|ErrorInvalidClientSecurityContext  <br/> |This error indicates that there was an internal error when an attempt was made to resolve the identity of the caller.  <br/> |
|ErrorInvalidCompleteDate  <br/> |This error is returned when an attempt is made to set the [CompleteDate](completedate.md) element value of a task to a time in the future. When it is converted to the local time of the Client Access server, the [CompleteDate](completedate.md) of a task cannot be set to a value that is later than the local time on the Client Access server.  <br/> |
|ErrorInvalidContactEmailAddress  <br/> |This error indicates that an invalid e-mail address was provided for a contact.  <br/> |
|ErrorInvalidContactEmailIndex  <br/> |This error indicates that an invalid e-mail index value was provided for an e-mail entry.  <br/> |
|ErrorInvalidCrossForestCredentials  <br/> |This error occurs when the credentials that are used to proxy a request to a different directory service forest fail authentication.  <br/> |
|ErrorInvalidDelegatePermission  <br/> |This error indicates that the specified folder permissions are invalid.  <br/> |
|ErrorInvalidDelegateUserId  <br/> |This error indicates that the specified delegate user ID is invalid.  <br/> |
|ErrorInvalidExchangeImpersonationHeaderData  <br/> |This error occurs during Exchange Impersonation when a caller does not specify a UPN, an e-mail address, or a user SID. This will also occur if the caller specifies one or more of those and the values are empty.  <br/> |
|ErrorInvalidExcludesRestriction  <br/> |This error occurs when the bitmask that was passed into an [Excludes](excludes.md) element restriction is unable to be parsed.  <br/> |
|ErrorInvalidExpressionTypeForSubFilter  <br/> |This response code is not used.  <br/> |
|ErrorInvalidExtendedProperty  <br/> | This error occurs when the following events take place: <br/> <br/>-  The caller tries to use an extended property that is not supported by Exchange Web Services.  <br/>-  The caller passes in an invalid combination of attribute values for an extended property. This also occurs if no attributes are passed. Only certain combinations are allowed.  <br/> |
|ErrorInvalidExtendedPropertyValue  <br/> |This error occurs when the value section of an extended property does not match the type of the property. <br/><br/>For example, setting an extended property that has PropertyType="String" to an array of integers will result in this error. Any string representation that is not coercible into the type that is specified for the extended property will give this error.  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |This error indicates that the sharing invitation sender did not create the sharing invitation metadata.  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |This error indicates that a sharing message is not intended for the caller.  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |This error indicates that the requestor's organization federation objects are not correctly configured.  <br/> |
|ErrorInvalidFolderId  <br/> |This error occurs when the folder ID is corrupt.  <br/> |
|ErrorInvalidFolderTypeForOperation  <br/> |This error indicates that the specified folder type is invalid for the current operation. For example, you cannot create a Search folder in a public folder.  <br/> |
|ErrorInvalidFractionalPagingParameters  <br/> | This error occurs in fractional paging when the user has specified one of the following: <br/> <br/>-  A numerator that is greater than the denominator  <br/>-  A numerator that is less than zero  <br/>-  A denominator that is less than or equal to zero  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |This error indicates that the [DataType](datatype.md) and ShareFolderId elements are both present in a request.  <br/> |
|ErrorInvalidFreeBusyViewType  <br/> |This error occurs when the [GetUserAvailability operation](getuseravailability-operation.md) is called with a [FreeBusyViewType](freebusyviewtype.md) of None.  <br/> |
|ErrorInvalidId  <br/> |This error indicates that the ID and/or change key is malformed.  <br/> |
|ErrorInvalidIdEmpty  <br/> |This error occurs when the caller specifies an **Id** attribute that is empty.  <br/> |
|ErrorInvalidLikeRequest  <br/> |This error occurs when the item can't be liked. Versions of Exchange starting with build number 15.00.0913.09 include this value.  <br/> |
|ErrorInvalidIdMalformed  <br/> |This error occurs when the caller specifies an **Id** attribute that is malformed.  <br/> |
|ErrorInvalidIdMalformedEwsLegacyIdFormat  <br/> |This error indicates that a folder or item ID that is using the Exchange 2007 format was specified for a request with a version of Exchange 2007 SP1 or later. You cannot use Exchange 2007 IDs in Exchange 2007 SP1 or later requests. You have to use the [ConvertId operation](convertid-operation.md) to convert them first.  <br/> |
|ErrorInvalidIdMonikerTooLong  <br/> |This error occurs when the caller specifies an **Id** attribute that is too long.  <br/> |
|ErrorInvalidIdNotAnItemAttachmentId  <br/> |This error is returned whenever an ID that is not an item attachment ID is passed to a Web service method that expects an attachment ID.  <br/> |
|ErrorInvalidIdReturnedByResolveNames  <br/> |This error occurs when a contact in your mailbox is corrupt.  <br/> |
|ErrorInvalidIdStoreObjectIdTooLong  <br/> |This error occurs when the caller specifies an **Id** attribute that is too long.  <br/> |
|ErrorInvalidIdTooManyAttachmentLevels  <br/> |This error is returned when the attachment hierarchy on an item exceeds the maximum of 255 levels deep.  <br/> |
|ErrorInvalidIdXml  <br/> |This response code is not used.  <br/> |
|ErrorInvalidImContactId  <br/> |This error is returned when the specified IM contact identifier does not represent a valid identifier. This error was introduced in Exchange 2013.  <br/> |
|ErrorInvalidImDistributionGroupSmtpAddress  <br/> |This error is returned when the specified IM distribution group SMTP address identifier does not represent a valid identifier. This error was introduced in Exchange 2013.  <br/> |
|ErrorInvalidImGroupId  <br/> |This error is returned when the specified IM group identifier does not represent a valid identifier. This error was introduced in Exchange 2013.  <br/> |
|ErrorInvalidIndexedPagingParameters  <br/> |This error occurs if the offset for indexed paging is negative.  <br/> |
|ErrorInvalidInternetHeaderChildNodes  <br/> |This response code is not used.  <br/> |
|ErrorInvalidItemForOperationArchiveItem  <br/> |Indicates that the item was invalid for an **ArchiveItem** operation.  <br/> |
|ErrorInvalidItemForOperationAcceptItem  <br/> |This error occurs when an attempt is made to use an AcceptItem response object for an item type other than a meeting request or a calendar item, or when an attempt is made to accept a calendar item occurrence that is in the Deleted Items folder.  <br/> |
|ErrorInvalidItemForOperationCancelItem  <br/> |This error occurs when an attempt is made to use a CancelItem response object on an item type other than a calendar item.  <br/> |
|ErrorInvalidItemForOperationCreateItemAttachment  <br/> | This error is returned when an attempt is made to create an item attachment of an unsupported type.  <br/><br/>  Supported item types for item attachments include the following objects:  <br/><br/>- [Item](item.md) <br/>- [Message](message-ex15websvcsotherref.md) <br/>- [CalendarItem](calendaritem.md) <br/>- [Task](task.md) <br/>- [Contact](contact.md) <br/> <br/> For example, if you try to create a [MeetingMessage](meetingmessage.md) attachment, you will encounter this response code.  <br/> |
|ErrorInvalidItemForOperationCreateItem  <br/> | This error is returned from a [CreateItem operation](createitem-operation.md) if the request contains an unsupported item type. <br/><br/>Supported items include the following objects:<br/>  <br/>- [Item](item.md) <br/>- [Message](message-ex15websvcsotherref.md) <br/>- [CalendarItem](calendaritem.md) <br/>- [Task](task.md) <br/>- [Contact](contact.md) <br/><br/>  Certain types are created as a side effect of doing something else. Meeting messages, for example, are created when you send a calendar item to attendees; they are not explicitly created.  <br/> |
|ErrorInvalidItemForOperationDeclineItem  <br/> |This error occurs when an attempt is made to use a DeclineItem response object for an item type other than a meeting request or a calendar item, or when an attempt is made to decline a calendar item occurrence that is in the Deleted Items folder.  <br/> |
|ErrorInvalidItemForOperationExpandDL  <br/> |This error indicates that the [ExpandDL operation](expanddl-operation.md) is valid only for private distribution lists.  <br/> |
|ErrorInvalidItemForOperationRemoveItem  <br/> |This error is returned from a RemoveItem response object if the request specifies an item that is not a meeting cancellation item.  <br/> |
|ErrorInvalidItemForOperationSendItem  <br/> |This error is returned from a [SendItem operation](senditem-operation.md) if the request specifies an item that is not a message item.  <br/> |
|ErrorInvalidItemForOperationTentative  <br/> |This error occurs when an attempt is made to use [TentativelyAcceptItem](tentativelyacceptitem.md) for an item type other than a meeting request or a calendar item, or when an attempt is made to tentatively accept a calendar item occurrence that is in the Deleted Items folder.  <br/> |
|ErrorInvalidLogonType  <br/> |This error is for internal use only. This error is not returned.  <br/> |
|ErrorInvalidMailbox  <br/> |This error indicates that the [CreateItem operation](createitem-operation.md) or the [UpdateItem operation](updateitem-operation.md) failed while creating or updating a personal distribution list.  <br/> |
|ErrorInvalidManagedFolderProperty  <br/> |This error occurs when the structure of the managed folder is corrupted and cannot be rendered.  <br/> |
|ErrorInvalidManagedFolderQuota  <br/> |This error occurs when the quota that is set on the managed folder is less than zero, which indicates a corrupted managed folder.  <br/> |
|ErrorInvalidManagedFolderSize  <br/> |This error occurs when the size that is set on the managed folder is less than zero, which indicates a corrupted managed folder.  <br/> |
|ErrorInvalidMergedFreeBusyInterval  <br/> |This error occurs when the supplied merged free/busy internal value is invalid. The default minimum value is 5 minutes. The default maximum value is 1440 minutes.  <br/> |
|ErrorInvalidNameForNameResolution  <br/> |This error occurs when the name is invalid for the [ResolveNames operation](resolvenames-operation.md). For example, a zero length string, a single space, a comma, and a dash are all invalid names.  <br/> |
|ErrorInvalidNetworkServiceContext  <br/> |This error indicates an error in the Network Service account on the Client Access server.  <br/> |
|ErrorInvalidOofParameter  <br/> |This response code is not used.  <br/> |
|ErrorInvalidOperation  <br/> | This is a general error that is used when the requested operation is invalid. <br/><br/>For example, you cannot do the following: <br/> <br/>-  Perform a "Deep" traversal by using the [FindFolder operation](findfolder-operation.md) on a public folder.  <br/>-  Move or copy the public folder root.  <br/>-  Delete an associated item by using any mode except "Hard" delete.  <br/>-  Move or copy an associated item.  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |This error indicates that a caller requested free/busy information for a user in another organization but the organizational relationship does not have free/busy enabled.  <br/> |
|ErrorInvalidPagingMaxRows  <br/> |This error occurs when a consumer passes in a zero or a negative value for the maximum rows to be returned.  <br/> |
|ErrorInvalidParentFolder  <br/> |This error occurs when a consumer passes in an invalid parent folder for an operation. For example, this error is returned if you try to create a folder within a search folder.  <br/> |
|ErrorInvalidPercentCompleteValue  <br/> |This error is returned when an attempt is made to set a task completion percentage to an invalid value. The value must be between 0 and 100 (inclusive).  <br/> |
|ErrorInvalidPermissionSettings  <br/> |This error indicates that the permission level is inconsistent with the permission settings.  <br/> |
|ErrorInvalidPhoneCallId  <br/> |This error indicates that the caller identifier is not valid.  <br/> |
|ErrorInvalidPhoneNumber  <br/> |This error indicates that the telephone number is not correct or does not fit the dial plan rules.  <br/> |
|ErrorInvalidPropertyAppend  <br/> | This error occurs when the property that you are trying to append to does not support appending. <br/><br/>The following are the only properties that support appending: <br/> <br/>-  Recipient collections (ToRecipients, CcRecipients, BccRecipients)  <br/>-  Attendee collections (RequiredAttendees, OptionalAttendees, Resources)  <br/>-  Body  <br/>-  ReplyTo  <br/><br/>  In addition, this error occurs when a message body is appended if the format specified in the request does not match the format of the item in the store.  <br/> |
|ErrorInvalidPropertyDelete  <br/> |This error occurs if the delete operation is specified in an [UpdateItem operation](updateitem-operation.md) or [UpdateFolder operation](updatefolder-operation.md) call for a property that does not support the delete operation. For example, you cannot delete the [ItemId](itemid.md) element of the [Item](item.md) object.  <br/> |
|ErrorInvalidPropertyForExists  <br/> |This error occurs if the consumer passes in one of the flag properties in an [Exists](exists.md) filter. For example, this error occurs if the [IsRead](isread.md) or [IsFromMe](isfromme.md) flags are specified in the [Exists](exists.md) element. The request should use the [IsEqualTo](isequalto.md) element instead for these as they are flags and therefore part of a single property.  <br/> |
|ErrorInvalidPropertyForOperation  <br/> |This error occurs when the property that you are trying to manipulate does not support the operation that is being performed on it.  <br/> |
|ErrorInvalidPropertyRequest  <br/> | This error occurs if a property that is specified in the request is not available for the item type. For example, this error is returned if a property that is only available on calendar items is requested in a [GetItem operation](getitem-operation.md) call for a message or is updated in an [UpdateItem operation](updateitem-operation.md) call for a message. <br/> <br/>  This occurs in the following operations: <br/> <br/>- [GetItem operation](getitem-operation.md) <br/>- [GetFolder operation](getfolder-operation.md) <br/>- [UpdateItem operation](updateitem-operation.md) <br/>- [UpdateFolder operation](updatefolder-operation.md) <br/> |
|ErrorInvalidPropertySet  <br/> |This error indicates that the property that you are trying to manipulate does not support the operation that is being performed on it. For example, this error is returned if the property that you are trying to set is read-only.  <br/> |
|ErrorInvalidPropertyUpdateSentMessage  <br/> | This error occurs during an [UpdateItem operation](updateitem-operation.md) when a client tries to update certain properties of a message that has already been sent.<br/><br/> For example, the following properties cannot be updated on a sent message: <br/> <br/>- [IsReadReceiptRequested](isreadreceiptrequested.md) <br/>- [IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |
|ErrorInvalidProxySecurityContext  <br/> |This response code is not used.  <br/> |
|ErrorInvalidPullSubscriptionId  <br/> |This error occurs if you call the [GetEvents operation](getevents-operation.md) or the [Unsubscribe operation](unsubscribe-operation.md) by using a push subscription ID. To unsubscribe from a push subscription, you must respond to a push request with an unsubscribe response, or disconnect your Web service and wait for the push notifications to time out.  <br/> |
|ErrorInvalidPushSubscriptionUrl  <br/> | This error is returned by the [Subscribe operation](subscribe-operation.md) when it creates a "push" subscription and indicates that the URL that is included in the request is invalid.<br/><br/>The following conditions must be met for Exchange Web Services to accept the URL: <br/> <br/>-  String length \> 0 and \< 2083.  <br/>-  Protocol is http or https.  <br/>-  The URL can be parsed by the URI Microsoft .NET Framework class.  <br/> |
|ErrorInvalidRecipients  <br/> |This error indicates that the recipient collection on your message or the attendee collection on your calendar item is invalid. For example, this error will be returned when an attempt is made to send an item that has no recipients.  <br/> |
|ErrorInvalidRecipientSubfilter  <br/> |This error indicates that the search folder has a recipient table filter that Exchange Web Services cannot represent. To get around this error, retrieve the folder without requesting the search parameters.  <br/> |
|ErrorInvalidRecipientSubfilterComparison  <br/> |This error indicates that the search folder has a recipient table filter that Exchange Web Services cannot represent. To get around this error, retrieve the folder without requesting the search parameters.  <br/> |
|ErrorInvalidRecipientSubfilterOrder  <br/> |This error indicates that the search folder has a recipient table filter that Exchange Web Services cannot represent. To get around this error, retrieve the folder without requesting the search parameters.  <br/> |
|ErrorInvalidRecipientSubfilterTextFilter  <br/> |This error indicates that the search folder has a recipient table filter that Exchange Web Services cannot represent. To get around this error, retrieve the folder without requesting the search parameters.  <br/> |
|ErrorInvalidReferenceItem  <br/> | This error is returned from the [CreateItem operation](createitem-operation.md) for Forward and Reply response objects in the following scenarios:<br/>  <br/>-  The referenced item identifier is not a [Message](message-ex15websvcsotherref.md), a [CalendarItem](calendaritem.md), or a descendant of a **Message** or **CalendarItem**.  <br/>-  The reference item identifier is for a **CalendarItem** and the organizer is trying to Reply or ReplyAll to himself.  <br/>-  The message is a draft and Reply or ReplyAll is selected.  <br/>-  The reference item, for [SuppressReadReceipt](suppressreadreceipt.md), is not a **Message** or a descendant of a **Message**.  <br/> |
|ErrorInvalidRequest  <br/> |This error occurs when the SOAP request has a SOAP action header, but nothing in the SOAP body. Note that the SOAP Action header is not required as Exchange Web Services can determine the method to call from the local name of the root element in the SOAP body.  <br/> |
|ErrorInvalidRestriction  <br/> |This response code is not used.  <br/> |
|ErrorInvalidRetentionTagTypeMismatch  <br/> |This error is returned when the specified retention tag has an incorrect action associated with it. This error was introduced in Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagInvisible  <br/> |This error is returned when an attempt is made to set a nonexistent or invisible tag on a **PolicyTag** property. This error was introduced in Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagInheritance  <br/> |This error is returned when an attempt is made to set an implicit tag on the **PolicyTag** property. This error was introduced in Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagIdGuid  <br/> |Indicates that the retention tag GUID was invalid.  <br/> |
|ErrorInvalidRoutingType  <br/> |This error occurs if the routing type that is passed for a [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) element is invalid. Typically, the routing type is set to Simple Mail Transfer Protocol (SMTP).  <br/> |
|ErrorInvalidScheduledOofDuration  <br/> |This error occurs if the specified duration end time is not greater than the start time, or if the end time does not occur in the future.  <br/> |
|ErrorInvalidSchemaVersionForMailboxVersion  <br/> |This error indicates that a proxy request that was sent to another server is not able to service the request due to a versioning mismatch.  <br/> |
|ErrorInvalidSecurityDescriptor  <br/> |This error indicates that the Exchange security descriptor on the Calendar folder in the store is corrupted.  <br/> |
|ErrorInvalidSendItemSaveSettings  <br/> |This error occurs during an attempt to send an item where the [SavedItemFolderId](saveditemfolderid.md) is specified in the request but the **SaveItemToFolder** property is set to **false**.  <br/> |
|ErrorInvalidSerializedAccessToken  <br/> |This error indicates that the token that was passed in the header is malformed, does not refer to a valid account in the directory, or is missing the primary group **ConnectingSID**.  <br/> |
|ErrorInvalidSharingData  <br/> |This error indicates that the sharing metadata is not valid. This can be caused by invalid XML.  <br/> |
|ErrorInvalidSharingMessage  <br/> |This error indicates that the sharing message is not valid. This can be caused by a missing property.  <br/> |
|ErrorInvalidSid  <br/> |This error occurs when an invalid SID is passed in a request.  <br/> |
|ErrorInvalidSIPUri  <br/> |This error indicates that the SIP name, dial plan, or the phone number are invalid SIP URIs.  <br/> |
|ErrorInvalidServerVersion  <br/> |This error indicates that an invalid request server version was specified in the request.  <br/> |
|ErrorInvalidSmtpAddress  <br/> |This error occurs when the SMTP address cannot be parsed.  <br/> |
|ErrorInvalidSubfilterType  <br/> |This response code is not used.  <br/> |
|ErrorInvalidSubfilterTypeNotAttendeeType  <br/> |This response code is not used.  <br/> |
|ErrorInvalidSubfilterTypeNotRecipientType  <br/> |This response code is not used.  <br/> |
|ErrorInvalidSubscription  <br/> |This error indicates that the subscription is no longer valid. This could be because the Client Access server is restarting or because the subscription is expired.  <br/> |
|ErrorInvalidSubscriptionRequest  <br/> |This error indicates that the subscribe request included multiple public folder IDs. A subscription can include multiple folders from the same mailbox or one public folder ID.  <br/> |
|ErrorInvalidSyncStateData  <br/> |This error is returned by [SyncFolderItems](syncfolderitems.md) or [SyncFolderHierarchy](syncfolderhierarchy.md) if the [SyncState](syncstate-ex15websvcsotherref.md) data that is passed is invalid. To fix this error, you must resynchronize without the sync state. Make sure that if you are persisting sync state BLOBs, you are not accidentally truncating the BLOB.  <br/> |
|ErrorInvalidTimeInterval  <br/> |This error indicates that the specified time interval is invalid. The start time must be greater than or equal to the end time.  <br/> |
|ErrorInvalidUserInfo  <br/> |This error indicates that an internally inconsistent [UserId](userid.md) was specified for a permissions operation. For example, if a distinguished user ID is specified (Default or Anonymous), this error is returned if you also try to specify a SID, or primary SMTP address or display name for this user.  <br/> |
|ErrorInvalidUserOofSettings  <br/> |This error indicates that the user Out of Office (OOF) settings are invalid because of a missing internal or external reply.  <br/> |
|ErrorInvalidUserPrincipalName  <br/> |This error occurs during Exchange Impersonation. The caller passed in an invalid UPN in the SOAP header that was not accessible in the directory.  <br/> |
|ErrorInvalidUserSid  <br/> |This error occurs when an invalid SID is passed in a request.  <br/> |
|ErrorInvalidUserSidMissingUPN  <br/> |This response code is not used.  <br/> |
|ErrorInvalidValueForProperty  <br/> |This error indicates that the comparison value in the restriction is invalid for the property you are comparing against.<br/><br/> For example, the comparison value of [DateTimeCreated](datetimecreated.md) > **true** would return this response code. <br/><br/>This response code is also returned if you specify an enumeration property in the comparison, but the value that you are comparing against is not a valid value for that enumeration.  <br/> |
|ErrorInvalidWatermark  <br/> |This error is caused by an invalid watermark.  <br/> |
|ErrorIPGatewayNotFound  <br/> |This error indicates that a valid VoIP gateway is not available.  <br/> |
|ErrorIrresolvableConflict  <br/> |This error indicates that conflict resolution was unable to resolve changes for the properties. The items in the store may have been changed and have to be updated. Retrieve the updated change key and try again.  <br/> |
|ErrorItemCorrupt  <br/> |This error indicates that the state of the object is corrupted and cannot be retrieved. When you are retrieving an item, only certain elements will be in this state, such as [Body](body.md) and [MimeContent](mimecontent.md). Omit these elements and retry the operation.  <br/> |
|ErrorItemNotFound  <br/> |This error occurs when the item was not found or you do not have permission to access the item.  <br/> |
|ErrorItemPropertyRequestFailed  <br/> |This error occurs if a property request on an item fails. The property may exist, but it could not be retrieved.  <br/> |
|ErrorItemSave  <br/> |This error occurs when attempts to save the item or folder fail.  <br/> |
|ErrorItemSavePropertyError  <br/> |This error occurs when attempts to save the item or folder fail because of invalid property values. The response code includes the path of the invalid properties.  <br/> |
|ErrorLegacyMailboxFreeBusyViewTypeNotMerged  <br/> |This response code is not used.  <br/> |
|ErrorLocalServerObjectNotFound  <br/> |This response code is not used.  <br/> |
|ErrorLogonAsNetworkServiceFailed  <br/> |This error indicates that the Availability service was unable to log on as the network service to proxy requests to the appropriate sites or forests. This response typically indicates a configuration error.  <br/> |
|ErrorMailboxConfiguration  <br/> |This error indicates that the mailbox information in AD DS is configured incorrectly.  <br/> |
|ErrorMailboxDataArrayEmpty  <br/> |This error indicates that the [MailboxDataArray](mailboxdataarray.md) element in the request is empty. You must supply at least one mailbox identifier.  <br/> |
|ErrorMailboxDataArrayTooBig  <br/> |This error occurs when more than 100 entries are supplied in a [MailboxDataArray](mailboxdataarray.md) element..  <br/> |
|ErrorMailboxFailover  <br/> |This error indicates that an attempt to access a mailbox failed because the mailbox is in a failover process.  <br/> |
|ErrorMailboxHoldNotFound  <br/> |Indicates that the mailbox hold was not found.  <br/> |
|ErrorMailboxLogonFailed  <br/> |This error occurs when the connection to the mailbox to get the calendar view information failed.  <br/> |
|ErrorMailboxMoveInProgress  <br/> | This error indicates that the mailbox is being moved to a different mailbox store or server. This error can also indicate that the mailbox is on another server or mailbox database.  <br/> |
|ErrorMailboxStoreUnavailable  <br/> | This error indicates that one of the following error conditions occurred:  <br/><br/>-  The mailbox store is corrupt.  <br/>-  The mailbox store is being stopped.  <br/>-  The mailbox store is offline.  <br/>-  A network error occurred when an attempt was made to access the mailbox store.  <br/>-  The mailbox store is overloaded and cannot accept any more connections.  <br/>-  The mailbox store has been paused.  <br/> |
|ErrorMailRecipientNotFound  <br/> |This error occurs if the [MailboxData](mailboxdata.md) element information cannot be mapped to a valid mailbox account.  <br/> |
|ErrorMailTipsDisabled  <br/> |This error indicates that mail tips are disabled.  <br/> |
|ErrorManagedFolderAlreadyExists  <br/> |This error occurs if the managed folder that you are trying to create already exists in a mailbox.  <br/> |
|ErrorManagedFolderNotFound  <br/> |This error occurs when the folder name that was specified in the request does not map to a managed folder definition in AD DS. You can only create instances of managed folders for folders that are defined in AD DS. Check the name and try again.  <br/> |
|ErrorManagedFoldersRootFailure  <br/> |This error indicates that the managed folders root was deleted from the mailbox or that a folder exists in the same parent folder that has the name of the managed folder root. This will also occur if the attempt to create the root managed folder fails.  <br/> |
|ErrorMeetingSuggestionGenerationFailed  <br/> |This error indicates that the suggestions engine encountered a problem when it was trying to generate the suggestions.  <br/> |
|ErrorMessageDispositionRequired  <br/> | This error occurs if the **MessageDisposition** attribute is not set.<br/><br/> This attribute is required for the following: <br/> <br/>-  The [CreateItem operation](createitem-operation.md) and the [UpdateItem operation](updateitem-operation.md) when the item being created or updated is a [Message](message-ex15websvcsotherref.md).  <br/>- [CancelCalendarItem](cancelcalendaritem.md), [AcceptItem](acceptitem.md), [DeclineItem](declineitem.md), or [TentativelyAcceptItem](tentativelyacceptitem.md) response objects.  <br/> |
|ErrorMessageSizeExceeded  <br/> |This error indicates that the message that you are trying to send exceeds the allowed limits.  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |This error indicates that the given domain cannot be found.  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |This error indicates that the message tracking service cannot track the message.  <br/> |
| ErrorMessageTrackingTransientError  <br/> |This error indicates that the message tracking service is either down or busy. This error code indicates a transient error. Clients can retry to connect to the server when this error is received.  <br/> |
|ErrorMimeContentConversionFailed  <br/> |This error occurs when the MIME content is not a valid iCal for a [CreateItem operation](createitem-operation.md). For a [GetItem operation](getitem-operation.md), this response indicates that the MIME content could not be generated.  <br/> |
|ErrorMimeContentInvalid  <br/> |This error occurs when the MIME content is invalid.  <br/> |
|ErrorMimeContentInvalidBase64String  <br/> |This error occurs when the MIME content in the request is not a valid base 64 string.  <br/> |
|ErrorMissingArgument  <br/> |This error indicates that a required argument was missing from the request. The response message text indicates which argument to check.  <br/> |
|ErrorMissingEmailAddress  <br/> |This error indicates that you specified a distinguished folder ID in the request, but the account that made the request does not have a mailbox on the system. In that case, you must supply a [Mailbox](mailbox.md) sub-element under [DistinguishedFolderId](distinguishedfolderid.md).  <br/> |
|ErrorMissingEmailAddressForManagedFolder  <br/> |This error indicates that you specified a distinguished folder ID in the request, but the account that made the request does not have a mailbox on the system. In that case, you must supply a [Mailbox](mailbox.md) sub-element under [DistinguishedFolderId](distinguishedfolderid.md). This response is returned from the [CreateManagedFolder operation](createmanagedfolder-operation.md).  <br/> |
|ErrorMissingInformationEmailAddress  <br/> |This error occurs if the [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element is missing.  <br/> |
|ErrorMissingInformationReferenceItemId  <br/> |This error occurs if the [ReferenceItemId](referenceitemid.md) is missing.  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |This error code is never returned.  <br/> |
|ErrorMissingItemForCreateItemAttachment  <br/> |This error is returned when an attempt is made to not include the item element in the **ItemAttachment** element of a [CreateAttachment operation](createattachment-operation.md) request.  <br/> |
|ErrorMissingManagedFolderId  <br/> |This error occurs when the policy IDs property, property tag 0x6732, for the folder is missing. You should consider this a corrupted folder.  <br/> |
|ErrorMissingRecipients  <br/> |This error indicates that you tried to send an item without including recipients. Note that if you call the [CreateItem operation](createitem-operation.md) with a message disposition that causes the message to be sent, you will get the following response code: **ErrorInvalidRecipients**.  <br/> |
|ErrorMissingUserIdInformation  <br/> |This error indicates that a [UserId](userid.md) has not been fully specified in a permissions set.  <br/> |
|ErrorMoreThanOneAccessModeSpecified  <br/> |This error indicates that you have specified more than one [ExchangeImpersonation](exchangeimpersonation.md) element value within a request.  <br/> |
|ErrorMoveCopyFailed  <br/> |This error indicates that the move or copy operation failed. Moving occurs in the [CreateItem operation](createitem-operation.md) when you accept a meeting request that is in the Deleted Items folder. In addition, if you decline a meeting request, cancel a calendar item, or remove a meeting from your calendar, it is moved to the Deleted Items folder.  <br/> |
|ErrorMoveDistinguishedFolder  <br/> |This error occurs if you try to move a distinguished folder.  <br/> |
|ErrorMultiLegacyMailboxAccess  <br/> |This error occurs when a request attempts to access multiple mailbox servers. This error was introduced in Exchange 2013.  <br/> |
|ErrorNameResolutionMultipleResults  <br/> |This error occurs if the [ResolveNames operation](resolvenames-operation.md) returns more than one result or the ambiguous name that you specified matches more than one object in the directory. The response code includes the matched names in the response data.  <br/> |
|ErrorNameResolutionNoMailbox  <br/> |This error indicates that the caller does not have a mailbox on the system. The [ResolveNames operation](resolvenames-operation.md) or [ExpandDL operation](expanddl-operation.md) is invalid for connecting a user without a mailbox.  <br/> |
|ErrorNameResolutionNoResults  <br/> |This error indicates that the [ResolveNames operation](resolvenames-operation.md) returns no results.  <br/> |
|ErrorNoApplicableProxyCASServersAvailable  <br/> |This error code MUST be returned when the Web service cannot find a server to handle the request.  <br/> |
|ErrorNoCalendar  <br/> |This error occurs if there is no Calendar folder for the mailbox.  <br/> |
|ErrorNoDestinationCASDueToKerberosRequirements  <br/> |This error indicates that the request referred to a mailbox in another Active Directory site, but no Client Access servers in the destination site were configured for Windows Authentication, and therefore the request could not be proxied.  <br/> |
|ErrorNoDestinationCASDueToSSLRequirements  <br/> |This error indicates that the request referred to a mailbox in another Active Directory site, but no Client Access servers in the destination site were configured for SSL connections, and therefore the request could not be proxied.  <br/> |
|ErrorNoDestinationCASDueToVersionMismatch  <br/> |This error indicates that the request referred to a mailbox in another Active Directory site, but no Client Access servers in the destination site were of an acceptable product version to receive the request, and therefore the request could not be proxied.  <br/> |
|ErrorNoFolderClassOverride  <br/> |This error occurs if you set the [FolderClass](folderclass.md) element when you are creating an item other than a generic folder. For typed folders such as [CalendarFolder](calendarfolder.md) and [TasksFolder](tasksfolder.md), the folder class is implied. Setting the folder class to a different folder type by using the [UpdateFolder operation](updatefolder-operation.md) results in the **ErrorObjectTypeChanged** response. Instead, use a generic folder type but set the folder class to the value that you require. Exchange Web Services will create the correct strongly typed folder.  <br/> |
|ErrorNoFreeBusyAccess  <br/> |This error indicates that the caller does not have free/busy viewing rights on the Calendar folder in question.  <br/> |
|ErrorNonExistentMailbox  <br/> | This error occurs in the following scenarios: <br/> <br/>-  The e-mail address is empty in [CreateManagedFolder](createmanagedfolder.md).  <br/>-  The e-mail address does not refer to a valid account in a request that takes an e-mail address in the body or in the SOAP header, such as in an Exchange Impersonation call.  <br/> |
|ErrorNonPrimarySmtpAddress  <br/> |This error occurs when a caller passes in a non-primary SMTP address. The response includes the correct SMTP address to use.  <br/> |
|ErrorNoPropertyTagForCustomProperties  <br/> |This error indicates that MAPI properties in the custom range, 0x8000 and greater, cannot be referenced by property tags. You must use the EWS Managed API [PropertySetId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition.propertysetid%28v=exchg.80%29.aspx)property or the EWS [ExtendedFieldURI](extendedfielduri.md) element with the PropertySetId attribute.  <br/> |
|ErrorNoPublicFolderReplicaAvailable  <br/> |This response code is not used.  <br/> |
|ErrorNoPublicFolderServerAvailable  <br/> |This error code MUST be returned if no public folder server is available or if the caller does not have a home public server.  <br/> |
|ErrorNoRespondingCASInDestinationSite  <br/> |This error indicates that the request referred to a mailbox in another Active Directory site, but none of the Client Access servers in that site responded, and therefore the request could not be proxied.  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |This error indicates that the caller tried to grant permissions in its calendar or contacts folder to a user in another organization, and the attempt failed.  <br/> |
|ErrorNotDelegate  <br/> |This error indicates that the user is not a delegate for the mailbox. It is returned by the [GetDelegate operation](getdelegate-operation.md), the [RemoveDelegate operation](removedelegate-operation.md), and the [UpdateDelegate operation](updatedelegate-operation.md) when the specified delegate user is not found in the list of delegates.  <br/> |
|ErrorNotEnoughMemory  <br/> |This error indicates that the operation could not be completed because of insufficient memory.  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |This error indicates that the sharing message is not supported.  <br/> |
|ErrorObjectTypeChanged  <br/> |This error occurs if the object type changed.  <br/> |
|ErrorOccurrenceCrossingBoundary  <br/> |This error occurs when the [Start](start.md) or [End ](end-ex15websvcsotherref.md) time of an occurrence is updated so that the occurrence is scheduled to happen earlier or later than the corresponding previous or next occurrence.  <br/> |
|ErrorOccurrenceTimeSpanTooBig  <br/> |This error indicates that the time allotment for a given occurrence overlaps with another occurrence of the same recurring item. This response also occurs when the length in minutes of a given occurrence is larger than Int32.MaxValue.  <br/> |
|ErrorOperationNotAllowedWithPublicFolderRoot  <br/> |This error indicates that the current operation is not valid for the public folder root.  <br/> |
|ErrorOrganizationNotFederated  <br/> |This error indicates that the requester's organization is not federated so the requester cannot create sharing messages to send to an external user or cannot accept sharing messages received from an external user.  <br/> |
|ErrorParentFolderIdRequired  <br/> |This response code is not used.  <br/> |
|ErrorParentFolderNotFound  <br/> |This error occurs in the [CreateFolder operation](createfolder-operation.md) when the parent folder is not found.  <br/> |
|ErrorPasswordChangeRequired  <br/> |This error indicates that you must change your password before you can access this mailbox. This occurs when a new account has been created and the administrator indicated that the user must change the password at first logon. You cannot update the password by using Exchange Web Services. You must use a tool such as Microsoft Office Outlook Web App to change your password.  <br/> |
|ErrorPasswordExpired  <br/> |This error indicates that the password has expired. You cannot change the password by using Exchange Web Services. You must use a tool such as Outlook Web App to change your password.  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |This error indicates that the requester tried to grant permissions in its calendar or contacts folder to an external user but the sharing policy assigned to the requester indicates that the requested permission level is higher than what the sharing policy allows.  <br/> |
|ErrorPhoneNumberNotDialable  <br/> |This error indicates that the telephone number was not in the correct form.  <br/> |
|ErrorPropertyUpdate  <br/> |This error indicates that the update failed because of invalid property values. The response message includes the invalid property paths.  <br/> |
|ErrorPromptPublishingOperationFailed  <br/> |This error is intended for internal use only. This error was introduced in Exchange 2013.  <br/> |
|ErrorPropertyValidationFailure  <br/> |This response code is not used.  <br/> |
|ErrorProxiedSubscriptionCallFailure  <br/> |This error indicates that the request referred to a subscription that exists on another Client Access server, but an attempt to proxy the request to that Client Access server failed.  <br/> |
|ErrorProxyCallFailed  <br/> |This response code is not used.  <br/> |
|ErrorProxyGroupSidLimitExceeded  <br/> |This error indicates that the request referred to a mailbox in another Active Directory site, and the original caller is a member of more than 3,000 groups.  <br/> |
|ErrorProxyRequestNotAllowed  <br/> |This error indicates that the request that Exchange Web Services sent to another Client Access server when trying to fulfill a [GetUserAvailabilityRequest](getuseravailabilityrequest.md) request was invalid. This response code typically indicates that a configuration or rights error has occurred, or that someone tried unsuccessfully to mimic an availability proxy request.  <br/> |
|ErrorProxyRequestProcessingFailed  <br/> |This error indicates that Exchange Web Services tried to proxy an availability request to another Client Access server for fulfillment, but the request failed. This response can be caused by network connectivity issues or request timeout issues.  <br/> |
|ErrorProxyServiceDiscoveryFailed  <br/> |This error code must be returned if the Web service cannot determine whether the request is to run on the target server or will be proxied to another server.  <br/> |
|ErrorProxyTokenExpired  <br/> |This response code is not used.  <br/> |
|ErrorPublicFolderMailboxDiscoveryFailed  <br/> |This error occurs when the public folder mailbox URL cannot be found. This error is intended for internal use only. This error was introduced in Exchange 2013.  <br/> |
|ErrorPublicFolderOperationFailed  <br/> |This error occurs when an attempt is made to access a public folder and the attempt is unsuccessful. This error was introduced in Exchange 2013Exchange Server 2013.  <br/> |
|ErrorPublicFolderRequestProcessingFailed  <br/> |This error occurs when the recipient that was passed to the [GetUserAvailability operation](getuseravailability-operation.md) is located on a computer that is running a version of Exchange Server that is earlier than Exchange 2007, and the request to retrieve free/busy information for the recipient from the public folder server failed.  <br/> |
|ErrorPublicFolderServerNotFound  <br/> |This error occurs when the recipient that was passed to the [GetUserAvailability operation](getuseravailability-operation.md) is located on a computer that is running a version of Exchange Server that is earlier than Exchange 2007, and the request to retrieve free/busy information for the recipient from the public folder server failed because the organizational unit did not have an associated public folder server.  <br/> |
|ErrorPublicFolderSyncException  <br/> |This error occurs when a synchronization operation succeeds against the primary public folder mailbox but does not succeed against the secondary public folder mailbox. This error was introduced in Exchange 2013.  <br/> |
|ErrorQueryFilterTooLong  <br/> |This error indicates that the search folder restriction may be valid, but it is not supported by EWS. Exchange Web Services limits restrictions to contain a maximum of 255 filter expressions. If you try to bind to an existing search folder that exceeds 255, this response code is returned.  <br/> |
|ErrorQuotaExceeded  <br/> |This error occurs when the mailbox quota is exceeded.  <br/> |
|ErrorReadEventsFailed  <br/> |This error is returned by the [GetEvents operation](getevents-operation.md) or push notifications when a failure occurs while retrieving event information. When this error is returned, the subscription is deleted. Re-create the event synchronization based on a last known watermark.  <br/> |
|ErrorReadReceiptNotPending  <br/> |This error is returned by the [CreateItem operation](createitem-operation.md) if an attempt was made to suppress a read receipt when the message sender did not request a read receipt on the message or if the message is in the Junk E-mail folder.  <br/> |
|ErrorRecurrenceEndDateTooBig  <br/> |This error occurs when the end date for the recurrence is after 9/1/4500.  <br/> |
|ErrorRecurrenceHasNoOccurrence  <br/> |This error occurs when the specified recurrence does not have any occurrence instances in the specified range.  <br/> |
|ErrorRemoveDelegatesFailed  <br/> |This error indicates that the delegate list failed to be saved after delegates were removed.  <br/> |
|ErrorRequestAborted  <br/> |This response code is not used.  <br/> |
|ErrorRequestStreamTooBig  <br/> | This error occurs when the request stream is larger than 400 KB.  <br/> |
|ErrorRequiredPropertyMissing  <br/> |This error is returned when a required property is missing in a [CreateAttachment operation](createattachment-operation.md) request. The missing property URI is included in the response.  <br/> |
|ErrorResolveNamesInvalidFolderType  <br/> |This error indicates that the caller has specified a folder that is not a contacts folder to the [ResolveNames operation](resolvenames-operation.md).  <br/> |
|ErrorResolveNamesOnlyOneContactsFolderAllowed  <br/> |This error indicates that the caller has specified more than one contacts folder to the [ResolveNames operation](resolvenames-operation.md).  <br/> |
|ErrorResponseSchemaValidation  <br/> |This response code is not used.  <br/> |
|ErrorRestrictionTooLong  <br/> |This error occurs if the restriction contains more than 255 nodes.  <br/> |
|ErrorRestrictionTooComplex  <br/> |This error occurs when the restriction cannot be evaluated by Exchange Web Services.  <br/> |
|ErrorResultSetTooBig  <br/> |This error indicates that the number of calendar entries for a given recipient exceeds the allowed limit of 1000. Reduce the window and try again.  <br/> |
|ErrorSavedItemFolderNotFound  <br/> |This error occurs when the [SavedItemFolderId](saveditemfolderid.md) is not found.  <br/> |
|ErrorSchemaValidation  <br/> | This error occurs when the request cannot be validated against the schema.  <br/> |
|ErrorSearchFolderNotInitialized  <br/> |This error indicates that the search folder was created, but the search criteria were never set on the folder. This only occurs when you access corrupted search folders that were created by using another API or client. To fix this error, use the [UpdateFolder operation](updatefolder-operation.md) to set the [SearchParameters](searchparameters.md) element to include the restriction that should be on the folder.  <br/> |
|ErrorSendAsDenied  <br/> | This error occurs when both of the following conditions occur: <br/> <br/>-  A user has been granted CanActAsOwner permissions but is not granted delegate rights on the principal's mailbox.  <br/>-  The same user tries to create and send an e-mail message in the principal's mailbox by using the SendAndSaveCopy option.<br/>  <br/>  The result is an ErrorSendAsDenied error and the creation of the e-mail message in the principal's Drafts folder.  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |This error is returned by the [DeleteItem operation](deleteitem-operation.md) if the **SendMeetingCancellations** attribute is missing from the request and the item to delete is a calendar item.  <br/> |
|ErrorSendMeetingInvitationsOrCancellationsRequired  <br/> |This error is returned by the [UpdateItem operation](updateitem-operation.md) if the **SendMeetingInvitationsOrCancellations** attribute is missing from the request and the item to update is a calendar item.  <br/> |
|ErrorSendMeetingInvitationsRequired  <br/> |This error is returned by the [CreateItem operation](createitem-operation.md) if the **SendMeetingInvitations** attribute is missing from the request and the item to create is a calendar item.  <br/> |
|ErrorSentMeetingRequestUpdate  <br/> |This error indicates that after the organizer sends a meeting request, the request cannot be updated. To modify the meeting, modify the calendar item, not the meeting request.  <br/> |
|ErrorSentTaskRequestUpdate  <br/> |This error indicates that after the task initiator sends a task request, that request cannot be updated.  <br/> |
|ErrorServerBusy  <br/> |This error occurs when the server is busy.  <br/> |
|ErrorServiceDiscoveryFailed  <br/> |This error indicates that Exchange Web Services tried to proxy a user availability request to the appropriate forest for the recipient, but it could not determine where to send the request because of a service discovery failure.  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |This error indicates that the external URL property has not been set in the Active Directory database.  <br/> |
|ErrorSharingSynchronizationFailed  <br/> |This error indicates that an attempt at synchronizing a sharing folder failed. <br/><br/>This error code is returned when the following occurs:<br/><br/>- The subscription for a sharing folder is not found.<br/>- The sharing folder is not found.<br/>- The corresponding directory user is not found.<br/>- The user no longer exists.<br/>- The appointment is invalid.<br/>- The contact item is invalid.<br/>- There is a communication failure with the remote server.  <br/> |
|ErrorStaleObject  <br/> |This error occurs in an [UpdateItem operation](updateitem-operation.md) or a [SendItem operation](senditem-operation.md) when the change key is not up-to-date or was not supplied. Call the [GetItem operation](getitem-operation.md) to retrieve an updated change key and then try the operation again.  <br/> |
|ErrorSubmissionQuotaExceeded  <br/> |This error Indicates that a user cannot immediately send more requests because the submission quota has been reached.  <br/> |
|ErrorSubscriptionAccessDenied  <br/> |This error occurs when you try to access a subscription by using an account that did not create that subscription. Each subscription can only be accessed by the creator of the subscription.  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |This error indicates that you cannot create a subscription if you are not the owner or do not have owner access to the mailbox.  <br/> |
|ErrorSubscriptionNotFound  <br/> |This error occurs if the subscription that corresponds to the specified [SubscriptionId (GetEvents)](subscriptionid-getevents.md) is not found. The subscription may have expired, the Exchange Web Services process may have been restarted, or an invalid subscription was passed in. If the subscription was valid, re-create the subscription with the latest watermark. This is returned by the [Unsubscribe operation](unsubscribe-operation.md) or the [GetEvents operation](getevents-operation.md) responses.  <br/> |
|ErrorSubscriptionUnsubsribed  <br/> |This error code must be returned when a request is made for a subscription that has been unsubscribed.  <br/> |
|ErrorSyncFolderNotFound  <br/> |This error is returned by the [SyncFolderItems operation](syncfolderitems-operation.md) if the parent folder that is specified cannot be found.  <br/> |
|ErrorTeamMailboxNotFound  <br/> |This error indicates that a team mailbox was not found. This error was introduced in Exchange 2013.  <br/> |
|ErrorTeamMailboxNotLinkedToSharePoint  <br/> |This error indicates that a team mailbox was found but that it is not linked to a SharePoint Server. This error was introduced in Exchange 2013.  <br/> |
|ErrorTeamMailboxUrlValidationFailed  <br/> |This error indicates that a team mailbox was found but that the link to the SharePoint Server is not valid. This error was introduced in Exchange 2013.  <br/> |
|ErrorTeamMailboxNotAuthorizedOwner  <br/> |This error code is not used. This error was introduced in Exchange 2013.  <br/> |
|ErrorTeamMailboxActiveToPendingDelete  <br/> |This error code is not used. This error was introduced in Exchange 2013.  <br/> |
|ErrorTeamMailboxFailedSendingNotifications  <br/> |This error indicates that an attempt to send a notification to the team mailbox owners was unsuccessful. This error was introduced in Exchange 2013.  <br/> |
|ErrorTeamMailboxErrorUnknown  <br/> |This error indicates a general error that can occur when trying to access a team mailbox. Try submitting the request at a later time. This error was introduced in Exchange 2013.  <br/> |
|ErrorTimeIntervalTooBig  <br/> |This error indicates that the time window that was specified is larger than the allowed limit. By default, the allowed limit is 42.  <br/> |
|ErrorTimeoutExpired  <br/> | This error occurs when there is not enough time to complete the processing of the request.  <br/> |
|ErrorTimeZone  <br/> |This error indicates that there is a time zone error.  <br/> |
|ErrorToFolderNotFound  <br/> |This error indicates that the destination folder does not exist.  <br/> |
|ErrorTokenSerializationDenied  <br/> |This error occurs if the caller tries to do a Token serialization request but does not have the ms-Exch-EPI-TokenSerialization right on the Client Access server.  <br/> |
|ErrorTooManyObjectsOpened  <br/> |This error occurs when the internal limit on open objects has been exceeded.  <br/> |
|ErrorUnifiedMessagingDialPlanNotFound  <br/> |This error indicates that a user's dial plan is not available.  <br/> |
|ErrorUnifiedMessagingReportDataNotFound  <br/> |This error is intended for internal use only. This error was introduced in Exchange 2013.  <br/> |
|ErrorUnifiedMessagingPromptNotFound  <br/> |This error is intended for internal use only. This error was introduced in Exchange 2013.  <br/> |
|ErrorUnifiedMessagingRequestFailed  <br/> |This error indicates that the user could not be found.  <br/> |
|ErrorUnifiedMessagingServerNotFound  <br/> |This error indicates that a valid server for the dial plan can be found to handle the request.  <br/> |
|ErrorUnableToGetUserOofSettings  <br/> |This response code is not used.  <br/> |
|ErrorUnableToRemoveImContactFromGroup  <br/> |This error occurs when an unsuccessful attempt is made to remove an IM contact from a group. This error was introduced in Exchange 2013.  <br/> |
|ErrorUnsupportedCulture  <br/> |This error occurs when you try to set the **Culture** property to a value that is not parsable by the **System.Globalization.CultureInfo** class.  <br/> |
|ErrorUnsupportedMapiPropertyType  <br/> |This error occurs when a caller tries to use extended properties of types object, object array, error, or null.  <br/> |
|ErrorUnsupportedMimeConversion  <br/> |This error occurs when you are trying to retrieve or set MIME content for an item other than a [PostItem](postitem.md), [Message](message-ex15websvcsotherref.md), or [CalendarItem](calendaritem.md) object.  <br/> |
|ErrorUnsupportedPathForQuery  <br/> |This error occurs when the caller passes a property that is invalid for a query. This can occur when calculated properties are used.  <br/> |
|ErrorUnsupportedPathForSortGroup  <br/> |This error occurs when the caller passes a property that is invalid for a sort or group by property. This can occur when calculated properties are used.  <br/> |
|ErrorUnsupportedPropertyDefinition  <br/> |This response code is not used.  <br/> |
|ErrorUnsupportedQueryFilter  <br/> |This error indicates that the search folder restriction may be valid, but it is not supported by EWS.  <br/> |
|ErrorUnsupportedRecurrence  <br/> |This error indicates that the specified recurrence is not supported for tasks.  <br/> |
|ErrorUnsupportedSubFilter  <br/> |This response code is not used.  <br/> |
|ErrorUnsupportedTypeForConversion  <br/> |This error indicates that Exchange Web Services found a property type in the store but it cannot generate XML for the property type.  <br/> |
|ErrorUpdateDelegatesFailed  <br/> |This error indicates that the delegate list failed to be saved after delegates were updated.  <br/> |
|ErrorUpdatePropertyMismatch  <br/> |This error occurs when the single property path that is listed in a change description does not match the single property that is being set within the actual [Item](item.md) or [Folder](folder.md) object.  <br/> |
|ErrorUserNotUnifiedMessagingEnabled  <br/> |This error indicates that the requester is not enabled.  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |This error indicates that the requester tried to grant permissions in its calendar or contacts folder to an external user but the sharing policy assigned to the requester indicates that the domain of the external user is not listed in the policy.  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |Indicates that the requester's organization has a set of federated domains but the requester's organization does not have any SMTP proxy addresses with one of the federated domains.  <br/> |
|ErrorValueOutOfRange  <br/> |This error indicates that a calendar view start date or end date was set to 1/1/0001 12:00:00 AM or 12/31/9999 11:59:59 PM.  <br/> |
|ErrorVirusDetected  <br/> |This error indicates that the Exchange store detected a virus in the message.  <br/> |
|ErrorVirusMessageDeleted  <br/> |This error indicates that the Exchange store detected a virus in the message and deleted it.  <br/> |
|ErrorVoiceMailNotImplemented  <br/> |This response code is not used.  <br/> |
|ErrorWebRequestInInvalidState  <br/> |This response code is not used.  <br/> |
|ErrorWin32InteropError  <br/> |This error indicates that there was an internal failure during communication with unmanaged code.  <br/> |
|ErrorWorkingHoursSaveFailed  <br/> |This response code is not used.  <br/> |
|ErrorWorkingHoursXmlMalformed  <br/> |This response code is not used.  <br/> |
|ErrorWrongServerVersion  <br/> |This error indicates that a request can only be made to a server that is the same version as the mailbox server.  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |This error indicates that a request was made by a delegate that has a different server version than the principal's mailbox server.  <br/> |
|ErrorMissingInformationSharingFolderId  <br/> |This error code is never returned.  <br/> |
|ErrorDuplicateSOAPHeader  <br/> |Specifies that there are duplicate SOAP headers.  <br/> |
|ErrorSharingSynchronizationFailed  <br/> | Specifies that an attempt at synchronizing a sharing folder failed.<br/><br/> This error code MUST be returned when:<br/><br/>-  The subscription for a sharing folder is not found.  <br/>-  The sharing folder was not found.  <br/>-  The corresponding directory user was not found.  <br/>-  The user no longer exists.  <br/>-  The appointment is invalid.  <br/>-  The contact item is invalid.  <br/>-  There was a communication failure with the remote server.  <br/> |
|ErrorSharingNoExternalEwsAvailable  <br/> |Specifies that the external URL property has not been set in the Active Directory database. This error code MUST be returned if the external URL property has not been set in the Active Directory database.  <br/> |
|ErrorFreeBusyDLLimitReached  <br/> |Specifies that the maximum group member count has been reached for obtaining free/busy information for a distribution list. This error MUST be returned when the maximum group member count has been reached for obtaining free/busy information for a distribution list.  <br/> |
|ErrorInvalidGetSharingFolderRequest  <br/> |Specifies that the DataType and ShareFolderId element are both present in a request. This error code MUST be returned if the DataType and ShareFolderId element are both present in a request.  <br/> |
|ErrorNotAllowedExternalSharingByPolicy  <br/> |Specifies that the caller attempted to grant permissions in its calendar or contacts folder to a user in another organization and the attempt failed. This error code MUST be returned when the sharing policy is disabled for the caller or when the sharing policy assigned to the caller disallows sharing for the requested level or the requested folder type.  <br/> |
|ErrorUserNotAllowedByPolicy  <br/> |Specifies that the requestor attempted to grant permissions in its calendar or contacts folder to an external user but the sharing policy assigned to the requestor specifies that the domain of the external user is not listed in the policy.  <br/> |
|ErrorPermissionNotAllowedByPolicy  <br/> |Specifies that the requestor attempted to grant permissions in its calendar or contacts folder to an external user but the sharing policy assigned to the requestor specifies that the requested permission level is higher is than what the sharing policy allows.  <br/> |
|ErrorOrganizationNotFederated  <br/> |Specifies that the requestor's organization is not federated so the requestor cannot create sharing messages to send to an external user or cannot accept sharing messages received from an external user. This error code MUST be returned if the requestor's organization is not federated.  <br/> |
|ErrorMailboxFailover  <br/> |Specifies that an attempt to access a mailbox failed because the mailbox is in a failover process.  <br/> |
|ErrorInvalidExternalSharingInitiator  <br/> |Specifies that the sharing invitation sender did not create the sharing invitation metadata. This error code MUST be returned if the sharing invitation sender did not create the sharing invitation metadata.  <br/> |
|ErrorMessageTrackingPermanentError  <br/> |Specifies that the message tracking service cannot track the message.  <br/> |
|ErrorMessageTrackingTransientError  <br/> |Specifies that either the message tracking service is down or busy. This error code specifies a transient error. Clients can retry to connect to the server when this error is received.  <br/> |
|ErrorMessageTrackingNoSuchDomain  <br/> |Specifies that the given domain cannot be found.  <br/> |
|ErrorUserWithoutFederatedProxyAddress  <br/> |Specifies that the requestor's organization has a set of federated domains but the requestor's organization does not have any SMTP proxy addresses with one of the federated domains.  <br/> |
|ErrorInvalidOrganizationRelationshipForFreeBusy  <br/> |Specifies that a caller requested free/busy information for a user in another organization but the organizational relationship does not have free/busy enabled.  <br/> |
|ErrorInvalidFederatedOrganizationId  <br/> |Specifies that the requestor's organization federation objects are not properly configured.  <br/> |
|ErrorInvalidExternalSharingSubscriber  <br/> |Specifies that a sharing message is not intended for the caller.  <br/> |
|ErrorInvalidSharingData  <br/> |Specifies that the sharing metadata is not valid. This can be caused by invalid XML.  <br/> |
|ErrorInvalidSharingMessage  <br/> |Specifies that the sharing message is not valid. This can be caused by a missing property.  <br/> |
|ErrorNotSupportedSharingMessage  <br/> |Specifies that the sharing message is not supported.  <br/> |
|ErrorApplyConversationActionFailed  <br/> |This error MUST be returned if an action cannot be applied to one or more items in the conversation.  <br/> |
|ErrorInboxRulesValidationError  <br/> |This error MUST be returned if any rule does not validate.  <br/> |
|ErrorOutlookRuleBlobExists  <br/> |This error MUST be returned when an attempt to manage Inbox rules occurs after another client has accessed the Inbox rules.  <br/> |
|ErrorRulesOverQuota  <br/> |This error MUST be returned when a user's rule quota has been exceeded.  <br/> |
|ErrorNewEventStreamConnectionOpened  <br/> |This error MUST be returned to the first subscription connection if a second subscription connection is opened.  <br/> |
|ErrorMissedNotificationEvents  <br/> |This error MUST be returned when event notifications are missed.  <br/> |
|ErrorDuplicateLegacyDistinguishedName  <br/> |This error is returned when there are duplicate legacy distinguished names in Active Directory Domain Services (AD DS). This error was introduced in Exchange 2013.  <br/> |
|ErrorInvalidClientAccessTokenRequest  <br/> |This error indicates that a request to get a client access token was not valid. This error was introduced in Exchange 2013.  <br/> |
|ErrorNoSpeechDetected  <br/> |This error is intended for internal use only. This error was introduced in Exchange 2013.  <br/> |
|ErrorUMServerUnavailable  <br/> |This error is intended for internal use only. This error was introduced in Exchange 2013.  <br/> |
|ErrorRecipientNotFound  <br/> |This error is intended for internal use only. This error was introduced in Exchange 2013.  <br/> |
|ErrorRecognizerNotInstalled  <br/> |This error is intended for internal use only. This error was introduced in Exchange 2013.  <br/> |
|ErrorSpeechGrammarError  <br/> |This error is intended for internal use only. This error was introduced in Exchange 2013.  <br/> |
|ErrorInvalidManagementRoleHeader  <br/> |This error is returned if the [ManagementRole](managementrole.md) header in the SOAP header is incorrect. This error was introduced in Exchange 2013.  <br/> |
|ErrorLocationServicesDisabled  <br/> |This error is intended for internal use only. This error was introduced in Exchange 2013.  <br/> |
|ErrorLocationServicesRequestTimedOut  <br/> |This error is intended for internal use only. This error was introduced in Exchange 2013.  <br/> |
|ErrorLocationServicesRequestFailed  <br/> |This error is intended for internal use only. This error was introduced in Exchange 2013.  <br/> |
|ErrorLocationServicesInvalidRequest  <br/> |This error is intended for internal use only. This error was introduced in Exchange 2013.  <br/> |
|ErrorWeatherServiceDisabled  <br/> |This error is intended for internal use only.  <br/> |
|ErrorMailboxScopeNotAllowedWithoutQueryString  <br/> |This error is returned when a scoped search attempt is performed without using a [QueryString (String)](querystring-string.md) element for a content indexing search. This is applicable to the **SearchMailboxes** and **FindConversation** operations. This error was introduced in Exchange 2013.  <br/> |
|ErrorArchiveMailboxSearchFailed  <br/> |This error is returned when an archive mailbox search is unsuccessful. This error was introduced in Exchange 2013.  <br/> |
|ErrorArchiveMailboxServiceDiscoveryFailed  <br/> |This error is returned when the URL of an archive mailbox is not discoverable. This error was introduced in Exchange 2013.  <br/> |
|ErrorGetRemoteArchiveFolderFailed  <br/> |This error occurs when the operation to get the remote archive mailbox folder failed.  <br/> |
|ErrorFindRemoteArchiveFolderFailed  <br/> |This error occurs when the operation to find the remote archive mailbox folder failed.  <br/> |
|ErrorGetRemoteArchiveItemFailed  <br/> |This error occurs when the operation to get the remote archive mailbox item failed.  <br/> |
|ErrorExportRemoteArchiveItemsFailed  <br/> |This error occurs when the operation to export remote archive mailbox items failed.  <br/> |
|ErrorInvalidPhotoSize  <br/> |This error is returned if an invalid photo size is requested from the server. This error was introduced in Exchange 2013.  <br/> |
|ErrorSearchQueryHasTooManyKeywords  <br/> |This error is returned when an unexpected photo size is requested in a **GetUserPhoto** operation request. This error was introduced in Exchange 2013.  <br/> |
|ErrorSearchTooManyMailboxes  <br/> |This error is returned when a **SearchMailboxes** operation request contains too many mailboxes to search. This error was introduced in Exchange 2013.  <br/> |
|ErrorInvalidRetentionTagNone  <br/> |This error indicates that no retention tags were found for this user. This error was introduced in Exchange 2013.  <br/> |
|ErrorDiscoverySearchesDisabled  <br/> |This error is returned when discovery searches are disabled on a tenant or server. This error was introduced in Exchange 2013.  <br/> |
|ErrorCalendarSeekToConditionNotSupported  <br/> |This error occurs when attempting to invoke the [FindItem operation](finditem-operation.md) with a [SeekToConditionPageItemView](seektoconditionpageitemview.md) for fetching calendar items, which is not supported.  <br/> |
|ErrorCalendarIsGroupMailboxForAccept  <br/> |This error is intended for internal use only.  <br/> |
|ErrorCalendarIsGroupMailboxForDecline  <br/> |This error is intended for internal use only.  <br/> |
|ErrorCalendarIsGroupMailboxForTentative  <br/> |This error is intended for internal use only.  <br/> |
|ErrorCalendarIsGroupMailboxForSuppressReadReceipt  <br/> |This error is intended for internal use only.  <br/> |
|ErrorOrganizationAccessBlocked  <br/> |The tenant is marked for removal.  <br/> |
|ErrorInvalidLicense  <br/> |The user doesn't have a valid license.  <br/> |
|ErrorMessagePerFolderCountReceiveQuotaExceeded  <br/> |The message per folder receive quota has been exceeded.  <br/> |
   
## Remarks

This element is not required and is not included in all responses. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

