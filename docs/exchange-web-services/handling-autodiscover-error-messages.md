---
title: "Handling Autodiscover error messages"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.assetid: e5939ec2-1100-4174-8a88-5a6e09b60b23
description: "Learn about the different types of Autodiscover errors and what to do with them."
localization_priority: Priority
---

# Handling Autodiscover error messages

Learn about the different types of Autodiscover errors and what to do with them.
  
Autodiscover enables your applications to retrieve configuration information automatically, and it works great. However, things don't always go according to plan. Let's look at the common errors that might occur and how you can handle them to minimize the need to prompt your user to manually configure your client.
  
## HTTP status errors
<a name="bk_HttpErrors"> </a>

The first type of error you might encounter when sending Autodiscover requests is the HTTP status. If the HTTP status in your response is anything other than 200 (OK), the response payload doesn't contain the Autodiscover response you were looking for. For simplicity, we can group non-200 status codes into three categories.
  
**Table 1. HTTP status codes**

|**Status code**|**Type of error**|**To handle…**|
|:-----|:-----|:-----|
|301 or 302  <br/> |Redirect error  <br/> |Resend your request to the URI contained in the "Location" HTTP response header. For details, see [Handling redirect errors](#bk_HandlingRedirects).  <br/> |
|401  <br/> |Unauthorized error  <br/> |Because the [Autodiscover process](autodiscover-for-exchange.md) involves trying multiple potential URLs, you could get this on one URL only to have the next one accept your credentials. For this reason, you shouldn't consider a single 401 error to indicate that the credentials are invalid. However, if you receive 401 errors from multiple URLs, you might want to prompt the user to reenter their password (if possible).  <br/> |
|Any other non-200 status  <br/> |Invalid Autodiscover endpoint error  <br/> |Consider the URL that returns any other non-200 status code to be invalid, and continue trying the next URL in your list.  <br/> |
   
## Autodiscover errors
<a name="bk_AutodiscoverErrors"> </a>

Even if you get a 200 (OK) status code after sending an Autodiscover request, that doesn't mean that the server sent the information you need. The 200 status only means that you have an Autodiscover response, and that response might contain an error within the payload. The location of the error information differs depending on whether the format is SOAP or POX.
  
### SOAP Autodiscover errors

For SOAP Autodiscover, the response can contain one or more [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) elements, in different places. Typically you can expect one as a child element of the [Response (SOAP)](https://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx) element, and one as a child of each [UserResponse (SOAP)](https://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx) element in the response. You might also encounter one as a child of a [UserSettingError (SOAP)](https://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx) element, if one is present. The context of the error depends on where the **ErrorCode** element is located, as follows: 
  
- As a child element of the **Response** element, the **ErrorCode** element represents an error that applies to the entire request. 
    
- As a child of the **UserResponse** element, it represents an error that applies just to that specific user. 
    
- As a child of a **UserSettingError** element, it represents an error that applies to a specific setting that was requested. 
    
Let's take a look at an example of a response. In this example, the **ErrorCode** element under the **Response** element has a value of "NoError", which indicates overall success. However, the **ErrorCode** element under the **UserResponse** element has a value of "RedirectAddress", which indicates that an error occurred for that particular user. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>14</h:MajorVersion>
      <h:MinorVersion>3</h:MinorVersion>
      <h:MajorBuildNumber>136</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2010_SP2</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>RedirectAddress</ErrorCode>
            <ErrorMessage>Redirection address.</ErrorMessage>
            <RedirectTarget>elvin@mail.contoso.com</RedirectTarget>
            <UserSettingErrors />
            <UserSettings />
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

The [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) article contains a full list of possible errors. Most of these indicate an unrecoverable error, but a few warrant special handling. 
  
**Table 2. SOAP Autodisover ErrorCode values**

|**ErrorCode value**|**To handle…**|
|:-----|:-----|
|RedirectAddress  <br/> |[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectTarget (SOAP)](https://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx) element.  <br/> |
|RedirectUrl  <br/> |[Resending your request to a new URL](#bk_ResendRequest) to the URL in the **RedirectTarget** element.  <br/> |
|ServerBusy  <br/> |Retry this URL after a small delay. You might wait a set amount of time or simply move this URL to the end of your list of URLs to try. If you receive this error multiple times from a URL, you should consider the URL to be invalid.  <br/> |
   
### POX Autodiscover errors

The POX Autodiscover service reports errors a little differently. Non-recoverable errors are contained in the [Error (POX)](https://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx) element. The [ErrorCode (POX)](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) article contains a full list of possible error codes. 
  
Redirect errors are contained in the [Action (POX)](https://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx) element. Any value of the **Action** element other than "settings" indicates a redirect error. 
  
**Table 3. POX Autodisover ErrorCode values**

|**Action value**|**To handle…**|
|:-----|:-----|
|redirectAddr  <br/> |[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectAddr (POX)](https://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx) element.  <br/> |
|redirectUrl  <br/> |[Resending your request to a new URL](#bk_ResendRequest) to the URL in the [RedirectUrl (POX)](https://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx) element.  <br/> |
   
In this example, the **Action** element has a value of "redirectAddr", which indicates that a new request should be sent with the new email address contained in the **RedirectAddr** element. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <Account>
      <Action>redirectAddr</Action>
      <RedirectAddr>elvin@mail.contoso.com</RedirectAddr>
    </Account>
  </Response>
</Autodiscover>
```

## Handling redirect errors
<a name="bk_HandlingRedirects"> </a>

You can handle redirect error scenarios in two ways:
  
- By restarting Autodiscover with a new email address.
    
- By resending your request to a new URL.
    
Both scenarios require some validation before proceeding.
  
### Restarting Autodiscover with a new email address
<a name="bk_RestartAutodiscover"> </a>

When you get a new email address in an Autodiscover redirect response, first verify that the new email address that was provided in the redirect error response is not the same address that you sent in the request that resulted in the error. If it is, you should not restart Autodiscover and instead consider the URL that generated the response to be invalid.
  
If the new email address is different, discard your existing list of potential Autodiscover endpoint URLs and generate a new list based on the new email address.
  
### Resending your request to a new URL
<a name="bk_ResendRequest"> </a>

When you get a new URL in an Autodiscover redirect response, you should first validate the URL as follows:
  
- Verify that the URL is an HTTPS URL.
    
- Verify that you have not received an error from this URL with the current email address before.
    
- If applicable to your application, inform the user of the redirection and get their permission to follow the redirect.
    
- Send a request to the URL and [verify that the SSL certificate presented by the server is valid](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).
    
If the URL passes validation, resend the request to this new URL.
  
## See also


- [Autodiscover for Exchange](autodiscover-for-exchange.md)
    
- [Find Autodiscover endpoints by using SCP lookup in Exchange](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)
    
- [ErrorCode (POX)](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)
    

