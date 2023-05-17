---
title: "ExpandDL operation" 
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: 1f7837e7-9eff-4e10-9577-c40f7ed6af94
description: "The ExpandDL operation exposes the full membership of distribution lists."
---

# ExpandDL operation

The ExpandDL operation exposes the full membership of distribution lists.
  
## Using the ExpandDL Web Method

The ExpandDL operation uses the Web service that is located in Exchange.asmx. This Web service method accepts a [Mailbox](mailbox.md) element that can contain either an [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) child element for an expansion of a public distribution list or an [ItemId](itemid.md) child element for the expansion of a private distribution list. 
  
Public distribution lists can be expanded by using one of the following:
  
1. Distribution list alias
    
2. The Simple Mail Transfer Protocol (SMTP) address
    
3. X400
    
4. X500
    
5. Exchange Legacy address
    
6. The distribution list name
    
7. The display name
    
> [!IMPORTANT]
> Display names are not unique. Multiple accounts can share the same display name. 
  
## Remarks

Recursive expansion is not supported. Only one distribution list can be expanded in a single call. If more than one distribution list match the criteria, the Web service reports an error. A client application can use ambiguous name resolution (ANR) to find ambiguous distribution lists and then chose the correct e-mail address of the required distribution list as a parameter for the [ExpandDL operation](expanddl-operation.md). For more information, see [ResolveNames operation](resolvenames-operation.md).
  
Public distribution lists are located in Active Directory. They can be any mail-enabled or dynamic distribution group. The group should not be hidden from the address list and each member should have a non-empty e-mail address. Members of the distribution list can be mail-enabled users and contacts, public folders, and mail-enabled distribution lists and dynamic groups.
  
Private distribution lists are located in the Contacts folder of a user's mailbox. Private distribution lists do not have e-mail addresses so their store item identifiers are used in an ExpandDL request. Members of a private distribution list can be any mail-enabled user, contacts or distribution lists from Active Directory, or contacts or private distribution lists from a user's Contacts folder.
  
For contacts or private distribution lists, the item identifiers are returned in the response. This can be used to get information about the object or to expand membership in a private distribution list.
  
## ExpandDL Private Distribution List request example

### Description

The following example of an ExpandDL request shows how to form a request to expand a private distribution list.
  
### Code

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ExpandDL>
      <m:Mailbox>
       <t:EmailAddress>test</t:EmailAddress>
      </m:Mailbox>
    </m:ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### Comments

To expand a private distribution list, the [Mailbox](mailbox.md) element will contain the [ItemId](itemid.md) element that identifies a private distribution list in the user's mailbox. 
  
## ExpandDL Public Distribution List request example

### Description

The following example of an ExpandDL request shows how to form a request to expand a public distribution list. The example shows the use of a display name to expand a distribution list.
  
### Code

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:EmailAddress>TheDistributionList</t:EmailAddress>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### Comments

The response to this request will contain **Mailbox** elements that identify each mailbox in the distribution list. If a distribution list is contained within a distribution list, a separate distribution list expansion must be performed on the embedded distribution list. If the distribution list has no members or the requested distribution list does not exist, the **ResponseClass** attribute will contain a value equal to Success. 
  
### Request elements

The following elements are used in the request:
  
- [ExpandDL](expanddl.md)
    
- [Mailbox](mailbox.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) is used to identify public distribution lists. The [ItemId](itemid.md) element is used to identify private distribution lists. 
    
> [!NOTE]
> The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed. 
  
## Successful ExpandDL response example

### Description

The following example of an ExpandDL response shows a response to the request described above. The distribution list expansion describes the following: 
  
- The number of members of the distribution list that are returned in the response.
    
- Whether the response contains all the members of the distribution list.
    
- The name of the mailbox.
    
- The e-mail address of the mailbox.
    
- The routing type for the mailbox.
    
- The type of mailbox.
    
> [!NOTE]
> The distribution list name is not included in the response; therefore, you must keep track of the name from the request. 
  
### Code

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DLExpansion TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Mailbox>
              <t:Name>Dan Park</t:Name>
              <t:EmailAddress>dpark@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Jeff Price</t:Name>
              <t:EmailAddress>jprice@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Tanja Plate</t:Name>
              <t:EmailAddress>tplate@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
          </m:DLExpansion>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### Successful response elements

The following elements are used in the response:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [DLExpansion](dlexpansion.md)
    
- [Mailbox](mailbox.md)
    
- [Name (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
To find other options for the response message of the ExpandDL operation, explore the schema hierarchy. Start at the [ExpandDLResponse](expanddlresponse.md) element. 
  
## ExpandDL error response

### Description

The following example shows an error response to an ExpandDL request.
  
### Code

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Error">
          <m:MessageText>No results are found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### Error response elements

The following elements are used in the error response:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
To find other options for the response message of the ExpandDL operation, explore the schema hierarchy. Start at the [ExpandDLResponse](expanddlresponse.md) element. 
  
## See also

- [ResolveNames operation](resolvenames-operation.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

