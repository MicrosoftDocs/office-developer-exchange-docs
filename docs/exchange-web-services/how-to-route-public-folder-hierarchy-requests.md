---
title: "Route public folder hierarchy requests"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: ec35df8e-4d75-4aa1-8b9c-ae1db7e05772
description: "All requests for public folder information that require knowledge of the public folder hierarchy, such as moving, updating, deleting, or finding public folders, need to be routed to the default public folder hierarchy mailbox for the given user. To route the requests to that mailbox, you need to set the X-AnchorMailbox and X-PublicFolderMailbox headers to specific values returned by the Autodiscover service."
---

# Route public folder hierarchy requests

All requests for public folder information that require knowledge of the public folder hierarchy, such as moving, updating, deleting, or finding public folders, need to be routed to the default public folder hierarchy mailbox for the given user. To route the requests to that mailbox, you need to set the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers to specific values returned by the Autodiscover service. 
  
**Overview of public folders**

|Header|What do I need?|How do I get it?|
|:-----|:-----|:-----|
|**X-AnchorMailbox** <br/>|The [PublicFolderInformation](/dotnet/api/microsoft.exchange.webservices.autodiscover.usersettingname) value from a [GetUserSettings](/exchange/client-developer/web-service-reference/getusersettings-operation-soap) Autodiscover SOAP response, which becomes the value of the **X-AnchorMailbox** header.|1. Send a **GetUserSetting** request with the SMTP address for the user's mailbox.<br/><br/>2. Use the **PublicFolderInformation** element to populate the value of the **X-AnchorMailbox** header. The value of the **PublicFolderInformation** element is an SMTP address.  <br/>
|**X-PublicFolderMailbox** <br/> |The [InternalRpcClientServer](/exchange/client-developer/web-service-reference/setting-soap) value from a [GetUserSettings](/exchange/client-developer/web-service-reference/getusersettings-operation-soap) Autodiscover SOAP response, which becomes the value of the **X-PublicFolderMailbox** header.|1. Send a **GetUserSetting** request with the SMTP address for the user's mailbox.<br/><br/>2. Use the **InternalRpcClientServer** element returned by the Autodiscover service to populate the value of the **X-PublicFolderMailbox** header. The value of the **X-PublicFolderMailbox** element is an SMTP address where the user part of the address is a GUID.|

