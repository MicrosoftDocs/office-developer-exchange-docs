---
title: "Control access to EWS in Exchange"
manager: sethgros
ms.date: 04/07/2025
ms.audience: Developer
ms.assetid: 61e29e54-e3e5-404a-84c0-93b61a25ca58
description: "Find out how to control access to EWS for users, applications, or the entire organization."
ms.localizationpriority: high
---

# Control access to EWS in Exchange

Find out how to control access to EWS for users, applications, or the entire organization.
  
Whether you are using the EWS Managed API, or EWS directly, in your application, you can control access to Exchange Web Services (EWS). If you have administrator access to your Exchange server, you can manage access to EWS by using the Exchange Management Shell to control access globally, for each user, and for each application. For more information, see [Connect to Exchange servers using remote PowerShell](/powershell/exchange/connect-to-exchange-servers-using-remote-powershell).
  
## Exchange Management Shell cmdlets for configuring access control
<a name="bk_Cmdlets"> </a>

You can use the following Exchange Management Shell cmdlets to view the current access configuration and set EWS access controls:
  
- [Get-CASMailbox](/powershell/module/exchange/get-casmailbox) - Shows you what parameters are set for a particular mailbox.   
- [Set-CASMailbox](/powershell/module/exchange/set-casmailbox) - Sets parameters for a particular mailbox.    
- [Get-OrganizationConfig](/powershell/module/exchange/get-organizationconfig) - Shows you the parameters for the entire organization.    
- [Set-OrganizationConfig](/powershell/module/exchange/set-organizationconfig) - Sets the parameters for the entire organization. 

