---
title: "AlternateId"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- AlternateId
api_type:
- schema
ms.assetid: 9c01fdc3-4adf-4e23-bc33-45d2a45ea08b
description: "The AlternateId element describes an identifier to convert in a request and the results of a converted identifier in the response."
---

# AlternateId

The **AlternateId** element describes an identifier to convert in a request and the results of a converted identifier in the response. 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 **AlternateIdType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|Id  <br/> |Describes the source identifier in a [ConvertId operation](convertid-operation.md) request and describes the destination identifier in a [ConvertId operation](convertid-operation.md) response.  <br/> |
|Format  <br/> |Describes the source format in a [ConvertId operation](convertid-operation.md) request and describes the destination format in a [ConvertId operation](convertid-operation.md) response. The destination format is described by the **DestinationFormat** attribute of the [ConvertId](convertid.md) element in the request. This attribute is of type **IdFormatType**.  <br/> |
|Mailbox  <br/> |Describes the mailbox primary Simple Mail Transfer Protocol (SMTP) address that contains the identifiers to translate.  <br/> |
|IsArchive  <br/> |Indicates whether the identifier represents an archived item or folder. A value of **true** indicates that the identifier represents an archived item or folder. This attribute is optional.  <br/> |
   
#### Format attribute values

|**Value**|**Description**|
|:-----|:-----|
|EwsLegacyId  <br/> |Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.  <br/> |
|EwsId  <br/> |Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.  <br/> |
|EntryId  <br/> |Describes MAPI identifiers, as in the **PR_ENTRYID** property.  <br/> |
|HexEntryId  <br/> |Describes a hexadecimal-encoded representation of the **PR_ENTRYID** property. This is the format of availability calendar event identifiers.  <br/> |
|StoreId  <br/> |Describes Exchange store identifiers.  <br/> |
|OwaId  <br/> |Describes an Outlook Web App identifier.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Contains the status and result of a [ConvertId operation](convertid-operation.md) request.  <br/> |
|[SourceIds](sourceids.md) <br/> |Contains the source identifiers to convert.  <br/> |
   
## Text value

None.
  
## Remarks

The **AlternateId** element describes two identifiers, the source identifier that is to be converted in the [ConvertId operation](convertid-operation.md) request, and the converted identifier in the [ConvertIdResponse](convertidresponse.md) element. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example | Type |
|:-----|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |Types schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |False  <br/> |
   
## See also

- [ConvertId operation](convertid-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
- [Converting Identifiers](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

