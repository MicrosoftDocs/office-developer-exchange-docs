---
title: "Assignees"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 20ef18c2-daa0-4f65-a515-e84e9993a77f
description: "The Assignees element specifies the people to whom a task is assigned."
---

# Assignees

The **Assignees** element specifies the people to whom a task is assigned. 
  
```XML
<Assignees>
    <Name></Name>
    <UserID></UserID>
</Assignees>
```

 **EmailUserType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Name (EmailAddress)](name-emailaddress.md) <br/> |Represents the display name of the mailbox user.  <br/> |
|[UserId (string)](userid-string.md) <br/> |Specifies the user identifier of an email user.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[TaskSuggestion](tasksuggestion.md) <br/> |Specifies a proposed task.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

