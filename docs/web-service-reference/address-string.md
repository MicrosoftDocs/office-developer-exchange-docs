---
title: "Address (string)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Address
api_type:
- schema
ms.assetid: a3cdfcbd-d0c5-46d6-8daa-52405fc63ff0
description: "The Address element represents the e-mail address of the mailbox user."
---

# Address (string)

The **Address** element represents the e-mail address of the mailbox user. 
  
```xml
<Address>...</Address>
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
|[Email (EmailAddressType)](email-emailaddresstype.md) <br/> |Specifies the e-mail address of the MailboxData object. This element is used in the [GetUserAvailability operation](getuseravailability-operation.md).<br/><br/> The following is the XPath to this element:<br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[Mailbox (Availability)](mailbox-availability.md) <br/> | Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.<br/><br/>  The following are the XPath expressions to this element:<br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## Text value

A text value is required if this element is used.
  
## Remarks

This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element and the [Mailbox (Availability)](mailbox-availability.md) element. 
  
> [!NOTE]
> The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed. 
  
## Element information

|**Element**|**Example**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [GetUserAvailability operation](getuseravailability-operation.md)
- [GetUserOofSettings operation](getuseroofsettings-operation.md)
- [SetUserOofSettings operation](setuseroofsettings-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [GetUserOofSettingsRequest](getuseroofsettingsrequest.md)
- [SetUserOofSettingsRequest](setuseroofsettingsrequest.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

