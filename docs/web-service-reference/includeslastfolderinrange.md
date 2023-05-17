---
title: "IncludesLastFolderInRange"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- IncludesLastFolderInRange
api_type:
- schema
ms.assetid: 95837904-17be-49b7-831c-de4fb20fccfb
description: "The IncludesLastFolderInRange element indicates whether the last item to synchronize has been included in the response."
---

# IncludesLastFolderInRange

The **IncludesLastFolderInRange** element indicates whether the last item to synchronize has been included in the response. 
  
[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
  
[IncludesLastFolderInRange](includeslastfolderinrange.md)
  
```xml
<IncludesLastFolderInRange/>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contains the status and result of a SyncFolderHierarchy request.  <br/> |
   
## Text value

A text value that represents a Boolean value is required.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[SyncFolderHierarchy operation](syncfolderhierarchy-operation.md)


[EWS reference for Exchange](ews-reference-for-exchange.md)
  
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

