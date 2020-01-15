---
title: "Perform an AQS search by using EWS in Exchange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: c136901a-313e-4adf-a223-1d090d16917a
description: "Find out how to search with query strings and AQS in your EWS Managed API or EWS application."
localization_priority: Priority
---

# Perform an AQS search by using EWS in Exchange

Find out how to search with query strings and AQS in your EWS Managed API or EWS application.
  
Query strings provide an alternative to [search filters](how-to-use-search-filters-with-ews-in-exchange.md) for expressing search criteria. The biggest advantage to using query strings is that you are not required to specify a single property to search. You can just provide a value, and the search will apply to all commonly used fields on the items. You can also refine your search by using Advanced Query Syntax (AQS) instead of a simple value. However, query strings have the following limitations that you should be aware of before you add them to your toolbox: 
  
- **Limited ability to search specific properties.** When you search with a simple value in a query string, the search is performed against all indexed properties. You can refine your search to specific properties, but the properties available to use in an AQS string are limited. If the property you want to search isn't one of the properties that are available for AQS, consider using a search filter. 
    
- **Custom properties aren't searched.** Query string searches are performed against an index, and custom properties are not included in that index. If you need to search custom properties, use a search filter instead. 
    
- **Limited control for string searches.** Query string searches always ignore case, and are always substring searches. If you want to do case-sensitive, prefix, or exact match searches, use a search filter. 
    
- **Not available for folders or search folders.** The EWS operations for searching for folders don't support using a query string. Additionally, search folders don't support query strings. In both cases, a search filter is your only option. 
    
## Creating a query string
<a name="bk_CreateQueryString"> </a>

Query strings in the EWS Managed API and EWS are interpreted as a subset of AQS syntax. AQS strings are composed of either values or keyword/value pairs, separated by a colon (:).
  
`keyword:value`

When a value is specified without a keyword, all indexed properties are searched for the value. If a keyword is paired with a value, the keyword specifies a property to search for the corresponding value.
  
**Table 1. Supported AQS keywords**

|**Keyword**|**Value type**|**Example**|
|:-----|:-----|:-----|
|subject  <br/> |String  <br/> |subject:project  <br/> |
|body  <br/> |String  <br/> |body:sales figures  <br/> |
|attachment  <br/> |String  <br/> |attachment:report  <br/> |
|to  <br/> |String  <br/> |to:"Sadie Daniels"  <br/> |
|from  <br/> |String  <br/> |from:hope  <br/> |
|cc  <br/> |String  <br/> |cc:"Ronnie Sturgis"  <br/> |
|bcc  <br/> |String  <br/> |bcc:mack  <br/> |
|participants  <br/> |String  <br/> |participants:sadie  <br/> |
|category  <br/> |String  <br/> |category:project  <br/> |
|importance  <br/> |String  <br/> |importance:high  <br/> |
|kind  <br/> |Item type  <br/> |kind:meetings  <br/> |
|sent  <br/> |Date  <br/> |sent:12/10/2013  <br/> |
|received  <br/> |Date  <br/> |received:yesterday  <br/> |
|hasattachment  <br/> |Boolean  <br/> |Has attachment:true  <br/> |
|isflagged  <br/> |Boolean  <br/> |isflagged:true  <br/> |
|isread  <br/> |Boolean  <br/> |isread:false  <br/> |
|size  <br/> |Number  <br/> |size:\>5000  <br/> |
   
Let's take a look at how the different value types work.
  
### Using a string value type

String value types are by default searched as prefix substring searches that are not case-sensitive. That means that searching for subject:project would match any of the following subjects: 
  
- Project meeting notes
    
- Do you have the project plans?
    
- December sales projections
    
You can change the search to require the whole word rather than matching prefixes by enclosing the string in quotation marks. Searching for subject:"project" would eliminate the "December sales projections" value from the list of matches. Note that the value is still not case-sensitive. 
  
If you use multiple words in a query string, a match requires that both words appear in the searched fields. For example, searching for subject:project plan would match any of the following subjects: 
  
- Project plan
    
- Do you have the project plans?
    
- Please send me the plan for our project
    
- Planning project milestones
    
If you enclose multiple words in quotation marks, they are treated as a single phrase. Searching for subject:"project plan" would only match the "Project plan" subject from the previous list. 
  
### Using an item type value type

You can use the following item type values with the **kind** keyword to limit your search results to only a specific type of item, such as email or meeting requests: 
  
- contacts    
- docs    
- email    
- faxes    
- im (corresponds to instant messages)    
- journals    
- meetings (corresponds to appointments and meeting requests)    
- notes    
- posts    
- rssfeeds    
- tasks    
- voicemail
    
### Using a date value type

