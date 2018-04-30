---
title: "ReferenceAttachmentType complexType (EWS)"
 
 
manager: sethgros
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
 
localization_priority: Normal
ms.assetid: 18bfa012-e903-d7f3-528a-31ccceb65463
---

# ReferenceAttachmentType complexType (EWS)

## Type information

|||
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
|[AttachLongPathName](http://msdn.microsoft.com/library/98464422-2c13-8d33-0fe3-b1978f2d5b4a%28Office.15%29.aspx) <br/> |xs:string  <br/> ||
   
### Attributes

None.
  

