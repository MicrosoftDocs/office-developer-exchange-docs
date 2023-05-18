---
title: "FindMailboxStatisticsByKeywords"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
ms.assetid: cfe0f0ff-5fea-4db8-ac96-a5724c85ed2f
description: "The FindMailboxStatisticsByKeywords element specifies a request to search for mailbox statistics by keyword."
---

# FindMailboxStatisticsByKeywords

The **FindMailboxStatisticsByKeywords** element specifies a request to search for mailbox statistics by keyword. 
  
```XML
<FindMailboxStatisticsByKeywords>
    <Mailboxes/>
    <Keywords/>
    <Language/>
    <Senders/>
    <Recipients/>
    <FromDate/>
    <ToDate/>
    <MessageTypes/>
    <SearchDumpster/>
    <IncludePersonalArchive/>
    <IncludeUnsearchableItems/>
</FindMailboxStatisticsByKeywords>
```

 **FindMailboxStatisticsByKeywordsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Mailboxes (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) <br/> |Contains an array of mailboxes affected by the hold.  <br/> |
|[Keywords](keywords-ex15websvcsotherref.md) <br/> |Specifies keywords for a search.  <br/> |
|[Language](language.md) <br/> |Contains the language used for the search query.  <br/> |
|[Senders](senders.md) <br/> |Specifies an array of SMTP addresses.  <br/> |
|[Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Specifies an array of recipients of a message.  <br/> |
|[FromDate](fromdate.md) <br/> |Specifies the date that the message was sent.  <br/> |
|[ToDate](todate.md) <br/> |Specifies the date that the message was received.  <br/> |
|[MessageTypes](messagetypes.md) <br/> |Specifies an array of messages to search.  <br/> |
|[SearchDumpster](searchdumpster.md) <br/> |Specifies whether to search in deleted items.  <br/> |
|[IncludePersonalArchive](includepersonalarchive.md) <br/> |Specifies whether to include the personal archive in the search.  <br/> |
|[IncludeUnsearchableItems](includeunsearchableitems.md) <br/> |Specifies whether to include items that cannot be searched.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Message schema  <br/> |
|Validation File  <br/> |messages.xsd  <br/> |
|Can Be Empty  <br/> ||
   
## See also



- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

