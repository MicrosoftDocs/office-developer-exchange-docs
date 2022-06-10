---
title: "Create a RoutingAgent transport agent for Exchange 2013"
manager: sethgros
ms.date: 09/21/2021
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3f0e745f-9289-4f31-8877-926692a8c133
description: "Find out how to create a custom RoutingAgent transport agent to use with Exchange 2013."
---

# Create a RoutingAgent transport agent for Exchange 2013

Find out how to create a custom RoutingAgent transport agent to use with Exchange 2013.
  
**Applies to:** Exchange Server 2013
  
Related code snippets and sample apps:

- [Exchange 2013: Build a bandwidth logging transport agent](/exchange/client-developer/transport-agents/transport-agent-code-samples-for-exchange-2013)
  
The [RoutingAgentFactory](/previous-versions/office/exchange-server-api/aa564164(v=exchg.150)) and [RoutingAgent](/previous-versions/office/exchange-server-api/aa564421(v=exchg.150)) classes are the base classes for transport agents that are designed to run on the transport service on an Exchange Server 2013 Mailbox server. The [RoutingAgent](/previous-versions/office/exchange-server-api/aa564421(v=exchg.150)) class provides the events listed in the following table for which you might implement handlers in your RoutingAgent transport agent. 
  
**Table 1. RoutingAgent class events**

|**Event**|**Description**|
|:-----|:-----|
|[OnCategorizedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |Occurs after the server performs content conversion, if it is required.  <br/> |
|[OnResolvedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |Occurs after all the recipients of the message have been resolved and before routing is determined.  <br/> |
|[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |Occurs after the server routes the message to the next hop and performs content conversion, if required. The server might use more resources to process each message in the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) event than the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) event because the server will perform any necessary content conversion and determine the next hop in the route for the message before it executes the code in the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) event handler.  <br/> |
|[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |Occurs after the message is taken off the submit queue. Use the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) event if your RoutingAgent transport agent does not require content conversion, resolved recipients, or routing data.  <br/> |
   
## Creating a custom RoutingAgent transport agent

The following procedure describes how to create a custom RoutingAgent transport agent. 
  
### To create the transport agent

1. Add references to the namespaces.
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   You can find these namespaces on your Exchange server. By adding a reference to these namespaces, you will have access to the [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) members as well as other classes used in the [Exchange 2013: Build a bandwidth logging transport agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) sample. 
    
2. Implement the derived class for the [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) class. 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent. Additional methods, such as **Close**, can also be overridden in this class to execute custom code. 
    
3. Define your agent.
    
   ```cs
      public class BandwidthLogger : RoutingAgent
      {
          // Your custom code goes here
          public BandwidthLogger(SmtpServer server)
          {
              Debug.WriteLine(logPrefix + "Agent constructor");
              this.server = server;
              this.OnSubmittedMessage += SubmittedMessage;
              this.OnRoutedMessage += RoutedMessage;
          }
      }
  
   ```

   After you define your agent class, you can add you custom functionality. In this example, the two events [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) and [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)are redirected to your custom event handlers. 
    
## See also

- [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Transport agent reference for Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
