---
title: "SerializedSecurityContext"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SerializedSecurityContext
api_type:
- schema
ms.assetid: a02c4fc1-ed1a-40d9-a18e-6cfdae21a690
description: "The SerializedSecurityContext element is used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication. Token serialization is not supported."
---

# SerializedSecurityContext

The **SerializedSecurityContext** element is used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication. Token serialization is not supported. 
  
```xml
<SerializedSecurityContext>
   <UserSid/>
   <GroupSids/>
   <RestrictedGroupSids/>
   <PrimarySmtpAddress/>
</SerializedSecurityContext>
```

 **SerializedSecurityContextType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[UserSid](usersid.md) <br/> |Represents the security descriptor definition language (SDDL) form of the user security identifier in a serialized security context SOAP header.  <br/> |
|[GroupSids](groupsids.md) <br/> |Represents a collection of Active Directory directory service group object security identifiers.  <br/> |
|[RestrictedGroupSids](restrictedgroupsids.md) <br/> |Represents the group security identifier and attributes for a restricted group.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for server-to-server authorization.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server (CAS) role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Server-to-server authorization in EWS](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

