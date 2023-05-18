---
title: "MSExchangeCertificate"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: c514f22f-be3e-4cad-ac56-bdff6bafcee6
description: "The MSExchangeCertificate element contains a value that encodes the Microsoft Exchange certificate of a contact."
---

# MSExchangeCertificate

The **MSExchangeCertificate** element contains a value that encodes the Microsoft Exchange certificate of a contact. 
  
```XML
<MSExchangeCertificate/>
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
   
### Parent elements

|**Element name**|**Description**|
|:-----|:-----|
|[Contact](contact.md) <br/> |Represents a contact item in the Exchange store.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Creating Contacts (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

