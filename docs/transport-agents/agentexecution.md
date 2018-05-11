---
title: "agentExecution"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agentExecution
api_type:
- schema
ms.assetid: 600c4690-941c-45af-a906-5528748d09cd
description: "Last modified: September 17, 2015"
---

# agentExecution

 **Last modified:** September 17, 2015 
  
 * **Applies to:** Exchange Server 2013 * 
  
The **agentExecution** element defines the time, in milliseconds, for the Client Access or Mailbox server to wait for an agent to return from an event before it writes to the event log. 
  
[configuration](configuration.md)
  
[monitoring](monitoring.md)
  
[agentExecution](agentexecution.md)
  
```XML
<agentExecution timeLimitInMilliseconds="" />
```

 **agentExecutionType (complexType)**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**timeLimitInMilliseconds** <br/> |A positive integer value that specifies the time, in milliseconds, for the server to wait for an agent to return from an event before it writes a warning to the event log. Performance can decrease if this value is too small. The suggested value for this attribute is 300,000, which equates to 5 minutes.  <br/> |
   
#### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[monitoring](monitoring.md) <br/> |Contains configuration information that defines how and when the Front End Transport service or the Transport service monitors agents that are installed.  <br/> |
   
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |This file does not define a namespace.  <br/> |
|Schema Name  <br/> |Not available.  <br/> |
|Validation File  <br/> |Not available.  <br/> |
|Can be Empty  <br/> |False.  <br/> |
   
## See also

#### Concepts

[Agents configuration file elements for Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

