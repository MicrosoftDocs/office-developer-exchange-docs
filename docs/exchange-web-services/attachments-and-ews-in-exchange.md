---
title: "Attachments and EWS in Exchange" 
description: "Learn about attachments and how your EWS Managed API or EWS in Exchange client represents them."
manager: sethgros
ms.date: 7/11/2016
ms.audience: Developer 
ms.assetid: 8e4289a4-ec9d-4502-9854-c593c95d5f98
localization_priority: Priority
---

# Attachments and EWS in Exchange

Learn about attachments and how your EWS Managed API or EWS in Exchange client represents them.
  
Usually, attachments are associated with email items, but in fact, all EWS items — email messages, calendar items, contacts, tasks — can include attachments.
  
## Types of attachments

EWS categorizes attachments into two groups: file attachments and item attachments.
  
- **Item attachments:** Strongly-typed [EWS items](folders-and-items-in-ews-in-exchange.md), such as email messages and calendar items, that are attached to another strongly-typed EWS item. Any strongly-typed item that can be created by using the EWS Managed API or EWS can be used as an item attachment. The content of an item attachment is the strongly-typed item, which provides easy access to all its properties. Item attachments can have their own item attachments, so a hierarchy of item attachments (or nesting of attachments) is possible.
    
- **File attachments:** Any file, such as a .txt, .jpg, .zip, .pdf, or even a .msg file. A file attachment only has a few properties, one of which is the base-64 encoded content of the file. 
    
- **Reference attachments:** Any attachment that is referenced by a file provider, such as a file located in the cloud. An attachment can be from multiple providers. 
    
When you add or retrieve attachments from an item, you'll do it differently depending on whether it's a file attachment or an item attachment. For example, to add a file attachment to an item, you can just pass in the location of the file. To add an existing item as an item attachment, you actually have to copy the properties or the MIME content of the existing item to a new item attachment; you can't just bind to the existing item. So distinguishing between the two types of attachments is important. More details about the differences between item attachments and file attachments are discussed in the articles [In this section](#bk_inthissection).
  
## How are attachments represented programmatically?

Attachments are stored in a collection on the EWS item. The attachments collection is made up of file attachments and/or item attachments. Metadata about the attachment collection is available when you get an item by using the EWS Managed API [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method or the EWS [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) operation, but additional calls are required to actually retrieve the contents of the attachments. 
  
**Table 1. Item metadata about attachments**

|**Metadata entity**|**EWS Managed API property**|**EWS element**|
|:-----|:-----|:-----|
|Attachment indicator (does not flag inline attachments)  <br/> |[Item.HasAttachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) <br/> |[HasAttachments](https://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx) <br/> |
|Attachment collection  <br/> |[Item.Attachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) <br/> |[Attachments](https://msdn.microsoft.com/library/b470e614-34bb-44f0-8790-7ddbdcbbd29d%28Office.15%29.aspx) <br/> |
|Attachment ID  <br/> |[Attachment.Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.id%28v=exchg.80%29.aspx) <br/> |[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) <br/> |
   
**Table 2. Attachment entities**

|**Attachment type**|**EWS Managed API class**|**EWS element**|
|:-----|:-----|:-----|
|File attachment  <br/> |[FileAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.fileattachment%28v=exchg.80%29.aspx) <br/> |[FileAttachment](https://msdn.microsoft.com/library/3ecea174-73d1-47fd-8917-6065cef1d565%28Office.15%29.aspx) <br/> |
|Item attachment  <br/> |[ItemAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemattachment%28v=exchg.80%29.aspx) <br/> [ItemAttachment\<TItem\>](https://msdn.microsoft.com/library/dd635165%28v=exchg.80%29.aspx) <br/> |[ItemAttachment](https://msdn.microsoft.com/library/089ee599-f45e-46f5-a18a-5cfb3d2851ff%28Office.15%29.aspx) <br/> |
|Reference attachment  <br/> |[ReferenceAttachmentType complexType (EWS)](https://msdn.microsoft.com/library/18bfa012-e903-d7f3-528a-31ccceb65463%28Office.15%29.aspx) <br/> |[ReferenceAttachment](https://msdn.microsoft.com/library/b9bde862-6b75-4a81-8033-00a47be4dc2f%28Office.15%29.aspx) <br/> |
   
## Inline attachments

Inline attachments are a special breed of attachment. Both file attachments and item attachments can be inline attachments. An inline attachment appears as part of the body content and retains its position relative to the rest of the content in the item. 
  
An attachment is an inline attachment if the EWS Managed API [IsInline](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx) property or the EWS [IsInline](https://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx) element is set to true. Inline attachments use the following optional properties and elements to identify the location of an inline attachment: 
  
- EWS Managed API — [ContentId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.contentid%28v=exchg.80%29.aspx) or [ContentLocation](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.contentlocation%28v=exchg.80%29.aspx) properties. 
    
- EWS — [ContentId](/exchange/client-developer/web-service-reference/contentid) or [ContentLocation](https://msdn.microsoft.com/library/d91cf587-24e3-4c13-8784-5ca29787cca7%28Office.15%29.aspx) element. 
    
Note that the EWS Managed API [HasAttachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) property and the EWS [HasAttachments](https://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx) element do not reflect the existence of inline attachments, and that's why inline attachments are also called hidden attachments. So if you set the EWS Managed API [IsInline](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx) property or the EWS [IsInline](https://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx) element to true, and the item has no other attachments, **HasAttachments** will be set to false. If your client uses **HasAttachments** to populate an attachment indicator or icon on an email, be aware that the icon will not appear for emails with inline attachments. 
  
## In this section
<a name="bk_inthissection"> </a>

- [Add attachments by using EWS in Exchange](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [Get attachments by using EWS in Exchange](how-to-get-attachments-by-using-ews-in-exchange.md)
    
- [Delete attachments by using EWS in Exchange](how-to-delete-attachments-by-using-ews-in-exchange.md)
    
## See also
<a name="bk_additionalresources"> </a>

- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)
    
- [Folders and items in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [Email and EWS in Exchange](email-and-ews-in-exchange.md)
    

