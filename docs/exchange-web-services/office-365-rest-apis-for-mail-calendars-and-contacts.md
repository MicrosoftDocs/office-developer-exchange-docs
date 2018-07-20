---
title: "Microsoft Graph REST APIs for mail, calendars, and contacts"
manager: sethgros
ms.date: 4/29/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3b2e71a6-5fa5-4008-b243-d3a6e9173b3d
description: "Find information about the Microsoft Graph APIs that you can use to access mail, calendars, and contacts in Office 365 or Exchange Online."
---

# Microsoft Graph REST APIs for mail, calendars, and contacts

Find information about the Microsoft Graph APIs that you can use to access mail, calendars, and contacts in Office 365 or Exchange Online.

Office 365 and Exchange Online provide a new way to work with email, calendars, and contacts. The Microsoft Graph Mail, Calendar, and Contact REST APIs provide a powerful, easy-to-use way to access and manipulate Exchange data. These APIs are based on open standards: OAuth version 2.0 for authentication, and OData version 4.0 and JSON for data abstraction. This provides the following advantages:

- Because these APIs require OAuth for authentication, your application does not have to handle or store user credentials.

- OAuth makes it possible to request tightly scoped permissions to user data. For example, you might design your application to request permission and read only a user's calendar.

## Work with email and mail folders

You can use the [Mail API](https://developer.microsoft.com/graph/docs/concepts/outlook-mail-concept-overview) to get, create, update, delete, move, copy, and send email. You can also get, create, update, and delete mail folders.

## Work with events, calendars, and calendar groups

You can use the [Calendar API](https://developer.microsoft.com/graph/docs/concepts/outlook-calendar-concept-overview) to get, create, update, and delete events. You can also get, create, update, and delete calendar groups and calendars.

## Work with contacts and contact folders

You can use the [Contacts API](https://developer.microsoft.com/graph/docs/concepts/outlook-contacts-concept-overview) to get, create, update, and delete contacts in a user's mailbox. You can also get contact folders.

## Next steps

Head over to the [Microsoft Graph overview](https://developer.microsoft.com/graph/docs/concepts/overview) page to get more information about the Mail, Calendar, and Contacts APIs, including guidance for setting up your environment and getting started with the APIs.

Also be sure to check out the [code samples](https://developer.microsoft.com/graph/code-samples-and-sdks) to see these APIs in action.

## See also

- [Microsoft Graph API reference](https://developer.microsoft.com/graph/docs/concepts/v1-overview)
