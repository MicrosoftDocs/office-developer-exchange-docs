---
title: "MaximumResultsByDay"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaximumResultsByDay
api_type:
- schema
ms.assetid: d581a12a-2b8e-4960-ae14-c8c4aa0b1849
description: "The MaximumResultsByDay element specifies the number of suggested meeting times per a day returned in the response."
---

# MaximumResultsByDay

The **MaximumResultsByDay** element specifies the number of suggested meeting times per a day returned in the response. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[SuggestionsViewOptions](suggestionsviewoptions.md)
  
[MaximumResultsByDay](maximumresultsbyday.md)
  
```
<MaximumResultsByDay>...</MaximumResultsByDay>
```

 **int**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SuggestionsViewOptions](suggestionsviewoptions.md) <br/> |Contains the options for obtaining meeting suggestion information.  <br/> The following is the XPath to this element:  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## Text value

A text value is required. The text value represents an integer.
  
## Remarks

This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used. 
  
> [!NOTE]
> The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed. 
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[GetUserAvailability operation](getuseravailability-operation.md)
#### Other resources

[Getting User Availability](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

