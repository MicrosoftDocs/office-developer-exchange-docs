---
title: "FractionalPageFolderView"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FractionalPageFolderView
api_type:
- schema
ms.assetid: ef681f8a-136a-4c0e-ade6-ddcdbf2d85ad
description: "The FractionalPageFolderView element describes where the paged view starts and the maximum number of folders returned in a FindFolder request."
---

# FractionalPageFolderView

The **FractionalPageFolderView** element describes where the paged view starts and the maximum number of folders returned in a [FindFolder](findfolder.md) request. 
  
[FindFolder](findfolder.md)
  
[FractionalPageFolderView](fractionalpagefolderview.md)
  
```xml
<FractionalPageFolderView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 **FractionalPageViewType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Identifies the maximum number of results to return in the [FindFolder](findfolder.md) response. This attribute is optional.  <br/> |
|**Numerator** <br/> |Represents the numerator of the fractional offset from the start of the result set. This attribute is required. The numerator must be equal to or less than the denominator. This attribute must represent an integral value that is equal to or greater than zero. For more information, see Remarks later in this topic.  <br/> |
|**Denominator** <br/> |Represents the denominator of the fractional offset from the start of the total number of folders in the result set. This attribute is required. This attribute must represent an integral value that is greater than one. For more information, see Remarks later in this topic.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Defines a request to identify folders in a mailbox.  <br/> The following is the XPath expression to this element:  <br/>  `/FindFolder` <br/> |
   
## Remarks

The paged view offset from the start of the set of found folders is described by a fraction. The fraction, which is defined by the **Numerator** and **Denominator** attributes, describes where the page of information starts. For example, if **Numerator** equals four and **Denominator** equals five, the page of returned information starts at an entry located four-fifths of the way in to the result set. 
  
If the fraction evaluates to zero, that indicates the start of the results set. If the fraction evaluates to one, that indicates the end of the result set.
  
> [!NOTE]
> The fraction represents the start point of page, not how many results in the result set will be returned. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[FindFolder operation](findfolder-operation.md)


[Finding Folders](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

