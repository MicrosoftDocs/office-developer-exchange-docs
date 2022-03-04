---
title: "Time zones and EWS in Exchange"
 
 
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
 
 
ms.assetid: 0e0a666c-0541-414b-a7fb-297d94f692e6
description: "Find out how time zones work with the EWS Managed API and EWS in Exchange."
localization_priority: Priority
---

# Time zones and EWS in Exchange

Find out how time zones work with the EWS Managed API and EWS in Exchange.
  
Time zones aren't something that most people give much thought to. However, they're an important concept when specifying dates and times using the EWS Managed API or EWS. Mishandling time zones in an EWS Managed API or EWS application can yield unexpected results. Handling time zones properly is easy, as long as you know how.
  
## Handling time zones in the EWS Managed API

If you're using the EWS Managed API, time zones are, for the most part, handled for you automatically. Without any explicit action on your part, the API uses the local time zone of the client computer and handles all necessary conversions behind the scenes. This is great when that's the desired effect, but you have other options.
  
One option is setting the [ExchangeService.TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property. This property controls the time zone for all requests executed by the EWS Managed API. This property is read-only; the only way to set it is via the class constructor. If you use either the [ExchangeService(System.TimeZoneInfo)](https://msdn.microsoft.com/library/dd635875%28v=exchg.80%29.aspx) or the [ExchangeService(ExchangeVersion, System.TimeZoneInfo)](https://msdn.microsoft.com/library/dd636248%28v=exchg.80%29.aspx) constructor, you can specify a specific time zone as a [System.TimeZoneInfo](https://msdn.microsoft.com/library/system.timezoneinfo%28v=vs.110%29.aspx) object. If you use one of the other constructors that do not take a **TimeZoneInfo** object as a parameter, the **ExchangeService** class sets the **TimeZone** property to the current time zone of the client computer.
  
Whether you set a specific time zone or leave it as the time zone of the client computer, all dates and times are expressed in the time zone represented by the **TimeZone** property. The EWS Managed API exposes all date/time properties as [System.DateTime](https://msdn.microsoft.com/library/system.datetime%28v=vs.110%29.aspx) structures. So if you set any date/time properties, be mindful that the time you specify is interpreted according to the [DateTime.Kind](https://msdn.microsoft.com/library/system.datetime.kind%28v=vs.110%29.aspx) property value on the **DateTime** object. If the value of the **Kind** property is set to **Unspecified**, the value of the **DateTime** is interpreted as being in the time zone specified by the **TimeZone** property. If you're reading date/time properties, all **DateTime** properties are expressed in that time zone.
  
If you are [creating new appointments or meetings](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md) or [updating existing appointments or meetings](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md), you have the ability to override the time zone specified in the **TimeZone** for new [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) objects. However, exactly what you can override depends on the [EWS schema version](ews-schema-versions-in-exchange.md) you are targeting. For all values of the [ExchangeService.RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) property, you can set the [Appointment.StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) to use a specific time zone for that appointment or meeting. If you're using a value for the **ExchangeService.RequestedServerVersion** property greater than **Exchange2007_SP1**, you can also set the [Appointment.EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) property, allowing you to specify a time zone for the [Appointment.End](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx) property. However, bear in mind that these properties only affect the interpretation of the date/time for the create request. If you retrieve the appointment, the start and end times will still be expressed in the time zone specified by the **TimeZone** property.
  
If you are updating existing appointments or meetings, you can change the time zone for an **Appointment** object by setting the **StartTimeZone** property and/or the **EndTimeZone** property. Doing so will cause the applicable times to shift accordingly. If you've set the **ExchangeService.RequestedServerVersion** to **Exchange2007_SP1**, you cannot set the **EndTimeZone** property; the value of the **StartTimeZone** property will be used in its place.
  
**Table 1. Time zone properties in the EWS Managed API**

|**Time zone property**|**Minimum server request version**|**Description**|
|:-----|:-----|:-----|
|[TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |If not set via the constructor for the **ExchangeService** class, this property is set to the time zone of the client computer. All **DateTime** properties when creating items and when retrieving existing items are expressed in this time zone. This time zone can be overridden in create requests for appointments and meetings by setting the **Appointment.StartTimeZone** and/or the **Appointment.EndTimeZone** property. If not overridden by the **Appointment.StartTimeZone** property, this time zone is considered the creation time zone for appointments and meetings.  <br/> |
|[StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |If set on new **Appointment** objects, this time zone is used to interpret the [Appointment.Start](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.start%28v=exchg.80%29.aspx) and [Appointment.ReminderDueBy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.reminderdueby%28v=exchg.80%29.aspx) properties. This time zone is also considered the creation time zone for the **Appointment** object.  <br/> When retrieving existing items, this property is informational only. The values of **DateTime** properties on existing appointment are always expressed in the time zone specified by the **ExchangeService.TimeZone** property.  <br/> |
|[EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2010** <br/> |If set on new **Appointment** objects, this time zone is used to interpret the [Appointment.End](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx) property.  <br/> When retrieving existing items, this property is informational only. The values of **DateTime** properties on existing appointment are always expressed in the time zone specified by the **ExchangeService.TimeZone** property.  <br/> |

## Handling time zones in EWS

If you're using EWS, time zones aren't handled for you automatically, and things are a bit more complicated. How time zones impact EWS requests and responses depends on a number of factors:
  
- The Exchange version specified in the [RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) element

- The time zone specified in the [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element (if present)

- The time zone specified in the [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx), [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx), or [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements (if present on appointments or meetings)

- The time zone specified in the XML **dateTime** elements (if any)

The time zone specified in the value of **dateTime** elements can take three forms. You can read all the details in [XML Schema Part 2: Datatypes Second Edition](http://www.w3.org/TR/xmlschema-2/#dateTime), but to paraphrase:
  
- **Universal Coordinated Time (UTC):** Specified by 'Z'. For example, `2014-06-06T19:00:00.000Z`

- **Specific time zone:** Specified by '+' or '-' followed by hours and minutes. For example, `2014-06-06T19:00:00.000-08:00`

- **No time zone:** Specified by the absence of any time zone. For example, `2014-06-06T19:00:00.000`

If a time zone is present in a **dateTime** value (either UTC or a specific time zone), that value is always interpreted as that time zone. If no time zone is present, then the interpretation of the value depends on the specific combination of the other time-zone related elements.
  
**Table 2. Time zone elements in EWS and their effects**

|**RequestServerVersion**|**TimeZoneContext present?**|**MeetingTimeZone, StartTimeZone, or EndTimeZone present (CalendarItem and MeetingRequest only)?**|**dateTime in UTC**|**dateTime in specific time zone**|**dateTime with no time zone**|**Appointment and meeting creation time zone**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|**Exchange2007_SP1** <br/> |Yes  <br/> |Yes ( **MeetingTimeZone** )  <br/> |Interpreted as UTC  <br/> |Interpreted as the time zone indicated in the value  <br/> |Elements within the [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) or [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) element that contains the **MeetingTimeZone** element are interpreted as the time zone in the **MeetingTimeZone** element, all others interpreted as UTC  <br/> |Time zone in **MeetingTimeZone** element  <br/> |
|**Exchange2007_SP1** <br/> |Yes  <br/> |No  <br/> |Interpreted as UTC  <br/> |Interpreted as the time zone indicated in the value  <br/> |Interpreted as UTC  <br/> |UTC  <br/> |
|**Exchange2007_SP1** <br/> |No  <br/> |Yes ( **MeetingTimeZone** )  <br/> |Interpreted as UTC  <br/> |Interpreted as the time zone indicated in the value  <br/> |Elements within the [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) or [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) element that contains the **MeetingTimeZone** element are interpreted as the time zone in the **MeetingTimeZone** element, all others interpreted as UTC  <br/> |Time zone in **MeetingTimeZone** element  <br/> |
|**Exchange2007_SP1** <br/> |No  <br/> |No  <br/> |Interpreted as UTC  <br/> |Interpreted as the time zone indicated in the value  <br/> |Interpreted as UTC  <br/> |UTC  <br/> |
|**Exchange2010** and later  <br/> |Yes  <br/> |Yes ( **StartTimeZone** and/or **EndTimeZone** )  <br/> |Interpreted as UTC  <br/> |Interpreted as the time zone indicated in the value  <br/> |If the **StartTimeZone** element is present, the value of the [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) and [ReminderDueBy](https://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx) elements are interpreted as the time zone in the **StartTimeZone** element. Otherwise, the value of those elements are interpreted as the time zone in the **TimeZoneContext** element.  <br/> If the **EndTimeZone** element is present, the value of the [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) element is interpreted as the time zone in the **EndTimeZone** element. Otherwise, the value of the **End** element is interpreted as the time zone in the **TimeZoneContext** element.  <br/> Elements outside the [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) or [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) are interpreted as the time zone in the **TimeZoneContext** element.  <br/> |Time zone in the **StartTimeZone** element if present, time zone in the **TimeZoneContext** element if not  <br/> |
|**Exchange2010** and later  <br/> |Yes  <br/> |No  <br/> |Interpreted as UTC  <br/> |Interpreted as the time zone indicated in the value  <br/> |Interpreted as the time zone in the **TimeZoneContext** element  <br/> |Time zone in the **TimeZoneContext** element  <br/> |
|**Exchange2010** and later  <br/> |No  <br/> |Yes ( **StartTimeZone** and/or **EndTimeZone** )  <br/> |Interpreted as UTC  <br/> |Interpreted as the time zone indicated in the value  <br/> |If the **StartTimeZone** element is present, the value of the [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) and [ReminderDueBy](https://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx) elements are interpreted as the time zone in the **StartTimeZone** element. Otherwise, the value of those elements are interpreted as UTC.  <br/> If the **EndTimeZone** element is present, the value of the [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) element is interpreted as the time zone in the **EndTimeZone** element. Otherwise, the value of the **End** element is interpreted as UTC.  <br/> Elements outside the [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) or [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) are interpreted as UTC.  <br/> |Time zone in the **StartTimeZone** element if present, UTC if not  <br/> |
|**Exchange2010** and later  <br/> |No  <br/> |No  <br/> |Interpreted as UTC  <br/> |Interpreted as the time zone indicated in the value  <br/> |Interpreted as UTC  <br/> |UTC  <br/> |

When interpreting responses from the server, you should always check the value of each element and interpret the value accordingly. Exchange will always include a time zone (either UTC or a specific time zone) in the value.
  
## Additional time zone considerations when creating appointments and meetings

When you create an appointment or meeting, the time zone that applies to the start time is considered the creation time zone for the appointment. In addition to controlling how the date/times are interpreted when an appointment or meeting is created, the creation time zone has the following effects on the item:
  
- If the item is an all-day event, it might display in an unexpected way if viewed from a client that is using a different time zone than the creation time zone. This is because [when an all-day event is created](how-to-create-all-day-events-by-using-ews-in-exchange.md), the start and end time of all-day events are adjusted to midnight of the creation time zone. That time will show as a time other than midnight in a different time zone, so the item may appear to span extra days. Because of this, we recommend that you use the time zone configured for the user's primary calendaring client to create all-day events when possible.

- If the item is a meeting, the creation time zone will be displayed in the Outlook information bar on the meeting requests received by the attendees, if that time zone differs from the time zone of their client.

## In this section

- [Create appointments in a specific time zone by using EWS in Exchange](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)

- [Update the time zone for an appointment by using EWS in Exchange](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)

## See also

- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)

- [EWS schema versions in Exchange](ews-schema-versions-in-exchange.md)

- [Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)

- [Update appointments and meetings by using EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)

- [Create all-day events by using EWS in Exchange](how-to-create-all-day-events-by-using-ews-in-exchange.md)

- [DateTime Structure](https://msdn.microsoft.com/library/system.datetime%28v=vs.110%29.aspx)

- [TimeZoneInfo Class](https://msdn.microsoft.com/library/system.timezoneinfo%28v=vs.110%29.aspx)
