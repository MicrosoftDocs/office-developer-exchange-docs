---
title: "MailTipsConfiguration (MailTipsServiceConfiguration)"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- MailTipsConfiguration
api_type:
- schema
ms.assetid: 9a34515e-815b-4c61-b118-d5f66b80238f
description: "The MailTipsConfiguration element contains service configuration information for the mail tips service."
---

# MailTipsConfiguration (MailTipsServiceConfiguration)

The **MailTipsConfiguration** element contains service configuration information for the mail tips service. 
  
```XML
<MailTipsConfiguration>
   <MailTipsEnabled/>
   <MaxRecipientsPerGetMailTipsRequest/>
   <MaxMessageSize/>
   <LargeAudienceThreshold/>
   <ShowExternalRecipientCount/>
   <InternalDomains/>
</MailTipsConfiguration>
```

 **MailTipsServiceConfiguration**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MailTipsEnabled](mailtipsenabled.md) <br/> |Indicates whether the mail tips service is available. This element is required.  <br/> |
|[MaxRecipientsPerGetMailTipsRequest](maxrecipientspergetmailtipsrequest.md) <br/> |Indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md). This element is required.  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |Represents the maximum message size a recipient can accept. This element is required.  <br/> |
|[LargeAudienceThreshold](largeaudiencethreshold.md) <br/> |Represents the large audience threshold for a client. This element is required.  <br/> |
|[ShowExternalRecipientCount](showexternalrecipientcount.md) <br/> |Indicates whether consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed. This element is required.  <br/> |
|[InternalDomains (SmtpDomainList)](internaldomains-smtpdomainlist.md) <br/> |Identifies the list of internal SMTP domains of the organization. This element is required.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contains service configuration settings.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

