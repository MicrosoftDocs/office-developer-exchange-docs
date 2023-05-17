---
title: "DataType"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DataType
api_type:
- schema
ms.assetid: 267fe5aa-f9b1-4d4c-ac11-0f2e50ec2627
description: "The DataType element describes the type of data that is shared by a shared folder."
---

# DataType

The **DataType** element describes the type of data that is shared by a shared folder. 
  
```xml
<DataType>Calendar or Contacts</DataType>
```

**SharingDataType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetSharingFolder](getsharingfolder.md) <br/> |Defines a request to get the local folder identifier of a specified shared folder.  <br/> |
   
## Text value

The following table lists the possible values for the **DataType** element. 
  
**DataType element values**

|**Value**|**Description**|
|:-----|:-----|
|Calendar  <br/> |Indicates that the shared folder contains calendar information.  <br/> |
|Contacts  <br/> |Indicates that the shared folder contains contact information.  <br/> |
   
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

