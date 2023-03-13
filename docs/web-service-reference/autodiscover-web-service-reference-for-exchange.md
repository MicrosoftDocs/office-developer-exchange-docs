---
title: "Autodiscover web service reference for Exchange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a01124a8-a8cf-4b80-8625-d7ee05690bca
description: "Find reference content for the Autodiscover web service in Exchange."
---

# Autodiscover web service reference for Exchange

Find reference content for the Autodiscover web service in Exchange.
  
The Autodiscover web service provides the configuration information that your application uses to create a connection to an Exchange server. You can use one of the following options to connect to Autodiscover:
  
- SOAP Autodiscover service —Available to clients that connect to versions of Exchange starting with Exchange 2010, including Exchange Online.
    
- "plain old XML" (POX) Autodiscover service — Available to clients that connect to versions of Exchange starting with Exchange 2007, including Exchange Online. 
    
Both the SOAP and the POX Autodiscover service can provide the configuration information that your client will use to create a connection to an Exchange server.
  
> [!NOTE]
> For versions of Exchange starting with Exchange 2010, we recommend that you use the SOAP Autodiscover service instead of the POX Autodiscover service. The SOAP Autodiscover service provides batched Autodiscover setting requests and more granular control over which settings are returned in the response. 
  
This section contains reference information for the SOAP Autodiscover service and the POX Autodiscover service.
  
## In this section
<a name="bk_InThisSection"> </a>

- [SOAP Autodiscover web service reference for Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [POX Autodiscover web service reference for Exchange](pox-autodiscover-web-service-reference-for-exchange.md)
    
## See also

- [Web services reference for Exchange](web-services-reference-for-exchange.md)
- [Autodiscover Service (SOAP)](https://msdn.microsoft.com/library/e24d1a1f-0d20-4bd9-ae4c-9112ecacea78%28Office.15%29.aspx)
- [Autodiscover Service (POX)](https://msdn.microsoft.com/library/13c54de3-a91c-4424-8732-99dd8f2162ec%28Office.15%29.aspx)
    

