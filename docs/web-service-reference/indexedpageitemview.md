---
title: "IndexedPageItemView"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- IndexedPageItemView
api_type:
- schema
ms.assetid: 6d1b0b04-cc35-4a57-bd7a-824136d14fda
description: "The IndexedPageItemView element describes how paged conversation or item information is returned for a FindItem operation or FindConversation operation request."
---

# IndexedPageItemView

The **IndexedPageItemView** element describes how paged conversation or item information is returned for a [FindItem operation](finditem-operation.md) or [FindConversation operation](findconversation-operation.md) request. 
  
```XML
<IndexedPageViewItemView MaxEntriesReturned="" Offset="" BasePoint=""/>
```

 **IndexedPageViewType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Describes the maximum number of items or conversations to return in the response. This attribute is optional.  <br/> |
|**Offset** <br/> |Describes the offset from the **BasePoint**. If **BasePoint** is equal to Beginning, the offset is positive. If **BasePoint** is equal to End, the offset is handled as if it were negative. This identifies which item or conversation will be the first to be delivered in the response. This attribute is required.  <br/> |
|**BasePoint** <br/> |Describes whether the page of items or conversations will start from the beginning or the end of the set of items or conversations that are found by using the search criteria. Seeking from the end always searches backward. This attribute is required.  <br/> |
   
#### BasePoint Attribute

|**Value**|**Description**|
|:-----|:-----|
|Beginning  <br/> |The paged view starts at the beginning of the found conversation or item set.  <br/> |
|End  <br/> |The paged view starts at the end of the found conversation or item set.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Defines a request to find items in a mailbox.  <br/> The following is the XPath expression to this element:  <br/>  `/FindItem` <br/> |
|[FindConversation](findconversation.md) <br/> |Defines a request to find conversations in a mailbox.  <br/> |
   
## Remarks

Seeking from the end involves moving to the origin identified by the offset. Additionally, the pointer is moved back by the number of requested records. For example, if there are 100 records and the offset is 25 from the end, the search starts from 75. If 10 records are returned, the pointer is moved backward an additional 10 records to 65 and returns records 65 through 75. The next index is 64. The next offset from the end for a page is 100 minus 64 which equals 36. 36 is the value for the next offset from the end to get the next indexed page.
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Example

The following example shows a [FindItem operation](finditem-operation.md) request. Each item is returned with its ID and subject. A maximum of six items are returned in the response, as specified by the **MaxEntriesReturned** attribute. The items are listed in ascending order grouped by importance. Items in a group are aggregated by subject. 
  
```XML
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
      <IndexedPageItemView MaxEntriesReturned="6" BasePoint="Beginning" Offset="0" />
      <GroupBy Order="Ascending">
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

## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[FindItem operation](finditem-operation.md)
  
[FindConversation operation](findconversation-operation.md)


[Finding Items](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

