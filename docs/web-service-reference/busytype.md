---
title: "BusyType"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- BusyType
api_type:
- schema
ms.assetid: 26d4fae0-8c78-4705-b5e8-d6033712c41e
description: "The BusyType element represents the free/busy status set for a calendar event."
---

# BusyType

The **BusyType** element represents the free/busy status set for a calendar event. 
  
```xml
<BusyType>Free or Tentative or Busy or OOF or NoData</BusyType>
```

 **BusyType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[IndividualAttendeeConflictData](individualattendeeconflictdata.md) <br/> |Contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time.  <br/> The following is the XPath expression to this element:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/IndividualAttendeeConflictData` <br/> |
|[CalendarEvent](calendarevent.md) <br/> |Represents a unique calendar item occurrence.  <br/> The following is the XPath expression to this element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## Text value

A text value is required for this element. The value is a string type. The following are the possible values for the [BusyType](busytype.md) element: 
  
- Free
    
- Tentative
    
- Busy
    
- OOF
    
- NoData
    
## Remarks

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

