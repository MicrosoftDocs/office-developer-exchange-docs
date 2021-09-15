---
title: "eDiscovery in EWS in Exchange"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: 3128419f-dd5f-46d2-bb0d-0940738d0bb6
description: "Learn about eDiscovery in EWS in Exchange."
---

# eDiscovery in EWS in Exchange

Learn about eDiscovery in EWS in Exchange.
  
eDiscovery is a federated query web service that enables external applications to perform queries of Exchange data.
  
Discovery consists of several phases, including identifying and preserving key data, culling down and reviewing the data, and producing data in court. eDiscovery queries facilitate the discovery process by providing a single discovery workflow across Exchange and SharePoint.
  
## eDiscovery operations

The eDiscovery functionality that is exposed by EWS is available via operations introduced in Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013. 
  
**Table 1. New operations for eDiscovery**

|**Operation name**|**Description**|
|:-----|:-----|
|[GetDiscoverySearchConfiguration](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |Gets configuration information for in-place holds, saved discovery searches, and the mailboxes that are enabled for discovery search.  <br/> |
|[GetHoldOnMailboxes](https://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |Gets the status of a query-based hold, which is set by using the [SetHoldOnMailboxes operation](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx).  <br/> |
|[GetNonIndexableItemDetails](https://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |Retrieves details about items that cannot be indexed. This includes, but is not limited to, the item identifier, an error code, an error description, when an attempt was made to index the item, and additional information about the file.  <br/> |
|[GetNonIndexableItemStatistics](https://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |Retrieves the count of items that cannot be indexed in a mailbox.  <br/> |
|[GetSearchableMailboxes](https://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |Gets a list of mailboxes that the client has permission to search or perform eDiscovery on.  <br/> |
|[SearchMailboxes](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |Searches for items in specific mailboxes that match query keywords.  <br/> |
|[SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |Sets a query-based hold on items.  <br/> |
   
## See also

- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)
    
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [EWS client design overview for Exchange](ews-client-design-overview-for-exchange.md)
    

