---
title: "SearchMailboxes operation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 8a67c1d8-d021-4e68-aa62-35f7d9c2edc7
description: "Find information about the SearchMailboxes EWS operation."
---

# SearchMailboxes operation

> [!NOTE]
> This operation is deprecated, and no longer supported by Microsoft.  As a replacement, please use the [FindItem](finditem-operation.md) operation.

Find information about the **SearchMailboxes** EWS operation. 
  
The **SearchMailboxes** operation searches mailboxes for occurrences of terms in mailbox items. 
  
This operation was introduced in Exchange Server 2013.
  
## Using the SearchMailboxes operation

The **SearchMailboxes** operation can use many simultaneous search queries to perform discovery search on multiple mailboxes. The results can be either statistical information about the number of times search terms occur, or a preview of the items that contain the search terms. 
  
### SearchMailboxes operation SOAP headers

The **SearchMailboxes** operation can use the SOAP headers that are listed in the following table. 
  
|**Header name**|**Element**|**Description**|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |Identifies the server roles that are necessary in order for the caller to make the request. This header is applicable to a request.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifies the schema version for the operation request. This header is applicable to a request.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifies the version of the server that responded to the request. This header is applicable to a response.  <br/> |
   
## SearchMailboxes operation request example: Search mailboxes for number of search term hits

The following example of a **SearchMailboxes** operation request shows how to use two different queries to search three different mailboxes for statistical information about how many times a term appears in each mailbox. 
  
> [!NOTE]
> In this example, the [Query](query.md) element is intentionaly left blank. This shows how a successful request can contain error conditions on a per mailbox search basis. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:SearchMailboxes>
         <m:SearchQueries>
            <t:MailboxQuery>
               <t:Query>Test Item</t:Query>
               <t:MailboxSearchScopes>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=12311a742f0e47e392c8201a60d13ecf-Steve</t:Mailbox>
                     <t:SearchScope>All</t:SearchScope>
                  </t:MailboxSearchScope>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=f00c9f70539844beb52341d8f40c572e-Antho</t:Mailbox>
                     <t:SearchScope>PrimaryOnly</t:SearchScope>
                  </t:MailboxSearchScope>
               </t:MailboxSearchScopes>
            </t:MailboxQuery>
            <t:MailboxQuery>
               <t:Query></t:Query>
               <t:MailboxSearchScopes>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=accba4fd5ddf12214a0e82ce1645f4e-Danie</t:Mailbox>
                     <t:SearchScope>ArchiveOnly</t:SearchScope>
                  </t:MailboxSearchScope>
               </t:MailboxSearchScopes>
            </t:MailboxQuery>
         </m:SearchQueries>
         <m:ResultType>StatisticsOnly</m:ResultType>
      </m:SearchMailboxes>
   </soap:Body>
</soap:Envelope>

```

The request SOAP body contains the following elements:
  
- [SearchMailboxes](searchmailboxes.md)
    
- [SearchQueries](searchqueries.md)
    
- [MailboxQuery](mailboxquery.md)
    
- [Query](query.md)
    
- [MailboxSearchScopes](mailboxsearchscopes.md)
    
- [MailboxSearchScope](mailboxsearchscope.md)
    
- [Mailbox (string)](mailbox-string.md)
    
- [SearchScope](searchscope.md)
    
- [ResultType](resulttype.md)
    
## Successful SearchMailboxes operation response

The following example shows a successful response to a **SearchMailboxes** operation request to get statistical information about the number of times search terms are found in the target mailboxes. The last query contains an empty **Query** element, which shows a failed mailbox search. 
  
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
      <m:SearchMailboxesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:SearchMailboxesResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:SearchMailboxesResult>
                  <t:SearchQueries>
                     <t:MailboxQuery>
                        <t:Query>Test Item</t:Query>
                        <t:MailboxSearchScopes>
                           <t:MailboxSearchScope>
                              <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=35181a94327e392c8201a60d13ecf-Steve</t:Mailbox>
                              <t:SearchScope>All</t:SearchScope>
                           </t:MailboxSearchScope>
                           <t:MailboxSearchScope>
                              <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=f00c9f789572-beb04001d8f40c572e-Antho</t:Mailbox>
                              <t:SearchScope>PrimaryOnly</t:SearchScope>
                           </t:MailboxSearchScope>
                        </t:MailboxSearchScopes>
                     </t:MailboxQuery>
                  </t:SearchQueries>
                  <t:ResultType>StatisticsOnly</t:ResultType>
                  <t:ItemCount>2</t:ItemCount>
                  <t:Size>20206</t:Size>
                  <t:PageItemCount>0</t:PageItemCount>
                  <t:PageItemSize>0</t:PageItemSize>
                  <t:KeywordStats>
                     <t:KeywordStat>
                        <t:Keyword>Test Item</t:Keyword>
                        <t:ItemHits>2</t:ItemHits>
                        <t:Size>20206</t:Size>
                     </t:KeywordStat>
                  </t:KeywordStats>
                  <t:FailedMailboxes>
                     <t:FailedMailbox>
                        <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=accba4as3df234234a0e82ce1645f4e-Danie</t:Mailbox>
                        <t:ErrorCode>0</t:ErrorCode>
                        <t:ErrorMessage>The search query can't be empty.</t:ErrorMessage>
                        <t:IsArchive>true</t:IsArchive>
                     </t:FailedMailbox>
                  </t:FailedMailboxes>
               </m:SearchMailboxesResult>
            </m:SearchMailboxesResponseMessage>
         </m:ResponseMessages>
      </m:SearchMailboxesResponse>
   </s:Body>
</s:Envelope>

```

