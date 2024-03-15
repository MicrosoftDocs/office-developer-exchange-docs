---
title: "configuration"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- configuration
api_type:
- schema
ms.assetid: 6fc04e4d-657a-4999-9431-186ccb7832b5
description: "Last modified: September 17, 2015"
---

# configuration
  
**Applies to:** Exchange Server 2013
  
The **configuration** element is the root element for the agents configuration file. 
  
- [configuration](configuration.md) 
- [mexRuntime](mexruntime.md)
  
```XML
<configuration>
      <mexRuntime/>
</configuration>
```

**configurationType (complexType)**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.  <br/> |
   
### Parent elements

None.
  
## Element information

|**Element**|**Description**|
|:-----|:-----|
|Namespace  <br/> |This file does not define a namespace.  <br/> |
|Schema Name  <br/> |Not available.  <br/> |
|Validation File  <br/> |Not available.  <br/> |
|Can be Empty  <br/> |False.  <br/> |
   
## See also

- [Agents configuration file elements for Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

