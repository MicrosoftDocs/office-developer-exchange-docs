---
title: "ResolutionSet"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ResolutionSet
api_type:
- schema
ms.assetid: 43d5b876-0e87-4414-9b1d-bff1c1ec825c
description: "The ResolutionSet element contains an array of resolutions for an ambiguous name."
---

# ResolutionSet

The **ResolutionSet** element contains an array of resolutions for an ambiguous name. 
  
[ResolveNamesResponse](resolvenamesresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
  
[ResolutionSet](resolutionset.md)
  
```xml
<ResolutionSet IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Resolution/>
</ResolutionSet>
```

 **ArrayOfResolutionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |Represents the next index that should be used for the next request when you are using an indexed page view.  <br/> |
|**NumeratorOffset** <br/> |Represents the new numerator value to use for the next request when you are using fraction page views.  <br/> |
|**AbsoluteDenominator** <br/> |Represents the next denominator to use for the next request when you are using fraction page views.  <br/> |
|**IncludesLastItemInRange** <br/> |This attribute will be true if the current results contain the last item in the query, so that additional paging is not needed.  <br/> |
|**TotalItemsInView** <br/> |Represents the total number of items in the view.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Resolution](resolution.md) <br/> |Contains a single resolved entity.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Contains the status and result of a ResolveNames request.  <br/> |
   
## Remarks

A **ResolutionSet** element can contain a maximum of 100 resolved entities. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[ResolveNames](resolvenames.md)
  
[ResolveNamesResponse](resolvenamesresponse.md)
  
[ResolveNames operation](resolvenames-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

