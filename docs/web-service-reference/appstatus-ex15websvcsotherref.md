---
title: "AppStatus"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: f3ab8bf1-abc5-45cf-a2e1-d7602f2c24ec
description: "The AppStatus element value indicates the status of the mail app."
---

# AppStatus

The **AppStatus** element value indicates the status of the mail app. 
  
```XML
<AppStatus/>
```

 **string**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

None.
  
### Parent elements

[Metadata](metadata-ex15websvcsotherref.md)
  
## Text value

The text value of the **AppStatus** element indicates the status of the mail app. If the user can fix an issue related to the status of the mail app, the [ActionUrl](actionurl.md) element provides the URL to perform the fix. 
  
**Table 1. AppStatus values**

|**Value**|**Description**|
|:-----|:-----|
|Null or 0  <br/> |The mail app has a healthy status.  <br/> |
|1.0  <br/> |The mail app could not be automatically updated. The mail app needs to be re-installed from the Office Store.  <br/> |
|1.1  <br/> |The mail app could not be automatically updated. The mail app requires increased permissions, and this requires your review and confirmation to install.  <br/> |
|1.2  <br/> |The mail app couldn't be updated automatically. The current license has expired or is invalid. Please update the mail app from the Office Store.  <br/> |
|2.0  <br/> |The mail app license could not be automatically updated. The license for the mail app needs to be recovered from the Office Store.  <br/> |
|2.1  <br/> |The mail app license could not be automatically updated. The current license has expired. A new license for this app needs to be installed from the Office Store.  <br/> |
|3.0  <br/> |The Office Store status for the mail app has changed. This may indicate that there is a problem with the mail app. Go to the mail app page in the Office Store for more information.  <br/> |
|3.1  <br/> |The mail app has been removed from the Office Store.  <br/> |
|3.2  <br/> |A problem has been discovered with the mail app and it has temporarily been withdrawn from the Office Store.  <br/> |
|3.3  <br/> |The mail app will be removed from the Office Store within 30 days.  <br/> |
|4.0  <br/> |The mail app has been automatically disabled by your mail client.  <br/> |
|4.1  <br/> |The mail app has been disabled by Outlook for performance reasons.  <br/> |
   
## Remarks

This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).
  
The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> | https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Not applicable  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [Metadata](metadata-ex15websvcsotherref.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

