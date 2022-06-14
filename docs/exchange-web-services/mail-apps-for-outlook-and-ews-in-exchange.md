---
title: "Outlook add-ins and EWS in Exchange"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 821c8eb9-bb58-42e8-9a3a-61ca635cba59
description: "Find information about Outlook add-ins and how they work with EWS in Exchange."
localization_priority: Priority
---

# Outlook add-ins and EWS in Exchange

Find information about Outlook add-ins and how they work with EWS in Exchange.

Outlook add-ins provide a single interface and programming model that uses web standards to enable you to create a custom experience for your email users. You can create mail apps that display contextual or helpful information in an HTML5 frame hosted in Outlook; for example, a mail app can show a Bing map with an address highlighted when an email message contains an address. Or when a user is composing a message, a mail app can show additional information about the recipient, and insert a standard greeting into the email at the touch of a button.

> [!NOTE]
> "Outlook" in this article refers to the Outlook rich client, Outlook RT, Outlook Web App, and OWA for Devices.

The mail apps interface is part of the JavaScript API for Office. You can use the API to access information in Exchange to enable your mail app to:

- [Recognize entities](https://msdn.microsoft.com/library/a6b0904b-afe9-4882-9136-3d8cfd57fcf8%28Office.15%29.aspx), like addresses, phone numbers, task suggestions, or meeting suggestions in an email.

- Open and display existing [messages](https://msdn.microsoft.com/library/d0bca550-70c3-457c-85f8-e19b39e3b892%28Office.15%29.aspx) and [appointments](https://msdn.microsoft.com/library/6cfbc29d-8581-474e-9a8b-510471e4bf8b%28Office.15%29.aspx) in a separate view so that users can cross-reference information in one or more messages.

- [Make EWS requests](https://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx) to the Exchange server that hosts the user's mailbox. A mail app can, for example, get a list of folders so that the user can choose one to store the message, or show all the items in a conversation, or mark an email message as junk.

- [Get a token](https://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx) to uniquely identify an email account to enable single sign on on a third-party service.

- [Get a token](https://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx) that enables a third-party service to make EWS requests on behalf of the user, for example, to extract the attachments from an item, or to get an item from the Exchange server for further processing.

You can use mail apps to customize the Outlook Web App experience for your users; if, however, you want to customize the "look and feel" of Outlook Web App, see these articles on TechNet:

- [Create a theme for Outlook Web App](https://technet.microsoft.com/library/bb201700%28v=exchg.150%29.aspx)

- [Customize the Outlook Web App sign-in, language selection, and error pages](https://technet.microsoft.com/library/ee633483%28v=exchg.150%29.aspx)

Your organization can install mail apps on an internal server to limit access to authorized users, or you and other mail app developers can put mail apps on the [Office Store](https://office.microsoft.com/store/) for sale to the general public. Anyone who is running Outlook can download, install, and use mail apps from the marketplace.

If you want to learn more about creating mail apps, check out the [Outlook add-ins documentation](/outlook/add-ins) or the [Make an EWS request](https://code.msdn.microsoft.com/exchange/Mail-apps-for-Outlook-Make-770b2528) sample.

## EWS and Outlook add-ins

You can use a subset of EWS operations on the Exchange server that hosts the account that runs a mail app.

The [mailbox.makeEwsRequestAsync](https://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx) function enables you to make EWS requests from your mail app back to the server that hosts the user's mailbox. You create the SOAP envelope and XML request, and the **makeEwsRequestAsync** function calls EWS with an authentication token that identifies the mailbox and mail app that is making the request. To help secure the user's mailbox, the Exchange server will reject any requests that do not come from the mail app or from a mailbox that is not hosted on the server.

Like any other application, a mail app needs permissions to work. Your administrator needs to:

- [Grant EWS access](controlling-client-application-access-to-ews-in-exchange.md) to the mail apps user.

- [Set "OAuthAuthentication" to true](https://technet.microsoft.com/library/aa997233%28v=exchg.150%29.aspx) on the Client Access Server EWS directory.

You also need to make sure that your app requests the read/write mailbox permission in the apps for Office [permission model](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).

When these steps are complete, a subset of folder and item EWS operations are available for the mail app to use.

**Table 1. EWS folder and item operations that mail apps can use**

|**Folder operations**|**Item operations**|
|:-----|:-----|
|[CreateFolder operation](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder operation](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [GetFolder operation](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [UpdateFolder operation](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |[CopyItem operation](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> [FindConversation operation](https://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> [GetConversationItems operation](https://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> [GetItem operation](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [MarkAsJunk operation](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) <br/> [MoveItem operation](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [SendItem operation](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) <br/> [UpdateItem operation](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |

### Service callback tokens

Service callback tokens enable mail apps to pass an access token to a third-party service so that the service can make EWS requests to the Exchange server that hosts the mailbox. For example, a mail app can pass a service callback token to a third-party service along with a list of attachment IDs for pictures attached to an email. The service can then use the attachment IDs and the callback token to make an EWS request to the user's Exchange server to get the attached pictures. Mail apps can also use the service callback token with a list of item IDs to get email and appointment items from the Exchange server.

The service callback token is an opaque token that the third-party service attaches to the EWS request in a bearer authentication header. The token identifies the mail app and the mailbox to help secure the EWS request. To learn how to use service callback tokens, see the [Outlook add-ins: Get attachments from an Exchange server](https://code.msdn.microsoft.com/exchange/Mail-apps-for-Office-Get-38babdc9) sample.

## See also


- [Controlling client application access to EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md)

- [Mailbox.makeEwsRequestAsync method (JavaScript API for Office)](https://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx)

- [Outlook add-ins](/office/dev/add-ins/outlook/outlook-add-ins-overview)

- [Mailbox.getUserIdentityTokenAsync method (JavaScript API for Office)](https://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx)

- [Authenticate an Outlook add-in by using Exchange identity tokens](https://msdn.microsoft.com/library/c0520a1e-d9ba-495a-a99f-6816d7d2a23e%28Office.15%29.aspx)

- [Understanding Outlook add-in permissions](/office/dev/add-ins/outlook/understanding-outlook-add-in-permissions)

- [Set-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa997233%28v=exchg.150%29.aspx)

- [Outlook add-ins: Make an EWS request](https://code.msdn.microsoft.com/office/Mail-apps-for-Outlook-Make-770b2528)

- [Outlook add-ins: Use a client identity token](https://code.msdn.microsoft.com/Mail-apps-for-Outlook-Use-b20a66b6)

- [Outlook add-ins: Get attachments from an Exchange server](https://code.msdn.microsoft.com/office/Mail-apps-for-Office-Get-38babdc9)
