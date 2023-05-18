---
title: "ExpandDLResponseMessage"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ExpandDLResponseMessage
api_type:
- schema
ms.assetid: 1140601b-98cf-4cb4-a019-321c7f63d5be
description: "The ExpandDLResponseMessage element contains the status and result of a single ExpandDL operation request."
---

# ExpandDLResponseMessage

The **ExpandDLResponseMessage** element contains the status and result of a single [ExpandDL operation](expanddl-operation.md) request. 
  
- [ExpandDLResponse](expanddlresponse.md)  
- [ResponseMessages](responsemessages.md) 
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
  
```xml
<ExpandDLResponseMessage ResponseClass="" IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DLExpansion/>
</ExpandDLResponseMessage>
```

**ExpandDLResponseMessageType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ResponseClass** <br/> | Describes the status of an [ExpandDL operation](expanddl-operation.md) response.<br/><br/>The following values are valid for this attribute: <br/> <br/>- Success  <br/>- Warning  <br/>- Error  <br/> |
|**IndexedPagingOffset** <br/> |Represents the next index that should be used for the next request when an indexed paging view is used.  <br/> |
|**NumeratorOffset** <br/> |Represents the new numerator value to use for the next request when fraction page views are used.  <br/> |
|**AbsoluteDenominator** <br/> |Represents the next denominator to use for the next request when doing fractional paging.  <br/> |
|**IncludesLastItemInRange** <br/> |Indicates that additional paging is not needed. This attribute will be true if the current results contain the last item in the query.  <br/> |
|**TotalItemsInView** <br/> |Represents the total number of items that pass the restriction.  <br/> |
   
#### ResponseClass attribute values

|**Value**|**Description**|
|:-----|:-----|
|**Success** <br/> |Describes a request that is fulfilled.  <br/> |
|**Warning** <br/> | Describes a request that was not processed. A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.<br/><br/> The following are examples of sources of warnings:<br/>  <br/>- The Exchange store is offline during the batch.  <br/>- Active Directory Domain Services (AD DS) is offline.  <br/>- Mailboxes are moved.  <br/>- The mailbox database (MDB) is offline.  <br/>- A password is expired.  <br/>- A quota was exceeded.  <br/> |
|**Error** <br/> | Describes a request that cannot be fulfilled.<br/><br/> The following are examples of sources of errors:  <br/><br/>- Invalid attributes or elements  <br/>- Attributes or elements that are out of range  <br/>- An unknown tag  <br/>- An attribute or element that is not valid in the context  <br/>- An unauthorized access attempt by any client  <br/>- A server-side failure in response to a valid client-side call <br/> <br/>  Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides an error code that identifies the specific error that the request encountered.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and is reserved for future use. It contains a value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
|[DLExpansion](dlexpansion.md) <br/> |Contains an array of mailboxes that are contained in a distribution list.  <br/> |
   
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.
  
## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [ExpandDL operation](expanddl-operation.md)
- [EWS reference for Exchange](ews-reference-for-exchange.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

