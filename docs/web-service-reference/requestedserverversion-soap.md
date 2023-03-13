---
title: "RequestedServerVersion (SOAP)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: exchange
ms.subservice: exchange-web-services
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: cf3f9d7a-2add-4457-b009-2929220f90b5
description: "The RequestedServerVersion element specifies the server version that an Autodiscover method call targets."
 
 
---

# RequestedServerVersion (SOAP)

The **RequestedServerVersion** element specifies the server version that an **Autodiscover** method call targets. 
  
```XML
<RequestedServerVersion/>
```

 **ExchangeVersion**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

None.
  
## Text value

The text value of the **RequestedServerVersion** element specifies the server version that an **Autodiscover** method call targets. The following table lists the valid server versions. 
  
|**Text value**|**Description**|
|:-----|:-----|
|Exchange2007_SP1  <br/> |Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|Exchange2010  <br/> |Exchange Server 2010.  <br/> |
|Exchange2010_SP1  <br/> |Exchange Server 2010 Service Pack 1 (SP1).  <br/> |
|Exchange2010_SP2  <br/> |Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
|Exchange2013  <br/> |Exchange Server 2013. The Exchange2013 field is applicable for clients that target Exchange Online and versions of Exchange starting with Exchange Server 2013.  <br/> |
|Exchange2013_SP1  <br/> |Exchange Server 2013 Service Pack 1 (SP1). The Exchange2013_SP1 field is applicable for clients that target Exchange Online and versions of Exchange starting with Exchange Server 2013 SP1.  <br/> |
   
## Remarks

The **RequestedServerVersion** element is set in the SOAP header. 
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   

