---
title: "Redistribution requirements for the EWS Managed API"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: "Find out how you can redistribute the EWS Managed API assemblies with your application."
---

# Redistribution requirements for the EWS Managed API

Find out how you can redistribute the EWS Managed API assemblies with your application.
  
As you design your EWS Managed API application, you'll also want to consider how you will release it to your users. 
  
## Redistributing your EWS Managed API application

Unless your application is located on the Exchange server, you will need to redistribute the EWS Managed API assemblies. The EWS Managed API download contains two assemblies that you can redistribute: Microsoft.Exchange.WebServices.dll and Microsoft.Exchange.WebServices.Auth.dll. Keep the following information in mind when you design how you will release your EWS Managed API application:
  
- The EWS Managed API was designed such that you can download it and distribute it with your application that targets an Exchange server. Alternatively, your application can download the EWS Managed API.
    
- You can use the EWS Managed API to communicate with an Exchange server running Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange Server 2007.
    
- In versions of the EWS Managed API starting with version 2.1, you can install the API in the Global Assembly Cache (GAC). The MSI will automatically add the DLL to the GAC and will be accessible on per computer basis, not on a per user basis.
    
The license terms are included in the EWS Managed API download. Review the terms for the authoritative information about what you can do with the EWS Managed API.
  
## See also


- [EWS client design overview for Exchange](ews-client-design-overview-for-exchange.md)
    
- [EWS Managed API (download)](https://aka.ms/ews-managed-api-readme)
    

