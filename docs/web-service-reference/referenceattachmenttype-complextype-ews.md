---
title: "ReferenceAttachmentType complexType (EWS)"
description: "Element information for ReferenceAttachmentType complexType"
manager: sethgros
ms.date: 04/04/2022
ms.audience: ITPro
ms.topic: article
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 18bfa012-e903-d7f3-528a-31ccceb65463
---

# ReferenceAttachmentType complexType (EWS)

## Type information

|Element|Description|
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|**Schema file** <br/> |types.xsd  <br/> |
|**Extension base** <br/> |t:AttachmentType  <br/> |
   
## Definition

```XML
<xs:complexType name="ReferenceAttachmentType">
    <xs:complexContent>
        <xs:extension base="t:AttachmentType">
            <xs:sequence>
                <xs:element name="AttachLongPathName" type="xs:string" maxOccurs="1" minOccurs="0"></xs:element>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>

```

## Elements and attributes

If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section. 
  
### Child elements

|**Element**|**Type**|**Description**|
|:-----|:-----|:-----|
|[AttachLongPathName](attachlongpathname.md) <br/> |xs:string  <br/> ||
   
### Attributes

None.