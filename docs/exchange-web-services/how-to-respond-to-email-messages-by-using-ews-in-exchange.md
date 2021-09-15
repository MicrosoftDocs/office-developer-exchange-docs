---
title: "Respond to email messages by using EWS in Exchange"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: 9d584991-4d67-4d36-ae2f-99970af8488f
description: "Learn how to respond to email messages by using the EWS Managed API or EWS in Exchange."
---

# Respond to email messages by using EWS in Exchange

Learn how to respond to email messages by using the EWS Managed API or EWS in Exchange.
  
You can use the EWS Managed API or EWS to respond to messages by replying to them or forwarding them to recipients.
  
**Table 1. EWS Managed API methods and EWS operations for responding to email messages**

|**Task**|**EWS Managed API method**|**EWS operation**|
|:-----|:-----|:-----|
|Reply to an email message  <br/> |[EmailMessage.Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> [EmailMessage.CreateReply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), where the [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element has a child element of either [ReplyToItem](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) or [ReplyAllToItem](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx).  <br/> |
|Forward an email message  <br/> |[EmailMessage.Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) <br/> [EmailMessage.CreateForward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), where the [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element has a child element of [ForwardItem](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx).  <br/> |
   
## Reply to an email message by using the EWS Managed API
<a name="bk_replyewsma"> </a>

The EWS Managed API provides two methods that you can use to respond to messages: [Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) and [CreateReply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx). The **Reply** method only takes two parameters: the response message to prepend to the existing body, and a **Boolean** value that indicates whether the response should go to all recipients (true) or just the sender (false). If you need to add additional recipients to a message, set additional properties on a response, or add an attachment, use the **CreateReply** method, which enables you to set all the [first-class properties](email-properties-and-elements-in-ews-in-exchange.md) that are available on an [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object. 
  
The following code example shows how to use the **Reply** method to respond to an email message. 
  
This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server. The local variable  *ItemId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to respond to. The example calls the [FindRecentlySent method](#bk_findlast) to verify that the message was marked as replied to. 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.LastModifiedTime);
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, propSet);
string myReply = "This is the message body of the email reply.";
bool replyToAll = false;
// Send the response message.
// This method call results in a CreateItem call to EWS.
message.Reply(myReply, replyToAll);
// Verify that the response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

The following code example shows how to use the **CreateReply** method to respond to an email message. 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
// Create the reply response message from the original email message.
// Indicate whether the message is a reply or reply all type of reply.
bool replyToAll = true;
ResponseMessage responseMessage = message.CreateReply(replyToAll);
// Prepend the reply to the message body. 
string myReply = "This is the message body of the email reply.";
responseMessage.BodyPrefix = myReply;
// Send the response message.
// This method call results in a CreateItem call to EWS.
responseMessage.SendAndSaveCopy();
// Check that the response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

If you need to add an attachment to the response message, replace the call to the **SendAndSaveCopy** method with the following code. 
  
```cs
EmailMessage reply = responseMessage.Save();
reply.Attachments.AddFileAttachment("attachmentname.txt");
reply.Update(ConflictResolutionMode.AutoResolve);
reply.SendAndSaveCopy();
```

## Reply to an email message by using EWS
<a name="bk_replyews"> </a>

The following code example shows how to reply to a message by using EWS. Use the [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the **MessageDisposition** attribute set to **SendAndSaveCopy** to send the message and save the response in the Sent Items folder. Include either the [ReplyAllToItem](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx) element as a child of the [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element to reply to everyone on the message thread, or include the [ReplyToItem](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) element to reply only to the sender. 
  
This is also the XML request that the EWS Managed API sends when calling either the [Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) or the [CreateReply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) method. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:ReplyAllToItem>
          <t:ReferenceItemId Id="AAMkADE4="
                             ChangeKey="CQAAABYA" />
          <t:NewBodyContent BodyType="HTML">This is the message body of the email reply.</t:NewBodyContent>
        </t:ReplyAllToItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the reply was created and sent successfully.
  
If you need to add an attachment to your response message, call the **CreateItem** operation as specified above, but change the **MessageDisposition** to **SaveOnly**. Then call the [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation, followed by the [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation. 
  
## Forward an email message by using the EWS Managed API
<a name="bk_forwardewsma"> </a>

The EWS Managed API provides two methods that you can use to forward messages: [Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) and [CreateForward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx). The **Forward** method only takes two parameters: the message to prepend to the existing body, and an array or collection of recipients, depending on the overload you choose to use. If you need to add an attachment to the message you're forwarding, or set additional properties on the new message, use the **CreateForward** method, which enables you to set all the properties that are available on an [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object. 
  
The following code example shows how to use the **Forward** method to forward an email message to one recipient. 
  
This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server. The local variable  *ItemId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to forward. The example calls the [FindRecentlySent method](#bk_findlast) to verify that the message was marked as forwarded. 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
string myForward = "This is the message body of the forwarded email.";
// Send the response message.
// This method call results in a CreateItem call to EWS.
message.Forward(myForward, "sadie@contoso.com");
// Verify that the forwarded response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

The following code example shows how to use the **CreateForward** method to forward an email message to one recipient. 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
// Create the reply response message from the original email message.
// Indicate whether the message is a reply or reply all type of reply.
ResponseMessage forwardMessage = message.CreateForward();
// Set properties on the email message.
forwardMessage.ToRecipients.Add("sadie@contoso.com");
forwardMessage.Body = "Sadie,<br><br>I thought you'd be interested in this thread.<br><br>-Mack";
// Send and save a copy of the replied email message in the default Sent Items folder. 
forwardMessage.SendAndSaveCopy();
// Verify that the forwarded message was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

If you need to add an attachment to the forwarded message, replace the call to the **SendAndSaveCopy** method with the following code. 
  
```cs
EmailMessage forward = forwardMessage.Save();
forward.Attachments.AddFileAttachment("attachmentname.txt");
forward.Update(ConflictResolutionMode.AutoResolve);
forward.SendAndSaveCopy();
```

## Forward an email message by using EWS
<a name="bk_forwardews"> </a>

The following code example shows how to forward a message by using EWS. Use the [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the **MessageDisposition** attribute set to **SendAndSaveCopy** to send the message and save the response in the Sent Items folder. The [ForwardItem](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx) element indicates that the item is a forwarded message. 
  
This is also the XML request that the EWS Managed API sends when calling either the [Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) or the [CreateForward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) method. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:ForwardItem>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
          <t:ReferenceItemId Id="AAAMkADE="
                             ChangeKey="CQAAABYA" />
          <t:NewBodyContent BodyType="HTML">This is the message body of the forwarded email.</t:NewBodyContent>
        </t:ForwardItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the forwarded message was created and sent successfully.
  
If you need to add an attachment to your response message, call the **CreateItem** operation, but change the **MessageDisposition** to **SaveOnly**. Then call the [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation, followed by the [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation. 
  
## Find the message last replied to or forwarded by using the EWS Managed API
<a name="bk_findlast"> </a>

The following code example shows how to find the last verb executed and the time the last verb was executed on the item specified. This method is called from other EWS Managed API code examples in this topic to verify that the items you replied to or forwarded were marked as replied to or forwarded in your Inbox. 
  
The example uses the [PidTagLastVerbExecuted](https://msdn.microsoft.com/library/cc841968.aspx) (0x10820003) extended property to determine whether the message was a reply, a reply all, or a forward, and the [PidTagLastVerbExecutionTime](https://msdn.microsoft.com/library/cc839918.aspx) (0x10820040) extended property to determine when the reply or forward was sent. 
  
```cs
public static void FindRecentlySent(EmailMessage messageToCheck)
{
    // Create extended property definitions for PidTagLastVerbExecuted and PidTagLastVerbExecutionTime.
    ExtendedPropertyDefinition PidTagLastVerbExecuted = new ExtendedPropertyDefinition(0x1081, MapiPropertyType.Integer);
    ExtendedPropertyDefinition PidTagLastVerbExecutionTime = new ExtendedPropertyDefinition(0x1082, MapiPropertyType.SystemTime);
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, PidTagLastVerbExecutionTime, PidTagLastVerbExecuted);
    messageToCheck = EmailMessage.Bind(service, messageToCheck.Id, propSet);
    // Determine the last verb executed on the message and display output.
    object responseType;
    if (messageToCheck.TryGetProperty(PidTagLastVerbExecuted, out responseType))
    {
        object ReplyTime = null;
        switch (((Int32)responseType))
        {
            case 102: Console.WriteLine("A reply was sent to the '" + messageToCheck.Subject.ToString() + "' email message at");
                break;
            case 103: Console.WriteLine("A reply all was sent to the '" + messageToCheck.Subject.ToString() + "' email message at");
                break;
            case 104: Console.WriteLine("The '" + messageToCheck.Subject.ToString() + "' email message was forwarded at");
                break;
        }
        if (messageToCheck.TryGetProperty(PidTagLastVerbExecutionTime, out ReplyTime))
        {
            Console.WriteLine(((DateTime)ReplyTime).ToString() + ".");
        }
    }
    else
    {
        Console.WriteLine("No changes were made to  '" + messageToCheck.Subject.ToString() + "'.");
    }
}
```

## See also


- [Email and EWS in Exchange](email-and-ews-in-exchange.md)
    
- [Send email messages by using EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

