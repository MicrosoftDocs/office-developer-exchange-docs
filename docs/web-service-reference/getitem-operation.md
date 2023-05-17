---
title: "GetItem operation"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
api_name:
- GetItem
api_type:
- schema
ms.assetid: e3590b8b-c2a7-4dad-a014-6360197b68e4
description: "Find information about the GetItem EWS operation."
localization_priority: Priority
---

# GetItem operation

Find information about the **GetItem** EWS operation. 
  
The **GetItem** operation gets items from the Exchange store. 
  
## Using the GetItem operation

The **GetItem** operation returns many item properties. The properties that are returned in a **GetItem** response vary based on the requested shape, requested additional properties, and the type of item returned. 
  
[Message](message-ex15websvcsotherref.md) elements represent email messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema. Items such as IPM.Sharing and IPM.InfoPath are returned as [Message](message-ex15websvcsotherref.md) elements. Exchange does not return the base [Item](item.md) element in responses. 
  
The **GetItem** operation does not return attachments. It does return metadata about an attached item or file. To return an attachment, use the [GetAttachment operation](getattachment-operation.md).
  
## GetItem operation SOAP headers

The **GetItem** operation can use the SOAP headers that are listed in the following table. 
  
|****Header****|****Element****|****Description****|
|:-----|:-----|:-----|
|**DateTimePrecision** <br/> |[DateTimePrecision](datetimeprecision.md) <br/> |Specifies the resolution of data/time values in responses from the server, either in seconds or in milliseconds.  <br/> |
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifies the user whom the client application is impersonating.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifies the schema version for the operation request.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifies the version of the server that responded to the request.  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Identifies the time zone to be used for all responses from the server.  <br/> |
   
## In This Section

[GetItem operation (email message)](getitem-operation-email-message.md)
  
[GetItem operation (calendar item)](getitem-operation-calendar-item.md)
  
[GetItem operation (task)](getitem-operation-task.md)
  
[GetItem operation (contact)](getitem-operation-contact.md)
  
## See also



[EWS reference for Exchange](ews-reference-for-exchange.md)

