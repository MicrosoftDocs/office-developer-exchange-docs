---
title: "DeleteItem operation"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 3e26c416-fa12-476e-bfd2-5c1f4bb7b348
description: "The DeleteItem operation deletes items in the Exchange store."
---

# DeleteItem operation

The **DeleteItem** operation deletes items in the Exchange store. 
  
> [!NOTE]
> An error response that includes the ErrorCannotDeleteObject error code will be returned for a **DeleteItem** operation when a delegate tries to delete an item in the principal's mailbox by setting the DisposalType to MoveToDeletedItems. To delete an item by moving it to the Deleted Items folder, a delegate must use the [MoveItem operation](moveitem-operation.md). 
  
## DeleteItem request example

### Description

The following example of a **DeleteItem** request shows how to perform a hard delete of an item from a mailbox. 
  
> [!NOTE]
> The item ID has been shortened to preserve readability. 
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteItem DeleteType="HardDelete" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemIds>
        <t:ItemId Id="AS4AUn=="/>
      </ItemIds>
    </DeleteItem>
  </soap:Body>
</soap:Envelope>
```

### Request elements

The following elements are used in the request:
  
- [DeleteItem](deleteitem.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
To find other options for the request message of the **DeleteItem** operation, explore the schema hierarchy. Start at the [DeleteItem](deleteitem.md) element. 
  
## Successful DeleteItem response

### Description

The following example shows a successful response to the **DeleteItem** request. 
  
### Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### Successful response elements

The following elements are used in the response:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [DeleteItemResponse](deleteitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [DeleteItemResponseMessage](deleteitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
To find other options for the response message of the **DeleteItem** operation, explore the schema hierarchy. Start at the [DeleteItemResponse](deleteitemresponse.md) element. 
  
## DeleteItem error response

### Description

The following example shows an error response to a **DeleteItem** request. The error was created because the operation tried to delete an item that was not found in the Exchange store. 
  
### Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### Error response elements

The following elements are used in the error response:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [DeleteItemResponse](deleteitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [DeleteItemResponseMessage](deleteitemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
To find other options for the error response message of the **DeleteItem** operation, explore the schema hierarchy. Start at the [DeleteItemResponse](deleteitemresponse.md) element. 
  
## See also

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
- [Deleting Contacts](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)  
- [Deleting E-mail Messages](https://msdn.microsoft.com/library/c40f2f0b-dae0-412f-b716-727e8c0949b4%28Office.15%29.aspx) 
- [Deleting Tasks](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

