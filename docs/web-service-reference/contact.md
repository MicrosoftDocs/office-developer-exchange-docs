---
title: "Contact"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Contact
api_type:
- schema
ms.assetid: 66bfff50-7a91-4d81-b6a0-610b9962f677
description: "The Contact element represents a contact item in the Exchange store."
---

# Contact

The **Contact** element represents a contact item in the Exchange store. 
  
```XML
<Contact>
   <MimeContent/>
   <ItemId/>
   <ParentFolderId/>
   <ItemClass/>
   <Subject/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <DateTimeReceived/>
   <Size/>
   <Categories/>
   <Importance/>
   <InReplyTo/>
   <IsSubmitted/>
   <IsDraft/>
   <IsFromMe/>
   <IsResend/>
   <IsUnmodified/>
   <InternetMessageHeaders/>
   <DateTimeSent/>
   <DateTimeCreated/>
   <ResponseObjects/>
   <ReminderDueBy/>
   <ReminderIsSet/>
   <ReminderMinutesBeforeStart/>
   <DisplayCc/>
   <DisplayTo/>
   <HasAttachments/>
   <ExtendedProperty/>
   <Culture/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
   <FileAs/>
   <FileAsMapping/>
   <DisplayName/>
   <GivenName/>
   <Initials/>
   <MiddleName/>
   <Nickname/>
   <CompleteName/>
   <CompanyName/>
   <EmailAddresses/>
   <PhysicalAddresses/>
   <PhoneNumbers/>
   <AssistantName/>
   <Birthday/>
   <BusinessHomePage/>
   <Children/>
   <Companies/>
   <ContactSource/>
   <Department/>
   <Generation/>
   <ImAddresses/>
   <JobTitle/>
   <Manager/>
   <Mileage/>
   <OfficeLocation/>
   <PostalAddressIndex/>
   <Profession/>
   <SpouseName/>
   <Surname/>
   <WeddingAnniversary/>
   <HasPicture/>
   <PhoneticFullName/>
   <PhoneticFirstName/>
   <PhoneticLastName/>
   <Alias/>
   <Notes/>
   <Photo/>
   <UserSMIMECertificate/>
   <MSExchangeCertificate/>
   <DirectoryId/>
   <ManagerMailbox/>
   <DirectReports/>
</Contact>
```

 **ContactItemType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element name**|**Description**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.  <br/> |
