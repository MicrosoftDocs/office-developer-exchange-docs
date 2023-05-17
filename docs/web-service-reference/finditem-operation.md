---
title: "FindItem operation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
api_name:
- FindItem
api_type:
- schema
ms.assetid: ebad6aae-16e7-44de-ae63-a95b24539729
description: "Find information about the FindItem EWS operation."
localization_priority: Priority
---

# FindItem operation

Find information about the **FindItem** EWS operation. 
  
The **FindItem** operation searches for items that are located in a user's mailbox. This operation provides many ways to filter and format how search results are returned to the caller. 
  
## Using the FindItem operation

The **FindItem** operation request provides many ways for you to search a mailbox and format how the data is returned in a response. You can specify the following in a **FindItem** request: 
  
- Whether the search is a shallow or soft-deleted traversal. Specifying this is required. Note that a soft-deleted traversal combined with a search restriction will result in zero items returned, even if there are items that match the search criteria.
    
- The response shape of items. This identifies the properties that are returned in the response. Specifying this is required.
    
- The folders from which to perform the search. Specifying this is required.
    
- The paging mechanism and view types for returning view data in pages. Specifying this is optional.
    
- Options for grouping and sorting the items that are returned. Specifying this is optional.
    
- Search restrictions or Advanced Query Syntax (AQS) strings for filtering the items that are returned. For more information about using AQS for content index searches, see [QueryString (String)](querystring-string.md). Specifying this is optional.
    
- The sort order for items returned in the response. Specifying this is optional.
    
The **FindItem** operation returns only the first 512 bytes of any streamable property. For Unicode, it returns the first 255 characters by using a null-terminated Unicode string. It does not return any of the message body formats or the recipient lists. **FindItem** will return a recipient summary. You can use the [GetItem operation](getitem-operation.md) to get the details of an item. 
  
 **FindItem** returns only the [Name (EmailAddressType)](name-emailaddresstype.md) element and does not return the [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element in the [Mailbox](mailbox.md) element for the following fields: 
  
- The [From](from.md) field for messages 
    
- The [Sender](sender.md) field for messages 
    
- The [Organizer](organizer.md) field for calendar items 
    
> [!NOTE]
> The **FindItem** operation can return results in a [CalendarView](calendarview.md) element. The **CalendarView** element returns single calendar items and all occurrences of recurring meetings. If a **CalendarView** element is not used, single calendar items and recurring master calendar items are returned. The occurrences must be expanded from the recurring master if a **CalendarView** element is not used. 
  
The **FindItem** operation can use the SOAP headers that are listed in the following table. 
  
**Table 1. FindItem operation SOAP headers**

|**Header**|**Element**|**Description**|
|:-----|:-----|:-----|
|**DateTimePrecision** <br/> |[DateTimePrecision](datetimeprecision.md) <br/> |Specifies the resolution of data/time values in responses from the server, either in seconds or in milliseconds. This is applicable to a request.  <br/> |
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifies the user whom the client application is impersonating. This is applicable to a request.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifies the RFC3066 culture to be used to access the mailbox. This is applicable to a request.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifies the schema version for the operation request. This is applicable to a request.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifies the version of the server that responded to the request. This is applicable to a response.  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Identifies the time zone to be used for all responses from the server. This is applicable to a request.  <br/> |
   
## FindItem operation request example

The following example of a **FindItem** request shows how to obtain the item identifier that is defined by the **IdOnly** enumeration of the [BaseShape](baseshape.md) element for items that are found in the Deleted Items folder. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
              Traversal="Shallow">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </ItemShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="deleteditems"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

The following elements are used in the request: 
  
- [FindItem](finditem.md)
    
- [ItemShape](itemshape.md)
    
- [BaseShape](baseshape.md)
    
- [ParentFolderIds](parentfolderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
For more options for a **FindItem** request message, explore the schema hierarchy. Start at the [FindItem](finditem.md) element. 
  
## Successful FindItem operation response

The following example shows a successful response to the **FindItem** request. 
  
[Message](message-ex15websvcsotherref.md) elements represent email messages and all other items that are not strongly typed by the EWS schema. Items such as IPM.Sharing and IPM.InfoPath are returned as [Message](message-ex15websvcsotherref.md) elements. Exchange does not return the base [Item](item.md) element in responses. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="10" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AS4AUn=" ChangeKey="fsVU4==" />
              </t:Message>
              <t:Message>
                <t:ItemId Id="AS4AUM=" ChangeKey="fsVUA==" />
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

The following elements are used in the response:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindItemResponse](finditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindItemResponseMessage](finditemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md)
    
- [Items](items.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [ItemId](itemid.md)
    
For more options for a **FindItem** response message, explore the schema hierarchy. Start at the [FindItemResponse](finditemresponse.md) element. 
  
## FindItem operation error response

The following example shows an error response to a **FindItem** request. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

The following elements are used in the error response:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindItemResponse](finditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindItemResponseMessage](finditemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
For more options for a **FindItem** error response message, explore the schema hierarchy. Start at the [FindItemResponse](finditemresponse.md) element. 
  
## Version differences

Versions of Exchange starting with major version 15 and ending with build 15.0.898.11 return an ErrorInvalidOperation value in the [ResponseCode](responsecode.md) element when the **FindItem** operation is used to search multiple folders in an archive mailbox. 
  
## See also

- [Finding Items](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)
    
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
    
- **FindItemType**
    

