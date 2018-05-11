---
title: "mexRuntime"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- mexRuntime
api_type:
- schema
ms.assetid: eabb2f12-10a7-4ce2-ae4b-9c04010c765f
description: "Last modified: September 17, 2015"
---

# mexRuntime

 **Last modified:** September 17, 2015 
  
 * **Applies to:** Exchange Server 2013 * 
  
The **mexRuntime** element contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed. 
  
[configuration](configuration.md)
  
[mexRuntime](mexruntime.md)
  
```XML
<mexRuntime>
   <monitoring/>
   <agentList/>
</mexRuntime>
```

 **mexRuntimeType (complexType)**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[monitoring](monitoring.md) <br/> |Contains configuration information that defines how and when transport monitors agents that are installed.  <br/> |
|[agentList](agentlist.md) <br/> |Contains an [agent](agent.md) element for each agent that is installed.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[configuration](configuration.md) <br/> |The root element for the agents configuration file.  <br/> |
   
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

