---
title: "messageSnapshot"
manager: lindalu
ms.date: 03/14/2022
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- messageSnapshot
api_type:
- schema
ms.assetid: f157e44c-b950-463f-b086-31d5da94b7ff
description: "Contains an attribute that specifies whether the pipeline tracing feature is enabled for the Exchange server that has the Client Access or the Mailbox server role installed."
---

# messageSnapshot

**Applies to:** Exchange Server 2013
  
The **messageSnapshot** element contains an attribute that specifies whether the pipeline tracing feature is enabled for the Exchange server that has the Client Access or the Mailbox server role installed. 
  
- [configuration](configuration.md)  
- [mexRuntime](mexruntime.md) 
- [monitoring](monitoring.md) 
- [messageSnapshot](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

**messageSnapshotType (Boolean)**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**enabled** <br/> |A Boolean value that indicates whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server. The value is **true** if pipeline tracing is enabled; otherwise, the value is **false** or the element is not present.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[monitoring](monitoring.md) <br/> |Contains configuration information that defines how and when the transport service monitors agents that are installed.  <br/> |
   
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |This file does not define a namespace.  <br/> |
|Schema Name  <br/> |Not available.  <br/> |
|Validation File  <br/> |Not available.  <br/> |
|Can be Empty  <br/> |False.  <br/> |
   
## See also

- [Agents configuration file elements for Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

