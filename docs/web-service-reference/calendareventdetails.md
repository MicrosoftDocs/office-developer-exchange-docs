---
title: "CalendarEventDetails"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CalendarEventDetails
api_type:
- schema
ms.assetid: 2dca0192-b91b-4154-aa09-84da74e875e9
description: "The CalendarEventDetails element provides additional information about a calendar event."
---

# CalendarEventDetails

The **CalendarEventDetails** element provides additional information about a calendar event. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[CalendarEventArray](calendareventarray.md)
  
[CalendarEvent](calendarevent.md)
  
[CalendarEventDetails](calendareventdetails.md)
  
```xml
<CalendarEventDetails>
   <ID/>
   <Subject/>
   <Location/>
   <IsMeeting/>
   <IsRecurring/>
   <IsException/>
   <IsReminderSet/>
   <IsPrivate/>
</CalendarEventDetails>
```

 **CalendarEventDetails**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ID](id.md) <br/> |Represents the entry ID of the calendar item.  <br/> |
|[Subject (CalendarEventDetails)](subject-calendareventdetails.md) <br/> |Represents the subject of the calendar item.  <br/> |
|[Location (CalendarEventDetails)](location-calendareventdetails.md) <br/> |Represents the location field of the calendar item.  <br/> |
|[IsMeeting (CalendarEventDetails)](ismeeting-calendareventdetails.md) <br/> |Indicates whether the calendar event is a meeting or an appointment.  <br/> |
|[IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) <br/> |Indicates whether the calendar event is an instance of a recurring calendar item or a single calendar item.  <br/> |
|[IsException](isexception.md) <br/> |Indicates whether an instance of a recurring calendar item is changed from the master.  <br/> |
|[IsReminderSet](isreminderset.md) <br/> |Indicates whether a reminder has been set for the calendar event.  <br/> |
|[IsPrivate](isprivate.md) <br/> |Indicates whether the calendar item is private.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarEvent](calendarevent.md) <br/> |Represents a unique calendar item occurrence.  <br/> The following is the XPath 2.0 expression to this element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## Remarks

All the child elements are listed in the sequence in which they occur. 
  
If the [IsPrivate](isprivate.md) element is **true**, all the other elements in the [CalendarEventDetails](calendareventdetails.md) element are not returned in the response. 
  
The GetUserAvailability operation does not return detailed caller information unless the caller has read access on the target user's calendar. You can set access permissions by using the Exchange Management Shell.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetUserAvailability operation](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

