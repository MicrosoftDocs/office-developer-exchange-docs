---
title: "Recurrence patterns and EWS"
 
 
manager: luken
ms.date: 03/9/2015
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: fd9ef706-1e01-49fa-af6f-2f6d3e173c16
description: "Learn about recurrence patterns and recurring series in Exchange."
---

# Recurrence patterns and EWS

Learn about recurrence patterns and recurring series in Exchange.
  
A recurring series is an appointment or meeting that repeats according to a defined pattern. A recurring series can either have a specific number of occurrences or can repeat indefinitely. Additionally, a recurring series can have exceptions that don't follow the pattern of the rest of the occurrences, and can have occurrences that have been deleted from the pattern. You can use the EWS Managed API and EWS to work with recurring series and their associated calendar items.
  
## Recurring calendar items

All calendar items fall into one of the following four categories:
  
- Non-recurring calendar items
    
- Recurring masters
    
- Occurrences in a series
    
- Modified occurrences in a series, known as exceptions
    
In this article, we'll look at the three types of calendar items that are part of a recurring series.
  
It's helpful to understand how recurring series are implemented on the Exchange server. Instead of creating a separate distinct item for each occurrence in a recurring series, the server creates only one actual item in the calendar, known as the recurring master. The format of a recurring master is very similar to a non-recurring appointment, with the addition of recurrence pattern information. The server then generates occurrences based on the recurrence pattern in response to client requests for appointment information, using a process called expansion. These generated occurrences are not permanently stored on the server. This is important to understand because the way that you search for calendar items determines what information you receive and whether expansion occurs.
  
## Recurrence patterns

The key piece to a recurring series that makes expansion possible is the recurrence pattern. The recurrence pattern is found on the recurring master, and describes a set of criteria for calculating occurrences based on the date and time of the recurring master.
  
**Table 1. Available recurrence patterns**

