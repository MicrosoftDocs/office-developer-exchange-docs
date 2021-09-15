---
title: "Create a recurring series by using EWS in Exchange"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: 88ed6e87-25f7-4a54-83fa-d757a0ff2528
description: "Learn how to create recurring meetings by using the EWS Managed API or EWS in Exchange."
---

# Create a recurring series by using EWS in Exchange

Learn how to create recurring meetings by using the EWS Managed API or EWS in Exchange.
  
Creating a recurring appointment or meeting isn't all that much different than creating [a single instance appointment or meeting](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md). You just need to assign values to a few additional recurrence-related properties. These are set on an [ExchangeService.Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object's [Recurrence](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence%28v=exchg.80%29.aspx) object (if you're using the EWS Managed API), or the [Recurrence](https://msdn.microsoft.com/library/5f164e5b-47b6-4242-b6b9-8d650090a831%28Office.15%29.aspx) child element of a [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) element (if you're using EWS). One thing to consider when you create a recurring, rather than a single-instance meeting, is that the calendar item you create is the recurring master for a series. A number of properties are set only on a recurring master; these properties can help you find, modify, or delete individual instances in a series. For this reason, it might be useful to keep track of the ID of the recurring master when you create a recurring series. 
  
**Table 1. Properties set on recurring master calendar items**

