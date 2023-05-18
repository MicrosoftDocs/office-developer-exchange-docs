---
title: "DLExpansion"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DLExpansion
api_type:
- schema
ms.assetid: 9e50278d-fe6a-45e2-a72b-0fb06809e128
description: "The DLExpansion element contains an array of mailboxes that are contained in a distribution list."
---

# DLExpansion

The **DLExpansion** element contains an array of mailboxes that are contained in a distribution list. 
  
- [ExpandDLResponse](expanddlresponse.md) 
- [ResponseMessages](responsemessages.md) 
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
- [DLExpansion](dlexpansion.md)
  
```xml
<DLExpansion AbsoluteDenominator"" IncludesLastItemInRange="" IndexedPagingOffset="" NumeratorOffset="" TotalItemsInView="">
   <Mailbox/>
</DLExpansion>
```

 **ArrayOfDLExpansionType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |Represents the next index that should be used for the next request when you are using an indexed page view.  <br/> |
|**NumeratorOffset** <br/> |Represents the new numerator value to use for the next request when you are using fraction page views.  <br/> |
|**AbsoluteDenominator** <br/> |Represents the next denominator to use for the next request when you are using fraction page views.  <br/> |
|**IncludesLastItemInRange** <br/> |Indicates whether the current results contain the last item in the query so that additional paging is not needed.  <br/> |
|**TotalItemsInView** <br/> |Represents the total number of items in the view.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |Identifies a mail-enabled Active Directory directory service object.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Contains the status and result of a single ExpandDL request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [ExpandDL operation](expanddl-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md) 
- [EWS reference for Exchange](ews-reference-for-exchange.md)

