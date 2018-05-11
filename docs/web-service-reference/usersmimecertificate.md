---
title: "UserSMIMECertificate"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66e6b4ba-368d-4469-bd47-e59441b7d64d
description: "The UserSMIMECertificate element contains a value that encodes a contact's SMIME certificate."
---

# UserSMIMECertificate

The **UserSMIMECertificate** element contains a value that encodes a contact's SMIME certificate. 
  
```XML
<UserSMIMECertificate/>
```

 **ArrayOfBinaryType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element name**|**Description**|
|:-----|:-----|
|[Base64Binary](base64binary.md) <br/> |Contains a Base64-encoded value.  <br/> |
   
#### Parent elements

|**Element name**|**Description**|
|:-----|:-----|
|[Contact](contact.md) <br/> |Represents a contact item in the Exchange store.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
#### Other resources

[Creating Contacts (Exchange Web Services)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

