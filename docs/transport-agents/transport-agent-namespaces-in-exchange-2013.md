---
title: "Transport agent namespaces in Exchange 2013"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
ms.assetid: 5c40788e-c182-4502-9202-206e6aaa53f8
description: "Learn about the .NET Framework classes and members that you can use to create custom transport agents for Exchange 2013."
---

# Transport agent namespaces in Exchange 2013

Learn about the .NET Framework classes and members that you can use to create custom transport agents for Exchange 2013.
  
**Applies to:** Exchange Server 2013 
  
This article provides information about the namespaces that contain reference information that you can use to create transport agents for Exchange Server 2013. It also describes the classes that your transport agents can use to read and modify email messages that pass through the transport pipeline.
  
## Transport agent class library

The following namespaces contain types that you can use to create and extend transport agents.

**Table 1. .NET Framework namespaces**

|**Namespace**|**Description**|
|:-----|:-----|
|[Microsoft.Exchange.Data](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx) <br/> |Contains types that specify data and configuration exceptions.  <br/> |
|[Microsoft.Exchange.Data.Common](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Common.aspx) <br/> |Contains types that support localization and error handling.  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |Contains types that enable you to read and write iCalendar data.  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |Contains types that enable you to read and write TNEF data.  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |Contains types that enable you to read and write vCard data.  <br/> |
|[Microsoft.Exchange.Data.Globalization](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Globalization.aspx) <br/> |Contains types that enable you to work with cultures and character sets to produce localized content.  <br/> |
|[Microsoft.Exchange.Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |Contains types that enable you to read and write MIME data.  <br/> |
|[Microsoft.Exchange.Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |Contains types that enable you to encode and decode MIME data.  <br/> |
|[Microsoft.Exchange.Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |Contains types that enable you to read and write data with different text formats, and convert data to and from those formats.  <br/> |
|[Microsoft.Exchange.Data.Transport](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.aspx) <br/> |Contains types that enable you to access routing, host, and domain information about the transport pipeline.  <br/> |
|[Microsoft.Exchange.Data.Transport.Delivery](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.aspx) <br/> |Contains types that support the extension of Exchange 2013 delivery agents.  <br/> |
|[Microsoft.Exchange.Data.Transport.Email](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.aspx) <br/> |Contains types that support creating, reading, writing, and modifying email messages.  <br/> |
|[Microsoft.Exchange.Data.Transport.Routing](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.aspx) <br/> |Contains types that support the extension of the Exchange 2013 transport routing behavior.  <br/> |
|[Microsoft.Exchange.Data.Transport.Smtp](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.aspx) <br/> |Contains types that support the extension of the Exchange 2013 transport SMTP behavior.  <br/> |
   
## See also

- [Transport agents in Exchange](transport-agents-in-exchange-2013.md)   
- [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md) 
- [Server API reference for Exchange](https://msdn.microsoft.com/library/6eddd052-f59f-45b4-b846-7e53d4d7eb16%28Office.15%29.aspx)
- [Agents configuration file elements for Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)
    

