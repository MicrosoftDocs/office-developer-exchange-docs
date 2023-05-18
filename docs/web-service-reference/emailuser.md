---
title: "EmailUser"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: dc8133ff-c34e-4921-bb56-06e79aee0a8a
description: "The EmailUser element specifies an email recipient."
---

# EmailUser

The **EmailUser** element specifies an email recipient. 
  
```XML
<EmailUser>
    <Name/>
    <UserId/>
</EmailUser>
```

 **EmailUserType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Name (string)](name-string.md) <br/> |Specifies a search refiner name or key or the name of an email user.  <br/> |
|[UserId (string)](userid-string.md) <br/> |Specifies the user identifier of an email user.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Attendees](attendees.md) <br/> |Specifies the recipients of an invitation to a meeting.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Type schema  <br/> |
|Validation File  <br/> |types.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

