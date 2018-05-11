---
title: "messageSnapshot"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- messageSnapshot
api_type:
- schema
ms.assetid: f157e44c-b950-463f-b086-31d5da94b7ff
description: "Last modified: September 17, 2015"
---

# messageSnapshot

 **Last modified:** September 17, 2015 
  
 * **Applies to:** Exchange Server 2013 * 
  
The **messageSnapshot** element contains an attribute that specifies whether the pipeline tracing feature is enabled for the Exchange server that has the Client Access or the Mailbox server role installed. 
  
[configuration](configuration.md)
  
[mexRuntime](mexruntime.md)
  
[monitoring](monitoring.md)
  
[messageSnapshot](messagesnapshot.md)
  
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
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[monitoring](monitoring.md) <br/> |Contains configuration information that defines how and when the transport service monitors agents that are installed.  <br/> |
   
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

