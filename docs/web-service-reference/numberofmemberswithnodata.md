---
title: "NumberOfMembersWithNoData"
description: "The NumberOfMembersWithNoData element represents the number of distribution list members who do not have published free/busy data to compare to a suggested meeting time. This element represents members of a distribution list that is too large or members who have No Data status."
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- NumberOfMembersWithNoData
api_type:
- schema
ms.assetid: 7ca9c57c-9519-442c-a9f4-dca2b0309716
---

# NumberOfMembersWithNoData

The **NumberOfMembersWithNoData** element represents the number of distribution list members who do not have published free/busy data to compare to a suggested meeting time. This element represents members of a distribution list that is too large or members who have **No Data** status. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[SuggestionsResponse](suggestionsresponse.md)
  
[SuggestionDayResultArray](suggestiondayresultarray.md)
  
[SuggestionDayResult](suggestiondayresult.md)
  
[SuggestionArray](suggestionarray.md)
  
[Suggestion](suggestion.md)
  
[AttendeeConflictDataArray](attendeeconflictdataarray.md)
  
[GroupAttendeeConflictData](groupattendeeconflictdata.md)
  
[NumberOfMembersWithNoData](numberofmemberswithnodata.md)
  
```xml
<NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
```

**int**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GroupAttendeeConflictData](groupattendeeconflictdata.md) <br/> |Contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.  <br/> The following is the XPath expression to this element:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData` <br/> |
   
## Remarks

A contact in a group who does not have a mailbox is an example of a distribution list member who does not have calendar data. A contact may also have **No Data** status for the following reasons: 
  
- Permissions are insufficient.
    
- The distribution list is too large to expand.
    
- The Active Directory directory service is unavailable.
    
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|Item|value|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

[GetUserAvailability operation](getuseravailability-operation.md)  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
[Getting User Availability](/previous-versions/office/developer/exchange-server-2010/aa494212(v=exchg.140))
