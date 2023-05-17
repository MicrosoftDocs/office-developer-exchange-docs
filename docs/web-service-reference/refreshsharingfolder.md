---
title: "RefreshSharingFolder"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- RefreshSharingFolder
api_type:
- schema
ms.assetid: 14571c28-effa-430a-802e-82fb99bafa7f
description: "The RefreshSharingFolder element defines a request to refresh the specified local folder. It is the base element for the RefreshSharingFolder operation."
---

# RefreshSharingFolder

The **RefreshSharingFolder** element defines a request to refresh the specified local folder. It is the base element for the [RefreshSharingFolder operation](refreshsharingfolder-operation.md).
  
```xml
<RefreshSharingFolder>   <SharingFolderId/></RefreshSharingFolder>
```

 **RefreshSharingFolderType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[SharingFolderId](sharingfolderid.md) <br/> |Represents the identifier of the local folder in a sharing relationship.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

