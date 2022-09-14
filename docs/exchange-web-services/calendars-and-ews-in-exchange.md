---
title: "Calendars and EWS in Exchange" 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer 
ms.assetid: b87b0180-f5b5-44e4-b6ac-4f23e476b03b
description: "Learn about calendars, calendar folders and items, appointments, and meetings in Exchange."
localization_priority: Priority
---

# Calendars and EWS in Exchange

Learn about calendars, calendar folders and items, appointments, and meetings in Exchange.
  
You're probably familiar with many of the calendar features in email clients like Outlook, which enable you to track appointments, schedule meetings, check people's availability, invite attendees, and change or cancel meetings.
  
Calendar-related features in Exchange are a little different than what you see in a client like Outlook. Instead of displaying information, EWS in Exchange enables you to do things like create, store, send, or change information. To use EWS to work with calendars, you'll need to be familiar with concepts such as information storage, time, recurrence, and message flow. More specifically, you'll need to be familiar with the following:
  
- Calendar folders, calendar items, and calendar views

- Meeting requests, responses, scheduling, attendees, resources, rooms, and availability

- Time durations, time zones, and start and end times of meetings and appointments

- Recurring series, recurrence patterns, exceptions, and single instance appointments and meetings

Fortunately, EWS and the EWS Managed API provide a rich set of operations and methods that enable you to perform a wide range of calendar-related tasks. For example, using the EWS Managed API, you can create a meeting and send invitations to attendees with just a few lines of code, as shown in the following example.
  
```cs
            Appointment meeting = new Appointment(service);
            // Set the properties on the meeting object to create the meeting.
            meeting.Subject = "Team building exercise";
            meeting.Body = "Let's learn to really work as a team and then have lunch!";
            meeting.Start = DateTime.Now.AddDays(2);
            meeting.End = meeting.Start.AddHours(2);
            meeting.Location = "Conference Room 12";
            meeting.RequiredAttendees.Add("Mack.Chaves@contoso.com");
            meeting.RequiredAttendees.Add("Sadie.Daniels@contoso.com");
            meeting.OptionalAttendees.Add("Magdalena.Kemp@contoso.com");
            meeting.ReminderMinutesBeforeStart = 60;
            // Send the meeting request
            meeting.Save(SendInvitationsMode.SendToAllAndSaveCopy);

```

## Calendar folders and calendar items
<a name="bk_CalendarFolder"> </a>

Calendar folders contain calendar items. Calendar folders have a [folder class](https://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) of **IPF.Appointment**, and can include only the items defined by the [ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) EWS Managed API property, which is associated with an [Appointment Class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object, or the EWS [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) element.
  
Items in a Calendar folder are a little different from items in other folders in a mailbox because occurrences in a recurring series and exceptions to a recurring series are not actual items in the mailbox, but rather are stored internally as attachments to a recurring master. Therefore, in order to retrieve all appointments in a given date range, you need to use a calendar view. To learn more about retrieving appointments and calendar views, see [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## Meetings and appointments
<a name="bk_meetings"> </a>

The essential difference between meetings and appointments is that meetings have attendees, and appointments don't. Internally, Exchange uses the same object for both meetings and appointments. You use the EWS Managed API [Appointment class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) element to work with meetings and appointments.
  
Both appointments and meetings can be single instances or part of a [recurring series](recurrence-patterns-and-ews.md), but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent.
  
Because meetings include sending and responding to requests and updates, they involve more than just accessing items in a Calendar folder. They also have an associated workflow. Meetings must be scheduled when attendees are available, and can also involve reserving a meeting room, or resources such as a projector or other equipment.
  
The meeting workflow typically involves the following steps:
  
1. A meeting is created and populated with information such as start and end time, location, and a message body.
2. A list of prospective attendees, resources, and rooms is created.
3. The availability status of attendees is checked.
4. A meeting request is sent to attendees.
5. Attendees reply to the meeting with their intention to attend or not. Attendees may also propose a new time for the meeting.
6. Meetings can be canceled or updated, which typically trigger new messages to be sent to attendees.

## Calendars and time
<a name="bk_Time"> </a>

Time-related functionality is integral to calendaring. Appointments and meetings have start and end times, durations, and other time-related properties, such as the time at which a message is created, sent, and received. Existing appointments and meetings can be retrieved from a Calendar folder based on a start and end time. Recurring series have beginnings and ends. And meetings occur within a given time zone, which is increasingly important in a global economy.
  
Times are stored internally on an Exchange server in Coordinated Universal Time (UTC). Exchange converts them to local time zone based on client settings. [DateTime](https://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx) properties are scoped to the computer's local time zone. 
  
## Recurring series
<a name="bk_recurrence"> </a>

A recurring series of appointments or meetings is comprised of a recurring master, a set of occurrence items, and optionally, a set of exception items. Recurrence information is stored on the recurring master item. The [RecurringMasterItemId](https://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) EWS element is associated with occurrences and exceptions in a series, or you can use the [Appointment.BindToRecurringMaster](https://msdn.microsoft.com/library/dd635978%28v=EXCHG.80%29.aspx) EWS Managed API method to get the recurring master. Using an instance of a series, you can find all the elements and information associated with the series.
  
Note that recurrence properties exist on all calendar items, but they are populated only on recurring master items. In addition to an index of all occurrences in a series, the recurring master has a reference to modified and deleted occurrences and the recurrence pattern of a series (for example, daily, weekly, monthly, or yearly).
  
## In this section
<a name="bk_inthissection"> </a>

- [Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)

- [Create all-day events by using EWS in Exchange](how-to-create-all-day-events-by-using-ews-in-exchange.md)

- [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)

- [Update appointments and meetings by using EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)

- [Delete appointments and cancel meetings by using EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)

- [Get room lists by using EWS in Exchange](how-to-get-room-lists-by-using-ews-in-exchange.md)

- [Get free/busy information by using EWS in Exchange](how-to-get-free-busy-information-by-using-ews-in-exchange.md)

- [Propose a new meeting time by using EWS in Exchange](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)

- [Process calendar items in batches in Exchange](how-to-process-calendar-items-in-batches-in-exchange.md)

- [Recurrence patterns and EWS](recurrence-patterns-and-ews.md)

## See also

- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
- [EWS client design overview for Exchange](ews-client-design-overview-for-exchange.md)