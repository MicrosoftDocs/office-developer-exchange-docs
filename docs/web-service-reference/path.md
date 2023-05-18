---
title: "Path"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- Path
api_type:
- schema
ms.assetid: 5829149e-7bfe-4820-bcc6-910e9264acc9
description: "The Path element is the base schema type for all property identifiers. This type is abstract and will never occur directly within instance documents."
---

# Path

The **Path** element is the base schema type for all property identifiers. This type is abstract and will never occur directly within instance documents. 
  
```xml
<Path/>
```

 **BasePathToElementType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

None.
  
## Remarks

The following elements are used to substitute for the **Path** element: 
  
- [FieldURI](fielduri.md)
    
- [IndexedFieldURI](indexedfielduri.md)
    
- [ExceptionFieldURI](exceptionfielduri.md)
    
- [ExtendedFieldURI](extendedfielduri.md)
    
The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

