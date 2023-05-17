---
title: "GetDelegate"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 6d5efe59-596f-46f8-bdc6-ca9cded9bb8e
description: "The GetDelegate element defines a request to get information about delegates to a mailbox. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# GetDelegate

The **GetDelegate** element defines a request to get information about delegates to a mailbox. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<GetDelegate IncludePermissions="">
      <Mailbox/>
   <UserIds/>
</GetDelegate>
```

 **GetDelegateType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**IncludePermissions** <br/> |Indicates whether the response contains permission settings for each delegate user.  <br/> |
   
#### IncludePermissions attribute values

|**Value**|**Description**|
|:-----|:-----|
|**True** <br/> |Delegate user permissions are returned in addition to the delegate user information that is returned in the [UserId](userid.md) element.  <br/> |
|**False** <br/> |[UserId](userid.md) information is returned.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |Identifies the principal's mailbox.  <br/> |
|[UserIds](userids.md) <br/> |Contains an array of delegate users to get from a principal's mailbox. This element was introduced in Exchange 2007 SP1.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[GetDelegate operation](getdelegate-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

