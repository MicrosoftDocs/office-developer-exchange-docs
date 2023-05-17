---
title: "QueryString (QueryStringType)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
api_name:
- QueryString
api_type:
- schema
ms.assetid: cadbf9a5-b87e-4d7f-b488-b76fb0ee7150
description: "The QueryString element contains a mailbox query string based on Advanced Query Syntax (AQS)."
localization_priority: Priority
---

# QueryString (QueryStringType)

The **QueryString** element contains a mailbox query string based on Advanced Query Syntax (AQS). 
  
```XML
<QueryString/>
```

 **QueryStringType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|ResetCache  <br/> |Indicates that the cache should be reset.  <br/> |
|ReturnDeletedItems  <br/> |Indicates that deleted items should be returned.  <br/> |
|ReturnHighlightTerms  <br/> |Indicates that highlighted terms should be returned.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Defines a request to find items in a mailbox.  <br/> The following is the XPath expression to this element: /FindItem.  <br/> |
   
## Text value

The **QueryString** element text value represents a mailbox query that is made by using a subset of [Advanced Query Syntax (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx). See the remarks section for information about the supported syntax options for query strings.
  
## Remarks

In Exchange Server 2010, this element is an XML schema string type. In versions of Exchange starting with Exchange Server 2013, including Exchange Online, the type for this element is **QueryStringType**. This change does not break any existing clients because it adds three new optional attributes. 
  
The **QueryString** element excludes the use of EWS restrictions. AQS in EWS supports three types of restrictions: word phase restriction, date range restriction, and message type restriction. The following tables list the supported search properties for each restriction type. 
  
**Word phase restriction**

|**Property**|**Example**|**Function**|
|:-----|:-----|:-----|
|from  <br/> |From:Dean  <br/> From:"Dean Halstead"  <br/> |Search items sent from Dean.  <br/> Search items sent from Dean Halstead. The sender must be exactly "Dean Halstead".  <br/> |
|to  <br/> |To:Dean  <br/> |Search items sent to Dean.  <br/> |
|cc  <br/> |Cc:Dean  <br/> |Search for items with Dean on the Cc line.  <br/> |
|bcc  <br/> |Bcc:Dean  <br/> |Search for items with Dean on the Bcc line.  <br/> |
|Participants  <br/> |Participants:Dean  <br/> |Search for items with Dean in the To, Cc, or Bcc fields.  <br/> |
|Subject  <br/> |Subject:product  <br/> Subject:(product development)  <br/> Subject:"product development"  <br/> |Search for items with product in the subject.  <br/> Search for items with product and development in the subject.  <br/> |
|Body  <br/> Content  <br/> |Body:progress  <br/> Content:progress  <br/> |Search for items with progress in the body.  <br/> |
|Attachment  <br/> |Attachment:report  <br/> |Search for items with report in the attachment file name or file body.  <br/> |
|(property is not specified)  <br/> |Product Development  <br/> |Search for items that contain both product and development in all word phase properties.  <br/> |
   
Word phase restriction match is always case insensitive. Word phase restriction supports two match types: prefix match or exact match. Prefix match is the default match behavior. If you want exact match, use double quotes. For example, subject:"product" matches 'product' but not 'production' in the subject. Multiple words in double quotes restrict both word phases and their order. For example "win product" matches only 'win product', not 'win95 product' or 'product of win'. You can use an asterisk (\*) to define a prefix match with order restricted. For example, "win product"\* matches 'win95 product', 'windows production line' but not 'windows new product' or 'product of win'. You can search all messages sent from or to a domain. For example, from:"@hotmail.com" returns all messages sent from hotmail.com.
  
The following table describes date range restrictions.
  
**Date range restriction**

|**Property**|**Example**|**Function**|
|:-----|:-----|:-----|
|Sent  <br/> |Sent:last week  <br/> Sent:01/01/2001  <br/> Sent:01/01/2001..01/15/2001  <br/> |Search items sent last week.  <br/> Search items sent on January 1st, 2001.  <br/> Search items sent between January 1st, 2001 and January 15th, 2001.  <br/> |
|Received  <br/> |Received:today  <br/> Received:01/01/2001  <br/> |Search items received today.  <br/> Search items received on January 1st, 2001.  <br/> |
   
The two dots (..) is a range operator. It can be used to define a range with a start and an end date. To specify a date, you can use relative dates. The following relative dates are supported:
  
- Relative dates: Today, tomorrow, yesterday
    
- Multiword relative dates: This week, next month, last week, past month, or coming year
    
- Days: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday
    
- January, February, March, April, May, June, July, August, September, October, November, December
    
The following table describes message type restrictions. 
  
**Message type restriction**

|**Property**|**Example**|**Function**|
|:-----|:-----|:-----|
|Kind  <br/> |Kind:tasks  <br/> |Search all task items.  <br/> |
   
AQS in EWS uses the **Kind** property to specify the message type. The Kind property can be used with the following item types: 
  
- email
    
- meetings
    
- tasks
    
- notes
    
- docs
    
- journals
    
- contacts
    
- im
    
The following table describes grouping logical connectors.
  
**Grouping logical connectors**

|**Connector**|**Example**|**Function**|
|:-----|:-----|:-----|
|AND  <br/> |Subject:product AND subject:development  <br/> Subject:(product AND development)  <br/> Subject:(product development)  <br/> |Search items with both product and development in the subject.  <br/> |
|OR  <br/> |Body:project OR body:proposal  <br/> Body:(project OR proposal)  <br/> |Search items with either product or development in the body.  <br/> |
|NOT  <br/> |NOT body:proposal  <br/> Body:(NOT proposal)  <br/> |Search messages without proposal in the body.  <br/> |
   
AND is always the default connector. For example, subject:project AND body:proposal is the same as subject:project body:proposal. Logical connectors are case sensitive. For example, body:(project Or proposal) searches messages with 'project', 'or', and 'proposal' in the body instead of 'project' or 'proposal'. The plus symbol (+) is equivalent to AND. The hyphen symbol (-) is equivalent to NOT. For example, body:(project - proposal) searches messages with 'project' but without 'proposal' in the body. 
  
The query string can also contain nonindexed properties for search. If the query string contains nonindexed properties, the search might perform an Exchange search on the indexed properties and a store search on the nonindexed properties. 
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Example

The following example shows a request to search for messages in the Inbox with Autodiscover in the subject.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
      <m:QueryString>subject:Autodiscover</m:QueryString>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

The following example shows a successful response to the request.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" 
                        TotalItemsInView="5" 
                        IncludesLastItemInRange="false">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkADEzOTExYjJkLTYx" ChangeKey="CQAAABY" />
                <t:Subject>How to use Autodiscover</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>

```

## Element information

|**Code**|**Name**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also



[FindItem operation](finditem-operation.md)
  
[FindConversation operation](findconversation-operation.md)


- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