> [!NOTE]
> The way the EWSEnabled parameter operates will change in October 2026 due to the EWS Deprecation. For more information, see [Exchange Online EWS, Your Time is Almost Up](https://techcommunity.microsoft.com/blog/exchange/exchange-online-ews-your-time-is-almost-up/4492361).

<a name="bk_Examples"> </a>

## Examples: Controlling access to EWS

Let's take a look at a few scenarios that show you how you can control access to your application.
  
**Table 1. Commands for controlling access to EWS**

|If you want to |Use this command|
|:-----|:-----|
|Allow a list of client applications to use EWS (Based on User Agent). | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList -EwsAllowList:"OWA/*"`<br/><br/>This allows specific applications to use EWS. In this example, any application that has a user agent string that starts with "OWA/" is allowed access. **Note: User Agent based blocking also impacts connections using REST/Graph API**|
|Allow a list of client applications to use EWS (Based on Application ID). | `Set-OrganizationConfig -EwsAllowedAppIDs "11111111-2222-3333-4444-555555555555,aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee"`<br/><br/> When EWSEnabled is set to True, only the Application IDs in this list can use EWS. |
|Allow all client applications to use EWS except those that are specifically blocked (Based on User Agent). | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList -EwsBlockList:"OWA/*"`<br/> <br/>This example only blocks applications from using EWS that have a user agent string that starts with "OWA/". **Note: User Agent based blocking also impacts connections using REST/Graph API**|
|Block the entire organization from using EWS. | `Set-OrganizationConfig -EwsEnabled:$false` <br/><br/> **Important**: Disabling EWS in the organization also disables per-user EWS overrides. |
|Allow the entire organization to use EWS. | `Set-OrganizationConfig -EwsEnabled:$true` <br/><br/> **Important**: The default value Null is treated as EwsEnabled set to True.|
|Block an individual mailbox from using EWS. | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$false`|
|Allow an individual mailbox to use EWS. | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$true`|

> [!NOTE]
> EwsAllowedAppIDs and the EWSAllowList/EWSBlockList are both evaluated for each connection, and both must pass for a connection to be allowed. If a tenant uses EwsApplicationAccessPolicy:EnforceAllowList in addition to configuring the EWSAllowedAppIDs list, they must keep all required user agents in the EwsAllowList. For example, it must include 'Teams CalendarSkypeSpaces/1.0a$*+' when the Teams AppID cc15fd57-2c6c-4117-a88c-83b1d56b4bbe is allowed, otherwise Teams Calendar will be blocked.

## Understand HTTP 403 responses in Exchange Online

When the EWS access controls described above block a request, Exchange Online returns **HTTP 403 Forbidden** with diagnostic information in the **`X-EWS-Policy-Reason`** response header. Applications should inspect this header rather than rely on an error message in the response body.

### Three reasons an application can be blocked

1. **EWS is disabled for the user or organization.**  
The applicable `EwsEnabled` setting prevents access. Organization-wide disablement also blocks users whose mailbox-level setting is enabled.
2. **The application is not allowed by the Application ID allow list.**  
When Application ID restrictions apply, the application's ID must be included in `EwsAllowedAppIDs`.
3. **The application is blocked by a User-Agent policy.**  
With `EnforceAllowList`, the application's User-Agent must match an entry in `EwsAllowList`. With `EnforceBlockList`, it must not match an entry in `EwsBlockList`.

### Two diagnostic messages

There are **two possible values for one response header**, not a separate error message for each blocking condition. Application ID and User-Agent policy blocks return the same message.

|`X-EWS-Policy-Reason` value|Meaning|Configuration to inspect|
|-|-|-|
|`EWS is disabled for this user or tenant`|EWS is disabled by the applicable user or organization configuration.|Organization and mailbox `EwsEnabled` settings.|
|`EWS is blocked by policy for this user or tenant`|An application access policy prevents the request. The message does not distinguish Application ID blocking from User-Agent blocking.|`EwsAllowedAppIDs`, and the applicable `EwsApplicationAccessPolicy`, `EwsAllowList`, or `EwsBlockList` settings.|

For example, when EWS is disabled:

```http
HTTP/1.1 403 Forbidden
X-EWS-Policy-Reason: EWS is disabled for this user or tenant
```

When an application is blocked by an Application ID or User-Agent policy:

```http
HTTP/1.1 403 Forbidden
X-EWS-Policy-Reason: EWS is blocked by policy for this user or tenant
```

Both policy types use the second header value.

> \[!NOTE]
> An HTTP 403 status alone does not establish that EWS disablement or one of these application policies caused the failure. These diagnostic messages identify the access-control blocks described in this section; other access restrictions can also produce HTTP 403 responses.

## Troubleshoot a blocked EWS request

### 1\. Inspect the response header

Check the HTTP status and the `X-EWS-Policy-Reason` value. Use the diagnostic message to determine whether to investigate EWS disablement or application access policies.

### 2\. Review the organization configuration

Inspect organization-level EWS enablement and User-Agent policies:

```powershell
Get-OrganizationConfig |
    Format-List EwsEnabled,EwsApplicationAccessPolicy,EwsAllowList,EwsBlockList
```

Retrieve the Application ID allow list separately:

```powershell
Get-OrganizationConfig -RetrieveEwsOperationAccessPolicy |
    Format-List EwsAllowedAppIDs
```

Use `-RetrieveEwsOperationAccessPolicy` to retrieve the configured `EwsAllowedAppIDs` value.

### 3\. Review the affected mailbox

Check whether EWS is enabled for the mailbox:

```powershell
Get-CASMailbox -Identity adam@contoso.com |
    Format-List EwsEnabled
```

Inspect the mailbox setting as well as the organization setting. Enabling EWS for a mailbox does not override organization-wide disablement.

### 4\. Identify the applicable restriction

If the header says **`EWS is disabled for this user or tenant`**:

* Review organization and mailbox `EwsEnabled` settings.
* If access should be permitted, correct the applicable disablement setting.
* Do not expect an Application ID or User-Agent allow-list change to restore access while EWS remains disabled.

If the header says **`EWS is blocked by policy for this user or tenant`**:

* Check whether the application's ID is included in `EwsAllowedAppIDs` when Application ID restrictions apply.
* Check whether its User-Agent satisfies the applicable allow-list or block-list policy.
* Review both policy types. The header does not identify which one blocked the request, and passing one check does not bypass the other.

Before changing a restriction, confirm that the application should be permitted under your organization's access policy.

### 5\. Allow time for changes to take effect

Changes to `EwsAllowedAppIDs` can take up to **24 hours** to take effect because of caching. An immediate retry might still reflect the previous configuration.

   
## See also

- [Setting up your EWS application](setting-up-your-ews-application.md)    
- [Controlling client application access to EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md)   
- [Exchange Server PowerShell (Exchange Management Shell)](/powershell/exchange/exchange-management-shell) 
- [Windows PowerShell](/powershell/scripting/overview)