|[ItemId](itemid.md) <br/> |Contains the unique identifier and change key of an item in the Exchange store.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Represents the identifier of the parent folder that contains the item or folder.  <br/> |
|[ItemClass](itemclass.md) <br/> |Represents the message class of an item.  <br/> |
|[Subject](subject.md) <br/> |Represents the subject for Exchange store items and response objects.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Indicates the sensitivity level of an item.  <br/> |
|[Body](body.md) <br/> |Represents the actual body content of a message.  <br/> |
|[Attachments](attachments-ex15websvcsotherref.md) <br/> |Contains the items or files that are attached to an item in the Exchange store.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Represents the date and time that an item in a mailbox was received.  <br/> |
|[Size](size.md) <br/> |Represents the size in bytes of an item. This property is read-only.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Represents a collection of strings that identify to which categories an item in the mailbox belongs.  <br/> |
|[Importance](importance.md) <br/> |Describes the importance of an item.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Represents the identifier of the item to which this item is a reply.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Indicates whether an item has been submitted to the Outbox default folder.  <br/> |
|[IsDraft](isdraft.md) <br/> |Represents whether an item has not yet been sent.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Indicates whether a user sent an item to himself or herself.  <br/> |
|[IsResend](isresend.md) <br/> |Indicates whether the item had previously been sent.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Indicates whether the item has been modified.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Represents the collection of all Internet message headers that are contained in an item in a mailbox.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Represents the date and time that an item in a mailbox was sent.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Represents the date and time that a given item in the mailbox was created.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contains a collection of all the response objects that are associated with an item in the Exchange store.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Represents the date and time when the event occurs. This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Indicates whether a reminder has been set for an item in the Exchange store.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Represents the number of minutes before an event when a reminder is displayed.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Represents the display string that is used for the contents of the Cc line. This is the concatenated string of all Cc recipient display names.  <br/> |
|[DisplayTo](displayto.md) <br/> |Represents the display string that is used for the contents of the To line. This is the concatenated string of all To recipient display names.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Represents a property that is set to **true** if an item has at least one visible attachment. This property is read-only.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifies extended properties on folders and items.  <br/> |
|[Culture](culture.md) <br/> |Represents the culture for a given item in a mailbox.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contains the client's rights based on the permission settings for the item or folder. This element is read-only.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Contains the display name of the last user to modify an item.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Indicates when an item was last modified.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Indicates whether the item is associated with a folder.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contains the identifier of an item or conversation.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Represents an HTML fragment or plain text which represents the unique body of this conversation.  <br/> |
|[FileAs](fileas.md) <br/> |Represents how a contact is filed in the Contacts folder.  <br/> |
|[FileAsMapping](fileasmapping.md) <br/> |Defines how to construct what is displayed for a contact.  <br/> |
|[DisplayName (string)](displayname-string.md) <br/> |Defines the display name of a contact.  <br/> |
|[GivenName](givenname.md) <br/> |Contains a contact's given name.  <br/> |
|[Initials](initials.md) <br/> |Represents the initials of a contact.  <br/> |
|[MiddleName](middlename.md) <br/> |Represents the middle name of a contact.  <br/> |
|[Nickname](nickname.md) <br/> |Represents the nickname of a contact.  <br/> |
|[CompleteName](completename.md) <br/> |Represents the complete name of a contact.  <br/> |
|[CompanyName](companyname.md) <br/> |Represents the company name that is associated with a contact.  <br/> |
|[EmailAddresses](emailaddresses.md) <br/> |Represents a collection of e-mail addresses for a contact.  <br/> |
|[PhysicalAddresses](physicaladdresses.md) <br/> |Contains a collection of physical addresses that are associated with a contact.  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |Represents a collection of telephone numbers for a contact.  <br/> |
|[AssistantName](assistantname.md) <br/> |Represents an assistant to a contact.  <br/> |
|[Birthday](birthday.md) <br/> |Represents the birth date of a contact.  <br/> |
|[BusinessHomePage](businesshomepage.md) <br/> |Represents the Home page (Web address) for the contact.  <br/> |
|[Children](children.md) <br/> |Contains the names of a contact's children.  <br/> |
|[Companies](companies.md) <br/> |Represents the collection of companies that are associated with a contact.  <br/> |
|[ContactSource](contactsource.md) <br/> |Describes whether the contact is located in the Exchange store or the Active Directory directory service.  <br/> |
|[Department](department.md) <br/> |Represents the contact's department at work.  <br/> |
|[Generation](generation.md) <br/> |Represents a generational abbreviation that follows the full name of a contact.  <br/> |
|[ImAddresses](imaddresses.md) <br/> |Represents a collection of instant messaging addresses for a contact.  <br/> |
|[JobTitle](jobtitle.md) <br/> |Represents the job title of a contact.  <br/> |
|[Manager](manager.md) <br/> |Represents a contact's manager.  <br/> |
|[Mileage](mileage.md) <br/> |Represents mileage for a contact item.  <br/> |
|[OfficeLocation](officelocation.md) <br/> |Represents the office location of a contact.  <br/> |
|[PostalAddressIndex](postaladdressindex.md) <br/> |Represents the display types for physical addresses.  <br/> |
|[Profession](profession.md) <br/> |Represents the profession of a contact.  <br/> |
|[SpouseName](spousename.md) <br/> |Represents the name of a contact's spouse/partner.  <br/> |
|[Surname](surname.md) <br/> |Represents the surname of a contact.  <br/> |
|[WeddingAnniversary](weddinganniversary.md) <br/> |Contains the wedding anniversary of a contact.  <br/> |
|[HasPicture](haspicture.md) <br/> |Indicates whether the contact item has a file attachment that represents the contact's picture.  <br/> |
|[PhoneticFullName](phoneticfullname.md) <br/> |Contains the full name of a contact, including the first and last name, spelled phonetically.  <br/> |
|[PhoneticFirstName](phoneticfirstname.md) <br/> |Contains the first name of a contact, spelled phonetically.  <br/> |
|[PhoneticLastName](phoneticlastname.md) <br/> |Contains the last name of a contact, spelled phonetically.  <br/> |
|[Alias](alias.md) <br/> |Contains the email alias of a contact.  <br/> |
|[Notes (Contact)](notes-contact.md) <br/> |Contains supplementary contact information.  <br/> |
|[Photo](photo.md) <br/> |Contains a value that encodes the photo of a contact.  <br/> |
|[UserSMIMECertificate](usersmimecertificate.md) <br/> |Contains a value that encodes the SMIME certificate of a contact.  <br/> |
|[MSExchangeCertificate](msexchangecertificate.md) <br/> |Contains a value that encodes the Microsoft Exchange certificate of a contact.  <br/> |
|[DirectoryId](directoryid.md) <br/> |Contains the directory ID of a contact.  <br/> |
|[ManagerMailbox](managermailbox.md) <br/> |Contains SMTP information that identifies the manager mailbox of the contact.  <br/> |
|[DirectReports](directreports.md) <br/> |Contains SMTP information that identifies the direct reports of a contact.  <br/> |
   
### Parent elements

|**Element name**|**Description**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describes all calendar items that are adjacent to a meeting time.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifies all items that conflict with a meeting time  <br/> |
|[Create (ItemSync)](create-itemsync.md) <br/> |Identifies a single folder to create in the local client store.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Represents an Exchange item that is attached to another Exchange item.  <br/> |
|[Items](items.md) <br/> |Contains an array of items.  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.  <br/> |
|[Resolution](resolution.md) <br/> |Contains a single resolved entity.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifies a single item to update in the local client store.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Creating Contacts (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[Updating Contacts](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[Deleting Contacts](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

