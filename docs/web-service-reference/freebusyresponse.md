---
title: "FreeBusyResponse"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FreeBusyResponse
api_type:
- schema
ms.assetid: 3038d106-9ac9-4ac7-bb43-96c783edbef5
description: "The FreeBusyResponse element contains the free/busy information for a single mailbox user."
---

# FreeBusyResponse

The **FreeBusyResponse** element contains the free/busy information for a single mailbox user. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
```xml
<FreeBusyResponse>
   <ResponseMessage>...</ResponseMessage>
   <FreeBusyView>...</FreeBusyView>
</FreeBusyResponse>
```

 **FreeBusyResponseType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> |Provides descriptive information about the response status.  <br/> |
|[FreeBusyView](freebusyview.md) <br/> |Contains availability information for a specific user.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FreeBusyResponseArray](freebusyresponsearray.md) <br/> |Contains the requested users' availability information and the response status.  <br/> The following is the XPath expression to this element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray` <br/> |
   
## Remarks

This element is not included in a GetUserAvailability response if free/busy information is not requested.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetUserAvailability operation](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

