---
title: "ResponseMessages"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: 2071bed8-ea66-4627-aa4f-a1d9a025cf3d
description: "The ResponseMessages element contains the response messages for an Exchange Web Services request."
---

# ResponseMessages

The **ResponseMessages** element contains the response messages for an Exchange Web Services request. 
  
```XML
<ResponseMessages>
   <CreateItemResponseMessage/>
</ResponseMessages>
```

```xml
<ResponseMessages>
   <DeleteItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UpdateItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SendItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <DeleteFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <EmptyFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CreateFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <FindFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UpdateFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <MoveFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CopyFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CreateAttachmentResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <DeleteAttachmentResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetAttachmentResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UploadItemsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ExportItemsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <FindItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <MoveItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CopyItemResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ResolveNamesResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ExpandDLResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetServerTimeZonesResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetEventsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetStreamingEventsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SubscribeResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UnsubscribeResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SendNotificationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SyncFolderHierarchyResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <SyncFolderItemsResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CreateManagedFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ConvertIdResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetSharingMetadataResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <RefreshSharingFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetSharingFolderResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <CreateUserConfigurationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <DeleteUserConfigurationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetUserConfigurationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <UpdateUserConfigurationResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetRoomListsResponse/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetRoomsResponse/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetRemindersResponse/>
</ResponseMessages
```

```xml 
<ResponseMessages>
   <PerformReminderActionResponse/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <ApplyConversationActionResponseMessage/>
</ResponseMessages>
```

```xml 
<ResponseMessages>
   <GetPasswordExpirationDateResponse />
</ResponseMessages>
```


