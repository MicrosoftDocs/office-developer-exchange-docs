---
title: "Creating transport agents for Exchange 2013"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d291ab78-7cdd-4dbe-a5f4-9dc8e9650a33
description: "Find information about how to create custom transport agents for Exchange 2013, and the system requirements for creating a custom agent."
---

# Creating transport agents for Exchange 2013

Find information about how to create custom transport agents for Exchange 2013, and the system requirements for creating a custom agent.
  
**Applies to:** Exchange Server 2013
  
Exchange Server 2013 includes several transport agents that you can use to process messages. By using the assemblies that come with Exchange, you can create your own custom agents to perform specific tasks according to the needs of your organization. For example, you can use an SmtpReceiveAgent transport agent to intercept messages that are received via the SMTP protocol and process the message to convert the format of the body to contain preformatted text. You can use a RoutingAgent transport agent to log the messages that pass through the server on route to another server. You can also create more complex features that make use of more than one type of agent. For example, to create an antivirus agent, you can implement an SmtpReceiveAgent and a RoutingAgent agent. If you have a component on your network that does not support the SMTP protocol, you can use a DeliveryAgent transport agent to handle the communication between your Exchange server and your external component.
  
This article provides information about the prerequisites for and tasks involved in creating your own transport agent. For information about creating specific transport agents, see [Create a RoutingAgent transport agent for Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [Create an SmtpReceiveAgent transport agent for Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md), and [Create a DeliveryAgent transport agent for Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).
  
## Prerequisites for creating a transport agent

<a name="bk_prerequisites"> </a>

The following are the prerequisites that you need in order to implement a transport agent:
  
- A computer running Exchange 2013 that is running the Front End Transport service on a Client Access or Edge Transport server, or the Transport service on a Mailbox server. For information about the server role architecture in Exchange 2013, see [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md).

- The following assemblies for the transport agent classes:

  - Microsoft.Exchange.Data.dll
  - Microsoft.Exchange.Data.Common.dll
  - Microsoft.Exchange.Transport.dll

- The .NET Framework 4.5

We also recommend that you install Visual Studio 2012. You can implement transport agents by using either Visual Basic .NET or C#.
  
## Referencing the assemblies

<a name="bk_ReferenceAssemblies"> </a>

Exchange 2013 provides a library of classes that support the extension of Exchange transport behavior. These classes require the .NET Framework 4.5. You can implement transport agents based on these classes by using Visual Studio 2012.
  
The Exchange 2013 installer installs assemblies that are used for transport agent development and registers them in the global assembly cache (GAC). To begin implementing a transport agent, create a reference to the Microsoft.Exchange.Data.Transport assembly in a class library project.
  
## Implementing a transport agent

<a name="bk_implementationExample"> </a>

The following example shows a minimal implementation of classes that derive from the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes.
  
> [!CAUTION]
> If multiple transport agents are installed and registered for the same event, all agents will be invoked, even if one agent removes all the recipients from a mail item. > To avoid unhandled errors or unpredictable behavior, your transport agent should handle cases in which the recipient count on a mail item is equal to zero.
  
```cs
using System;
using System.Collections.Generic;
using System.Text;
using Microsoft.Exchange.Data.Transport;
using Microsoft.Exchange.Data.Transport.Smtp;
namespace MyAgents
{
    public sealed class MyAgentFactory : SmtpReceiveAgentFactory
    {
        public override SmtpReceiveAgent CreateAgent(SmtpServer server)
        {
            return new MyAgent();
        }
    }
    public class MyAgent : SmtpReceiveAgent
    {
        public MyAgent()
        {
            this.OnEndOfData += new EndOfDataEventHandler(MyEndOfDataHandler);
        }
        private void MyEndOfDataHandler (ReceiveMessageEventSource source, EndOfDataEventArgs e)
        {
            // The following line appends text to the subject of the message that caused the event.
            e.MailItem.Message.Subject += " - this text appended by MyAgent";
        }
    }
}
```

```vb
Imports System
Imports System.Collections.Generic
Imports System.Text
Imports Microsoft.Exchange.Data.Transport
Imports Microsoft.Exchange.Data.Transport.Smtp
Namespace MyAgents
    NotInheritable Class MyAgentFactory
        Inherits SmtpReceiveAgentFactory
        Public Overrides Function CreateAgent(ByVal server as SmtpServer) As SmtpReceiveAgent
            Return New MyAgent
        End Function
    End Class
    Public Class MyAgent
        Inherits SmtpReceiveAgent
        Private Sub MyEndOfDataHandler(ByVal source As ReceiveMessageEventSource, ByVal e As EndOfDataEventArgs) Handles Me.OnEndOfData
            ' The following line appends text to the subject of the message that caused the event.
            e.MailItem.Message.Subject &amp;= e.MailItem.Message.Subject + " - this text appended by MyAgent"
        End Sub
    End Class
End Namespace
```

## Installing and enabling an agent

<a name="bk_InstallEnable"> </a>

After you compile your agent to a DLL, you must install and enable the agent on your development Exchange server. In the Exchange Management Shell, use the [Install-TransportAgent](https://technet.microsoft.com/library/aa997998.aspx) cmdlet to install your agent, and the [Enable-TransportAgent](https://technet.microsoft.com/library/bb124921.aspx) cmdlet to enable your agent. For information about how to use the Exchange Management Shell, see [Exchange Server PowerShell (Exchange Management Shell)](/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).
  
> [!CAUTION]
> Transport agents have full access to all email messages that they encounter. Exchange 2013 does not restrict the behavior of a transport agent. Transport agents that are unstable or that contain security flaws might affect the stability and security of Exchange 2013. Therefore, you should only install transport agents that you fully trust and that have been fully tested.
  
When you use the **Install-TransportAgent** cmdlet to install an agent, the Exchange Management Shell keeps a lock on the assembly. To release the lock on the assembly, you must close the instance of the Exchange Management Shell that you used to install the agent. You will be unable to update the assembly until you release the lock.
  
The following example shows how to use the Exchange Management Shell to install and enable an agent named MyAgent by using a class derived from [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) named MyAgents.MyAgentFactory.
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
This example names the agent MyCustomAgent on the server on which the agent is installed. The following example shows how to enable the agent named MyCustomAgent.
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
To manage a transport agent in the Front End Transport service on a Client Access server, add the following value to the command: `-TransportService FrontEnd`. For example, to view the transport agents in the Front End Transport service, run the following command.
  
 `Get-TransportAgent -TransportService FrontEnd`
  
For more information about installing, enabling, and managing your agent, see [Manage Transport Agents](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx).
  
## In this section

<a name="bk_inthissection"> </a>

- [Create a RoutingAgent transport agent for Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
- [Create an SmtpReceiveAgent transport agent for Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
- [Create a DeliveryAgent transport agent for Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)

## See also

- [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)
- [Transport agent reference for Exchange 2013](transport-agent-reference-for-exchange-2013.md)
