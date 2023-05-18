---
title: "FolderName"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FolderName
api_type:
- schema
ms.assetid: c5a2cd55-ac47-43bf-94b5-3ab3a4c28a62
description: "The FolderName element identifies a single managed custom folder to add to a mailbox."
---

# FolderName

The **FolderName** element identifies a single managed custom folder to add to a mailbox. 
  
[CreateManagedFolder](createmanagedfolder.md)
  
[FolderNames](foldernames.md)
  
[FolderName](foldername.md)
  
```xml
<FolderName>...</FolderName>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FolderNames](foldernames.md) <br/> |Contains an array of named managed custom folders to add to a mailbox.  <br/> The following is the XPath expression to this element:  <br/>  `/CreateManagedFolder/FolderNames` <br/> |
   
## Text value

A text value is required. The text value represents a folder name.
  
## Remarks

Although you can use Exchange Web Services to add managed custom folders to a mailbox, you cannot use the same technology to access the list of available managed custom folders. You can obtain a list of managed custom folders by using an Exchange Management Shell command or by using an API that interfaces with the Active Directory directory service. The folder name is the name of the corresponding Active Directory object.
  
You can use the [FindFolder operation](findfolder-operation.md) to find managed custom folders. Use the [DeleteFolder operation](deletefolder-operation.md) to delete managed custom folders. 
  
It is important to note that **FolderName** is the name of an existing managed custom folder in the organization. An attempt to add a folder that is not in the organization will result in an error response. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[FindFolder operation](findfolder-operation.md)


[Finding Folders](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adding Managed Folders](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

