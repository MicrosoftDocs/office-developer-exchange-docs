---
title: "Create appointments in a specific time zone by using EWS in Exchange"
manager: sethgros
ms.date: 02/04/2023
ms.audience: Developer 
ms.localizationpriority: medium
ms.assetid: e68aaa27-250e-4170-b099-077a979c127c
description: Create appointments in specific time zones by using the EWS Managed API or EWS in Exchange
---

# Create appointments in a specific time zone by using EWS in Exchange

When an appointment or meeting is created on an Exchange calendar, the time zone used to specify the start and end times is saved as the creation time zone for the appointment. That time zone is also used to [interpret date and time values that do not have an explicit time zone specified](time-zones-and-ews-in-exchange.md), so it is important to understand your options to specify the time zone.
  
## Create appointments in different time zones by using the EWS Managed API

When creating appointments or meetings using the EWS Managed API, you have three options for specifying the time zone:
  
- To use the time zone of the computer where your EWS Managed API is executing, do not specify a time zone when creating the [ExchangeService](/dotnet/api/microsoft.exchange.webservices.data.exchangeservice) object. 
    
- To use a specific time zone for all date/time properties, including properties when creating a new appointment or meeting, specify a time zone in the constructor for the **ExchangeService** object. 
    
- To use a different time zone than the one specified in the [ExchangeService.TimeZone](/dotnet/api/microsoft.exchange.webservices.data.exchangeservice.timezone) property, use the [Appointment.StartTimeZone](/dotnet/api/microsoft.exchange.webservices.data.appointment.starttimezone) and [Appointment.EndTimeZone](/dotnet/api/microsoft.exchange.webservices.data.appointment.endtimezone) properties. 

> [!NOTE]
> The **EndTimeZone** property is only available when the [ExchangeService.RequestedServerVersion](/dotnet/api/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion) property is set to **Exchange2010** or later. If it's not available, setting the **StartTimeZone** applies to both the start and end times of the appointment. 
  
In the following example, the EWS Managed API is used to create three appointments. Each appointment is set to start at 1:00 PM two days from now, in an unspecified time zone, and end one hour later. The first appointment is created in the client computer's time zone by using default EWS Managed API behavior. The second is created in the Central time zone by using the **Appointment.StartTimeZone** and **Appointment.EndTimeZone** properties, in this case we also set the TimeZoneDescription Extended Property to the same value as TimeZone being used. The third is created in the Mountain time zone by using the **ExchangeService.TimeZone** property. 
  
```cs
using Microsoft.Exchange.WebServices.Data;
using System.Security;
static void CreateAppointments(string userEmail, SecureString userPass)
{
    // *****************************************************
    // Create an appointment using the client computer's time zone.
    // *****************************************************
    // Do not specify a time zone when creating the ExchangeService.
    ExchangeService clientTZService = new ExchangeService(ExchangeVersion.Exchange2010);
    clientTZService.Credentials = new NetworkCredential(userEmail, userPass);
    clientTZService.AutodiscoverUrl(userEmail, redirectionCallback);
    // Create the appointment.
    Appointment clientTZAppt = new Appointment(clientTZService);
    clientTZAppt.Subject = "Appointment created using client time zone";
    clientTZAppt.Body = new MessageBody(string.Format("Time zone: {0}", clientTZService.TimeZone.DisplayName));
    // Set the start time to 1:00 PM two days from today.
    DateTime startTime = new DateTime(DateTime.Now.Year, DateTime.Now.Month, DateTime.Now.Day + 2);
    startTime = startTime.AddHours(13);
    clientTZAppt.Start = startTime;
    // Set the end time to 2:00 PM on that same day.
    DateTime endTime = startTime.AddHours(1);
    clientTZAppt.End = endTime;
    // Save the appointment to the default calendar.
    try
    {
        // This method results in a call to EWS.
        clientTZAppt.Save(SendInvitationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving appointment: {0}", ex.Message);
    }
    // *****************************************************
    // Create an appointment in the Central time zone by
    // using the StartTimeZone property.
    // *****************************************************
    // Extended Property for the TimeZone Description
    ExtendedPropertyDefinition tzDescription = new ExtendedPropertyDefinition(DefaultExtendedPropertySet.Appointment, 33332, MapiPropertyType.String);
    // Retrieve the Central time zone.
    TimeZoneInfo centralTZ = TimeZoneInfo.FindSystemTimeZoneById("Central Standard Time");
    // Create the appointment.
    Appointment centralTZAppt = new Appointment(clientTZService);
    centralTZAppt.Subject = "Appointment created using Central time zone";
    centralTZAppt.Body = new MessageBody(string.Format("Time zone: {0}", centralTZ.DisplayName));
    // Set the time zone on the appointment.
    centralTZAppt.StartTimeZone = centralTZ;
    centralTZAppt.EndTimeZone = centralTZ;
    // Set the start time to 1:00 PM two days from today.
    centralTZAppt.Start = startTime;
    // Set the end time to 2:00 PM on that same day.
    centralTZAppt.End = endTime;
    // Set the TimeZone Description on the appointment/meeting
    centralTZAppt.SetExtendedProperty(tzDescription, centralTZ.DisplayName);
    // Save the appointment to the default calendar.
    try
    {
        // This method results in a call to EWS.
        centralTZAppt.Save(SendInvitationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving appointment: {0}", ex.Message);
    }
    // *****************************************************
    // Create an appointment in the Mountain time zone by
    // using the ExchangeService.TimeZone property.
    // *****************************************************
    // Specify the Mountain time zone when creating the ExchangeService.
    TimeZoneInfo mountainTZ = TimeZoneInfo.FindSystemTimeZoneById("Mountain Standard Time");
    ExchangeService mountainTZService = new ExchangeService(ExchangeVersion.Exchange2010, mountainTZ);
    mountainTZService.Credentials = new NetworkCredential(userEmail, userPass);
    mountainTZService.AutodiscoverUrl(userEmail, redirectionCallback);
    // Create the appointment.
    Appointment mountainTZAppt = new Appointment(mountainTZService);
    mountainTZAppt.Subject = "Appointment created using Mountain time zone";
    mountainTZAppt.Body = new MessageBody(string.Format("Time zone: {0}", mountainTZService.TimeZone.DisplayName));
    // Set the start time to 1:00 PM two days from today.
    mountainTZAppt.Start = startTime;
    // Set the end time to 2:00 PM on that same day.
    mountainTZAppt.End = endTime;
    // Save the appointment to the default calendar.
    try
    {
        // This method results in a call to EWS.
        mountainTZAppt.Save(SendInvitationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving appointment: {0}", ex.Message);
    }
}
```

