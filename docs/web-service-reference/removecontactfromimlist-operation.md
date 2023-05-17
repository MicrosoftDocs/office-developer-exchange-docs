---
title: "RemoveContactFromImList operation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: 28ec96c3-45af-48ff-9f17-718a527dc0ad
description: "Find information about the RemoveContactFromImList EWS operation."
---

# RemoveContactFromImList operation

Find information about the **RemoveContactFromImList** EWS operation. 
  
The **RemoveContactFromImList** operation removes contacts from the Lync instant messaging (IM) list when Lync uses Exchange for the contact store. 
  
This operation was introduced in Exchange Server 2013.
  
## Using the RemoveContactFromImList operation

The **RemoveContactFromImList** operation accepts a single argument that identifies a contact to remove from the Lync contact list stored on an Exchange server. The list of contacts that this operation targets is called **Lync Contacts** in Outlook 2013. 
  
> [!CAUTION]
> Do not use the [DeleteItem operation](deleteitem-operation.md) to remove contacts from a contact list. Additional server-side processing might have to occur to support removing a contact from the **Lync Contacts** list. Note that the **Lync Contacts** list is the conceptual equivalent of the default **Lync Contacts** mailbox folder. 
  
### RemoveContactFromImList operation SOAP headers

The **RemoveContactFromImList** operation can use the SOAP headers that are listed in the following table. 
  
|**Header name**|**Element**|**Description**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifies the user whom the client application is impersonating. This header is applicable to a request.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox. This header is applicable to a request.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifies the schema version for the operation request. This header is applicable to a request.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifies the version of the server that responded to the request. This header is applicable to a response.  <br/> |
   
## RemoveContactFromImList operation request example: Remove a contact from the Lync Contacts list

The following example of a **RemoveContactFromImList** operation request shows how to remove a contact from the **Lync Contacts** list. The **RemoveContactFromImList** operation accepts a single unique contact identifier to identify the contact that is removed from the **Lync Contacts** list. 
  
> [!NOTE]
> All item identifiers and change keys in this article have been shortened to preserve readability. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:RemoveContactFromImList>
         <m:ContactId Id=""/>
      </m:RemoveContactFromImList>
   </soap:Body>
</soap:Envelope>

```

The following elements are used in the request SOAP body:
  
- [RemoveContactFromImList](removecontactfromimlist.md)
    
- [ContactId](contactid.md)
    
## Successful RemoveContactFromImList operation response

The following example shows a successful response to a **RemoveContactFromImList** operation request to remove a contact from the **Lync Contacts** list. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Success" 
                                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>
```

The following elements are used in the response SOAP body:
  
- [RemoveContactFromImListResponse](removecontactfromimlistresponse.md)
    
- [ResponseCode](responsecode.md)
    
## RemoveContactFromImList operation error response

The following example shows an error response to a **RemoveContactFromImList** operation request. This is a response to a request to remove a contact from the **Lync Contacts** list when the contact no longer exists in the list. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Error" 
                                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>

```

The following elements are used in the error response SOAP body:
  
- [RemoveContactFromImListResponse](removecontactfromimlistresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## See also

- [EWS operations in Exchange](ews-operations-in-exchange.md)
    
- [GetImItemList operation](getimitemlist-operation.md)
    

