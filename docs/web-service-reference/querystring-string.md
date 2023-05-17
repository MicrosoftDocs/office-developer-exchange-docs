---
title: "QueryString (String)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: "The QueryString element specifies a set of values to be returned that match the query string in a FindPeople operation request. A search with no QueryString specified returns all items from the specified folder."
---

# QueryString (String)

The **QueryString** element specifies a set of values to be returned that match the query string in a [FindPeople operation](findpeople-operation.md) request. A search with no **QueryString** specified returns all items from the specified folder. 
  
```XML
<QueryString/> 
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindPeople](findpeople.md) <br/> |Contains the arguments for a [FindPeople operation](findpeople-operation.md) search.  <br/> |
   
## Text value

The **QueryString** text value represents a mailbox query made by using a subset of [Advanced Query Syntax (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx). For information about the syntax for this element, see [QueryString (QueryStringType)](querystring-querystringtype.md).
  
## Remarks

This element was introduced in Exchange Server 2013.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[FindPeople operation](findpeople-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

