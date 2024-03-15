---
title: "agent"
manager: lindalu
ms.date: 03/10/2022
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- agent
api_type:
- schema
ms.assetid: 0bf744a5-9d79-4c82-8ea7-45fdb3f55300
description: "Configuration information about an installed agent. "
---

# agent
  
**Applies to:** Exchange Server 2013
  
The **agent** element contains configuration information about an installed agent. 
  
- [configuration](configuration.md) 
- [mexRuntime](mexruntime.md)
- [agentList](agentlist.md)
- [agent](agent.md)
  
```XML
<agent
        name=""
        baseType=""
        classFactory=""
        assemblyPath=""
        enabled="" />
</agent>
```

**agentType (complexType)**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**name** <br/> |The name that was specified when the agent was installed. This attribute requires a nonempty string value that contains a maximum of 64 characters.  <br/> |
|**baseType** <br/> |The full name, including the namespace, of the class from which the agent derives. This attribute requires a nonempty string value that contains at least one character.  <br/> |
|**classFactory** <br/> |The full name, including the namespace, of the class that implements the agent factory that creates instances of the agent. This attribute must contain the fully qualified name of the class that implements the agent factory that creates instances of the agent. This class must derive from either the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) or [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) class.  <br/> |
|**assemblyPath** <br/> |The fully qualified path, including the file name, of the assembly that contains the code for the agent. This attribute requires a nonempty string value that contains at least one character.  <br/> |
|**enabled** <br/> |A Boolean value that indicates whether the agent is enabled. The value is **true** if the agent is enabled; otherwise, the value is **false**. This attribute is required.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[agentList](agentlist.md) <br/> |Contains an **agent** element for each installed agent.  <br/> |
   
## Element information

|**Element**|**Example**|
|:-----|:-----|
|Namespace  <br/> |This file does not define a namespace.  <br/> |
|Schema Name  <br/> |Not available.  <br/> |
|Validation File  <br/> |Not available.  <br/> |
|Can be Empty  <br/> |False.  <br/> |
   
## See also

- [Agents configuration file elements for Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

