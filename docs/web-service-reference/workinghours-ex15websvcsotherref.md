---
title: "WorkingHours"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- WorkingHours
api_type:
- schema
ms.assetid: bbe97777-f728-46c5-b2aa-565112c24f3a
description: "The WorkingHours element represents the time zone settings and working hours for the requested mailbox user."
---

# WorkingHours

The **WorkingHours** element represents the time zone settings and working hours for the requested mailbox user. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[WorkingHours](workinghours-ex15websvcsotherref.md)
  
```xml
<WorkingHours>
   <TimeZone>...</TimeZone>
   <WorkingPeriodArray>...</WorkingPeriodArray>
</WorkingHours>
```

 **WorkingHours**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[TimeZone (Availability)](timezone-availability.md) <br/> |Contains elements that identify time zone information. This element also contains information about the transition between standard time and daylight saving time. This element is required if the **WorkingHours** element is used.  <br/> |
|[WorkingPeriodArray](workingperiodarray.md) <br/> |Contains working period information for the mailbox user. This element is required if the **WorkingHours** element is used.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FreeBusyView](freebusyview.md) <br/> |Contains availability information for a specific user.  <br/> The following is the XPath expression to this element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/` <br/> |
   
## Remarks

All the child elements are listed in the sequence in which they occur. The level of detail provided by this element depends on the permissions granted to the requestor.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetUserAvailability operation](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

