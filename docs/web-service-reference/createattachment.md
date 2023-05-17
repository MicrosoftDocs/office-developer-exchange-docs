---
title: "CreateAttachment"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e33b403a-b7d3-48ee-8d24-6b7abf0d70bc
description: "The CreateAttachment element defines a request to create an attachment to an item in the Exchange store."
---

# CreateAttachment

The **CreateAttachment** element defines a request to create an attachment to an item in the Exchange store. 
  
```xml
<CreateAttachment>
   <ParentItemId/>
   <Attachments/>
</CreateAttachment>
```

 **CreateAttachmentType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

None.
  
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ParentItemId](parentitemid.md) <br/> |Identifies the parent Exchange store item that contains the created attachment. The [ParentItemId](parentitemid.md) element must provide the ID of a real Exchange store item. Real store items can be retrieved by using the [GetItem operation](getitem-operation.md); attachments are retrieved by using the [GetAttachment operation](getattachment-operation.md). An error occurs if the [ParentItemId](parentitemid.md) is passed the ID of a file attachment. If the [ParentItemId](parentitemid.md) represents the ID of an existing item attachment, the [CreateAttachment operation](createattachment-operation.md) adds the new attachment to the existing attachment.  <br/> This element is required for the [CreateAttachment operation](createattachment-operation.md).  <br/> |
|[Attachments](attachments-ex15websvcsotherref.md) <br/> |Contains the items or files to attach to an item in the Exchange store.  <br/> |
   
### Parent elements

None.
  
## Remarks

An item attachment does not exist as a store item. It only exists as an attachment to an item or another attachment. Item attachments can only be retrieved by using the [GetAttachment](getattachment.md) request. 
  
The following item attachments can be created:
  
- Item
    
- Message
    
- CalendarItem
    
- Contact
    
- Task
    
- MeetingMessage
    
- MeetingRequest
    
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Example

The following example shows how to create and attach an item to another item in the Exchange store.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="ASkAS"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>MyAttachment</t:Name>
          <t:Message>
            <t:ItemClass>IPM>Note</t:ItemClass>
            <t:Subject>My attachment subject</t:Subject>
            <t:Body BodyType="Text">My attachment body</t:Body>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

## Element information

| Element | Example |
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also



[CreateAttachment operation](createattachment-operation.md)
  
[DeleteAttachment operation](deleteattachment-operation.md)
  
[GetAttachment operation](getattachment-operation.md)

