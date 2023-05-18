---
title: "RoutingType (EmailAddress)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 74d83198-0d9d-4c78-a2bc-9a671859ff37
description: "The RoutingType element represents the routing protocol for the recipient."
---

# RoutingType (EmailAddress)

The **RoutingType** element represents the routing protocol for the recipient. 
  
```XML
<RoutingType/>
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
|[Email (EmailAddressType)](email-emailaddresstype.md) <br/> |Specifies the e-mail address of the MailboxData object. This element is used in the [GetUserAvailability operation](getuseravailability-operation.md).  <br/><br/> The following is the XPath to this element:  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[Mailbox (Availability)](mailbox-availability.md) <br/> | Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.  <br/><br/>  The following are the XPath expressions to this element: <br/> <br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## Text value

A text value is optional. The following are the possible values:

* SMTP
* EX

If no value is provided, the default value of SMTP is used.
  
## Remarks

This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element. This element is not required. This element exists for the inclusion of future protocols. Another **RoutingType** element is used for accessing items in a user's mailbox. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetUserAvailability operation](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

