---
title: "ConvertId"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 9684c22c-29d4-4f7f-befc-8cd41da56d38
description: "The ConvertId element defines a request to convert item and folder identifiers between supported Exchange formats. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1)."
---

# ConvertId

The **ConvertId** element defines a request to convert item and folder identifiers between supported Exchange formats. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<ConvertId DestinationFormat="">
   <SourceIds/>
</ConvertId>
```

 **ConvertIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**DestinationFormat** <br/> |Describes the identifier format that will be returned for all the converted identifiers. The DestinationFormat is described by the IdFormatType.  <br/> |
   
#### DestinationFormat Attribute

|**Value**|**Description**|
|:-----|:-----|
|**EwsLegacyId** <br/> |Represents the identifier format that is used for Exchange Web Services identifiers that are provided in the initial release version of Exchange 2007.  <br/> |
|**EwsId** <br/> |Represents the identifier format that is used for Exchange Web Services identifiers starting with Exchange Server 2007 SP1.  <br/> |
|**EntryId** <br/> |Represents the MAPI identifier, as in the PR_ENTRYID property.  <br/> |
|**HexEntryId** <br/> |Represents the availability calendar event identifier. This is a hexadecimal-encoded representation of the PR_ENTRYID property.  <br/> |
|**StoreId** <br/> |Represents the Exchange store identifier.  <br/> |
|**OwaId** <br/> |Represents the Outlook Web Access identifier format.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |Contains the source identifiers to convert.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[ConvertId operation](convertid-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Converting Identifiers](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