|**EWS Managed API class**|**EWS element**|**Examples**|
|:-----|:-----|:-----|
|[Recurrence.DailyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.dailypattern%28v=exchg.80%29.aspx) <br/> |[DailyRecurrence](https://msdn.microsoft.com/library/0aaf265d-b723-49c6-8e9c-9ba60141e9ab%28Office.15%29.aspx) <br/> |Repeat every day.  <br/> Repeat every other day.  <br/> |
|[Recurrence.MonthlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.monthlypattern%28v=exchg.80%29.aspx) <br/> |[AbsoluteMonthlyRecurrence](https://msdn.microsoft.com/library/178fa0ae-9dfc-417f-933c-d657d31c2161%28Office.15%29.aspx) <br/> |Repeat every month on the tenth day of the month.  <br/> Repeat every other month on the twenty-first day of the month.  <br/> |
|[Recurrence.RelativeMonthlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativemonthlypattern%28v=exchg.80%29.aspx) <br/> |[RelativeMonthlyRecurrence](https://msdn.microsoft.com/library/a76595db-7460-44ac-ac2a-53241caa33a7%28Office.15%29.aspx) <br/> |Repeat on the second Tuesday of every month.  <br/> Repeat on the third Thursday of the month every three months.  <br/> |
|[Recurrence.RelativeYearlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx) <br/> |[RelativeYearlyRecurrence](https://msdn.microsoft.com/library/25b67876-9979-4a30-a637-357ea10a93b8%28Office.15%29.aspx) <br/> |Repeat on the first Monday of August every year.  <br/> |
|[Recurrence.WeeklyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.weeklypattern%28v=exchg.80%29.aspx) <br/> |[WeeklyRecurrence](https://msdn.microsoft.com/library/69c41dd5-597c-45bc-be3f-e2f2b5615aa3%28Office.15%29.aspx) <br/> |Repeat every Monday.  <br/> Repeat every Tuesday and Thursday every other week.  <br/> |
|[Recurrence.YearlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx) <br/> |[AbsoluteYearlyRecurrence](https://msdn.microsoft.com/library/96f53e2c-3893-4f6e-a78a-ac179f45c5db%28Office.15%29.aspx) <br/> |Repeat on September 1st every year.  <br/> |
   
The other important piece of information for a recurrence pattern is when the recurrence ends. This can be expressed as either a set number of occurrences, as an end date, or as having no end.
  
**Table 2. Options for the end of a recurring series**

|**EWS Managed API method/property**|**EWS element**|**Description**|
|:-----|:-----|:-----|
|[Recurrence.NumberOfOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.numberofoccurrences%28v=exchg.80%29.aspx) <br/> |[NumberedRecurrence](https://msdn.microsoft.com/library/53746909-ef21-4764-8715-a7769b943cca%28Office.15%29.aspx) <br/> |The value of this property or element specifies the number of occurrences.  <br/> |
|[Recurrence.EndDate](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) <br/> |[EndDateRecurrence](https://msdn.microsoft.com/library/a5ee2504-db84-49ee-870c-cca9269f2e26%28Office.15%29.aspx) <br/> |The last occurrence in the series falls on or before the date specified by this property or element.  <br/> |
|[Recurrence.HasEnd](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.hasend%28v=exchg.80%29.aspx) <br/> [Recurrence.NeverEnds](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.neverends%28v=exchg.80%29.aspx) <br/> |[NoEndRecurrence](https://msdn.microsoft.com/library/ab2ebd9c-388e-45f1-abf9-56e293ef123b%28Office.15%29.aspx) <br/> |The series has no end.  <br/> |
   
## Expanded vs. non-expanded views

Using the **FindAppointments** method in the EWS Managed API (or the **FindItem** operation with a **CalendarView** element in EWS) invokes the expansion process. This hides recurring master appointments from the result set, and instead presents an expanded view of that recurring series. Occurrences of and exceptions to the recurring master that fall within the parameters of the calendar view are included in the result set. Conversely, using the **FindItems** method in the EWS Managed API (or the **FindItem** operation with a **IndexedPageItemView** or **FractionalPageItemView** element in EWS), does not invoke the expansion process, and occurrences and exceptions are not included. Let's look at an example comparing the two methods. 
  
**Table 3. Methods and operations for finding appointments**

|**EWS Managed API method**|**EWS operation**|**Expands series?**|**Items included in results**|
|:-----|:-----|:-----|:-----|
|[ExchangeService.FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) <br/> |[FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with a [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element  <br/> |Yes  <br/> |Non-recurring appointments, single occurrences of recurring series, and exceptions to recurring series  <br/> |
|[ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with an [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or [FractionalPageItemView](https://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx) element  <br/> |No  <br/> |Non-recurring appointments and recurring master appointments  <br/> |
   
Sadie has just signed her son up for swim team. The team has practice every Wednesday morning at 8:30 AM, starting July 2, with the last practice being on August 6. Not wanting to forget about practice, Sadie adds a recurring appointment to her calendar to remind her.
  
**Table 4. Sadie's recurring appointment**

|**Appointment field**|**Value**|
|:-----|:-----|
|Subject  <br/> |Swim Team Practice  <br/> |
|Start  <br/> |July 2, 2014 8:30 AM  <br/> |
|End  <br/> |July 2, 2014 10:00 AM  <br/> |
|Recurs  <br/> |Every Wednesday  <br/> |
|Last occurrence  <br/> |August 6, 2014 8:30 AM  <br/> |
   
A quick look at a calendar shows that the team will have a total of six practices. However, there aren't six distinct appointment items in the calendar. Instead, there is just one recurring master appointment representing the series.
  
Now let's look at finding appointments on Sadie's calendar that occur within the month of July. The following code example uses the **FindItems** method in the Exchange Managed API to produce a non-expanded view of Sadie's calendar. 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
#region FindItems + ItemView method
ItemView itemView = new ItemView(100);
itemView.PropertySet = propSet;
List<SearchFilter> filterList = new List<SearchFilter>();
// Find appointments that start after midnight on July 1, 2014.
SearchFilter.IsGreaterThan startFilter = new SearchFilter.IsGreaterThan(AppointmentSchema.Start,
    new DateTime(2014, 7, 1));
// Find appointments that end before midnight on July 31, 2014
SearchFilter.IsLessThan endFilter = new SearchFilter.IsLessThan(AppointmentSchema.End,
    new DateTime(2014, 7, 31));
filterList.Add(startFilter);
filterList.Add(endFilter);
SearchFilter.SearchFilterCollection calendarFilter = new SearchFilter.SearchFilterCollection(LogicalOperator.And, filterList);
// This results in a call to EWS.
FindItemsResults<Item> results = service.FindItems(WellKnownFolderName.Calendar, calendarFilter, itemView);
foreach(Item appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

That code results in the following [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with an [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="100" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:And>
          <t:IsGreaterThan>
            <t:FieldURI FieldURI="calendar:Start" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-01T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsGreaterThan>
          <t:IsLessThan>
            <t:FieldURI FieldURI="calendar:End" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-31T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsLessThan>
        </t:And>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

The server's response includes only a single item, the recurring master, indicated by the [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) element value of **RecurringMaster**. The value of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>RecurringMaster</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

Now let's compare with an expanded view. The following code example uses the **FindAppointments** method in the EWS Managed API to create an expanded view of Sadie's calendar. 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
CalendarView calView = new CalendarView(new DateTime(2014, 7, 1),
    new DateTime(2014, 7, 31));
calView.PropertySet = propSet;
FindItemsResults<Appointment> results = service.FindAppointments(WellKnownFolderName.Calendar, calView);
foreach(Appointment appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

This code results in the following [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with a [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView StartDate="2014-07-01T07:00:00.000Z" EndDate="2014-07-31T07:00:00.000Z" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

This time, the server response includes five occurrences, one for each Wednesday in July. The [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) elements on these items all have a value of **Occurrence**. Note that the recurring master is not present in the response. The values of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) elements have been shortened for readability. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="5" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA6..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-09T15:30:00Z</t:Start>
                <t:End>2014-07-09T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA8..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-16T15:30:00Z</t:Start>
                <t:End>2014-07-16T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA9..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-23T15:30:00Z</t:Start>
                <t:End>2014-07-23T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADAA..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-30T15:30:00Z</t:Start>
                <t:End>2014-07-30T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

After you have a recurring master, an occurrence, or an exception, you can always [retrieve the other related items](how-to-access-a-recurring-series-by-using-ews-in-exchange.md). Given an occurrence or exception, you can retrieve the recurring master, and vice versa.
  
## Working with recurring calendar items

You use all the same methods and operations to work with recurring series as you use to work with non-recurring calendar items. The difference is that, depending on the item you use to invoke those methods or operations, the actions you take can apply to the entire series, or just a single occurrence. [Actions taken on the recurring master](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) will apply to all occurrences in the series, while [actions taken to a single occurrence or exception](how-to-update-a-recurring-series-by-using-ews.md) will only apply to that occurrence or exception. 
  
## In this section

- [Access a recurring series by using EWS in Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Create a recurring series by using EWS in Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Delete appointments in a recurring series by using EWS in Exchange](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Update a recurring series by using EWS](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Update a recurring series by using EWS in Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
## See also


- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)
    
- [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

