---
title: "FreeBusyViewType"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FreeBusyViewType
api_type:
- schema
ms.assetid: 7c7f82ba-fa52-4a3e-bec7-39d373c66fc7
description: "The FreeBusyViewType element represents the type of free/busy information returned in the response."
---

# FreeBusyViewType

The **FreeBusyViewType** element represents the type of free/busy information returned in the response. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[FreeBusyViewType](freebusyviewtype.md)
  
```xml
<FreeBusyViewType>None or MergedOnly or FreeBusy or FreeBusyMerged or Detailed or DetailedMerged</FreeBusyViewType>
```

 **FreeBusyViewType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FreeBusyView](freebusyview.md) <br/> |Contains availability information for a specific user.  <br/> The following is the XPath expression to this element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## Text value

A text value is required. The following table lists the possible values for this element.
  
|**Value**|**Description**|
|:-----|:-----|
|None  <br/> |This value is not valid for requests. This value is valid for responses.  <br/> |
|MergedOnly  <br/> |Represents an aggregated free/busy stream. In cross-forest scenarios in which the target user in one forest does not have an Availability service configured, the Availability service of the requestor retrieves the target user's free/busy information from the free/busy public folder. Because public folders only store free/busy information in merged form, **MergedOnly** is the only available information.  <br/> |
|FreeBusy  <br/> |Represents the legacy status information: free, busy, tentative, and OOF. This also includes the start/end times of the appointments. This view is richer than the legacy free/busy view because individual meeting start and end times are provided instead of an aggregated free/busy stream.  <br/> |
|FreeBusyMerged  <br/> |Represents all the properties in **FreeBusy** with a stream of merged free/busy availability information.  <br/> |
|Detailed  <br/> |Represents the legacy status information: free, busy, tentative, and OOF; the start/end times of the appointments; and various properties of the appointment such as subject, location, and importance. This requested view will return the maximum amount of information for which the requesting user is privileged. If merged free/busy information only is available, as with requesting information for users in a Microsoft Exchange Server 2003 forest, **MergedOnly** will be returned. Otherwise, **FreeBusy** or **Detailed** will be returned.  <br/> If **Detailed** is specified for a distribution list, the free/busy information for the members of the list is merged, and **MergedOnly** is returned.  <br/> |
|DetailedMerged  <br/> |Represents all the properties in **Detailed** with a stream of merged free/busy availability information. If only merged free/busy information is available, for example if the mailbox exists on a computer running Exchange 2003, **MergedOnly** will be returned. Otherwise, **FreeBusyMerged** or **DetailedMerged** will be returned.  <br/> |
   
## Remarks

This element is required if the [FreeBusyView](freebusyview.md) element is used. The type of free/busy information returned is designated in the [RequestedView](requestedview.md) element. The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed. 
  
The following table shows what is returned for the different view types and the corresponding MAPI property. Each view type builds upon the former view type.
  
|**FreeBusyViewType**|**Properties**|**MAPI Calendar Property**|
|:-----|:-----|:-----|
|**MergedOnly** <br/> |MergedFreeBusyStream  <br/> ||
|**FreeBusy** <br/> |Classical status  <br/> |PropTag (0x80860003)  <br/> |
|**FreeBusy** <br/> |Working hours  <br/> ||
|**FreeBusy** <br/> |Start time  <br/> |PR_START_DATE  <br/> |
|**FreeBusy** <br/> |End time  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |Classical status  <br/> |PropTag (0x80860003)  <br/> |
|**FreeBusyMerged** <br/> |Working hours  <br/> ||
|**FreeBusyMerged** <br/> |Start time  <br/> |PR_START_DATE  <br/> |
|**FreeBusyMerged** <br/> |End time  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**Detailed** <br/> |Classical status  <br/> |PropTag (0x80860003)  <br/> |
|**Detailed** <br/> |Working hours  <br/> ||
|**Detailed** <br/> |Start time  <br/> |PR_START_DATE  <br/> |
|**Detailed** <br/> |End time  <br/> |PR_END_DATE  <br/> |
|**Detailed** <br/> |Subject  <br/> |PR_SUBJECT  <br/> |
|**Detailed** <br/> |Location  <br/> |PR_LOCATION  <br/> |
|**Detailed** <br/> |Entry-Id(unless private)  <br/> ||
|**Detailed** <br/> |Private Flag  <br/> ||
|**Detailed** <br/> |IsMeeting  <br/> ||
|**Detailed** <br/> |IsRecurring  <br/> ||
|**Detailed** <br/> |IsException  <br/> ||
|**Detailed** <br/> |IsReminderSet  <br/> ||
|**Detailed** <br/> |Out of Office Message (if requested)  <br/> ||
|**DetailedMerged** <br/> |Classical status  <br/> |PropTag (0x80860003)  <br/> |
|**DetailedMerged** <br/> |Working hours  <br/> ||
|**DetailedMerged** <br/> |Start time  <br/> |PR_START_DATE  <br/> |
|**DetailedMerged** <br/> |End time  <br/> |PR_END_DATE  <br/> |
|**DetailedMerged** <br/> |Subject  <br/> |PR_SUBJECT  <br/> |
|**DetailedMerged** <br/> |Location  <br/> |PR_LOCATION  <br/> |
|**DetailedMerged** <br/> |Entry-Id(unless private)  <br/> ||
|**DetailedMerged** <br/> |Private Flag  <br/> ||
|**DetailedMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**DetailedMerged** <br/> |IsMeeting  <br/> ||
|**DetailedMerged** <br/> |IsRecurring  <br/> ||
|**DetailedMerged** <br/> |IsException  <br/> ||
|**DetailedMerged** <br/> |IsReminderSet  <br/> ||
   
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

