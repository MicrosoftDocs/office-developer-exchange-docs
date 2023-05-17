---
title: "ReadItems (CalendarPermissionType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ReadItems
api_type:
- schema
ms.assetid: bec01982-26a1-4373-b1e6-2e0c838d83c4
description: "The ReadItems element indicates whether a user has permission to read items within a Calendar folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# ReadItems (CalendarPermissionType)

The **ReadItems** element indicates whether a user has permission to read items within a Calendar folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<ReadItems>None or TimeOnly or TimeAndSubjectAndLocation or FullDetails</ReadItems>
```

 **CalendarPermissionReadAccessType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CalendarPermission](calendarpermission.md) <br/> |Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.  <br/> |
   
## Text value

The following table lists the possible values for the **ReadItems** element. 
  
**ReadItems element text values**

|**Value**|**Description**|
|:-----|:-----|
|None  <br/> |Indicates that the user does not have permission to view items in the calendar.  <br/> |
|TimeOnly  <br/> |Indicates that the user has permission to view only free/busy time in the calendar.  <br/> |
|TimeAndSubjectAndLocation  <br/> |Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.  <br/> |
|FullDetails  <br/> |Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

- [Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)
