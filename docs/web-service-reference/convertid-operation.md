---
title: "ConvertId operation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 47d96cf6-9e2f-4fc0-9682-7258d3fbf918
description: "Find information about the ConvertId EWS operation."
---

# ConvertId operation

Find information about the **ConvertId** EWS operation. 
  
The **ConvertId** Exchange Web Services (EWS) operation converts item and folder identifiers between formats that are accepted by Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with Exchange Server 2013. 
  
## Using the ConvertId operation
<a name="bk_usingConvertId"> </a>

You can convert the following identifiers by using the **ConvertId** operation: 
  
- The identifier format for EWS in the initial release version of Exchange 2007. This is represented by the  `EwsLegacyId` enumeration value in the [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration. 
    
- The identifier format for EWS in Exchange 2007 SP1 or Exchange 2010. This is represented by the  `EwsId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).
    
- The MAPI identifier, as in the **PR_ENTRYID** property. This is represented by the  `EntryId` enumeration value in the [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration. 
    
- The availability calendar event identifier. This is a hexadecimal-encoded representation of the **PR_ENTRYID** property. This is represented by the  `HexEntryId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).
    
- The Exchange store identifier. This is represented by the  `StoreId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx). The **ConvertId** operation does not convert public folder identifiers from the EWS identifier to the store identifier. 
    
- The Outlook Web App identifier. This is represented by the  `OwaId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)
    
    The passing of URLs that are created from this identifier to Outlook Web App is not supported. The Outlook Web App identifier is applicable to Exchange 2007 and Exchange 2010. Outlook Web App for Exchange Online and versions of Exchange starting with Exchange Server 2013 uses EWS identifiers.
    
The **ConvertId** operation does not work as expected when converting public folder identifiers from the EWS identifier to the store identifier in Exchange Online and Exchange 2013. You can manually update the identifier that is returned as a workaround. To manually update the identifier: 
  
1. In your application code, determine whether the target item/folder is in a public folder. 
    
2. Decode the Base64-encoded identifier string.
    
3. Verify that the type byte (21st byte) has a value of 7. A value of 7 indicates that the identifier is in the incorrect format.
    
4. Skip the first four bytes. They must be set to zero.
    
5. Update the next 16 bytes with the following GUID: 1A447390AA6611CD9BC800AA002FC45A
    
6. Update the next byte (type byte) with a value of 9.
    
7. Change the identifier to a Base64-encoded string.
    
> [!NOTE]
> The **ConvertId** operation validates that a given SMTP address has a valid format. The operation does not determine whether an SMTP address represents a valid mailbox. 
  
The **ConvertId** operation can use the SOAP headers that are listed in the following table. 
  
**Table 1. ConvertId operation SOAP headers**

|**Header**|**Element**|**Description**|
|:-----|:-----|:-----|
|Impersonation  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifies the user whom the client application is impersonating. This is applicable to a request.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifies the schema version for the operation request This is applicable to a request.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifies the version of the server that responded to the request. This is applicable to a response.  <br/> |
   
## ConvertId operation request example
<a name="bk_usingConvertId"> </a>

The following example of a **ConvertId** request shows how to convert from an EWS identifier to an Outlook Web App identifier. 
  
The [RequestServerVersion](requestserverversion.md) element in the SOAP header must be set to Exchange2007_SP1 or later for this operation to work. 
  
> [!NOTE]
> The item identifier has been shortened to preserve readability. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <ConvertId xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               DestinationFormat="OwaId">
      <SourceIds>
        <t:AlternateId Format="EwsId" Id="AAMkAGZhN2IxYTA0LWNiNzItN="
                       Mailbox="user1@example.com"/>
      </SourceIds>
    </ConvertId>
  </soap:Body>
</soap:Envelope>
```

## ConvertId operation response example
<a name="bk_usingConvertId"> </a>

The following example shows a successful response to a **ConvertId** request. This response example contains an Outlook Web App identifier. 
  
> [!NOTE]
> The Outlook Web App identifier has been shortened to preserve readability. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                         MajorBuildNumber="191" MinorBuildNumber="0" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <AlternateId xsi:type="t:AlternateIdType" Format="OwaId" Id="RgAAAAAS2%2" 
                         Mailbox="user@example.com" />
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## ConvertId operation error response example
<a name="bk_usingConvertId"> </a>

The following example shows the response to a request that contains the wrong type of identifier format.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                       MajorBuildNumber="206" MinorBuildNumber="0"
                       Version="Exchange2010" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Error">
          <MessageText>Id is malformed.</MessageText>
          <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
          <DescriptiveLinkKey>0</DescriptiveLinkKey>
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## Version differences
<a name="bk_ConvertIdVersionDiff"> </a>

The EWS identifier format changed between the initial release version of Exchange 2007 and Exchange 2007 Service Pack 1 (SP1). Exchange Online as part of Office 365, Exchange Online, and on-premises versions of Exchange starting with Exchange 2010 use the same identifier format that Exchange 2007 SP1 uses.
  
The **ConvertId** operation converts public folder identifiers from the EWS identifier to the store identifier in Exchange 2007 and Exchange 2010. 
  
## See also
<a name="bk_ConvertIdVersionDiff"> </a>

- [Converting Identifiers](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [ConvertIdType](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [ConvertId](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

