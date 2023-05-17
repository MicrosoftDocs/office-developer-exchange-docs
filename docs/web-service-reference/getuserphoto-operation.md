---
title: "GetUserPhoto operation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e
description: "Find information about the GetUserPhoto EWS operation."
---

# GetUserPhoto operation

Find information about the **GetUserPhoto** EWS operation. 
  
The **GetUserPhoto** operation gets a user photo from Active Directory Domain Services (AD DS). 
  
This operation was introduced in Exchange Server 2013.
  
## Using the GetUserPhoto operation

The **RemoveContactFromImList** operation is a simple operation that accepts a user's email address and the requested photo size and returns the photo stream in the response. 
  
> [!NOTE]
> EWS has both a SOAP and a REST-based operation to get user photos. For information about the REST interface, see [Get user photos by using EWS in Exchange](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx). 
  
### GetUserPhoto operation SOAP headers

The **GetUserPhoto** operation can use the SOAP headers that are listed in the following table. 
  
|**Header name**|**Element**|**Description**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifies the schema version for the operation request. This header is applicable to a request.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifies the version of the server that responded to the request. This header is applicable to a response.  <br/> |
   
## GetUserPhoto operation request example: Get a user's photo

The following example of a **GetUserPhoto** operation request shows how to get a user's photo. This example requests a user photo that is 48x48 pixels. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body>
      <m:GetUserPhoto>
         <m:Email>user1@contoso.com</m:Email>
         <m:SizeRequested>HR48x48</m:SizeRequested>
      </m:GetUserPhoto>
   </soap:Body>
</soap:Envelope>
```

The following elements are used in the request SOAP body:
  
- [GetUserPhoto](getuserphoto.md)
    
- [Email (String)](email-string.md)
    
- [SizeRequested](sizerequested.md)
    
## Successful GetUserPhoto operation response

The following example shows a successful response to a **GetUserPhoto** operation to get a user's photo. 
  
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
      <GetUserPhotoResponse ResponseClass="Success" 
                            xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <HasChanged>true</HasChanged>
         <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/02</PictureData>
      </GetUserPhotoResponse>
   </s:Body>
</s:Envelope>

```

The following elements are used in the response SOAP body:
  
- [GetUserPhotoResponse](getuserphotoresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [HasChanged](haschanged.md)
    
- [GetUserPhotoResponse](getuserphotoresponse.md)
    
## GetUserPhoto operation error response

The SOAP envelope will not return an error code if an attempt is made to get a user photo for an email address that doesn't exist in the organization. A 500 HTTP status code will be returned in the response to indicate that the request was unsuccessful. 
  
## See also

- [EWS operations in Exchange](ews-operations-in-exchange.md)   
- [Get user photos by using EWS in Exchange](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx)
    