**ArrayOfResponseMessagesType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Contains the status and result of a single CopyFolder request.  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Contains the status and result of a single CopyItem request.  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |Contains the status and result of a single CreateAttachment request.  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Contains the status and result of a single CreateFolder request.  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Contains the status and result of a single CreateItem request.  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Contains the status and result of a single CreateManagedFolder request.  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Contains the status and result of a single DeleteAttachment request.  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |Contains the status and result of a single DeleteFolder request.  <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |Contains the status and result of a single DeleteItem request.  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |Contains the status and result of a single [EmptyFolder](emptyfolder.md) request.  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Contains the status and result of a single ExpandDL request.  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Contains the status and result of a single FindFolder request.  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Contains the status and result of a single FindItem request.  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |Contains the status and result of a single GetAttachment request.  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Contains the status and results of a single UploadItems request.  <br/> |
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |Contains the status and results of a single ExportItems request.  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Contains the status and result of a single GetEvents request.  <br/> |
|[GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md) <br/> |Contains the status and result of a single GetStreamingEvents request.  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Contains the status and result of a single GetFolder request.  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Contains the status and result of a single GetItem request.  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Contains the status and result of a single MoveFolder request.  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Contains the status and result of a single MoveItem request.  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Contains the status and result of a ResolveNames request.  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |Contains the status and result of a single SendItem request.  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Contains the status and result of a single SendNotification request.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Contains the status and result of a single Subscribe request.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contains the status and result of a SyncFolderHierarchy request.  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Contains the status and result of a SyncFolderItems request.  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |Contains the status and result of a single Unsubscribe request.  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Contains the status and result of a single UpdateFolder request.  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Contains the status and result of a single UpdateItem request.  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Contains the status and result of a ConvertId request.  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Contains the status and results of a GetSharingMetadata request.  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |Contains the status and results of a RefreshSharingFolder request.  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Contains the status and results of a GetSharingFolder request.  <br/> |
|[CreateUserConfigurationResponseMessage](createuserconfigurationresponsemessage.md) <br/> |Contains the status and results of a CreateUserConfiguration request.  <br/> |
|[DeleteUserConfigurationResponseMessage](deleteuserconfigurationresponsemessage.md) <br/> |Contains the status and results of a DeleteUserConfiguration request.  <br/> |
|[GetUserConfigurationResponseMessage](getuserconfigurationresponsemessage.md) <br/> |Contains the status and results of a GetUserConfiguration request.  <br/> |
|[UpdateUserConfigurationResponseMessage](updateuserconfigurationresponsemessage.md) <br/> |Contains the status and results of an UpdateUserConfiguration request.  <br/> |
|[GetRoomListsResponse](getroomlistsresponse.md) <br/> |Contains the status and results of a GetRoomLists request.  <br/> |
|[GetRoomsResponse](getroomsresponse.md) <br/> |Contains the status and results of a GetRooms request.  <br/> |
|[GetRemindersResponse](getremindersresponse.md) <br/> |Contains the status and results of a GetReminders request.  <br/> |
|[PerformReminderActionResponse](performreminderactionresponse.md) <br/> |Contains the status and results of a PerformReminderAction request.  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |Contains the status and result of a single GetServerTimeZones request.  <br/> |
|[ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md) <br/> |Contains the status and results of an [ApplyConversationAction operation](applyconversationaction-operation.md) request.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CopyFolderResponse](copyfolderresponse.md) <br/> |Defines a response to a CopyFolder request.  <br/> |
|[CopyItemResponse](copyitemresponse.md) <br/> |Defines a response to a CopyItem request.  <br/> |
|[CreateAttachmentResponse](createattachmentresponse.md) <br/> |Defines a response to a CreateAttachment request.  <br/> |
|[CreateFolderResponse](createfolderresponse.md) <br/> |Defines a response to a CreateFolder request.  <br/> |
|[CreateItemResponse](createitemresponse.md) <br/> |Defines a response to a CreateItem request.  <br/> |
|[CreateManagedFolderResponse](createmanagedfolderresponse.md) <br/> |Defines a response to a CreateManagedFolder request.  <br/> |
|[DeleteAttachmentResponse](deleteattachmentresponse.md) <br/> |Defines a response to a DeleteAttachment request.  <br/> |
|[DeleteFolderResponse](deletefolderresponse.md) <br/> |Defines a response to a DeleteFolder request.  <br/> |
|[DeleteItemResponse](deleteitemresponse.md) <br/> |Defines a response to a DeleteItem request.  <br/> |
|[EmptyFolderResponse](emptyfolderresponse.md) <br/> |Defines a response to an EmptyFolder request.  <br/> |
|[ExpandDLResponse](expanddlresponse.md) <br/> |Defines a response to an ExpandDL request.  <br/> |
|[ExportItemsResponse](exportitemsresponse.md) <br/> |Represents response to a single ExportItems request.  <br/> |
|[FindFolderResponse](findfolderresponse.md) <br/> |Defines a response to a FindFolder request.  <br/> |
|[FindItemResponse](finditemresponse.md) <br/> |Defines a response to a FindItem request.  <br/> |
|[GetAttachmentResponse](getattachmentresponse.md) <br/> |Defines a response to a GetAttachment request.  <br/> |
|[GetEventsResponse](geteventsresponse.md) <br/> |Defines a response to a GetEvents request.  <br/> |
|[GetStreamingEventsResponse](getstreamingeventsresponse.md) <br/> |Defines a response to a GetStreamingEvents request.  <br/> |
|[GetFolderResponse](getfolderresponse.md) <br/> |Defines a response to a GetFolder request.  <br/> |
|[GetItemResponse](getitemresponse.md) <br/> |Defines a response to a GetItem request.  <br/> |
|[MoveFolderResponse](movefolderresponse.md) <br/> |Defines a response to a MoveFolder request.  <br/> |
|[MoveItemResponse](moveitemresponse.md) <br/> |Defines a response to a MoveItem request.  <br/> |
|[ResolveNamesResponse](resolvenamesresponse.md) <br/> |Defines a response to a ResolveNames request.  <br/> |
|[SendItemResponse](senditemresponse.md) <br/> |Defines a response to a SendItem request.  <br/> |
|[SendNotificationResult](sendnotificationresult.md) <br/> |Defines a response to a SendNotification request.  <br/> |
|[SubscribeResponse](subscriberesponse.md) <br/> |Defines a response to a Subscribe request.  <br/> |
|[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md) <br/> |Defines a response to a SyncFolderHierarchy request.  <br/> |
|[SyncFolderItemsResponse](syncfolderitemsresponse.md) <br/> |Defines a response to a SyncFolderItems request.  <br/> |
|[UnsubscribeResponse](unsubscriberesponse.md) <br/> |Defines a response to an Unsubscribe request.  <br/> |
|[UpdateFolderResponse](updatefolderresponse.md) <br/> |Defines a response to an UpdateFolder request.  <br/> |
|[UpdateItemResponse](updateitemresponse.md) <br/> |Defines a response to an UpdateItem request.  <br/> |
|[ConvertIdResponse](convertidresponse.md) <br/> |Contains a response to a ConvertId request.  <br/> |
|[GetServerTimeZonesResponse](getservertimezonesresponse.md) <br/> |Defines a response to a GetServerTimeZones request.  <br/> |
|[CreateUserConfigurationResponse](createuserconfigurationresponse.md) <br/> |Defines a response to a CreateUserConfiuration request.  <br/> |
|[DeleteUserConfigurationResponse](deleteuserconfigurationresponse.md) <br/> |Defines a response to a DeleteUserConfiguration request.  <br/> |
|[GetUserConfigurationResponse](getuserconfigurationresponse.md) <br/> |Defines a response to a GetUserConfiguration request.  <br/> |
|[UpdateUserConfigurationResponse](updateuserconfigurationresponse.md) <br/> |Defines a response to an UpdateUserConfiguration request.  <br/> |
|[ApplyConversationActionResponse](applyconversationactionresponse.md) <br/> |Defines a response to an [ApplyConversationAction operation](applyconversationaction-operation.md) request.  <br/> |
|[GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md) <br/> |Defines a response to a [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) operation request.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [ExportItems operation](exportitems-operation.md) 
- [UploadItems operation](uploaditems-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