After you have determined the header values, include them [when you make public folder hierarchy requests](#bk_setheadervalues).
  
The steps in this article are specific to public folder hierarchy requests. To determine whether your request is a public folder hierarchy or content request, see [Routing public folder requests](public-folder-access-with-ews-in-exchange.md#bk_routing). 
  
## Determine the header values using the EWS Managed API
<a name="bk_getpfinfoewsma"> </a>

You can use a single call to [GetUserSettings](/exchange/client-developer/web-service-reference/getusersettings-operation-soap) using the following code, which retrieves both **InternalRpcClientServer** and **PublicFolderInformation** elements. Include the SMTP address of the mailbox user as an input parameter.
  
```cs
GetUserSettingsResponse userResponse = GetUserSettings(adservice, "sonyaf@contoso.com", 3, UserSettingName.PublicFolderInformation, UserSettingName.InternalRpcClientServer);
Console.WriteLine("X-AnchorMailbox value for public folder hierarchy requests: {0}", userResponse.Settings[UserSettingName.PublicFolderInformation]);
Console.WriteLine("X-PublicFolderMailbox value for public folder hierarchy requests: {0}", userResponse.Settings[UserSettingName.InternalRpcClientServer]);
```

After running the code, the following information is displayed on the console:
  
`X-AnchorMailbox for public folder hierarchy requests: SharedPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox value for public folder hierarchy requests: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`

Now that you have the **PublicFolderInformation** value, include it as the value for the X-AnchorMailbox header in all public folder hierarchy requests. The **InternalRpcClientServer** value is used for the X-PublicFolderMailbox header.  Both headers are required.
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`

## Determine the the header values using SOAP
<a name="bk_getpfinfoews"></a>

The following code example shows how to retrieve the **PublicFolderInformation** and **InternalRpcClientServer** values using the [GetUserSettings](/exchange/client-developer/web-service-reference/getusersettings-operation-soap) SOAP operation. The mailbox user is specified in the [Mailbox](/exchange/client-developer/web-service-reference/mailbox-soap) element, and the [RequestedSettings](/exchange/client-developer/web-service-reference/requestedsettings-soap) element limits the response to the [PublicFolderInformation](/dotnet/api/microsoft.exchange.webservices.autodiscover.usersettingname) and [InternalRpcClientServer](/exchange/client-developer/web-service-reference/setting-soap) values.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2016</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover-s.outlook.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>sonyaf@contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>PublicFolderInformation</a:Setting>
          <a:Setting>InternalRpcClientServer</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>
```

The response includes the **PublicFolderInformation** value. 
  
```XML
<UserSetting i:type="StringSetting">
  <Name>InternalRpcClientServer</Name>
  <Value>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</Value>
</UserSetting>
<UserSetting i:type="StringSetting">
    <Name>PublicFolderInformation</Name>
    <Value>SharedPublicFolder@contoso.com</Value>
</UserSetting>
```

Now that you have the **PublicFolderInformation** value, include it as the value for the X-AnchorMailbox header in all public folder hierarchy requests. Use the **InternalRpcClientServer** value for the X-PublicFolderMailbox header. Both headers are required.
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`


For more information about the Autodiscover process, see [Autodiscover for Exchange](autodiscover-for-exchange.md), [Generate a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).
  
## Set the values of the X-AnchorMailbox and X-PublicFolderMailbox headers
<a name="bk_setheadervalues"></a>


Using the values of **PublicFolderInformation** and **InternalRpcClientServer** acquired in [Determine the value of the X-AnchorMailbox header by using the EWS Managed API](#bk_getpfinfoewsma) or [Determine the value of the X-AnchorMailbox header using SOAP](#bk_getpfinfoews), set the values of **X-AnchorMailbox** and **X-PublicFolderMailbox** headers in your public folder content request.
  
For example, given a **PublicFolderInformation** SMTP address of SharedPublicFolder@contoso.com and an **InternalRpcClientServer** value of 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com, include the following headers when making calls to the following methods or operations.
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com` <br/>
`X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`

**Public folder calls that require the X-AnchorMailbox and X-PublicFolder headers**

|**EWS Managed API methods**|**EWS operations**|
|:-----|:-----|
|[Folder.FindFolders](/dotnet/api/microsoft.exchange.webservices.data.folder.findfolders) <br/> [Folder.Delete](/dotnet/api/microsoft.exchange.webservices.data.folder.delete) <br/> [Folder.Update](/dotnet/api/microsoft.exchange.webservices.data.folder.update) <br/> [Folder.Move](/dotnet/api/microsoft.exchange.webservices.data.folder.update) <br/> |[CreateFolder](/exchange/client-developer/web-service-reference/createfolder-operation) <br/> [FindFolder](/exchange/client-developer/web-service-reference/findfolder-operation) <br/> [DeleteFolder](/exchange/client-developer/web-service-reference/deletefolder-operation) <br/> [UpdateFolder](/exchange/client-developer/web-service-reference/updatefolder-operation) <br/> [MoveFolder](/exchange/client-developer/web-service-reference/movefolder-operation) <br/> |

To add these headers by using the EWS Managed API, use the [HttpHeaders.Add](/previous-versions/visualstudio/hh193855(v=vs.118)) method.
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "SharedPublicFolder@contoso.com");
service.HttpHeaders.Add("X-PublicFolderMailbox", "1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com");
```

For example, the following code shows a [FindFolder](/exchange/client-developer/web-service-reference/findfolder-operation) request with the **X-AnchorMailbox** and **X-PublicFolderMailbox** header set to the values retrieved in the examples in this article. 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
X-AnchorMailbox: SharedPublicFolder@contoso.com
X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com
Host: outlook.office365.com
Content-Length: 1174
Expect: 100-continue
Connection: Keep-Alive
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Shallow">
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:IsEqualTo>
          <t:FieldURI FieldURI="folder:DisplayName" />
          <t:FieldURIOrConstant>
            <t:Constant Value="My Public Contacts" />
          </t:FieldURIOrConstant>
        </t:IsEqualTo>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:FolderId Id="AQEuAAADy/LIWjRCp0GFb0W6aGPbwwEARg5aCLUc8k6wLfl1c0a/2AAAAwIAAAA=" ChangeKey="AQAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/XB" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

## See also

- [Public folder access with EWS in Exchange](public-folder-access-with-ews-in-exchange.md)
- [Route public folder content requests](how-to-route-public-folder-content-requests.md)
- [Get user settings by using the EWS Managed API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)
