---
title: "EndTime"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- EndTime
api_type:
- schema
ms.assetid: 82e4ef4f-a557-4044-b9b7-d91622f4ac55
description: "The EndTime element represents the end of a time span."
---

# EndTime

The **EndTime** element represents the end of a time span. 
  
```xml
<EndTime>dateTime</EndTime>
```

 **dateTime**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[TimeWindow](timewindow.md) <br/> |Identifies the time span queried for the user availability information.<br/><br/> The following is the XPath expression to this element:<br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Identifies the time span that is queried for detailed information about suggested meeting times.<br/><br/> The following is the XPath expression to this element:<br/><br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.  <br/> |
|[Duration (UserOofSettings)](duration-useroofsettings.md) <br/> | Specifies the duration for which the Out of Office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.  <br/><br/>  The following are the possible XPath expressions to this element:<br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[Occurrence](occurrence.md) <br/> |Represents a single modified occurrence of a recurring calendar item.  <br/> |
|[CalendarEvent](calendarevent.md) <br/> |Represents a unique calendar item occurrence. This is used for Availability inquiries. The **EndTime** element is required in the **CalendarEvent** element. The **EndTime** element in the **CalendarEvent** element is unique to the **CalendarEvent** type.<br/><br/> The following is the XPath expression to this element:<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## Text value

A text value is required.
  
## Remarks

The [StartTime](starttime.md) element represents the beginning of a time span. 
  
The end time represents the client's time.
  
The schema includes many [EndTime](endtime.md) elements. 
  
> [!NOTE]
> The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed. 
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetUserAvailability operation](getuseravailability-operation.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

