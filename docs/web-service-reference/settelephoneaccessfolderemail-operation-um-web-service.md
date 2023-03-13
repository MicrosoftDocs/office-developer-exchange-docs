---
title: "SetTelephoneAccessFolderEmail operation (UM web service)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_name:
- SetTelephoneAccessFolderEmail
api_type:
- schema
ms.assetid: 2c92d914-bdee-4337-b3ea-0655fdb658e9
description: "The SetTelephoneAccessFolderEmail operation sets the folder from which Unified Messaging will read back messages to the user over the telephone."
 
 
---

# SetTelephoneAccessFolderEmail operation (UM web service)

The SetTelephoneAccessFolderEmail operation sets the folder from which Unified Messaging will read back messages to the user over the telephone.
  
## SetTelephoneAccessFolderEmail request example

### Description

The following example of a SetTelephoneAccessFolderEmail request shows how to form a request to set the folder from which Unified Messaging will read back to the user over the telephone.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetTelephoneAccessFolderEmail xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <base64FolderID>AAAAAGsd2rbQLVtLobUGbrq/9IUBAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAAA==</base64FolderID>
    </SetTelephoneAccessFolderEmail>
  </soap:Body>
</soap:Envelope>
```

## Successful SetTelephoneAccessFolderEmail response example

### Description

The following example of a SetTelephoneAccessFolderEmail response shows a response to the SetTelephoneAccessFolderEmail request.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetTelephoneAccessFolderEmailResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## See also



[SetTelephoneAccessFolderEmail (UM web service)](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmailResponse (UM web service)](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[base64FolderId (UM web service)](base64folderid-um-web-service.md)

