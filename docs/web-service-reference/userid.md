---
title: "UserId"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- UserId
api_type:
- schema
ms.assetid: 244af9e0-bf3c-46b4-8bfa-9719a1ed3107
description: "The UserId element identifies a delegate user or a user who has folder access permissions."
---

# UserId

The **UserId** element identifies a delegate user or a user who has folder access permissions. 
  
```xml
<UserId>
   <SID/>
   <PrimarySmtpAddress/>
   <DisplayName/>
   <DistinguishedUser/>
   <ExternalUserIdentity/>
</UserId>
```

 **UserIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SID](sid.md) <br/> |Represents the security descriptor definition language (SDDL) form of the security identifier (SID).  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for delegate access.  <br/> |
|[DisplayName (string)](displayname-string.md) <br/> |Defines the display name of a folder, contact, distribution list, or delegate user.  <br/> |
|[DistinguishedUser](distinguisheduser.md) <br/> |Identifies Anonymous and Default user accounts for delegate access.  <br/> |
|[ExternalUserIdentity](externaluseridentity.md) <br/> |Identifies an external delegate user or an external user who has folder access permissions.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DelegateUser](delegateuser.md) <br/> |Identifies a single delegate to add or update in a mailbox.  <br/> |
|[Permission](permission.md) <br/> |Defines the access that a user has to a folder.  <br/> |
|[CalendarPermission](calendarpermission.md) <br/> |Defines the access that a user has to a Calendar folder.  <br/> |
|[UserIds](userids.md) <br/> |Contains an array of delegate users to get or remove from a principal's mailbox.  <br/> |
   
## Text value

None.
  
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



[AddDelegate operation](adddelegate-operation.md)
  
[UpdateDelegate operation](updatedelegate-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Adding Delegates](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

