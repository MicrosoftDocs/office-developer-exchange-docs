---
title: "agentList"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- agentList
api_type:
- schema
ms.assetid: e877b7ef-e303-4270-964d-8d116ff2a865
description: "Last modified: September 17, 2015"
---

# agentList
  
**Applies to:** Exchange Server 2013
  
The **agentList** element contains an [agent](agent.md) element for each installed agent. 
  
- [configuration](configuration.md)
- [mexRuntime](mexruntime.md)
- [agentList](agentlist.md)
  
```XML
<agentList>
      <agent/>
</agentList>
```

**agentListType (complexType)**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[agent](agent.md) <br/> |Contains configuration information about an installed agent.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |Contains elements that define configuration information for agent monitoring and configuration information about installed agents.  <br/> |
   
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |This file does not define a namespace.  <br/> |
|Schema Name  <br/> |Not available.  <br/> |
|Validation File  <br/> |Not available.  <br/> |
|Can be Empty  <br/> |False.  <br/> |
   
## See also

- [Agents configuration file elements for Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

