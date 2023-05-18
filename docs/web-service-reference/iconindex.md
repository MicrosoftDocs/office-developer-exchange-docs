---
title: "IconIndex"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 92020822-2a86-4dfc-aee1-3067af4d4edf
description: "The IconIndex element identifies the icon index for an item or conversation."
---

# IconIndex

The **IconIndex** element identifies the icon index for an item or conversation. 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MailIrmForwarded | MailIrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 **IconIndexType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[Conversation (ConversationType)](conversation-conversationtype.md) | [Item](item.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Message](message-ex15websvcsotherref.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)
  
## Text value

The following table contains the possible text values for the **IconIndex** element. 
  
|**Value**|**Description**|
|:-----|:-----|
|||
|Default  <br/> |Specifies the default icon.  <br/> |
|PostItem  <br/> |Specifies the icon for a post item.  <br/> |
|MailRead  <br/> |Specifies the mail read icon.  <br/> |
|MailUnread  <br/> |Specifies the unread mail icon.  <br/> |
|MailReplied  <br/> |Specifies the replied to mail icon.  <br/> |
|MailForwarded  <br/> |Specifies the forwarded mail icon.  <br/> |
|MailEncrypted  <br/> |Specifies the encrypted mail icon.  <br/> |
|MailSmimeSigned  <br/> |Specifies the Secure/Multipurpose Internet Mail Extensions (S/MIME) signed mail icon.  <br/> |
|MailEncryptedReplied  <br/> |Specifies the encrypted replied to mail icon.  <br/> |
|MailSmimeSignedReplied  <br/> |Specifies the S/MIME signed replied to mail icon.  <br/> |
|MailEncryptedForwarded  <br/> |Specifies the encrypted forwarded mail icon.  <br/> |
|MailSmimeSignedForwarded  <br/> |Specifies the S/MIME signed forwarded mail icon.  <br/> |
|MailEncryptedRead  <br/> |Specifies the encrypted read mail icon.  <br/> |
|MailSmimeSignedRead  <br/> |Specifies the S/MIME signed read mail icon.  <br/> |
|MailIrm  <br/> |Specifies the Information Rights Management (IRM)-protected mail icon.  <br/> |
|MailIrmForwarded  <br/> |Specifies the IRM-protected forwarded mail icon.  <br/> |
|MailIrmReplied  <br/> |Specifies the IRM-protected replied to mail icon.  <br/> |
|SmsSubmitted  <br/> |Specifies the icon mail submitted for Short Message Service (SMS) routing.  <br/> |
|SmsRoutedToDeliveryPoint  <br/> |Specifies the icon for SMS routing to an external delivery point.  <br/> |
|SmsRoutedToExternalMessagingSystem  <br/> |Specifies the icon for SMS routing to an external messaging system.  <br/> |
|SmsDelivered  <br/> |Specifies the SMS delivered mail icon.  <br/> |
|OutlookDefaultForContacts  <br/> |Specifies the default icon for contacts.  <br/> |
|AppointmentItem  <br/> |Specifies the appointment item icon.  <br/> |
|AppointmentRecur  <br/> |Specifies the recurring appointment icon.  <br/> |
|AppointmentMeet  <br/> |Specifies the meeting icon.  <br/> |
|AppointmentMeetRecur  <br/> |Specifies the recurring meeting icon.  <br/> |
|AppointmentMeetNY  <br/> |Specifies the icon for a tentative response to the meeting.  <br/> |
|AppointmentMeetYes  <br/> |Specifies the meeting acceptance icon.  <br/> |
|AppointmentMeetNo  <br/> |Specifies the meeting declined icon.  <br/> |
|AppointmentMeetMaybe  <br/> |Specifies the icon for a maybe response to the meeting.  <br/> |
|AppointmentMeetCancel  <br/> |Specifies the meeting cancel icon.  <br/> |
|AppointmentMeetInfo  <br/> |Specifies the meeting information icon.  <br/> |
|TaskItem  <br/> |Specifies the task item icon.  <br/> |
|TaskRecur  <br/> |Specifies the recurring task icon.  <br/> |
|TaskOwned  <br/> |Specifies the task owned icon.  <br/> |
|TaskDelegated  <br/> |Specifies the task delegated icon.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Type|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |false  <br/> |
   

