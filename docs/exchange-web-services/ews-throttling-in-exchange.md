---
title: "EWS throttling in Exchange"
manager: sethgros
ms.date: 05/10/2019
ms.audience: Developer
ms.assetid: b4fff4c9-c625-4d2a-9d14-bb28a5da5baf
description: "Learn about the throttling policies that affect EWS when you are using Exchange."
localization_priority: Priority
---

# EWS throttling in Exchange

Learn about the throttling policies that affect EWS when you are using Exchange.

**Provided by:** Glen Scales; Michael Mainer, Microsoft Corporation

The article provides information about EWS throttling in Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with Exchange 2010. Throttling in Exchange helps to ensure server reliability and uptime by limiting the amount of server resources that a single user or application can consume. Throttling is a reactive response to overuse of system resources that may affect service reliability and functionality. Exchange constantly monitors the health of critical infrastructure resources, such as mailbox databases. When high load factors are detected that degrade the performance of these resources, EWS connections are throttled proportionally based on the amount that each caller has contributed to this high load condition. The result is that a user may be within their throttling limit and still experience slowdowns until the health of the resource is back to operational levels.

Each client access protocol in Exchange, including EWS, has a throttling policy. When you design applications that use EWS, it is important to account for throttling policies, to help ensure application reliability and the health of your Exchange server. This article identifies the different throttling policies and service limits for EWS, whether you are targeting Exchange Online or versions of Exchange on-premises starting with Exchange Server 2010. As applicable, this article also identifies differences in throttling policies in different versions of Exchange.

> [!IMPORTANT]
> Default throttling policy, access to throttling policy, and throttling policy configuration differs between Exchange Online and Exchange on-premises. Specific throttling setting values are only accurate for a specific version of Exchange. Because setting values vary across versions, and because Exchange administrators can change the default throttling policies for on-premises deployments, this article does not provide the default setting values. It is more important for you to be aware of the considerations for designing an application that functions within throttling limits and reacts appropriately to throttling scenarios.

If you are an application developer, you need to factor throttling into your application design. Different versions of Exchange have different default values for the EWS throttling parameters. Client and service applications that are designed to access different versions of Exchange will need to account for these settings, whether they be default values, custom values set by an Exchange administrator, or, as for Exchange Online, set by default and not discoverable. Because throttling parameter values cannot be discovered programmatically, your client design specifications should include a plan for the application to adapt to different potential throttling limits. When you design multi-threaded applications that will access a large number of mailboxes, or when many clients are accessing the same mailbox, consider the limits on concurrency that the default policy applies to Exchange.

## Throttling policies that affect EWS

The throttling polices in Exchange affect not only EWS, but also all client connections to the Exchange server, including the protocols used by Office Outlook, Outlook Web App, and Exchange ActiveSync.

The **CPUStartPercent** throttling policy can affect EWS performance when you are running Exchange 2010. When the average CPU utilization of Exchange processes running on the Client Access server — including, but not limited to, the EWS process — exceeds the value specified by this policy, inbound requests will be delayed to reduce CPU utilization. You cannot change the value of this policy, but knowing about it can help you troubleshoot performance issues. The sampling logic the Client Access server performs for this value is an average over a 10 second rolling window. This allows the process to respond appropriately to quick spikes in CPU utilization. When this threshold is exceeded, inbound connections to EWS are delayed. This delay is capped at 500 milliseconds (msecs) at a theoretical 100% CPU usage per EWS request. If a batch EWS request to get 100 items is passed, the server will check the CPU usage 100 times (once per item) for a maximum delay of 50 seconds. The delay time is linearly proportional to CPU usage. At **CPUStartPercent**, the delay is 0 (a thread yield) and it increases linearly up to 500 msec at 100% CPU usage. Because throttling policies apply to all Exchange users, it's unlikely that CPU usage would exceed the **CPUStartPercent** limit on an Exchange Client Access server, because individual users or applications cannot gain enough CPU utilization to affect server operation.

The following table lists the throttling policy parameters that affect applications that use EWS.

