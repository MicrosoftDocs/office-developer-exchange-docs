---
title: "mexRuntime"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- mexRuntime
api_type:
- schema
ms.assetid: eabb2f12-10a7-4ce2-ae4b-9c04010c765f
description: "Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed."
---

# mexRuntime
  
**Applies to:** Exchange Server 2013
  
The **mexRuntime** element contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed. 
  
- [configuration](configuration.md)  
- [mexRuntime](mexruntime.md)
  
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
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[monitoring](monitoring.md) <br/> |Contains configuration information that defines how and when transport monitors agents that are installed.  <br/> |
|[agentList](agentlist.md) <br/> |Contains an [agent](agent.md) element for each agent that is installed.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[configuration](configuration.md) <br/> |The root element for the agents configuration file.  <br/> |
   
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |This file does not define a namespace.  <br/> |
|Schema Name  <br/> |Not available.  <br/> |
|Validation File  <br/> |Not available.  <br/> |
|Can be Empty  <br/> |False.  <br/> |
   
## See also

- [Agents configuration file elements for Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

