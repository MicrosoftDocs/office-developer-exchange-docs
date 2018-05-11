---
title: "Transport agent code samples for Exchange 2013"
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 626345ec-918f-4d91-932f-e6ce92553ccb
description: "Find information about the sample transport agents that are available for Exchange 2013."
---

# Transport agent code samples for Exchange 2013

Find information about the sample transport agents that are available for Exchange 2013.
  
**Applies to:** Exchange Server 2013
  
You can use the APIs that are included in Exchange Server 2013 to develop agents that extend transport functionality. This article provides information about the sample agents that are available to help you to learn how to extend transport behavior programmatically. The sample agents include the source code for each component. 
  
The following table lists the sample agents for Exchange 2013.
  
**Table 1. Transport agent samples**

|**Sample name**|**Description**|
|:-----|:-----|
|[Exchange 2013: Build an antivirus transport agent](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-6e544269) <br/> |This agent responds to the [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) and [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) events and sends the incoming message to an out-of-process server that asynchronously examines the message and returns a modified version.  <br/> |
|[Exchange 2013: Build a bandwidth logging transport agent](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) <br/> |This agent responds to the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) and [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) events, captures bandwidth usage for specified recipients, and logs the bandwidth usage information to a text file.  <br/> |
|[Exchange 2013: Build a body conversion transport agent](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) <br/> |This agent filters scripts out of email messages by determining the format of the incoming message and deciding if filtering must occur. If filtering is needed, the content is converted to HTML, filtered, and then converted back to the source format.  <br/> |
|[Exchange 2013: Build an SMTP logging transport agent](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-fc23dc33) <br/> |This agent responds to the [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) event, and asynchronously logs the message to a file on the local hard disk.  <br/> |
|[Exchange 2013: Build a transport agent that blocks senders temporarily](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-52a767d8) <br/> |This agent responds to the [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) and [OnRcptCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnRcptCommand.aspx) events and determines whether the message sender has previously sent messages to the Front End Transport service. If the sender has not previously sent a message to the Front End Transport service, the sender is added to a list of senders, and the message is rejected with a response that tells the client to try again later (also known as graylisting). If the sender is in the list of previous senders, the agent does not reject the message.  <br/> |
|[Exchange 2013: Build a Mailbox server logging transport agent](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-fc8632e5) <br/> |This agent responds to the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) transport pipeline event and synchronously logs the message to a file on the local hard disk.  <br/> |
|[Exchange 2013: Build an X-header transport agent](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-32f62f5a) <br/> |This agent responds to the [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) event and read and modify X-headers in messages.  <br/> |
   
## See also

- [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Transport agent reference for Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [How to: Create a RoutingAgent transport agent for Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)   
- [How to: Create an SmtpReceiveAgent transport agent for Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)    
- [How to: Create a DeliveryAgent transport agent for Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    

