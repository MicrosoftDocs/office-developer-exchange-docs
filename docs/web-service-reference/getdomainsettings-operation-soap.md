---
title: "GetDomainSettings operation (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a6f4a53d-d7f6-4ad1-8afb-78745c500eaa
description: "The GetDomainSettings operation retrieves the specified settings of the domain for the user. Autodiscover returns the domains that are to be discovered and the requested settings of those domains."
 
 
---

# GetDomainSettings operation (SOAP)

The **GetDomainSettings** operation retrieves the specified settings of the domain for the user. Autodiscover returns the domains that are to be discovered and the requested settings of those domains. 
  
## GetDomainSettings request example

### Description

The following example of a **GetDomainSettings** request shows a request for a user's **ExternalEWSUrl** domain settings. The client sends this request to the server. 
  
### Code

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soap:Header> 
        <a:RequestedServerVersion>Exchange2010</a:RequestedServerVersion>
        <wsa:Action>https://schemas.microsoft.com/exchange/2010/
            Autodiscover/Autodiscover/GetDomainSettings</wsa:Action>
        <wsa:To>
            https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc
        </wsa:To>
    </soap:Header> 
    <soap:Body> 
        <a:GetDomainSettingsRequestMessage xmlns:a="https://schemas.microsoft.com
            /exchange/2010/Autodiscover"> 
            <a:Request> 
                <a:Domains> 
                    <a:Domain>contoso.com<</a:Domain> 
                </a:Domains> 
                <a:RequestedSettings> 
                    <a:Setting>ExternalEwsUrl</a:Setting> 
                </a:RequestedSettings> 
            </a:Request> 
        </a:GetDomainSettingsRequestMessage> 
    </soap:Body> 
</soap:Envelope>
```

### Request elements

The following elements are used in the request:
  
- [GetDomainSettingsRequestMessage (SOAP)](getdomainsettingsrequestmessage-soap.md)
    
- [Request (SOAP)](request-soap.md)
    
- [Domains (SOAP)](domains-soap.md)
    
- [Domain (SOAP)](domain-soap.md)
    
- [RequestedSettings (SOAP)](requestedsettings-soap.md)
    
- [Setting (SOAP)](setting-soap.md)
    
## GetDomainSettings response example

### Description

The following example shows a successful response to the **GetDomainSettings** request that the server sends to the client. 
  
### Code

```XML
//www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/ 
            Autodiscover/Autodiscover/GetDomainSettingsResponse
        </a:Action> 
        <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
            xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
        <h:MajorVersion>14</h:MajorVersion> 
        <h:MinorVersion>0</h:MinorVersion> 
        <h:MajorBuildNumber>639</h:MajorBuildNumber> 
        <h:MinorBuildNumber>20</h:MinorBuildNumber> 
        <h:Version>Exchange2010</h:Version> 
        </h:ServerVersionInfo>
    </s:Header> 
    <s:Body> 
        <GetDomainSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
                <ErrorCode>NoError</ErrorCode> 
                <ErrorMessage /> 
                <DomainResponses> 
                    <DomainResponse> 
                        <ErrorCode>NoError</ErrorCode> 
                        <ErrorMessage>No error.</ErrorMessage> 
                        <DomainSettingErrors /> 
                        <DomainSettings> 
                            <DomainSetting i:type="DomainStringSetting"> 
                                <Name>ExternalEwsUrl</Name> 
                                <Value>https://emea.mail.microsoft.com/EWS/Exchange.asmx</Value> 
                            </DomainSetting> 
                        </DomainSettings> 
                        <RedirectTarget i:nil="true" /> 
                    </DomainResponse> 
                </DomainResponses> 
            </Response> 
        </GetDomainSettingsResponseMessage> 
    </s:Body> 
</s:Envelope>
```

### Response elements

The following elements are used in the response:
  
- [GetDomainSettingsResponseMessage (SOAP)](getdomainsettingsresponsemessage-soap.md)
    
- [Response (SOAP)](response-soap.md)
    
- [ErrorCode (SOAP)](errorcode-soap.md)
    
- [ErrorMessage (SOAP)](errormessage-soap.md)
    
- [DomainResponses (SOAP)](domainresponses-soap.md)
    
- [DomainResponse (SOAP)](domainresponse-soap.md)
    
- [DomainSettingErrors (SOAP)](domainsettingerrors-soap.md)
    
- [DomainSettings (SOAP)](domainsettings-soap.md)
    
- [DomainSetting (SOAP)](domainsetting-soap.md)
    
- [Name (SOAP)](name-soap.md)
    
- [Value (SOAP)](value-soap.md)
    
- [RedirectTarget (SOAP)](redirecttarget-soap.md)
    
## See also



[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
  
[GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md)

