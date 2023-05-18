---
title: "CreateAttachment operation" 
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
ms.assetid: e066db95-6963-4507-a8d0-8efad287f550
description: "The CreateAttachment operation creates either an item or file attachment and attaches it to the specified item."
---

# CreateAttachment operation

The CreateAttachment operation creates either an item or file attachment and attaches it to the specified item.
  
## File CreateAttachment request example

The following example of a CreateAttachment request shows how to create a file attachment.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
<soap:Body>
  <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
    <ParentItemId Id="AAAtAE..." ChangeKey="CQAAABYA..."/>
    <Attachments>
      <t:FileAttachment>
        <t:Name>SomeFile</t:Name>
        <t:Content>AQIDBAU=</t:Content>
      </t:FileAttachment>
    </Attachments>
  </CreateAttachment>
</soap:Body>
</soap:Envelope>
```

A name for the attachment must be provided.
  
> [!NOTE]
> The parent item identifier and change key have been shortened to preserve readability.
  
### File CreateAttachment request elements

The following elements are used in the request:
  
- [CreateAttachment](createattachment.md)
- [ParentItemId](parentitemid.md)
- [Attachments](attachments-ex15websvcsotherref.md)
- [FileAttachment](fileattachment.md)
- [Name (AttachmentType)](name-attachmenttype.md)
- [Content](content.md)

## Successful file CreateAttachment response example

The following example shows a successful response to the CreateAttachment request.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="AAAtAE=" RootItemId="AAAtAEFk=" RootItemChangeKey="CQAAAB"/>
            </t:FileAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

The response contains the identifier of the attached file. It also contains the identifier and change key of the root item. The item identifiers and change key have been shortened to preserve readability.
  
### Successful file CreateAttachment response elements

The following elements are used in the response:
  
- [ServerVersionInfo](serverversioninfo.md)
- [CreateAttachmentResponse](createattachmentresponse.md)
- [ResponseMessages](responsemessages.md)
- [CreateAttachmentResponseMessage](createattachmentresponsemessage.md)
- [ResponseCode](responsecode.md)
- [Attachments](attachments-ex15websvcsotherref.md)
- [FileAttachment](fileattachment.md)
- [AttachmentId](attachmentid.md)

## Item CreateAttachment request example

The following example of a CreateAttachment request shows how to create an item attachment.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="AAAtAE=" ChangeKey="CQAAABYA"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>An item attachment</t:Name>
          <t:Message>
            <t:Subject>A message to attach</t:Subject>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

A name for the attachment must be provided. The parent item identifier and change key have been shortened to preserve readability.
  
### Item CreateAttachement request elements

The following elements are used in the request:
  
- [CreateAttachment](createattachment.md)
- [ParentItemId](parentitemid.md)
- [Attachments](attachments-ex15websvcsotherref.md)
- [ItemAttachment](itemattachment.md)
- [Name (AttachmentType)](name-attachmenttype.md)
- [Message](message-ex15websvcsotherref.md)
- [Subject](subject.md)

## Successful item CreateAttachment response example

The following example shows a successful response to the CreateAttachment request.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:ItemAttachment>
              <t:AttachmentId Id="AAAtAEFk=" RootItemId="AAAtAEFkb=" RootItemChangeKey="CQAAABYA"/>
            </t:ItemAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

The response contains the identifier of the new attachment. It also contains the identifier and change key of the root item. The root item is the item that contains the attachment. The item identifiers and change key have been shortened to preserve readability.
  
### Successful item CreateAttachment response elements

The following elements are used in the response:
  
- [ServerVersionInfo](serverversioninfo.md)
- [CreateAttachmentResponse](createattachmentresponse.md)
- [ResponseMessages](responsemessages.md)
- [CreateAttachmentResponseMessage](createattachmentresponsemessage.md)
- [ResponseCode](responsecode.md)
- [Attachments](attachments-ex15websvcsotherref.md)
- [ItemAttachment](itemattachment.md)
- [AttachmentId](attachmentid.md)

## CreateAttachment error response example

The following example shows an error response to the CreateAttachment request. The error is due to the fact that the name of the attachment was not specified.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Error">
          <m:MessageText>Required property is missing.</m:MessageText>
          <m:ResponseCode>ErrorRequiredPropertyMissing</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:MessageXml>
            <t:ExceptionFieldURI FieldURI="attachment:Name"/>
          </m:MessageXml>
          <m:Attachments/>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### CreateAttachment error response elements

The following elements are used in the error response:
  
- [ServerVersionInfo](serverversioninfo.md)
- [CreateAttachmentResponse](createattachmentresponse.md)
- [ResponseMessages](responsemessages.md)
- [CreateAttachmentResponseMessage](createattachmentresponsemessage.md)
- [MessageText](messagetext.md)
- [ResponseCode](responsecode.md)
- [DescriptiveLinkKey](descriptivelinkkey.md)
- [MessageXml](messagexml.md)
- [ExceptionFieldURI](exceptionfielduri.md)
- [Attachments](attachments-ex15websvcsotherref.md)

## Remarks

If multiple attachments are attached to an item in a single round trip, the RootItemChangeKey in the last response message is the one that represents the new change key of the item that has the attachments.
  
## See also

[DeleteAttachment operation](deleteattachment-operation.md)
[GetAttachment operation](getattachment-operation.md)
