---
title: "Member"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Member
api_type:
- schema
ms.assetid: af9c5ff8-02a4-41fc-876d-14ac05f1ee77
description: "The Member element represents a member of a distribution list."
---

# Member

The **Member** element represents a member of a distribution list. 
  
```xml
<Member Key="">
   <Mailbox/>
   <Status/>
</Member>
```

**MemberType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Key  <br/> |Provides a unique identifier for the distribution list member. This attribute is optional.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |Represents the e-mail address of the distribution list member. This element is optional.  <br/> |
|[Status (MemberStatusType)](status-memberstatustype.md) <br/> |Provides information about the status of a distribution list member. This element is optional.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Members (MemberListType)](members-memberlisttype.md) <br/> |Contains a list of distribution list members.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

