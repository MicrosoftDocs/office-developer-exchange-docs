---
title: "CanDelete"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CanDelete
api_type:
- schema
ms.assetid: 55e17121-aad0-4f90-889f-2c3512e9579c
description: "The CanDelete element indicates whether a managed folder can be deleted by a customer."
---

# CanDelete

The **CanDelete** element indicates whether a managed folder can be deleted by a customer. 
  
```xml
<CanDelete/>
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Contains information about a managed folder.  <br/> |
   
## Text value

A text value that represents a Boolean value is required if this element is present. A value of **true** indicates that the folder can be deleted; a value of **false** means that the folder cannot be deleted. 
  
## Remarks

To delete a managed folder, use the [DeleteFolder operation](deletefolder-operation.md).
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[CreateManagedFolder operation](createmanagedfolder-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)


[Deleting Folders](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

