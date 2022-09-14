---
title: "Agents configuration file elements for Exchange 2013"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Agents
api_type:
- schema
ms.assetid: 3047653b-d712-46c1-ae0a-73f3975f5e9d
description: "Find information about the XML elements in the agents.config and fetagents.config configuration file in Exchange 2013."
---

# Agents configuration file elements for Exchange 2013

Find information about the XML elements in the agents.config and fetagents.config configuration file in Exchange 2013.
  
**Applies to:** Exchange Server 2013
  
When you install the Client Access or the Mailbox server role on an Exchange server, the installer creates an XML file that contains configuration information about agents that are installed on the server. You cannot write directly to this file. 
  
The Front End Transport service runs on Client Access servers and writes to a file named fetagents.config. The Transport service and the Mailbox Transport service run on Mailbox servers, and write to a file named agents.config. A computer that has both the Client Access server role and the Mailbox server role will have both a fetagents.config and an agents.config file.
  
The only supported way to write to these files is by using the transport agent cmdlets in the Exchange Management Shell. For information about the transport agent cmdlets, see [Mail Flow Cmdlets](https://technet.microsoft.com/library/aa998553%28v=exchg.150%29.aspx) on TechNet.
  
> [!NOTE]
> To distinguish between agents that extend the Front End Transport service on the Client Access server and the Transport service on the Mailbox server, transport agent cmdlets have a _TransportService_ parameter with a value of "Hub" for the Transport service and "FrontEnd" for the Front End Transport service.
  
You can read the agents.config or fetagents.config file to determine the presence of and configuration information for one or more agents on the server. This documentation provides a reference that you can use to read the information in either the agents.config file or the fetagents.config. The format for both of these files is the same. This documentation does not provide information about how to write to the files.
  
> [!CAUTION]
> Using unsupported methods to write to the agents.config file or fetagents.config can produce unexpected results, including failure of the transport service or transport agents, or both. Do not write directly to either of these files. The only supported method for writing to these files is by using the Exchange Management Shell transport agent cmdlets.
  
## Location of the transport agent configuration files

When you install Exchange 2013, the installer creates an XML file that is named either agents.config.template or fetagents.config.template, depending on the server role installed, in the \<ExchangeInstallFolder\>\TransportRoles\Agents folder (where \<ExchangeInstallFolder\> is the folder in which you installed Exchange 2013). If you install the Client Access server role, Exchange 2013 copies the fetagents.config.template file to fetagents.config. If you install the Mailbox server role, Exchange 2013 copies the agents.config.template file to agents.config. Exchange 2013 reads and writes this file when you change the transport agents configuration on the server.
  
## Verifying a transport agent installation

You can use the XML capabilities that the .NET Framework provides to read and validate the agents.config or the fetagents.config XML file. To verify the installation and configuration of a transport agent, read the XML in the configuration file and find the [agent](agent.md) element that corresponds to the transport agent. If an **agent** element for the specific transport agent does not exist, the transport agent is not installed. If the transport agent is installed, you can read the attributes of the **agent** element to determine its configuration.
  
## Configuration file element hierarchy

The following code shows the element hierarchy in the configuration XML file.
  
```XML
<configuration>
    <mexRuntime>
        <monitoring>
            <agentExecution/>
            <messageSnapshot/>
        </monitoring>
        <agentList>
            <agent/>
            <agent/>
            <agent />
        </agentList>
    </mexRuntim>
</configuration>
```

## In this section

- [agent](agent.md)
- [agentExecution](agentexecution.md)
- [agentList](agentlist.md)
- [configuration](configuration.md)
- [messageSnapshot](messagesnapshot.md)
- [mexRuntime](mexruntime.md)
- [monitoring](monitoring.md)

## See also

- [Transport agents in Exchange](transport-agents-in-exchange-2013.md)
- [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)
- [Transport agent reference for Exchange 2013](transport-agent-reference-for-exchange-2013.md)
- [Transport agent namespaces in Exchange 2013](transport-agent-namespaces-in-exchange-2013.md)
- [Mail Flow Cmdlets](/powershell/exchange/?view=exchange-ps)
