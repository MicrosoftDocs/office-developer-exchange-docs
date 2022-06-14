---
title: "GetSearchableMailboxes operation"
manager: sethgros
ms.date: 01/24/2020
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 47f8ff57-4835-4d2d-9136-44afb31a4cbe
description: "Find information about the GetSearchableMailboxes EWS operation."
---

# GetSearchableMailboxes operation

> [!IMPORTANT]
> Starting on April 1, 2020, the GetSearchableMailboxes operation will no longer be available in Exchange Online. This operation won't be affected in on-premises versions of Exchange Server. For more information, see [Retirement of legacy eDiscovery tools in Exchange Online](/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).

Find information about the **GetSearchableMailboxes** EWS operation. 
  
The **GetSearchableMailboxes** operation gets a scoped set of searchable mailboxes for discovery searches. The scope of searchable mailboxes returned in the response is determined by the search filter and whether distribution group membership is expanded. 

> [!NOTE] 
> This operation is intended to be used with the search filter and to retrieve only the first few thousands; it's not intended for exhaustive retrieval.
  
This operation was introduced in Exchange Server 2013.
  
## Using the GetSearchableMailboxes operation

The **GetSearchableMailboxes** operation gets information about searchable mailboxes. The following arguments can be passed in the request: 
  
- [SearchFilter](searchfilter.md) - Accepts a single email alias as an argument. 
    
- [ExpandGroupMembership](expandgroupmembership.md) - Indicates whether the distribution group membership is expanded in the results returned in the response. 
    
If the email alias set in the search filter is a distribution group and the distribution group membership is not expanded, the response will contain the mailbox information for the distribution group. If the email alias set in the search filter is a distribution group and the distribution group membership is expanded, the response will contain the mailbox information for each mailbox that is a member of the distribution group. If the search filter contains a single user's alias, the response will contain the mailbox information for the single user. The response will contain all searchable mailboxes if the [GetSearchableMailboxes](getsearchablemailboxes.md) element is empty. This is the same as having an empty [SearchFilter](searchfilter.md) element and the [ExpandGroupMembership](expandgroupmembership.md) element set to **false**.
  
### GetSearchableMailboxes operation SOAP headers

The **GetSearchableMailboxes** operation can use the SOAP headers that are listed in the following table. 
  
|Header name|Element|Description|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |Identifies the server roles that are necessary in order for the caller to make the request. This header is applicable to a request.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifies the schema version for the operation request. This header is applicable to a request.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifies the version of the server that responded to the request. This header is applicable to a response.  <br/> |
   
## GetSearchableMailboxes operation request example: Request information about a distribution group

The following example of a **GetSearchableMailboxes** operation request shows how to get the mailbox information for the lolgroup distribution group. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetSearchableMailboxes>
         <m:SearchFilter>lolgroup</m:SearchFilter>
         <m:ExpandGroupMembership>false</m:ExpandGroupMembership>
      </m:GetSearchableMailboxes>
   </soap:Body>
</soap:Envelope>

```

The request SOAP body contains the following elements:
  
- [GetSearchableMailboxes](getsearchablemailboxes.md)   
- [SearchFilter](searchfilter.md)    
- [ExpandGroupMembership](expandgroupmembership.md)
    
## Successful GetSearchableMailboxes operation response: Get information about a distribution group

The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information for the lolgroup distribution group. 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Success" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <SearchableMailboxes>
            <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Guid>33a408fe-2574-4e3b-49f5-5e1e000a3035</Guid>
               <PrimarySmtpAddress>LOLgroup@contoso.com</PrimarySmtpAddress>
               <IsExternalMailbox>false</IsExternalMailbox>
               <ExternalEmailAddress/>
               <DisplayName>LOLgroup</DisplayName>
               <IsMembershipGroup>true</IsMembershipGroup>
               <ReferenceId>/o=First/ou=Exchange(FYLT)/cn=Recipients/cn=81213b958a0b5295b13b3f02b812bf1bc-LOLgroup</ReferenceId>
            </SearchableMailbox>
         </SearchableMailboxes>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

The response SOAP body contains the following elements:
  
- [GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)   
- [ResponseCode](responsecode.md)   
- [SearchableMailboxes](searchablemailboxes.md)    
- [SearchableMailbox](searchablemailbox.md)    
- [Guid](guid-ex15websvcsotherref.md)    
- [PrimarySmtpAddress](primarysmtpaddress.md)    
- [IsExternalMailbox](isexternalmailbox.md)   
- [ExternalEmailAddress](externalemailaddress.md)    
- [DisplayName (string)](displayname-string.md)    
- [IsMembershipGroup](ismembershipgroup.md)    
- [ReferenceId](referenceid.md)
    
## Successful GetSearchableMailboxes operation response: Get information about an expanded distribution group

The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information about members of the expanded lolgroup distribution group. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetSearchableMailboxesResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <SearchableMailboxes>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>e2d42cdf-a227-1ec3-486b-6fa0ebaadb9f5</Guid>
          <PrimarySmtpAddress>JSmith@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Julia Smith</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=0a1fc86f883846152405d60956dd02e7-Julia</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>45d0fff1-6541-459a-a343-52453b30e12ca</Guid>
          <PrimarySmtpAddress>LMoore@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Laura Moore</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=2910d8f8316f4378bbf9338d8f9d714b-Laura</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>3c620d04-8b33-435a-95be-5b939375576</Guid>
          <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Steven Brown</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=90312341a742f0e47e392c80a60d13ecf-Steve</ReferenceId>
        </SearchableMailbox>
      </SearchableMailboxes>
    </GetSearchableMailboxesResponse>
  </s:Body>
</s:Envelope>
```

The response SOAP body contains the following elements:
  
- [GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)    
- [ResponseCode](responsecode.md)   
- [SearchableMailboxes](searchablemailboxes.md)    
- [SearchableMailbox](searchablemailbox.md)    
- [Guid](guid-ex15websvcsotherref.md)    
- [PrimarySmtpAddress](primarysmtpaddress.md)    
- [IsExternalMailbox](isexternalmailbox.md)    
- [ExternalEmailAddress](externalemailaddress.md)    
- [DisplayName (string)](displayname-string.md)    
- [IsMembershipGroup](ismembershipgroup.md)    
- [ReferenceId](referenceid.md)
    
## GetSearchableMailboxes operation error response

The following example shows an error response to a **GetSearchableMailboxes** operation request. This is a response to a request to get all searchable mailboxes when the **ExpandGroupMembership** argument is set to **true**. 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Error" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot use wildcard or empty query when auto group expansion is enabled.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <SearchableMailboxes/>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

The error response SOAP body contains the following elements:
  
- [GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)  
- [MessageText](messagetext.md)   
- [ResponseCode](responsecode.md)   
- [DescriptiveLinkKey](descriptivelinkkey.md) 
- [SearchableMailboxes](searchablemailboxes.md)
    
For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).
  
## See also

- [EWS operations in Exchange](ews-operations-in-exchange.md)   
- [SetHoldOnMailboxes operation](setholdonmailboxes-operation.md)   
- [SearchMailboxes operation](searchmailboxes-operation.md)   
- [GetHoldOnMailboxes operation](getholdonmailboxes-operation.md)    
- [GetDiscoverySearchConfiguration operation](getdiscoverysearchconfiguration-operation.md)   
- [GetNonIndexableItemDetails operation](getnonindexableitemdetails-operation.md)   
- [GetNonIndexableItemStatistics operation](getnonindexableitemstatistics-operation.md)
