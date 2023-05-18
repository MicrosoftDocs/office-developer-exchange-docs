---
title: "FolderShape"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FolderShape
api_type:
- schema
ms.assetid: 244f4f46-a33d-4764-92e3-1bddb4dc6a49
description: "The FolderShape element identifies the folder properties to include in a GetFolder, FindFolder, or SyncFolderHierarchy response."
---

# FolderShape

The **FolderShape** element identifies the folder properties to include in a [GetFolder](getfolder.md), [FindFolder](findfolder.md), or [SyncFolderHierarchy](syncfolderhierarchy.md) response. 
  
```xml
<FolderShape>
   <BaseShape/>
   <AdditionalProperties/>
</FolderShape>
```

 **FolderResponseShapeType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[BaseShape](baseshape.md) <br/> |Identifies the basic configuration of properties to return in a response.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifies additional properties to return in a response.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Defines a request to identify folders in a mailbox.  <br/> The following is the XPath expression to this element:  <br/>  `/FindFolder` <br/> |
|[GetFolder](getfolder.md) <br/> |Defines a request to get a folder from the Exchange store.  <br/> The following is the XPath expression to this element:  <br/>  `/GetFolder` <br/> |
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |Defines a request to synchronize a folder hierarchy on a client.  <br/> The following is the XPath expression to this element:  <br/>  `/SyncFolderHierarchy` <br/> |
   
## Remarks

The **FolderShape** element is a required child element of the [FindFolder](findfolder.md) element. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Example

The following example of a request demonstrates how to find all folders located in the first level of the Inbox folder.
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[FindFolder](findfolder.md)

