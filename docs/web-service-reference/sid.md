---
title: "SID"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- SID
api_type:
- schema
ms.assetid: 2f33b29b-163b-4106-a74d-6fb76ec38951
description: "The SID element represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation or delegate access."
---

# SID

The **SID** element represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation or delegate access. 
  
```xml
<SID/>
```

 **SIDType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |Represents an account to impersonate when using the ExchangeImpersonation SOAP header.  <br/> The following is the XPath expression to this element:  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[UserId](userid.md) <br/> |Identifies a delegate user or a user with folder access permissions.  <br/> |
   
## Text value

The text value is a string representation of a SID.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

