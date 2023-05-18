---
title: "FractionalPageItemView"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FractionalPageItemView
api_type:
- schema
ms.assetid: 4111afec-35e7-4c6f-b291-9bbba603f633
description: "The FractionalPageItemView element describes where the paged view starts and the maximum number of items returned in a FindItem request."
---

# FractionalPageItemView

The **FractionalPageItemView** element describes where the paged view starts and the maximum number of items returned in a [FindItem](finditem.md) request. 
  
[FindItem](finditem.md)
  
[FractionalPageItemView](fractionalpageitemview.md)
  
```xml
<FractionalPageItemView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 **FractionalPageViewType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Identifies the maximum number of results to return in the [FindItem](finditem.md) response. This attribute is optional. If this attribute is not specified, the call will return all available items.  <br/> |
|**Numerator** <br/> |Represents the numerator of the fractional offset from the start of the result set. This attribute is required. The numerator must be equal to or less than the denominator. This attribute must represent an integral value that is equal to or greater than zero.  <br/> For more information, see Remarks later in this topic.  <br/> |
|**Denominator** <br/> |Represents the denominator of the fractional offset from the start of the total number of items in the result set. This attribute is required. This attribute must represent an integral value that is greater than one.  <br/> For more information, see Remarks later in this topic.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Defines a request to find items in a mailbox.  <br/> The following is the XPath expression to this element:  <br/>  `/FindItem` <br/> |
   
## Remarks

The paged view offset from the start of the set of found items is described by a fraction. The fraction, which is defined by the **Numerator** and **Denominator** attributes, describes where the page of information starts. For example, if **Numerator** equals four and **Denominator** equals five, the page of returned information starts at an entry located four-fifths of the way in to the result set. 
  
If the fraction evaluates to zero, that indicates the start of the results set. If the fraction evaluates to one, that indicates the end of the result set.
  
> [!NOTE]
> The fraction represents the start point of page, not how many results in the result set will be returned. 
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Example

The following example shows a [FindItem](finditem.md) request. The request returns items from the search results that start after the second third of all the items in the result set. 
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <FractionalPageItemView MaxEntriesReturned="12" Numerator="2" Denominator="3"/>
      <GroupBy Order="Descending">
        <t:FieldURI FieldURI="item:Importance"/>
        <t:AggregateOn Aggregate="Maximum">
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AggregateOn>
      </GroupBy>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

For example, if the result set contains nine items, the paged view will return up to 12 items, starting at the item found two-thirds of the way in to the result set. In this case, the page starts at the seventh item. The page will contain the seventh, eighth, and ninth items. If the numerator is set to zero, the page view will return all the items in the result set as long as the number is less than the **MaxEntriesReturned** attribute. 
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[FindItem operation](finditem-operation.md)


[Finding Items](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