The response SOAP body contains the following elements:
  
- [SearchMailboxesResponse](searchmailboxesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SearchMailboxesResponseMessage](searchmailboxesresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [SearchMailboxesResult](searchmailboxesresult.md)
    
- [SearchQueries](searchqueries.md)
    
- [MailboxQuery](mailboxquery.md)
    
- [Query](query.md)
    
- [MailboxSearchScopes](mailboxsearchscopes.md)
    
- [MailboxSearchScope](mailboxsearchscope.md)
    
- [Mailbox (string)](mailbox-string.md)
    
- [SearchScope](searchscope.md)
    
- [ResultType](resulttype.md)
    
- [ItemCount](itemcount.md)
    
- [Size (long)](size-long.md)
    
- [PageItemCount](pageitemcount.md)
    
- [KeywordStats](keywordstats.md)
    
- [KeywordStat](keywordstat.md)
    
- [Keyword](keyword.md)
    
- [ItemHits](itemhits.md)
    
- [FailedMailboxes](failedmailboxes.md)
    
- [FailedMailbox](failedmailbox.md)
    
- [Mailbox (string)](mailbox-string.md)
    
- [ErrorCode (int)](errorcode-int.md)
    
- [ErrorMessage](errormessage.md)
    
- [IsArchive](isarchive.md)
    
## SearchMailboxes operation error response

The following example shows an error response to a **SearchMailboxes** operation request. This is a response to a request to search a mailbox when the mailbox identifier is incorrect. 
  
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
      <m:SearchMailboxesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:SearchMailboxesResponseMessage ResponseClass="Error">
               <m:MessageText>No mailbox is specified for search operation. If specified in the request, 
               then it could be due to permission issue.</m:MessageText>
               <m:ResponseCode>ErrorInvalidOperation</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:SearchMailboxesResult>
                  <t:SearchQueries>
                     <t:MailboxQuery>
                        <t:Query>subject:Test Item</t:Query>
                        <t:MailboxSearchScopes>
                           <t:MailboxSearchScope>
                              <t:Mailbox>sbrown@contoso.com</t:Mailbox>
                              <t:SearchScope>All</t:SearchScope>
                           </t:MailboxSearchScope>
                        </t:MailboxSearchScopes>
                     </t:MailboxQuery>
                  </t:SearchQueries>
                  <t:ResultType>StatisticsOnly</t:ResultType>
                  <t:ItemCount>0</t:ItemCount>
                  <t:Size>0</t:Size>
                  <t:PageItemCount>0</t:PageItemCount>
                  <t:PageItemSize>0</t:PageItemSize>
                  <t:FailedMailboxes>
                     <t:FailedMailbox>
                        <t:Mailbox>sbrown@contoso.com</t:Mailbox>
                        <t:ErrorCode>0</t:ErrorCode>
                        <t:ErrorMessage>No mailbox is specified for search operation. If specified in the request, 
                        then it could be due to permission issue.</t:ErrorMessage>
                        <t:IsArchive>false</t:IsArchive>
                     </t:FailedMailbox>
                  </t:FailedMailboxes>
               </m:SearchMailboxesResult>
            </m:SearchMailboxesResponseMessage>
         </m:ResponseMessages>
      </m:SearchMailboxesResponse>
   </s:Body>
</s:Envelope>

```

The error response SOAP body contains the following elements:
  
- [SearchMailboxesResponse](searchmailboxesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SearchMailboxesResponseMessage](searchmailboxesresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [SearchMailboxesResult](searchmailboxesresult.md)
    
- [SearchQueries](searchqueries.md)
    
- [MailboxQuery](mailboxquery.md)
    
- [Query](query.md)
    
- [MailboxSearchScopes](mailboxsearchscopes.md)
    
- [MailboxSearchScope](mailboxsearchscope.md)
    
- [Mailbox (string)](mailbox-string.md)
    
- [SearchScope](searchscope.md)
    
- [ResultType](resulttype.md)
    
- [ItemCount](itemcount.md)
    
- [Size (long)](size-long.md)
    
- [PageItemCount](pageitemcount.md)
    
- [PageItemSize](pageitemsize.md)
    
- [FailedMailboxes](failedmailboxes.md)
    
- [FailedMailbox](failedmailbox.md)
    
- [Mailbox (string)](mailbox-string.md)
    
- [ErrorCode (int)](errorcode-int.md)
    
- [ErrorMessage](errormessage.md)
    
- [IsArchive](isarchive.md)
    
For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).
  
## See also

- [EWS operations in Exchange](ews-operations-in-exchange.md)
    
- [GetSearchableMailboxes operation](getsearchablemailboxes-operation.md)
    
- [SetHoldOnMailboxes operation](setholdonmailboxes-operation.md)
    
- [GetHoldOnMailboxes operation](getholdonmailboxes-operation.md)
    
- [GetDiscoverySearchConfiguration operation](getdiscoverysearchconfiguration-operation.md)
    
- [GetNonIndexableItemDetails operation](getnonindexableitemdetails-operation.md)
    
- [GetNonIndexableItemStatistics operation](getnonindexableitemstatistics-operation.md)
    