> [!NOTE]
> In the second example, the TimeZoneDescription Extended Property need to be set to avoid a potention issue when meeting updates are being sent out to enternal recipient. 

When this example is executed on a client computer configured in the Eastern time zone, and the three appointments it creates are viewed from a client configured in the Eastern time zone, they appear at 1:00 PM, 2:00 PM, and 3:00 PM, respectively.
  
## Create appointments in different time zones by using EWS

When creating appointments or meetings using EWS, you have three options for specifying the time zone:
  
- To use Coordinated Universal Time (UTC), do not include a [TimeZoneContext](/exchange/client-developer/web-service-reference/timezonecontex.md) element, [MeetingTimeZone](/exchange/client-developer/web-service-reference/meetingtimezone.md) element (Exchange 2007 only), or [StartTimeZone](/exchange/client-developer/web-service-reference/starttimezone.md) and [EndTimeZone](/exchange/client-developer/web-service-reference/endtimezone.md) elements (Exchange 2010 and later) in the [CreateItem operation](/exchange/client-developer/web-service-reference/createitem-operation.md) request. 
    
- To use a specific time zone for all date/time properties, including properties when creating a new appointment or meeting, specify a time zone in the [TimeZoneContext](/exchange/client-developer/web-service-reference/timezonecontext.md) element in the [CreateItem operation](/exchange/client-developer/web-service-reference/createitem-operation.md) request. 
    
- To use a different time zone than the one specified in the [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, include a [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) element (Exchange 2007 only), or [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements (Exchange 2010 and later) in the [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request. 
    
The following example [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request creates an appointment using UTC. Notice that the **TimeZoneContext** element, the **StartTimeZone** element, and the **EndTimeZone** element are absent. The **Start** and **End** element values are expressed in UTC. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Appointment created using UTC</t:Subject>
          <t:Body BodyType="HTML">Time zone: UTC</t:Body>
          <t:Start>2023-02-07T17:00:00.000Z</t:Start>
          <t:End>2023-02-07T18:00:00.000Z</t:End>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

The following example [CreateItem operation](/exchange/client-developer/web-service-reference/createitem-operation.md) request uses the **StartTimeZone** and **EndTimeZone** elements to specify the Central time zone for the appointment. Notice that the **TimeZoneContext** element is absent. However, if it were present, the values of the **StartTimeZone** and **EndTimeZone** elements would override its value. Again, the **Start** and **End** element values are expressed in UTC. We also set the TimeZoneDescription Extended Property to the same value as TimeZone being used.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Appointment created using Central time zone</t:Subject>
          <t:Body BodyType="HTML">Time zone: (UTC-06:00) Central Time (US &amp;amp; Canada)</t:Body>
          <t:ExtendedProperty>
             <t:ExtendedFieldURI DistinguishedPropertySetId="Appointment" PropertyId="33332" PropertyType="String" />
             <t:Value>(UTC-06:00) Central Time (US &amp; Canada)</t:Value>
          </t:ExtendedProperty>
          <t:Start>2023-02-07T18:00:00.000</t:Start>
          <t:End>2023-02-07T19:00:00.000</t:End>
          <t:StartTimeZone Id="Central Standard Time" />
          <t:EndTimeZone Id="Central Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

The following example [CreateItem operation](/exchange/client-developer/web-service-reference/createitem-operation.md) request sets the **TimeZoneContext** element to the Mountain time zone. Notice that the **StartTimeZone** and **EndTimeZone** elements are absent. Again, the **Start** and **End** element values are expressed in UTC. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Mountain Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Appointment created using Mountain time zone</t:Subject>
          <t:Body BodyType="HTML">Time zone: (UTC-07:00) Mountain Time (US &amp;amp; Canada)</t:Body>
          <t:Start>2023-02-07T19:00:00.000</t:Start>
          <t:End>2023-02-07T20:00:00.000</t:End>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

When the three appointments created by the previous EWS example requests are viewed from a client configured in the Eastern time zone, they appear at 1:00 PM, 2:00 PM, and 3:00 PM, respectively. 

Now that you know how to create appointments in specific time zones, you can [update the time zones on existing appointments](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md) to a different one. 
  
## See also

- [Time zones and EWS in Exchange](time-zones-and-ews-in-exchange.md)
    
- [Update the time zone for an appointment by using EWS in Exchange](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
- [Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