|**EWS Managed API class or property**|**EWS XML element**|**Description**|
|:-----|:-----|:-----|
|[Recurrence class](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence%28v=exchg.80%29.aspx) <br/> The **Recurrence** class is the base class for a derived pattern class, either [IntervalPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.intervalpattern%28v=exchg.80%29.aspx), [RelativeYearlyPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx), or [YearlyPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx).  <br/> |[Recurrence (RecurrenceType)](https://msdn.microsoft.com/library/3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12%28Office.15%29.aspx) <br/> |Contains recurrence-related information, including the recurrence pattern (daily, weekly, monthly, and so on), start and end date, number of occurrences, and so on.  <br/> |
|[FirstOccurrence property](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx) <br/> |[FirstOccurrence](https://msdn.microsoft.com/library/d6748860-ce0d-4d2e-b7e4-9ed834f1e45a%28Office.15%29.aspx) <br/> |Contains the start and end times and the item ID for the first meeting in a series.  <br/> |
|[LastOccurrence property](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx) <br/> |[LastOccurrence](https://msdn.microsoft.com/library/c9ef0fcb-4265-4e60-9986-fff0f211d00b%28Office.15%29.aspx) <br/> |Contains the start and end times and the item ID for the last meeting in a series.  <br/> |
|[ModifiedOccurrences property](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) <br/> |[ModifiedOccurrences](https://msdn.microsoft.com/library/552932fc-b3b4-486e-8d73-32c0bb10bd68%28Office.15%29.aspx) <br/> |Contains the set of all meetings in the series that have been modified from the original recurrence pattern.  <br/> |
|[DeletedOccurrences property](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx) <br/> |[DeletedOccurrences](https://msdn.microsoft.com/library/736fb305-9528-4be8-ad37-65d7556edbf2%28Office.15%29.aspx) <br/> |Contains the set of all meetings in the series that have been deleted from the original recurrence pattern.  <br/> |
   
Because meetings are essentially appointments that include attendees, the code examples in this article show how to create recurring meetings. If you want to create a recurring appointment, you can modify the examples by removing code related to attendees.
  
## Create a recurring meeting by using the EWS Managed API
<a name="bk_CreateMtgEWSMA"> </a>

The following code example shows how to create a recurring meeting. First, assign values to the properties of an [Appointment object](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) used to create a meeting, then use the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to save the recurring series to your calendar folder, and send meeting requests to your attendees. Finally, use the [Appointment.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) method to look at the values set on the recurring master for the recurring series you just created. 
  
This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**. The method in this example returns the [item ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the recurring series' recurring master. 
  
```cs
public static ItemId CreateARecurringMeeting(ExchangeService service)
{        Appointment recurrMeeting = new Appointment(service);
        // Set the properties you need to create a meeting.
        recurrMeeting.Subject = "Weekly Update Meeting";
        recurrMeeting.Body = "Come hear about how the project is coming along!";
        recurrMeeting.Start = DateTime.Now.AddDays(1);
        recurrMeeting.End = recurrMeeting.Start.AddHours(1);
        recurrMeeting.Location = "Contoso Main Gallery";
        recurrMeeting.RequiredAttendees.Add("Mack@contoso.com");
        recurrMeeting.RequiredAttendees.Add("Sadie@contoso.com");
        recurrMeeting.RequiredAttendees.Add("Magdalena@contoso.com"); recurrMeeting.ReminderMinutesBeforeStart = 30;
             
        DayOfTheWeek[] dow = new DayOfTheWeek[] { (DayOfTheWeek)recurrMeeting.Start.DayOfWeek };
        // The following are the recurrence-specific properties for the meeting.
        recurrMeeting.Recurrence = new Recurrence.WeeklyPattern(recurrMeeting.Start.Date, 1, dow);
        recurrMeeting.Recurrence.StartDate = recurrMeeting.Start.Date;
        recurrMeeting.Recurrence.NumberOfOccurrences = 10;
        // This method results in in a CreateItem call to EWS.
        recurrMeeting.Save(SendInvitationsMode.SendToAllAndSaveCopy);
        // Retrieve the meeting subject and the properties that are set on a recurring master when a recurring series is created.
        recurrMeeting = Appointment.Bind(service, recurrMeeting.Id, new PropertySet(AppointmentSchema.Subject,
                                                                                    AppointmentSchema.AppointmentType, 
                                                                                    AppointmentSchema.Recurrence, 
                                                                                    AppointmentSchema.FirstOccurrence,
                                                                                    AppointmentSchema.LastOccurrence,
                                                                                    AppointmentSchema.ModifiedOccurrences,
                                                                                    AppointmentSchema.DeletedOccurrences));
        // Print out the recurring master properties.
        Console.WriteLine("\nAppointment created: " + recurrMeeting.Subject);
        Console.WriteLine("Appointment Type: {0}\n", recurrMeeting.AppointmentType);
        Console.WriteLine("These property values are always null unless the item is a recurring master:\n");
        Console.WriteLine("\tRecurrence pattern: {0}", recurrMeeting.Recurrence.ToString());
        Console.WriteLine("\tRecurring series start Date: {0}", recurrMeeting.Recurrence.StartDate.ToString());
        Console.WriteLine("\tRecurring series end Date: {0}", 
                        recurrMeeting.Recurrence.EndDate == null ? "Null" : recurrMeeting.Recurrence.EndDate.ToString());
        Console.WriteLine("\tHas end: {0}", recurrMeeting.Recurrence.HasEnd.ToString());
        Console.WriteLine("\tNumber of occurrances: {0}", recurrMeeting.Recurrence.NumberOfOccurrences);
        Console.WriteLine("\tLast 24 characters of the first occurrence's item ID:\t {0}", 
                        recurrMeeting.FirstOccurrence.ItemId.ToString().Substring(144));
        Console.WriteLine("\tLast 24 characters of the last occurrence's item ID:\t {0}", 
                        recurrMeeting.LastOccurrence.ItemId.ToString().Substring(144)); 
        Console.WriteLine("\tModified Occurrences: {0}", 
                        (recurrMeeting.ModifiedOccurrences == null ? "Null" : recurrMeeting.ModifiedOccurrences.Count.ToString()));
        Console.WriteLine("\tDeleted Occurrences: {0}", 
                        recurrMeeting.DeletedOccurrences == null ? "Null" : recurrMeeting.ModifiedOccurrences.Count.ToString());
        // Return the ID of the recurring master.
        return recurrMeeting.Id;
}

```

## Create a recurring meeting by using EWS
<a name="bk_CreateMtgEWS"> </a>

The request and response XML in the following examples correspond to calls made to [create a recurring meeting by using the EWS Managed API](#bk_CreateMtgEWSMA). Note that other than setting recurrence-specific values on the [Recurrence](https://msdn.microsoft.com/library/5f164e5b-47b6-4242-b6b9-8d650090a831%28Office.15%29.aspx) element, the request is essentially the same as one you would use to create a single-instance appointment. The following example shows the request XML when you use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a meeting. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Name="(UTC-08:00) Pacific Time (US &amp;amp; Canada)" Id="Pacific Standard Time">
        <t:Periods>
          <t:Period Bias="P0DT8H0M0.0S" Name="Standard" Id="Std" />
          <t:Period Bias="P0DT7H0M0.0S" Name="Daylight" Id="Dlt/1" />
          <t:Period Bias="P0DT7H0M0.0S" Name="Daylight" Id="Dlt/2007" />
        </t:Periods>
        <t:TransitionsGroups>
          <t:TransitionsGroup Id="0">
            <t:RecurringDayTransition>
              <t:To Kind="Period">Dlt/1</t:To>
              <t:TimeOffset>P0DT2H0M0.0S</t:TimeOffset>
              <t:Month>4</t:Month>
              <t:DayOfWeek>Sunday</t:DayOfWeek>
              <t:Occurrence>1</t:Occurrence>
            </t:RecurringDayTransition>
            <t:RecurringDayTransition>
              <t:To Kind="Period">Std</t:To>
              <t:TimeOffset>P0DT2H0M0.0S</t:TimeOffset>
              <t:Month>10</t:Month>
              <t:DayOfWeek>Sunday</t:DayOfWeek>
              <t:Occurrence>-1</t:Occurrence>
            </t:RecurringDayTransition>
          </t:TransitionsGroup>
          <t:TransitionsGroup Id="1">
            <t:RecurringDayTransition>
              <t:To Kind="Period">Dlt/2007</t:To>
              <t:TimeOffset>P0DT2H0M0.0S</t:TimeOffset>
              <t:Month>3</t:Month>
              <t:DayOfWeek>Sunday</t:DayOfWeek>
              <t:Occurrence>2</t:Occurrence>
            </t:RecurringDayTransition>
            <t:RecurringDayTransition>
              <t:To Kind="Period">Std</t:To>
              <t:TimeOffset>P0DT2H0M0.0S</t:TimeOffset>
              <t:Month>11</t:Month>
              <t:DayOfWeek>Sunday</t:DayOfWeek>
              <t:Occurrence>1</t:Occurrence>
            </t:RecurringDayTransition>
          </t:TransitionsGroup>
        </t:TransitionsGroups>
        <t:Transitions>
          <t:Transition>
            <t:To Kind="Group">0</t:To>
          </t:Transition>
          <t:AbsoluteDateTransition>
            <t:To Kind="Group">1</t:To>
            <t:DateTime>2007-01-01T08:00:00.000Z</t:DateTime>
          </t:AbsoluteDateTransition>
        </t:Transitions>
      </t:TimeZoneDefinition>
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToAllAndSaveCopy">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Weekly Update Meeting</t:Subject>
          <t:Body BodyType="HTML">Come hear about how the Organized Observational Paradigm SkyNet project is coming along!</t:Body>
          <t:ReminderMinutesBeforeStart>30</t:ReminderMinutesBeforeStart>
          <t:Start>2014-03-08T13:21:32.868-08:00</t:Start>
          <t:End>2014-03-08T14:21:32.868-08:00</t:End>
          <t:Location>Contoso Main Gallery</t:Location>
          <t:RequiredAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Mack@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Sadie@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Magdalena@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:RequiredAttendees>
          <t:Recurrence>
            <t:WeeklyRecurrence>
              <t:Interval>1</t:Interval>
              <t:DaysOfWeek>Saturday</t:DaysOfWeek>
            </t:WeeklyRecurrence>
            <t:NumberedRecurrence>
              <t:StartDate>2014-03-08-08:00</t:StartDate>
              <t:NumberOfOccurrences>10</t:NumberOfOccurrences>
            </t:NumberedRecurrence>
          </t:Recurrence>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

 The following example shows the response XML that is returned by the **CreateItem** operation. 
  
The **ItemId** and **ChangeKey** attributes are shortened for readability. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="893" MinorBuildNumber="10" 
                         Version="V2_10" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkAD" ChangeKey="DwAAAB" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>

```

The following example shows the request XML that is generated when you use the [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) operation and the **ItemId** for the series you created, and request properties only set on a recurring master to confirm that the **ItemId** returned by the server when creating a recurring series is for a recurring master. 
  
The **ItemId** and **ChangeKey** attributes are shortened for readability. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
          <t:FieldURI FieldURI="calendar:Recurrence" />
          <t:FieldURI FieldURI="calendar:FirstOccurrence" />
          <t:FieldURI FieldURI="calendar:LastOccurrence" />
          <t:FieldURI FieldURI="calendar:ModifiedOccurrences" />
          <t:FieldURI FieldURI="calendar:DeletedOccurrences" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkAD" ChangeKey="DwAAAB" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>

```

 The following example shows the response XML that is returned by the **GetItem** operation. 
  
The **ItemId** and **ChangeKey** attributes are shortened for readability. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="893" MinorBuildNumber="10" 
                         Version="V2_10" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkAD" ChangeKey="DwAAAB" />
              <t:Subject>Weekly Update Meeting</t:Subject>
              <t:CalendarItemType>RecurringMaster</t:CalendarItemType>
              <t:Recurrence>
                <t:WeeklyRecurrence>
                  <t:Interval>1</t:Interval>
                  <t:DaysOfWeek>Saturday</t:DaysOfWeek>
                </t:WeeklyRecurrence>
                <t:NumberedRecurrence>
                  <t:StartDate>2014-03-08-08:00</t:StartDate>
                  <t:NumberOfOccurrences>10</t:NumberOfOccurrences>
                </t:NumberedRecurrence>
              </t:Recurrence>
              <t:FirstOccurrence>
                <t:ItemId Id="AAMkAD" ChangeKey="DwAAABY" />
                <t:Start>2014-03-08T21:21:00Z</t:Start>
                <t:End>2014-03-08T22:21:00Z</t:End>
                <t:OriginalStart>2014-03-08T21:21:00Z</t:OriginalStart>
              </t:FirstOccurrence>
              <t:LastOccurrence>
                <t:ItemId Id="AAMkAD" ChangeKey="DwAAABY" />
                <t:Start>2014-05-10T20:21:00Z</t:Start>
                <t:End>2014-05-10T21:21:00Z</t:End>
                <t:OriginalStart>2014-05-10T20:21:00Z</t:OriginalStart>
              </t:LastOccurrence>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>

```

## See also


- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Recurrence patterns and EWS](recurrence-patterns-and-ews.md)
    
- [Access a recurring series by using EWS in Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Delete appointments in a recurring series by using EWS in Exchange](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Update a recurring series by using EWS](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Update a recurring series by using EWS in Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    

