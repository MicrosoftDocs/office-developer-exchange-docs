---
title: "monitoring"
manager: lindalu
ms.date: 03/10/2022
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- monitoring
api_type:
- schema
ms.assetid: 350d7b46-9260-41a7-8613-3cb8cc1b29a5
description: "The monitoring element contains configuration information that defines how and when the Front End transport service or the Transport service monitors agents that are installed."
---

# monitoring
  
**Applies to:** Exchange Server 2013
  
The **monitoring** element contains configuration information that defines how and when the Front End transport service or the Transport service monitors agents that are installed. 
  
- [configuration](configuration.md)  
- [mexRuntime](mexruntime.md)  
- [monitoring](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

**monitoringType (complexType)**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[agentExecution](agentexecution.md) <br/> |Defines the time, in milliseconds, for the Client Access or the Mailbox server to wait for an agent to return from an event before it writes to the event log.  <br/> |
|[messageSnapshot](messagesnapshot.md) <br/> |Contains an attribute that specifies whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.  <br/> |
   
## Element information

|**Element** |**Example** |
|:-----|:-----|
|Namespace  <br/> |This file does not define a namespace.  <br/> |
|Schema Name  <br/> |Not available.  <br/> |
|Validation File  <br/> |Not available.  <br/> |
|Can be Empty  <br/> |False.  <br/> |
   
## See also

- [Agents configuration file elements for Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)
