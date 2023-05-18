---
title: "DayQuality"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DayQuality
api_type:
- schema
ms.assetid: cd0eb239-6e7f-4a5a-b245-659f170550b7
description: "The DayQuality element represents the quality of the day for containing quality suggested meeting times."
---

# DayQuality

The **DayQuality** element represents the quality of the day for containing quality suggested meeting times. 
  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)  
- [SuggestionsResponse](suggestionsresponse.md) 
- [SuggestionDayResultArray](suggestiondayresultarray.md)  
- [SuggestionDayResult](suggestiondayresult.md) 
- [DayQuality](dayquality.md)
  
```xml
<DayQuality>Excellent or Good or Fair or Poor</DayQuality>
```

**SuggestionQuality**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SuggestionDayResult](suggestiondayresult.md) |Represents a single day that contains suggested meeting times. <br/>The following is the XPath 2.0 expression to this element: <br/>`/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` |

## Text value

A text value is required. The following are the possible values for this element:
  
- **Excellent**
- **Good**
- **Fair**
- **Poor**

## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace | https://schemas.microsoft.com/exchange/services/2006/types |
|Schema Name | Types schema |
|Validation File | Types.xsd |
|Can be Empty | False |

## See also

- [GetUserAvailability operation](getuseravailability-operation.md)  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
