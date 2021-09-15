---
title: "Handling synchronization-related errors in EWS in Exchange"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: a0807b90-645a-4ea6-aee1-96828df14be0
description: "Find out how to handle synchronization-related errors in applications that you develop by using the EWS Managed API or EWS in Exchange."
---

# Handling synchronization-related errors in EWS in Exchange

Find out how to handle synchronization-related errors in applications that you develop by using the EWS Managed API or EWS in Exchange.
  
If your application synchronizes items and folders, you might have to handle synchronization-related errors. You can handle these errors at runtime, or while you are developing your EWS application. Most of these errors are defined by the [ResponseCodeType](https://msdn.microsoft.com/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) enumeration in the EWS Managed API, and the [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) element in Exchange Web Services (EWS). 
  
**Table 1. Sync-related errors and how to handle them**

|**Error**|**Occurs when you try to…**|**Handle it by…**|
|:-----|:-----|:-----|
|ErrorInvalidSyncStateData  <br/> | Synchronize items or folders by using an invalid sync state value.  <br/>  Exclude a root folder in your initial SyncFolderHierarchy request, when your subsequent request does include a root folder.  <br/>  Use different root folders in subsequent requests.  <br/> | Ensuring that the sync state value you are sending matches the sync state value returned during a previous synchronization.  <br/>  Ensuring that you are not sending the sync state for the folder hierarchy when you attempt to sync items, and vice versa.  <br/>  Ensuring that you are sending the sync state for the correct root folder.  <br/>  Ensuring that the same root folder is specified in each request.  <br/>  Ensuring that the previous request did not specify a root folder of null, while the current request includes a root folder of root. Null and root are not treated the same.  <br/> |
|ErrorSyncFolderNotFound  <br/> |Synchronize subfolders or items in a folder that cannot be found on the server.  <br/> |Ensuring that the folder ID specified in the request matches a folder ID returned from the server in a previous sync response.  <br/> |
|ErrorTimeoutExpired  <br/> |Send too many requests.  <br/> |Limiting your batches to 10 items per batch to avoid getting [throttled](ews-throttling-in-exchange.md).  <br/> |
|[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) <br/> |Connect to EWS when the server is offline or there is a problem with connectivity.  <br/> |Checking connectivity with the server and retrying your request later. This is likely a transient service error or network error.  <br/> |
   
## See also


- [Mailbox synchronization and EWS in Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    
- [Synchronize folders by using EWS in Exchange](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [Synchronize items by using EWS in Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)
    

