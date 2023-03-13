---
title: "GetUserSettings operation (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 758d965c-ef63-4de4-9120-e293abf14ff8
description: "The GetUserSettings operation contains a query for users' client access configuration."
 
 
---

# GetUserSettings operation (SOAP)

The **GetUserSettings** operation contains a query for users' client access configuration. 
  
## GetUserSettings request example

### Description

The following XML example shows an Autodiscover request body that requests a user's display name, distinguished name, deployment ID, mailbox server, mailbox distinguished name, Active Directory server, Client Access server version, and supported Exchange Web Services schemas.
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover"      
               xmlns:wsa="http://www.w3.org/2005/08/addressing" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"      
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2010</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://myserver.contoso.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>UserName@domain.contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>UserDisplayName</a:Setting>
          <a:Setting>UserDN</a:Setting>
          <a:Setting>UserDeploymentId</a:Setting>
          <a:Setting>InternalMailboxServer</a:Setting>
          <a:Setting>MailboxDN</a:Setting>
          <a:Setting>ActiveDirectoryServer</a:Setting>
          <a:Setting>CasVersion</a:Setting>
          <a:Setting>EwsSupportedSchemas</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

### Request elements

The following elements are used in the request body:
  
- [GetUserSettingsRequestMessage (SOAP)](getusersettingsrequestmessage-soap.md)
    
- [Mailbox (SOAP)](mailbox-soap.md)
    
- [Request (SOAP)](request-soap.md)
    
- [RequestedServerVersion (SOAP)](requestedserverversion-soap.md)
    
- [RequestedSettings (SOAP)](requestedsettings-soap.md)
    
- [Setting (SOAP)](setting-soap.md)
    
- [User (SOAP)](user-soap.md)
    
- [Users (SOAP)](users-soap.md)
    
## GetUserSettings response example

### Description

The following example shows a successful **GetUserSettings** response. 
  
### Code

```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
  </s:Header>
  <s:Body>
  <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>NoError</ErrorCode>
            <ErrorMessage>No error.</ErrorMessage>
            <RedirectTarget i:nil="true" />
            <UserSettingErrors />
            <UserSettings>
              <UserSetting i:type="StringSetting">
                <Name>UserDisplayName</Name>
                <Value>UserDisplayName</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDN</Name>
                <Value>/o=First Organization/ou=Exchange Administrative Group (SDASDASDJ)/cn=Recipients/cn=UserDisplayName</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDeploymentId</Name>
                <Value>a40E2742-21c6-4050-8Ed2-d41f100c22b8</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>CasVersion</Name>
                <Value>14.00.0478.000</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EwsSupportedSchemas</Name>
                <Value>Exchange2007, Exchange2010</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>InternalMailboxServer</Name>
                <Value>machinename.domain.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ActiveDirectoryServer</Name>
                <Value>machinename.domain.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>MailboxDN</Name>
                <Value>/o=First Organization/ou=Exchange Administrative Group (SDASDASDJ)/cn=Configuration/cn=Servers/cn=server/cn=Contoso Pri MDB</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

### Response elements

The following elements are used in the response body:
  
- [ErrorCode (SOAP)](errorcode-soap.md)
    
- [ErrorMessage (SOAP)](errormessage-soap.md)
    
- [GetUserSettingsResponseMessage (SOAP)](getusersettingsresponsemessage-soap.md)
    
- [Name (SOAP)](name-soap.md)
    
- [RedirectTarget (SOAP)](redirecttarget-soap.md)
    
- [Response (SOAP)](response-soap.md)
    
- [UserResponse (SOAP)](userresponse-soap.md)
    
- [UserResponses (SOAP)](userresponses-soap.md)
    
- [UserSetting (SOAP)](usersetting-soap.md)
    
- [UserSettingErrors (SOAP)](usersettingerrors-soap.md)
    
- [UserSettings (SOAP)](usersettings-soap.md)
    
- [Value (SOAP)](value-soap.md)
    
## See also



[GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md)


[SOAP Autodiscover XML elements for Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

