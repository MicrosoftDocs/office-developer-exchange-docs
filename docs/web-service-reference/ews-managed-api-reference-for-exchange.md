---
title: Exchange Web Services (EWS) Managed API reference
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
api_type:
- schema
ms.assetid: c6ca36f4-a67c-4e3c-aae7-9ead7b704e15
description: Learn about the namespaces that are included in the EWS Managed API.
localization_priority: Priority
---

# EWS Managed API reference

**Applies to**: EWS Managed API | Exchange Online | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013 | Office 365

The Exchange Web Services (EWS) Managed API includes two APIs: Microsoft.Exchange.WebServices.dll and Microsoft.Exchange.WebServices.Auth.dll.

## EWS Managed API namespaces

|Namespace |Description |
|:---------|:-----------|
|[Microsoft.Exchange.WebServices.Auth.Validation](/dotnet/api/microsoft.exchange.webservices.auth.validation?view=exchange-ews-api) |Contains types and methods that are used to validate user identity tokens sent from an Exchange server. The Microsoft.Exchange.WebServices.Auth.Validation namespace is applicable to clients that target Exchange Online and versions of Exchange starting with Exchange Server 2013. This namespace is included in the Microsoft.Exchange.WebServices.Auth.dll API.|
|[Microsoft.Exchange.WebServices.Autodiscover](/dotnet/api/microsoft.exchange.webservices.autodiscover?view=exchange-ews-api)|Contains types that are used to communicate with the Autodiscover service that is hosted by an Exchange Server. This namespace is also used to look up service connection point objects in Active Directory Doman Services (AD DS). The Autodiscover services provide configuration information to EWS clients. This enables the clients to target the appropriate service URL.<br/><br/>The namespace functionality can be used to target the POX Autodiscover service introduced in Microsoft Exchange Server 2007, the service connection point object lookup if the client is domain joined, or the SOAP Autodiscover endpoint introduced in Exchange Server 2010. The main type in this namespace is the [AutodiscoverService class](/dotnet/api/microsoft.exchange.webservices.autodiscover.autodiscoverservice?view=exchange-ews-api). This namespace is included in the Microsoft.Exchange.WebServices.dll API.|
|[Microsoft.Exchange.WebServices.Data](/dotnet/api/microsoft.exchange.webservices.data?view=exchange-ews-api)| Contains types that are used to communicate with an Exchange server by means of EWS. This namespace provides the core EWS Managed API functionality. The main type in this namespace is the [ExchangeService class](/dotnet/api/microsoft.exchange.webservices.data.exchangeservice?view=exchange-ews-api).|

## See also

- [Web services reference for Exchange](web-services-reference-for-exchange.md)
- [Explore the EWS Managed API, EWS, and web services in Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [What’s new in EWS and other web services in Exchange](../exchange-web-services/whats-new-in-ews-and-other-web-services-in-exchange.md)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [Develop web service clients for Exchange](../exchange-web-services/develop-web-service-clients-for-exchange.md)