You can search date value types in a number of different ways. The simplest is to search for a specific date. Searching with received:12/11/2013 will return all items received on December 11, 2013. However, you can also be less specific. Searching with received:12/11 will return all items received on December 11 of the current year. 
  
Another option is to use the month names. You can search with received:December 11, 2013 or December 11 to get the same results as received:12/11/2013 and received:12/11, respectively. You can also search with received:December to get all items received in the month of December, in the current year. 
  
Using the names of the days of the week is also an option. Searching with received:Tuesday will return all items received on Tuesday of the current week. 
  
Date value types also support a set of keywords for searches relative to the current time. The following keywords are supported:
  
- today  
- tomorrow
- yesterday
- this week    
- last week    
- next month    
- past month    
- coming year
    
Date value types can also be compared with relational operators like greater than or less than, or specified as a range with the range operator **..**. For example, received:\>11/30/2013, sent:\>=yesterday, and received:12/1/2013..today are all valid query strings. 
  
### Using a Boolean value type

Boolean value types can be "true" or "false". The values are not case-sensitive, so isread:false will produce the same results as isread:FALSE.
  
### Using a number value type

Number value types can be searched as exact matches, but they can also be searched using relational operators like greater than or less than. For example, size:10000 will return only items that have a size of exactly 10000 bytes, but size:\>=10000 will return items that have a size greater than or equal to 10000 bytes. You can also specify a range by using the range operator ( **..**). For example, size:7000..8000 will return items that have a size between 7000 and 8000. 
  
### Using logical operators

Query strings support the following logical operators.
  
**Table 2. Supported logical operators**

|**Operator**|**Examples**|
|:-----|:-----|
|AND  <br/> |project AND from:"Sadie Daniels"  <br/> subject:(project AND plan)  <br/> |
|OR  <br/> |subject:meeting OR from:"Hope Gross"  <br/> from:("Sadie Daniels" OR "Hope Gross")  <br/> |
|NOT  <br/> |NOT from:"Ronnie Sturgis"  <br/> received:NOT today  <br/> |
   
Notice that you can use these operators to join multiple criteria together or to join multiple values within a single keyword/value pair together. However, when joining multiple values in a single keyword/value pair, you should use parentheses to enclose the multiple values. To understand why, consider searching with from:"Sadie Daniels" OR "Hope Gross". This search actually is interpreted as the following criteria:
  
- The item is from Sadie Daniels, OR
    
- The item has the phrase "Hope Gross" in any of its indexed properties.
    
In contrast, from:("Sadie Daniels" OR "Hope Gross") is interpreted as: 
  
- The item is from Sadie Daniels, OR
    
- The item is from Hope Gross
    
The default operator when multiple criteria are specified but no logical operator is included is AND. For example, has attachment:true subject:project is equivalent to has:attachment:true AND subject:project.
  
## Example: Find items by using a query string and the EWS Managed API
<a name="bk_ExampleEWSMA"> </a>

In this example, a method called **SearchWithQueryString** is defined. It takes an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, a [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object, and a **string** object that represents the query string as parameters. This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties. 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void SearchWithQueryString(ExchangeService service, WellKnownFolderName folder, string queryString)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       ItemSchema.Size,
                                       ItemSchema.Importance,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support Deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Execute the search based on the query string.
        // Example: "subject:project plan"
        FindItemsResults<Item> results = service.FindItems(folder, queryString, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Received: {0}", item.DateTimeReceived.ToString());
            Console.WriteLine("Size: {0}", item.Size.ToString());
            Console.WriteLine("Importance: {0}", item.Importance.ToString());
            if (item is EmailMessage)
            {
                EmailMessage message = item as EmailMessage;
                Console.WriteLine("Read: {0}", message.IsRead.ToString());
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

You can use this method to search for all items with the phrase "project plan" in the subject, as shown in this example.
  
```cs
string queryString = "subject:\"project plan\"";
SearchWithQueryString(service, WellKnownFolderName.Inbox, queryString);
```

## Example: Find items by using a query string and EWS
<a name="bk_ExampleEWS"> </a>

In this example, a SOAP [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request finds all items in the Inbox with the phrase "project plan" in the subject. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="item:Size" />
          <t:FieldURI FieldURI="item:Importance" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
      <m:QueryString>subject:"project plan"</m:QueryString>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

The following example shows the response from the server with the search results.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>project plan</t:Subject>
                <t:DateTimeReceived>2013-12-11T15:42:02Z</t:DateTimeReceived>
                <t:Size>7406</t:Size>
                <t:Importance>Normal</t:Importance>
                <t:IsRead>false</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## See also

- [Search and EWS in Exchange](search-and-ews-in-exchange.md)    
- [Use search filters with EWS in Exchange](how-to-use-search-filters-with-ews-in-exchange.md)    
- [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

