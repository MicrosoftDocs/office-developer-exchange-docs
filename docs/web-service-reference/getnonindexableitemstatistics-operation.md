---
title: "GetNonIndexableItemStatistics operation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: ed077877-9d98-4434-b8b6-a4a905e7f7a6
description: "Find information about the GetNonIndexableItemStatistics EWS operation."
---

# GetNonIndexableItemStatistics operation

Find information about the **GetNonIndexableItemStatistics** EWS operation. 
  
The **GetNonIndexableItemStatistics** operation retrieves the count of items that cannot be indexed in a mailbox. 
  
This operation was introduced in Exchange Server 2013.
  
## Using the GetNonIndexableItemStatistics operation

The **GetNonIndexableItemStatistics** operation counts mailbox items that cannot be indexed. Items that cannot be indexed are not searched during a discovery search. 
  
### GetNonIndexableItemStatistics operation SOAP headers

The **GetNonIndexableItemStatistics** operation can use the SOAP headers that are listed in the following table. 
  
|**Header name**|**Element**|**Description**|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |Identifies the server roles that are necessary in order for the caller to make the request. This header is applicable to a request.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifies the schema version for the operation request. This header is applicable to a request.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifies the version of the server that responded to the request. This header is applicable to a response.  <br/> |
   
## GetNonIndexableItemStatistics operation request example: Get the count of items that cannot be indexed in a mailbox

The following example of a **GetNonIndexableItemStatistics** operation request shows how to request the count of items that cannot be indexed in a mailbox. 
  
> [!NOTE]
> All legacy domain names in this example have be shortened to preserve readability. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetNonIndexableItemStatistics>
         <m:Mailboxes>
            <t:LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYDIDLT)/cn=Recipients/cn=3518cf-Steve</t:LegacyDN>
         </m:Mailboxes>
         <m:SearchArchiveOnly>false</m:SearchArchiveOnly>
      </m:GetNonIndexableItemStatistics>
   </soap:Body>
</soap:Envelope>

```

The request SOAP body contains the following elements:
  
- [GetNonIndexableItemStatistics](getnonindexableitemstatistics.md)
    
- [Mailboxes (NonEmptyArrayOfLegacyDNsType)](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [LegacyDN](legacydn.md)
    
- [SearchArchiveOnly](searcharchiveonly.md)
    
## Successful GetNonIndexableItemStatistics operation response

The following example shows a successful response to a **GetNonIndexableItemStatistics** operation request to get the count of items that cannot be indexed in a mailbox. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0"
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetNonIndexableItemStatisticsResponse ResponseClass="Success" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemStatistics>
            <NonIndexableItemStatistic xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYT)/cn=Recipients/cn=35181acf-Steve</Mailbox>
               <ItemCount>2</ItemCount>
            </NonIndexableItemStatistic>
         </NonIndexableItemStatistics>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

The response SOAP body contains the following elements:
  
- [GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [NonIndexableItemStatistics](nonindexableitemstatistics.md)
    
- [NonIndexableItemStatistic](nonindexableitemstatistic.md)
    
- [Mailbox (string)](mailbox-string.md)
    
- [ItemCount](itemcount.md)
    
## GetNonIndexableItemStatistics operation error response

The following example shows an error response to a **GetNonIndexableItemStatistics** operation request. This is a response to a request to get the count of items that cannot be indexed from more than one mailbox. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetNonIndexableItemStatisticsResponse ResponseClass="Error" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

The error response SOAP body contains the following elements:
  
- [GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).
  
## See also

- [EWS operations in Exchange](ews-operations-in-exchange.md)
    
- [GetSearchableMailboxes operation](getsearchablemailboxes-operation.md)
    
- [SearchMailboxes operation](searchmailboxes-operation.md)
    
- [GetHoldOnMailboxes operation](getholdonmailboxes-operation.md)
    
- [SetHoldOnMailboxes operation](setholdonmailboxes-operation.md)
    
- [GetDiscoverySearchConfiguration operation](getdiscoverysearchconfiguration-operation.md)
    
- [GetNonIndexableItemDetails operation](getnonindexableitemdetails-operation.md)
    

