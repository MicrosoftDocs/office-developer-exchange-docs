---
title: "RequestServerVersion"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RequestServerVersion
api_type:
- schema
ms.assetid: af4032d5-42b3-463e-9d0a-8236d78e5b75
description: "The RequestServerVersion element contains the versioning information that identifies the schema version to target for a request."
---

# RequestServerVersion

The **RequestServerVersion** element contains the versioning information that identifies the schema version to target for a request. 
  
```XML
<RequestServerVersion Version=""/>
```

 **ExchangeVersionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Version  <br/> |Describes the version to target for the request. This attribute is required when the target server version is a version of Exchange starting with Exchange Server 2010.  <br/> |
   
#### Version attribute values

|**Value**|**Description**|
|:-----|:-----|
|Exchange2007  <br/> |Target the schema files for the initial release version of Exchange 2007.  <br/> |
|Exchange2007_SP1  <br/> |Target the schema files for Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2), and Exchange 2007 Service Pack 3 (SP3).  <br/> |
|Exchange2010  <br/> |Target the schema files for Exchange 2010.  <br/> |
|Exchange2010_SP1  <br/> |Target the schema files for Exchange 2010 Service Pack 1 (SP1).  <br/> |
|Exchange2010_SP2  <br/> |Target the schema files for Exchange 2010 Service Pack 2 (SP2) and Exchange 2010 Service Pack 3 (SP3).  <br/> |
|Exchange2013  <br/> |Target the schema files for Exchange 2013.  <br/> |
|Exchange2013_SP1  <br/> |Target the schema files for Exchange 2013 Service Pack 1 (SP1).  <br/> |
   
### Child elements

None.
  
### Parent elements

The **RequestServerVersion** element is located in the SOAP header. 
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Versioning Requests](https://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

