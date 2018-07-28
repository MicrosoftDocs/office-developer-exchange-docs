---
title: "Email and EWS in Exchange"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
localization_priority: Normal
ms.assetid: 4d7bdb37-f7f1-409f-9749-f8bcde7dc52a
description: "Find out how to work with email messages, including how to create an email and how to perform other email-related tasks by using the EWS Managed API or EWS in Exchange."
---

# Email and EWS in Exchange

Find out how to work with email messages, including how to create an email and how to perform other email-related tasks by using the EWS Managed API or EWS in Exchange.
  

  
At its core, Exchange is about email. But what makes an email an email? Well, email messages are one of the [strongly typed items](folders-and-items-in-ews-in-exchange.md#bk_item) in Exchange, which means that they contain a particular [set of properties](email-properties-and-elements-in-ews-in-exchange.md), even before they're sent. Email messages are represented by the [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) class in the EWS Managed API and by the [Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) element and its child elements in EWS. 
  
In the EWS Managed API, the **EmailMessage** object derives from the [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object. The **EmailMessage** class extends the **Item** class by providing additional properties like [EmailMessage.Sender](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sender%28v=exchg.80%29.aspx) and [EmailMessage.IsRead](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.isread%28v=exchg.80%29.aspx), which are now common to nearly all messaging scenarios. When you get, update, or delete an email message, in most cases you can do that by using the **EmailMessage** object or the base **Item** object, depending on whether the properties you're working with are in the [EmailMessageSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema%28v=exchg.80%29.aspx) or the [ItemSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx) class. Item creation is different because the **Item** class does not have a constructor, so when you're creating an email, you'll use the [EmailMessage constructor](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) to create it and the [EmailMessage.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) or [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) methods to save it, or send it and save it. 
  
Similarly, in EWS, use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the [Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) element to create an email message. To get, update, or delete emails by using EWS, the fact that the item being modified is an email message is not important, aside from the fact that additional properties are available on email messages. The same operations that are used for other strongly typed items are also used for email messages. 
  
|**Task**|**EWS Managed API method**|**EWS operation**|
|:-----|:-----|:-----|
|Create  <br/> |[EmailMessage.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|Get  <br/> |[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|Update  <br/> |[Item.Update](http://msdn.microsoft.com/en-us/library/dd635915%28v=exchg.80%29.aspx) <br/> |[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Delete  <br/> |[Item.Delete](http://msdn.microsoft.com/en-us/library/dd635072%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
Because email messages are simply [strongly typed items](folders-and-items-in-ews-in-exchange.md#bk_item), in some cases you work with them in the same way that you [work with generic items](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md). 
  
## Create an email message by using the EWS Managed API
<a name="bk_createewsma"> </a>

You can create an email message by using the EWS Managed API [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) method, as shown in the code in the following example. Note that the example only saves the message in the Drafts folder, it does not send the message. For information about how to send the message or create and send the message in one step, see [Send email messages by using EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).
  
This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server. 
  
```cs
// Create a new email message.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.ToRecipients.Add("mack@contoso.com");
message.Subject = "Project priorities";
message.Body = "(1) Buy pizza, (2) Eat pizza";
// Save the email message to the Drafts folder (where it can be retrieved, updated, and sent at a later time).
// This method call results in a CreateItem call to EWS.
message.Save(WellKnownFolderName.Drafts);
Console.WriteLine("A draft email message with the subject '" + message.Subject + "' has been saved to the Drafts folder.");
```

## Create an email message by using EWS
<a name="bk_createews"> </a>

You can create an email message by using the EWS [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation, as shown in the following example. This is also the XML request that the EWS Managed API sends when you [create an email message](#bk_createewsma). Note that the following example only saves the message in the Drafts folder, it does not send the message. For information about how to send the message or create and send the message in one ste, see [Send email messages by using EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP2" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Project priorities</t:Subject>
          <t:Body BodyType="HTML">(1) Buy pizza, (2) Eat pizza</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>mack@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message. 
  
## Get, update, and delete an email message by using the EWS Managed API
<a name="bk_getewsma"> </a>

You can use the EWS Managed API to get, update, or delete an email message in the same way that you perform these actions on any generic item from the Exchange store. For more information, see [Work with Exchange mailbox items by using EWS in Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).
  
If you're updating an email message, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md) for a list of writable email message properties. To send a draft message after you've updated it, see [Send a draft email message by using the EWS Managed API](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftewsma).
  
## Get, update, and delete an email message by using EWS
<a name="bk_getews"> </a>

You can use EWS to get, update, and delete an email message in the same way that you perform these actions on any generic item from the Exchange store. For more information, see [Work with Exchange mailbox items by using EWS in Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).
  
If you're updating an email message, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md) for a list of writable email message properties. To send a draft message after you've updated it, see [Send a draft email message by using EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).
  
## In this section
<a name="bk_inthissection"> </a>

- [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md)
    
- [Send email messages by using EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md)
    
- [Respond to email messages by using EWS in Exchange](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    
- [Move and copy email messages by using EWS in Exchange](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)
    
- [Work with conversations by using EWS in Exchange](how-to-work-with-conversations-by-using-ews-in-exchange.md)
    
- [Extract an entity from an email message by using EWS in Exchange](how-to-extract-an-entity-from-an-email-message-by-using-ews-in-exchange.md)
    
- [Process email messages in batches by using EWS in Exchange](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
## See also


- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)
    
- [Folders and items in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)
    

