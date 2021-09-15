---
title: "Handling notification-related errors in EWS in Exchange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 519e1e52-5f1f-4f06-931e-8c20a586a563
description: "Find out how to handle notification-related errors in applications that you develop by using the EWS Managed API or EWS in Exchange."
---

# Handling notification-related errors in EWS in Exchange

Find out how to handle notification-related errors in applications that you develop by using the EWS Managed API or EWS in Exchange.

If your application subscribes to and gets notifications, you might have to handle notification-related errors. You can handle these errors at runtime, or while you are developing your EWS application.

**Table 1. Notification-related errors and how to handle them**

|Error|Occurs when you try to…|Handle it by…|
|:-----|:-----|:-----|
|**ErrorExceededConnectionCount** |Open a connection to get events when the account reached its connection limit of open streaming connections. | <ul><li>Using [impersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) to [open connections](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).</li><li>Using fewer connections to get events. Maximize the number of subscriptions in each connection by [using affinity](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md) and [placing a maximum of 200 subscription IDs in the same group](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howdoimaintain). You can then use the same connection to retrieve events for the entire group, reducing the number of connections required.</li><li>  Changing the value of the HangingConnectionLimit in the web.config file for Exchange on-premises to override the default value of three open connections. Exchange Online has a default HangingConnectionLimit of 10, which is not configurable.</li></ul> |
|**ErrorExceededSubscriptionCount** |Create too many subscriptions. The [EwsMaxSubscriptions](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx) throttling policy parameter determines the maximum number of subscriptions that an account can create. | <ul><li>Using [impersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) to [create subscriptions](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).</li><li>Reducing the number of subscriptions.</li></ul> |
|**ErrorInvalidSubscriptionRequest** |Create subscriptions for multiple mailboxes or multiple folders from a single request.  |Creating a subscription for a single public folder or a single mailbox in a single request.|
|**ErrorInvalidWatermark** |Get events by using an invalid watermark.| <ul><li>Checking the subscription ID returned in a previous response.</li><li>Ensuring that you're sending the subscription ID for the correct **ExchangeService** object.</li><li>[Creating a new subscription](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).</li></ul> |
|**ErrorMissedNotificationEvents** |Get events when some previous events were missed.   |Comparing the extended folder properties **PR_LOCAL_COMMIT_TIME_MAX** (0x670a) and **PR_DELETED_COUNT_TOTAL** (0x670b) to determine what changes were missed, and [creating a new subscription](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).  |
|**ErrorProxyRequestNotAllowed** |Subscribe to events for a user in a batched request whose mailbox has moved to another site.   |Using [Autodiscover](autodiscover-for-exchange.md) to rediscover the ExternalEwsUrl or EwsPartnerUrl, and creating a new subscription.  |
|**ErrorReadEventsFailed** |Get events from a subscription that cannot be found.  |Using [Autodiscover](autodiscover-for-exchange.md) to rediscover the ExternalEwsUrl or EwsPartnerUrl, and creating a new subscription.  |
|**ErrorServerBusy** | Exceed [throttling](ews-throttling-in-exchange.md#throttling-considerations-for-ews-notification-applications) limits. Be aware of the following regarding throttling:<ul><li>The [EwsMaxSubscriptions](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx) throttling limit identifies the maximum number of push, pull, or streaming notification subscriptions that can be active at one time. This is the value of mailbox subscriptions, not the number of individual folder subscriptions in a mailbox subscription. Starting with service mailbox versions 14.16.0135 and 14.15.0057.000, a mailbox hosted by Exchange Online or Exchange Online as part of Office 365 can have up to 20 subscriptions, and a target Exchange 2013 on-premises mailbox can have up to 5000 subscriptions.</li><li>The [EwsMaxConcurrency](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxconcurrency%28v=exchg.150%29.aspx) throttling limit identifies the maximum number of active requests for non-streaming connections and has a default value of 27.</li><li>The default limit for open streaming connections is ten.</li></ul> |<ul><li>[Considering the implications of the notification-related throttling policies](ews-throttling-in-exchange.md#throttling-considerations-for-ews-notification-applications) and limiting the number of active subscriptions and active connections so that the application is not throttled.</li><li>Using fewer connections to get events. Maximize the number of subscriptions in each connection by [placing a maximum of 200 subscription IDs in the same group](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md). You can then use the same connection to retrieve events for the entire group, reducing the number of connections required.</li><li>Changing the value of the HangingConnectionLimit in the web.config file to override the default value of ten open streaming connections.</li></ul>|
|**ErrorSubscriptionNotFound** |Get events for a subscription that cannot be found. The subscription might have expired, the EWS process might have been restarted, or an invalid subscription was passed in. | <ul><li>Verifying that you're using the same subscription ID that was returned in a previous response.</li><li>Ensuring that you're sending the subscription ID for the correct **ExchangeService** object.</li><li> [Creating a new subscription](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover).</li></ul> |
|**[ServiceLocalException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)** |Add a subscription to a new folder while a subscription connection is open on another folder.  |Changing your subscription to subscribe to all folders in the mailbox, instead of a specific folder.  |
|**[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)** |Get events for a subscription that cannot be located in the Exchange store.  | <ul><li>Verifying that you're using the same subscription ID that was returned in a previous response.</li><li>Ensuring that you're sending the subscription ID for the correct **ExchangeService** object.</li></ul> |

## Recovering from lost subscriptions
<a name="bk_recover"> </a>

When a subscription is lost, or is no longer accessible, it is best to create a new subscription and not include the old watermark in the new subscription. Resubscribing with the old watermark causes a linear scan for events, which is costly. Instead, create a new subscription and compare folder properties to look for content changes that occurred between the lost subscription and the new subscription. The extended folder properties that we recommend that you check are **PR_LOCAL_COMMIT_TIME_MAX** (0x670a0040) and **PR_DELETED_COUNT_TOTAL** (0x670b0003). You can do this by [creating an extended property definition](properties-and-extended-properties-in-ews-in-exchange.md).

## See also

- [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [Stream notifications about mailbox events by using EWS in Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [Pull notifications about mailbox events by using EWS in Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [Maintain affinity between a group of subscriptions and the Mailbox server in Exchange](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)