**Table 1: Throttling policy parameters that affect EWS**

|**Throttling policy parameter name**|**Applies to**|**Description**|
|:-----|:-----|:-----|
|**DiscoveryMaxConcurrency** |Exchange 2013 Exchange Online |Specifies the number of concurrent discovery search connections that a user can have at the same time. |
|**DiscoveryMaxKeywords** |Exchange 2013 Exchange Online |Specifies the maximum number of keywords that a user can include in a discovery search. |
|**DiscoveryMaxKeywordsPerPage** |Exchange 2013 Exchange Online |Specifies the number of keywords for which to show statistics. |
|**DiscoveryMaxMailboxes** |Exchange 2013 Exchange Online |Specifies the maximum number of source mailboxes that a user can include in a discovery search. |
|**DiscoveryMaxMailboxesResultsOnly** |Exchange 2013 Exchange Online |Specifies the maximum number of mailboxes you can search in an In-Place eDiscovery search without being able to view the statistics. |
|**DiscoveryPreviewSearchResultsPageSize** |Exchange 2013 Exchange Online |Specifies the number of messages returned in a eDiscovery search preview response. |
|**EwsCutoffBalance** |Exchange 2013 Exchange Online |Defines the resource consumption limits for EWS user before that user is completely blocked from performing operations on a specific component. |
|**EwsMaxBurst** |Exchange 2013 Exchange Online |Defines the amount of time that an EWS user can consume an elevated amount of resources before being throttled. This is measured in milliseconds. This value is set separately for each component. |
|**EwsRechargeRate** |Exchange 2013 Exchange Online |Defines the rate at which an EWS user's budget is recharged (budget grows by) during the budget time. |
|**EWSMaxSubscriptions** |Exchange 2010 Exchange 2013 Exchange Online |Defines the maximum number of active push, pull, and streaming notification subscriptions that a user can have on a specific Client Access server at one time. This is budgeted differently for different Exchange versions. |
|**EWSFastSearchTimeoutInSeconds** |Exchange 2010 |Defines the amount of time in seconds that fast searches made by using Exchange Search in EWS continue before they time out. Fast searches are searches made by using an Advanced Query Syntax (AQS) query string in a [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx). |
|**EWSFindCountLimit** |Exchange 2010 Exchange 2013 Exchange Online |Defines the maximum number of items from a [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) or [FindFolder operation](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) that can exist in memory on the Client Access server at one time for one user. The default value for this property is 1000. The [fallback value](https://technet.microsoft.com/library/dd297964%28v=exchg.141%29.aspx#fallback)for this value is 1000. In Exchange Online and on-premises versions of Exchange starting with Exchange 2013, this throttling policy cannot be queried or configured by a cmdlet. In Exchange Online and on-premises versions of Exchange starting with Exchange 2013, the EWSFindCountLimit for [AQS search](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md) and any Exchange search with a restriction is 250 results. An Exchange search without a restriction will return up to 1000 results. |
|**EWSPercentTimeInAD** |Exchange 2010 |Defines the percentage of time per minute during which a specific user can execute Active Directory requests. |
|**EWSPercentTimeInCAS** |Exchange 2010 |Defines the percentage of time per minute during which a specific user can execute Client Access server code. |
|**EWSPercentTimeInMailboxRPC** |Exchange 2010 |Defines the percentage of time per minute during which a specific user can execute mailbox RPC requests |
|**EWSMaxConcurrency** |Exchange 2010 Exchange 2013 Exchange Online |Defines the number of concurrent open connections that a specific user can have against an Exchange server that is using EWS at one time. The default value for Exchange 2010 is 10. The default value for Exchange 2013 and Exchange Online is 27. This policy applies to all operations except for streaming notifications. Streaming notifications use the **HangingConnectionLimit** to indicate the number of open streaming event connections that are available. For more information, see [What throttling values do I need to take into consideration?](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling). |
|**MessageRateLimit** |Exchange 2010 Exchange 2013 Exchange Online |Defines the number of messages per minute that can be submitted. |
|**RecipientRateLimit** |Exchange 2010 Exchange 2013 Exchange Online |Defines the limit to the number of recipients that a user can address in a 24-hour period. |
|**ForwardeeLimit** |Exchange 2010 Exchange 2013 Exchange Online |Defines the limit to the number of recipients for Inbox forward/redirect actions in a 24-hour period. |
|**ConcurrentSyncCalls** |Exchange 2019 Exchange 2016 Exchange Online |Defines the limit to the number of concurrent sync calls (SyncFolderHierarchy, SyncFolderItems) for a user. |

> [!CAUTION]
> Do not set throttling polices to **null**. This will set the policy to equal unlimited, which indicates that a throttling policy isn't set.

## Displaying the policies that apply to Exchange mailboxes

Exchange on-premises provides Exchange Management Shell cmdlets that you can use to set and get throttling policy. Exchange Online does not provide access to the throttling policy cmdlets.

Use the following cmdlets to display throttling polices for an on-premises Exchange Server deployment:

- **Get-ThrottlingPolicy** — Gets the client throttling settings for one or more throttling policies. For more information, see [Get-ThrottlingPolicy](https://technet.microsoft.com/library/dd351264.aspx) on TechNet.

- **Get-ThrottlingPolicyAssociation** — Enables you to view the relationship between an object and its associated throttling policies. The object can be a user with a mailbox, a user without a mailbox, or a contact. For more information, see [Get-ThrottlingPolicyAssociation](https://technet.microsoft.com/library/ff459241.aspx) on TechNet.

Use the following command to show the default throttling policy for Exchange 2010.

- **Get-ThrottlingPolicy | Where-Object {$_.IsDefault -eq "True"} | format-list**

Use the following command to show the global throttling policy (which equates to the default throttling policy in Exchange 2010) in Exchange 2013.

- **Get-ThrottlingPolicy | Where-Object {$_.ThrottlingPolicyScope -eq "Global"} | format-list**

Use the following command to show the throttling policy associated with a user in Exchange 2010 or Exchange 2013. Replace the user name john@contoso.com with the user name of the target user for whom you want to get throttling policy information.

- **Get-ThrottlingPolicyAssociation john@contoso.com | format-list**

Running this command in Exchange Management Shell results in an output similar to the following.

```powershell
PS C:\>Get-ThrottlingPolicyAssociation john@contoso.com
RunspaceId               : 72153d6-9dce-2fae-8dbd-5ca5f760g2df
ObjectId                 : john
ThrottlingPolicyId       :
Name                     : john
Identity                 : FHXB-28178dom.contoso.com/Users/john
IsValid                  : True
NeedsToSuppressPii       : False
ExchangeVersion          : 0.10 (15.0.0.0)
DistinguishedName        : CN=john,CN=Users,DC=FHXB-28178dom,DC=contoso,DC=com
Guid                     : 2c10dab6-de28-1937-ad8g-535832613a08
```

> [!NOTE]
> When the **ThrottlingPolicyId** property is blank, the default policy is applied to the mailbox.

You can set throttling policy on an Exchange server by using the [Set-ThrottlingPolicy](https://technet.microsoft.com/library/dd298094.aspx) and [Set-ThrottlingPolicyAssociation](https://technet.microsoft.com/library/ff459231.aspx) cmdlets. You can create and remove non-default throttling policies by using the [New-ThrottlingPolicy](https://technet.microsoft.com/library/dd351045.aspx) and [Remove-ThrottlingPolicy](https://technet.microsoft.com/library/dd351178.aspx) cmdlets.

> [!TIP]
> We recommend that you design your applications to adhere to the default throttling policy. Only make changes to default throttling policies if your client application design cannot accommodate the default policy. Be aware that less restrictive throttling policies can negatively affect service reliability.

## Throttling considerations for applications that use EWS impersonation

[Impersonation](impersonation-and-ews-in-exchange.md) is an authorization method that enables a single account to access many accounts. When a service account impersonates users, it acts as the users and therefore assumes the rights that are assigned to those users. Log files record the access as the impersonated user. Administrators use role-based access control (RBAC) to configure impersonation via the Exchange Management Shell.

When impersonation is used, the budgets for all the throttling thresholds apply differently depending on the version of Exchange. The budget is either calculated against the account that is impersonated, or the service account. If your application is multi-threaded and makes concurrent requests against multiple mailboxes, you should consider how the throttling threshold will affect your application's performance. In general, be aware of the following limits on service accounts when you create a service-based application that uses impersonation to access all mailboxes:

- When you use Impersonation, the service account has a separate budget for the following policy parameters:

  - **EWSMaxConcurrency**
  - **EWSPercentTimeInAD**
  - **EWSPercentTimeInCAS**
  - **EWSPercentTimeInMailboxRPC**
  - **EWSMaxSubscriptions**
  - **EWSFastSearchTimeoutInSeconds**
  - **EWSFindCountLimit**

- The **EWSMaxConcurrency** budget is shared for the service account and the account being impersonated for all connections to versions of Exchange earlier than Exchange 2010 Service Pack 2 (SP2) Update Rollup 4 (RU4). Starting with Exchange 2010 SP2 RU4, and including Exchange Online, the service account access uses a separate budget from the user **EWSMaxConcurrency** budget. For more information about the update to the Exchange concurrent connection throttling policy for EWS, see [Description of Update Rollup 4 for Exchange Server 2010 Service Pack 2](https://support.microsoft.com/kb/2706690).

    EWS streaming notifications in versions of Exchange starting with Exchange 2010, and including Exchange Online, have an additional cloned **EWSMaxConcurrency** budget from all other EWS client connections. Streaming notification connections are counted against a separate budget than all other EWS operations. The streaming notification maximum concurrency budget is actually two different budgets: one budget is for all service accounts, and one budget is for the account being impersonated. Streaming notifications in Exchange Online and versions of Exchange starting with Exchange 2013 use the [HangingConnectionLimit](#throttling-considerations-for-ews-notification-applications) to limit the number of connections.

    For example, let's assume that **EWSMaxConcurrency** is equal to five. A user can have five open pull notification connections, while an service account can have five concurrent pull notification connections against the user's mailbox at the same time as the user.

- The following table identifies how **EWSMaxSubscriptions** throttling budgets are calculated between the service account and the account to impersonate.

   **Table 2: EWSMaxSubscriptions budget accounting**

   |**Exchange version**|**EWSMaxSubscriptions throttling budget accounting**|
   |:-----|:-----|
   |Exchange Online |Charged against the target mailbox. |
   |Exchange 2013 |Charged against the target mailbox. |
   |Exchange 2010 SP3 |Charged against the target mailbox. |
   |Exchange 2010 SP2 |Charged against the calling account. Starting with Exchange 2010 SP2 RU4, the budget is charged against the target mailbox. |
   |Exchange 2010 SP1 |Charged against the calling account. |
   |Exchange 2010 |Charged against the calling account. |

- Because the **EWSMaxSubscriptions** throttling budget is charged against the account being impersonated, there is no limit on the number of mailboxes a service account can subscribe to and receive streaming notifications for, as long as impersonation is being used. For the account being impersonated, you can't have more than _n_ concurrent requests per target mailbox, where _n_ is the **EWSMaxSubscriptions** value. If you were not using impersonation, the same service account could not have more than _n_ concurrent requests total. So, the takeaway is that by using impersonation on a service account, you exponentially increase the number of mailboxes you can service. For more information, see [Maintain affinity between a group of subscriptions and the Mailbox server in Exchange](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md).

- The **EWSPercentTimeInMailboxRPC**, **EWSPercentTimeInCAS**, and **EWSPercentTimeInAD** policy parameters refer to actions performed by a single thread. When an application performs multiple concurrent operations, you should account for the cumulative effect of these operations on the user resource budget.

## Throttling implications for EWS batch requests

EWS enables you to batch multiple item requests into a single request that is executed by the Client Access server. This allows for greater efficiency and performance. When an Exchange server executes a batched request, it checks the user's budget after the execution of each item within the batch. If the application is over budget, the processing of the next item in the batch is delayed until the budget for that user has recharged. To ensure that applications that use batch operations run successfully, limit the number of item requests that can be included in a single batch, and divide large batches across multiple smaller batches to increase the reliability of the results. The effect that a batch operation has on particular throttling thresholds depends on the type of the request, the size of the items to be processed (for example in **UploadItems** or **ExportItems** operations) and the mailbox content. Throttling policies affect batch operations by causing the request to take longer to process. The caller will therefore have to wait longer for the response, and, because EWS limits the execution time of a batch request to one minute, the call could time out.

To determine the optimum batch size for an application, perform unit testing using various input sets to ensure that the application does not encounter any errors in a production environment.

## Throttling policy parameters that affect EWS search operations

[Search operations in EWS](search-and-ews-in-exchange.md) can require large amounts of time and resources, depending on how the search is run and what information is requested. To control resource usage during searches, two policy parameters take effect: **EWSFastSearchTimeoutInSeconds** and **EWSFindCountLimit**.

The **EWSFastSearchTimeoutInSeconds** policy parameter specifies the amount of time, in seconds, that EWS fast searches (also known as content indexing search) run before they time out. A fast search is a search made by using an Advanced Query Syntax (AQS) query string in a [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx).

You can search an Exchange mailbox folder in two ways:

- By using an Exchange store search, which performs a sequential scan of all messages in the target search scope.

- By using the Exchange Search service (content indexing).

Both of these types of searches can result in timeouts. When possible, use the Exchange Search service because these searches are often targeted against mailbox indexes and use AQS queries. The following example shows how to perform an AQS search of the Inbox by using EWS and the Exchange Search service.

```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiitems = service.FindItems(WellKnownFolderName.Inbox, "subject:football", iv);
```

If you can't use an AQS search, avoid using overly complex search filters. Also try to avoid creating search filters based on computed values if the query involves extended MAPI properties. AQS search was introduced in Exchange 2010.

> [!NOTE]
> The first time you run a complex Exchange store search query, it runs very slowly and may time out. After that, the query will respond more quickly. For more information about the backend Exchange server processes that occur during Exchange store search queries, see [Understanding the Performance Impact of High Item Counts and Restricted Views](https://technet.microsoft.com/library/cc535025%28EXCHG.80%29.aspx) on TechNet. Using a **SearchFilter** creates a dynamic restriction that helps similar queries in the future, but because these restrictions are dynamic in nature, they are not permanent or reliable, and are deleted after a maximum of three days.

The **EWSFindCountLimit** policy parameter specifies the maximum number of items from the results of a **FindItem** or **FindFolder** operation that can exist in memory on a Client Access server at the same time for one user. Every item or folder that EWS processes in a **FindItem** or **FindFolder** request is counted against the budget specified in the **EWSFindCountLimit** element. When the response is sent back to the requester, the find count charge for the current call is released. The response the server returns to a requester when the budget is exceeded is based on the **RequestServerVersion** element value and whether the requester specified paging. When the value of the **RequestServerVersion** element indicates Exchange 2010 or an earlier version of Exchange, the server sends a failure response with error code **ErrorServerBusy**. If the value of the **RequestServerVersion** element indicates a version of Exchange starting with Exchange 2010 SP1 or Exchange Online, and the client is using paging, EWS may return a partial result set instead of an error. Your application should expect that EWS might not return all items. If the value of the **IncludesLastItemInRange** element is false, the application should make another **FindItem** or **FindFolder** request with the new offset and continue until the **IncludesLastItemInRange** element returns true.

When you use a **FindItem** or **FindFolder** operation, it is important to use paging. The EWS Managed API enforces the use of paging, but if you are using other methods, such as EWS proxy objects or raw SOAP, you need to explicitly set paging. The following example shows how to use paging in the EWS Managed API.

```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiFindItemResults = service.FindItems(WellKnownFolderName.Inbox, iv);
```

> [!NOTE]
> The default policy in Exchange limits the page size to 1000 items. Setting the page size to a value that is greater than this number has no practical effect.

Applications should also account for the fact that the _EWSFindCountLimit_ throttling parameter value may result in a partial result set being returned for applications that make concurrent requests. The following example shows how to use the **MoreAvailable** property in the EWS Managed API to ensure that all results are included in a query.

```cs
ItemView iv = new ItemView(1000);
service.TraceEnabled = false;
FindItemsResults<Item> fiResults = null;
Do
{
    fiResults = service.FindItems(WellKnownFolderName.Inbox, iv);
    PropertySet itItemPropSet = new PropertySet(BasePropertySet.IdOnly) { EmailMessageSchema.Body };
    //Process Items in Result Set
    iv.Offset += fiResults.Items.Count;
}
while (fiResults.MoreAvailable == true);
```

## Throttling policies and concurrency

Concurrency refers to the number of connections from a specific user. A connection is held from the moment a request is received until a response is sent to the requester. If users try to make more concurrent requests than their policy allows, the new connection attempt fails. However, the existing connections remain valid. Throttling policies can affect concurrency in a number of different ways.

The **EWSMaxConcurrency** throttling policy parameter sets the number of concurrent connections that a specific user can have against an Exchange server at one time. To determine the maximum number of concurrent connections to allow, consider the connections that Outlook clients will use. Outlook 2007 and Outlook 2010 use EWS to access availability and Out of Office (OOF) information. Mac Outlook 2011 uses EWS for all client access functionality. Depending on the number of Outlook clients that are actively connecting to a user's mailbox, the number of concurrent connections available for a user might be limited. Also, if your application has to connect to multiple mailboxes simultaneously while using a single security context, it is important to take the value of the **EWSMaxConcurrency** policy into account. For more information about using a single security context with concurrent connections, see [Throttling considerations for applications that use EWS impersonation](#throttling-considerations-for-applications-that-use-ews-impersonation) earlier in this article.

Applications that concurrently connect to multiple mailboxes have to be able to track resource usage on the client side. Because EWS operations are request/response-based, you can ensure that your applications function well within the **EWSMaxConcurrency** threshold by tracking the number of connections that occur between the start of a request and when the response is received and ensuring that no more than ten open requests occur concurrently.

The **EWSFindCountLimit** policy parameter specifies the maximum result size a **FindItem** or **FindFolder** operation can use on a Client Access server at the same time for one user. If an application (or potentially multiple applications) makes two concurrent EWS **FindItem** requests that return 100 items each for a specific user, the **EWSFindCountLimit** charge against that specific user's budget will be 200. When the first request returns, the budget drops to 100, and when the second request returns, the budget drops to zero. If the same application were to make two simultaneous requests for 1000 items, the budget value would be 2000 items, which exceeds the **EWSFindCountLimit** value. If the user's budget for items drops below zero, the next request results in an error until the user's budget recharges to one or more.

## Throttling considerations for EWS notification applications

If you are building EWS notification applications that make use of either push, pull, or streaming notifications, you should consider the implications of the **EWSMaxSubscriptions** and the **EWSMaxConcurrency** throttling policies, and the **HangingConnectionLimit**.

The **EWSMaxSubscriptions** policy parameter specifies the maximum number of active push, pull, and streaming subscriptions that a user can have on a specific Client Access server at the same time. Different versions of Exchange have different default values for this parameter. A user can subscribe to all folders in a mailbox by using the **SubscribeToAllFolders** property - this uses a single subscription against the **EWSMaxSubscriptions** budget. Users can subscribe to individual folders, with each folder subscription counting towards the **EWSMaxSubscriptions** budget, up to the limit set by the value of the **EWSMaxSubscriptions** parameter (for example, users can subscribe to 20 calendar folders in different mailboxes if **EWSMaxSubscriptions** is set to 20).

For information about impersonation and the **EWSMaxSubscriptions** parameter, see [Throttling considerations for applications that use EWS impersonation](#throttling-considerations-for-applications-that-use-ews-impersonation) earlier in this article.

The **EWSMaxConcurrency** policy parameter can also be an issue for EWS notifications; for example:

- When EWS increments the connection count for the owner of the subscription while the notification is being generated by a push subscription.

- When an application is designed to listen to multiple users' mailboxes, and users receive simultaneous notifications for an instance of a message that is sent to a distribution list.

If the notification application is multi-threaded and makes simultaneous connection requests to get more information about a particular message that was received by a user account, the **EWSMaxConcurrency** policy limit can be exceeded. To account for this, consider monitoring the concurrent connections in your application, including those that might be used by the server, and implementing request queuing on the client.

The **HangingConnectionLimit** is only applicable to streaming notifications. This limit is set in the web.config file, which means that an Exchange administrator can set this value on an on-premises Exchange server, but Exchange Online mailboxes must use the default value for this limit, which is 10 for Exchange Online, Exchange 2019, Exchange 2016 and 3 for Exchange 2013. To learn more, see [What throttling values do I need to take into consideration?](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).

## Throttling policy and application performance

The following three parameters of the **PercentTimeIn** throttling policy affect the amount of time an EWS application can consume on a Client Access server:

- **EWSPercentTimeInAD**
- **EWSPercentTimeInCAS**
- **EWSPercentTimeInMailboxRPC**

The values specified in the **PercentTimeIn** policy parameters indicate the amount of time that one thread making one request is allocated. For example, assuming a **EWSPercentTimeInCAS** value of 90, if a process makes two concurrent requests that spend 54 seconds each running code on the Client Access server, the process uses 108 seconds in a 60 second window. This represents an **EWSPercentTimeInCAS** parameter value of 180 percent.

> [!NOTE]
> The **EWSPercentTimeInCAS** parameter value is an overlapping superset of the **EWSPercentTimeInAD** and **EWSPercentTimeInMailboxRPC** parameter values. This means that the expenditure in Client Access server processing time will always be larger than the expenditures in **EWSPercentTimeInAD** and **EWSPercentTimeInMailboxRPC**. This is because for the Exchange component to make an Active Directory or RPC call, it must already be running Client Access server code. In addition, the expenditure in processing time for **EWSPercentTimeInCAS** doesn't stop while LDAP or RPC calls are being made. Although the request might be synchronously waiting for a response from Active Directory Domain Services (AD DS) or the Exchange store, the process is still consuming a thread on the server, and therefore the thread should continue to be charged for that usage.

The amount of CPU time an application may take in a 60-second period might exceed these throttling limits; therefore, it is important to consider the volume and type of requests that are being made. For example, a large batch of **ResolveNames** operations that are made simultaneously can exceed the **EWSPercentTimeInAD** policy parameter value. The policy values that are contained in the default throttling policy are designed to allow most EWS applications to function without issue; however, when multi-threaded high-volume applications place a large volume of requests on one particular Client Access server, this can create problems. To avoid this, consider limiting the size of batches that are going to execute against the server.

## Throttling policies and applications that send a large volume of email

The default throttling policies include three rate limit policy parameters that can affect applications that use EWS to send a large volume of messages or send messages in large batches in a short period of time.

> [!NOTE]
> In general, we recommend that you do not use EWS to send bulk email. Use an SMTP host that specializes in bulk mail services to submit frequent large bulk email messages.

The **MessageRateLimit** policy parameter specifies the number of messages per minute that can be submitted by any Exchange client, including EWS. By default, this policy is set to 30 messages per minute in Exchange Online (it's unlimited in Exchange Server). For ordinary users in Exchange Online, this rate limit is generally sufficient. However, applications that send large batches of email messages, for example as part of an invoicing program, can run into problems. When this policy limit is exceeded, message delivery for the mailbox is delayed. Specifically, messages will appear in the Outbox or Drafts folder for longer periods of time when a user or application submits a larger number of messages than the value specified by the **MessageRateLimit** parameter. Be sure to consider this when you are developing a delivery tracking system, especially if your application uses a mailbox that users connect to via Outlook. When deferred items are stored in the Outbox or drafts folder, users might interpret that as an error.

The **RecipientRateLimit** policy parameter specifies the limit on the number of recipients that a user can address in a 24-hour period. For example, if this value is set to 500, it means that a single Exchange mailbox account can send messages to no more than 500 recipients each day. This limit applies to messages to recipients that are inside and outside the organization. This default limit might cause problems for some line-of-business applications that do end-of-month invoice runs and need to send messages to more than this number of recipients. You can use external services that enable batch processing of messages or separate on-premises outbound relay solutions to work around this limitation.

The **ForwardeeLimit** policy parameter specifies the maximum number of recipients that messages can be forwarded or redirected to by means of Inbox rules. This parameter doesn't limit the number of messages that can be forwarded or redirected to the recipients.

## Errors generated when throttling limits are exceeded

When throttling polices are exceeded, EWS generates one of the errors listed in the following table.

**Table 3: Throttling limit errors**

|**Error**|**Throttling policy parameter**|**Description**|
|:-----|:-----|:-----|
|ErrorExceededConnectionCount |**EWSMaxConcurrency** |Indicates that there are more concurrent requests against the server than are allowed by a user's policy. |
|ErrorExceededSubscriptionCount |**EWSMaxSubscriptions** |Indicates that a user's throttling policy maximum subscription count has been exceeded. |
|ErrorExceededFindCountLimit |**EWSFindCountLimit** |Indicates that a search operation call has exceeded the total number of items that can be returned. |
|ErrorServerBusy |**EWSPercentTimeInMailboxRPC**<br/>**EWSPercentTimeInCAS**<br/>**EWSPercentTimeInAD** |Occurs when the server is busy. The BackOffMilliseconds value returned with ErrorServerBusy errors indicates to the client the amount of time it should wait until it should resubmit the request that caused the response that returned this error code. |

The following table lists the HTTP status codes that are returned by throttling errors.

**Table 4: HTTP status codes returned by throttling errors**

|**HTTP status code**|**Description**|
|:-----|:-----|
|HTTP 503 |Indicates that EWS requests are queuing with IIS. The client should delay sending additional requests until a later time. |
|HTTP 500 |Indicates an internal server error with the ErrorServerBusy error code. This indicates that the client should delay sending additional requests until a later time. The response may contain a back off hint called BackOffMilliseconds. If present, the value of BackOffMilliseconds should be used as the duration until the client resubmits a request. |
|HTTP 200 |Contains an EWS schema-based error response with an ErrorInternalServerError error code. An inner ErrorServerBusy error code may be present. This indicates that the client should delay sending additional requests until a later time. |

## See also

- [Exchange Workload Management](https://technet.microsoft.com/library/jj150503.aspx)
- [New-ThrottlingPolicy cmdlet](https://technet.microsoft.com/library/dd351045.aspx)
- [Understanding Client Throttling Policies](https://technet.microsoft.com/library/dd297964.aspx)
- [ThrottlingPolicy Class](https://msdn.microsoft.com/library/ff342496%28v=EXCHG.140%29.aspx)
- [Throttling Policies and the EWSFindCountLimit](https://blogs.msdn.com/b/exchangedev/archive/2010/03/12/throttling-policies-and-the-ewsfindcountlimit.aspx)
- [Budget Snapshots in the IIS Logs](https://blogs.msdn.com/b/exchangedev/archive/2010/03/10/budget-snapshots-in-the-iis-logs.aspx)
- [Effects of Throttling on Your Deployment in Exchange 2010 SP1](http://msexchangeteam.com/archive/2010/08/27/456040.aspx)
- [Throttling Policy Associations in Exchange 2010 SP1](http://msexchangeteam.com/archive/2010/08/02/455707.aspx)
- [Throttling Policies and CPUStartPercent](https://blogs.msdn.com/b/exchangedev/archive/2010/03/11/throttling-policies-and-cpustartpercent.aspx)
- [Impersonation and EWS in Exchange](impersonation-and-ews-in-exchange.md)
