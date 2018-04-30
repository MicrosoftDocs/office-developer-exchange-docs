---
title: "Office 365 REST APIs for mail, calendars, and contacts"
 
 
manager: sethgros
ms.date: 4/29/2016
ms.audience: Developer
 
 
localization_priority: Normal
ms.assetid: 3b2e71a6-5fa5-4008-b243-d3a6e9173b3d
description: "Find information about the Office 365 APIs that you can use to access mail, calendars, and contacts in Office 365 or Exchange Online."
---

# Office 365 REST APIs for mail, calendars, and contacts

Find information about the Office 365 APIs that you can use to access mail, calendars, and contacts in Office 365 or Exchange Online.
  
Office 365 and Exchange Online provide a new way to work with email, calendars, and contacts. The Mail, Calendar, and Contact REST APIs provide a powerful, easy-to-use way to access and manipulate Exchange data. These APIs are based on open standards: OAuth version 2.0 for authentication, and OData version 4.0 and JSON for data abstraction. This provides the following advantages:
  
- Because these APIs require OAuth for authentication, your application does not have to handle or store user credentials.
    
- OAuth makes it possible to request tightly scoped permissions to user data. For example, you might design your application to request permission and read only a user's calendar.
    
## Work with email and mail folders

You can use the [Mail API](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx) to get, create, update, delete, move, copy, and send email. You can also get, create, update, and delete mail folders. 
  
## Work with events, calendars, and calendar groups

You can use the [Calendar API](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx) to get, create, update, and delete events. You can also get, create, update, and delete calendar groups and calendars. 
  
## Work with contacts and contact folders

You can use the [Contacts API](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx) to get, create, update, and delete contacts in a user's mailbox. You can also get contact folders. 
  
## Work with file providers

You can use the [File Providers REST API](http://msdn.microsoft.com/library/8bab5403-de68-4b49-ab19-9a6470f2a2ce%28Office.15%29.aspx) to get, create, update, and delete information about supported file providers, such as mailbox, Dropbox, and so on. 
  
## Next steps

Head over to the [Developing on the Office 365 platform](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx) page to get more information about the Mail, Calendar, and Contacts APIs, including guidance for setting up your environment and getting started with the APIs. Also be sure to check out the [starter projects and code samples](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx) to see these APIs in action. 
  
## Additional resources
<a name="bk_addresources"> </a>

- [Developing on the Office 365 platform](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx)
    
- [Building an Office 365 ASP.NET MVC app](http://msdn.microsoft.com/office/office365/howto/Build-your-first-ASPNET-MVC-app%28Office.15%29.aspx)
    
- [Mail REST operations](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx)
    
- [Calendar REST operations](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx)
    
- [Contacts REST operations](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx)
    
- [Office 365 APIs starter projects and code samples](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx)
    

