---
title: "Add appointments by using Exchange impersonation"
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: 78d5e51b-900f-4302-b9a8-fdc9aa4b65a5
description: "Learn how to use impersonation with the EWS Managed API or EWS in Exchange to add appointments to users' calendars."
localization_priority: Priority
---

# Add appointments by using Exchange impersonation

Learn how to use impersonation with the EWS Managed API or EWS in Exchange to add appointments to users' calendars.
  
You can create a service application that inserts appointments directly into an Exchange calendar by using a service account that has the **ApplicationImpersonation** [role enabled](how-to-configure-impersonation.md). When you use impersonation, the application is acting as the user; it's as if the user added the appointment to the calendar by using a client such as Outlook.
  
When you are using impersonation, keep in mind the following:
  
- Your [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx) object must be bound to the service account. You can use the same **ExchangeService** object to impersonate multiple accounts by changing the [ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) property for each account that you want to impersonate.
- Any item that you save to an impersonated account can only be used once. If you want to save the same appointment in multiple accounts, for example, you have to create an [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx) object for each account.

## Prerequisites

Your application needs an account to use to connect to the Exchange server before it can use impersonation. We suggest that you use a service account for the application that has been granted the Application Impersonation role for the accounts that it will be accessing. For more information, see [Configure impersonation](how-to-configure-impersonation.md)
  
## Add appointments by using impersonation with the EWS Managed API

The following example adds an appointment or meeting to the calendar of one or more Exchange accounts. The method takes three parameters.
  
- _service_ — An **ExchangeService** object bound to the service application's account on the Exchange server.
- _emailAddresses_ — A [System.List](https://msdn.microsoft.com/library/6sh2ey19.aspx) object containing a list of SMTP email address strings.
- _factory_ — An object that implements the **IAppointmentFactory** interface. This interface has one method, **GetAppointment** that takes an **ExchangeService** object as a parameter and returns an **Appointment** object. The **IAppointmentFactory** interface is defined [IAppointmentFactory interface](#bk_IAppointmentFactory).

```cs
private static void CreateAppointments(ExchangeService service, List<string> emailAddresses, IAppointmentFactory factory)
{
  // Loop through the list of email addresses to add the appointment.
  foreach (var emailAddress in emailAddresses)
  {
    Console.WriteLine(string.Format("  Placing appointment in calendar for {0}.", emailAddress));
    // Set the email address of the account to get the appointment.
    service.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, emailAddress);
    // Get the appointment to add.
    Appointment appointment = factory.GetAppointment(service);
    // Save the appointment.
    try
    {
      if (appointment.RequiredAttendees.Count > 0)
      {
        // The appointment has attendees so send them the meeting request.
        appointment.Save(SendInvitationsMode.SendToAllAndSaveCopy);
      }
      else
      {
        // The appointment does not have attendees, so just save to calendar.
        appointment.Save(SendInvitationsMode.SendToNone);
      }
    }
    catch (ServiceResponseException ex)
    {
      Console.WriteLine(string.Format("Could not create appointment for {0}", emailAddress));
      Console.WriteLine(ex.Message);
    }
  }
}
```

When saving the appointment, the code checks to determine whether any attendees have been added to the [RequiredAttendees](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx) property. If they have, the [Appointment.Save](https://msdn.microsoft.com/library/dd635394.aspx) method is called with the [SendToAllAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) enumeration value so that the attendees receive meeting requests; otherwise, the **Appointment.Save** method is called with the [SendToNone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) enumeration value so that the appointment is saved into the impersonated user's calendar with the [Appointment.IsMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx) property set to **false**.
  
### IAppointmentFactory interface

<a name="bk_IAppointmentFactory"> </a>

Because you need a new **Appointment** object each time that you want to save an appointment on an impersonated user's calendar, the **IAppointmentFactory** interface abstracts the object used to populate each **Appointment** object. This version is a simple interface that contains only one method, **GetAppointment**, that takes an **ExchangeService** object as a parameter and returns a new **Appointment** object bound to that **ExchangeService** object.
  
```cs
interface IAppointmentFactory
{
  Appointment GetAppointment(ExchangeService service);
}
```

The following **AppointmentFactory** class example shows an implementation of the **IAppointmentFactory** interface that returns a simple appointment that occurs three days from now. If you uncomment the `appointment.RequiredAttendees.Add` line, the **GetAppointment** method will return a meeting and the email address specified in that line will receive a meeting request with the impersonated user listed as the organizer.
  
```cs
class AppointmentFactory : IAppointmentFactory
{
  public Appointment GetAppointment(ExchangeService service)
  {
    // First create the appointment to add.
    Appointment appointment = new Appointment(service);
    // Set the properties on the appointment.
    appointment.Subject = "Tennis lesson";
    appointment.Body = "Focus on backhand this week.";
    appointment.Start = DateTime.Now.AddDays(3);
    appointment.End = appointment.Start.AddHours(1);
    appointment.Location = "Tennis club";
    // appointment.RequiredAttendees.Add(new Attendee("sonyaf@contoso1000.onmicrosoft.com"));
    return appointment;
  }
}

```

## Add appointments by using impersonation with EWS

EWS enables you application to use impersonation to add items to a calendar on behalf the calendar's owner. This example shows how to use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to add an appointment to the calendar of an impersonated account.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>alfred@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Tennis lesson</t:Subject>
          <t:Body BodyType="HTML">Focus on backhand this week.</t:Body>
          <t:ReminderDueBy>2013-09-19T14:37:10.732-07:00</t:ReminderDueBy>
          <t:Start>2013-09-21T19:00:00.000Z</t:Start>
          <t:End>2013-09-21T20:00:00.000Z</t:End>
          <t:Location>Tennis club</t:Location>
          <t:MeetingTimeZone TimeZoneName="Pacific Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Note that other than the addition of the **ExchangeImpersonation** element in the SOAP header to specify the account that we are impersonating, this is the same XML request used to create an appointment without using impersonation.
  
The following example shows the response XML that is returned by the **CreateItem** operation.
  
> [!NOTE]
> The **ItemId** and **ChangeKey** attributes are shortened for readability.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
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
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>

```

Again, this is the same XML that is returned when you use the **CreateItem** operation without using impersonation.
  
## See also

- [Impersonation and EWS in Exchange](impersonation-and-ews-in-exchange.md)
- [ApplicationImpersonation role](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)
- [Configure impersonation](how-to-configure-impersonation.md)
- [Identify the account to impersonate](how-to-identify-the-account-to-impersonate.md)
- [Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
- [CreateItem operation (calendar item)](../web-service-reference/createitem-operation-calendar-item.md)
- [ExchangeService.ImpersonatedUserId property](/dotnet/api/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid?view=exchange-ews-api)
