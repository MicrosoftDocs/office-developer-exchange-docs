---
title: "CreateItem"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CreateItem
api_type:
- schema
ms.assetid: c3707feb-3fd4-4b8a-a68f-2abadd455163
description: "The CreateItem element defines a request to create an item in the Exchange store."
---

# CreateItem

The **CreateItem** element defines a request to create an item in the Exchange store. 
  
```xml
<CreateItem MessageDisposition="" SendMeetingInvitations="">
   <SavedItemFolderId/>
   <Items/>
</CreateItem>
```

**CreateItemType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|Attribute|Description|
|:-----|:-----|
|**MessageDisposition** <br/> |Describes how the item will be handled after it is created. The attribute is required for e-mail messages. This attribute is only applicable to e-mail messages.  <br/> |
|**SendMeetingInvitations** <br/> |Describes how meeting requests are handled after they are created. This attribute is required for calendar items.  <br/> |
   
#### MessageDisposition Attribute

|Value|Description|
|:-----|:-----|
|SaveOnly  <br/> |The message item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element. Messages can be sent later by using the [SendItem operation](senditem-operation.md). An item identifier is returned in the response. Item identifiers are not returned for any item types except for message items. This includes response objects.  <br/> |
|SendOnly  <br/> |The item is sent but no copy is saved in the Sent Items folder. An item identifier is not returned in the response.<br/><br/>**NOTE**: **CreateItem** does not support delegate access when the SendOnly option is used because a destination folder cannot be specified with this option. The workaround is to create the item, get the item identifier, and then use the SendItem operation to send the item.           |
|SendAndSaveCopy  <br/> |The item is sent and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element. An item identifier is not returned in the response.<br/><br/>**NOTE**: Meeting requests are not saved to the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) property. For calendaring, only the save location for calendar items can be specified by the **SavedItemFolderId** property. You cannot control where a meeting request item is saved. Only the associated calendar items are copied and saved into the folder that is identified by the **SavedItemFolderId** property.           |
   
#### SendMeetingInvitations Attribute

|Value|Description|
|:-----|:-----|
|SendToNone  <br/> |If the item is a meeting request, it is saved as a calendar item but not sent.  <br/> |
|SendOnlyToAll  <br/> |The meeting request is sent to all attendees but is not saved in the Sent Items folder.  <br/> |
|SendToAllAndSaveCopy  <br/> |The meeting request is sent to all attendees and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.  <br/> |
   
### Child elements

|Element|Description|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifies the target folder where a new item can be created. If the **MessageDisposition** attribute is set to SendOnly, a created message will only be sent. The message will not be put in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contains an array of items to create in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [CreateItemResponse](createitemresponse.md)  
- [CreateItem operation](createitem-operation.md)
- [Creating E-mail Messages](https://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx) 
- [Creating Contacts (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [Creating Tasks](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx) 
- [Creating Appointments](https://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

