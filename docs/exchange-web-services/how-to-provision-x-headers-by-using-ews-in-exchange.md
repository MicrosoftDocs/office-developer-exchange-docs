---
title: "Provision x-headers by using EWS in Exchange"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: 45a99a14-a85f-47f8-af48-18eb6c6cc230
description: "Learn how to provision x-headers for a mailbox by using the EWS Managed API or EWS in Exchange."
---

# Provision x-headers by using EWS in Exchange

Learn how to provision x-headers for a mailbox by using the EWS Managed API or EWS in Exchange.
  
X-headers are non-standard headers that are added to the header collection of an email to communicate information. For example, Exchange stamps messages with the **X-MS-Exchange-Organization-SCL** header to indicate the spam confidence level (SCL) attributed to the email. Email clients like Outlook can use that information to determine what type of action to take on the email (for example, Outlook can prevent images from displaying unless the user takes an action). 
  
Exchange adds incoming x-headers to the mailbox schema as a named property the first time it receives an email with that x-header. The x-header value is not saved on that first email; however, it is saved on all subsequent emails that include the x-header. For this reason, your application should provision x-headers before you expect to use them. The mapping between a named property and an x-header occurs in the transport delivery of the email to the mailbox. This means that you need to receive the email via transport delivery; you cannot just save an email that includes the x-header to a mailbox to create the mapping to a named property.
  
> [!NOTE]
> If you find that x-headers aren't being saved, determine whether a [transport agent](https://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a) or [header firewall](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx) is filtering out your x-headers before they get to the mailbox. 
r
  
## Provision an x-header by using the EWS Managed API
<a name="bk_example1"> </a>

The following code example shows how to use the EWS Managed API [EmailMessage.Send](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) method to provision an x-header for a mailbox. This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the target mailbox hasn't exceeded the [quota for named properties](https://technet.microsoft.com/library/bb851492%28v=EXCHG.80%29.aspx).
  
```cs
private static void ProvisionCustomXHeaderByEmail(ExchangeService service)
{
    // Create a definition for an extended property that will represent a custom x-header. X-headers must be created in the
    // InternetHeaders property set. The x-header name must match the name of the x-header sent in the subsequent emails so
    // the x-header and value are saved on the email.
    ExtendedPropertyDefinition xExperimentalHeader = new ExtendedPropertyDefinition(DefaultExtendedPropertySet.InternetHeaders,
                                                                                            "X-Experimental",
                                                                                            MapiPropertyType.String);
    // Create an item that is used to provision the custom x-header.
    EmailMessage email = new EmailMessage(service);
    email.ToRecipients.Add("user@contoso.com");
    email.SetExtendedProperty(xExperimentalHeader, "Provision X-Experimental Internet message header");
    try
    {
        // The mapping of the named property happens in transport delivery.
        email.Send();
        if (service.ServerInfo.MajorVersion == 12)
        {
            Console.WriteLine("Provisioned the X-Experimental across the mailbox database that hosts the user's mailbox.");
        }
        else // For versions of Exchange starting with Exchange 2010
        {
            Console.WriteLine("Provisioned the X-Experimental for the user's mailbox. You will need to run this " +
                                "for each mailbox that needs to process this x-header.");
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error: {0}", ex.Message);
    }
}
```

## Provision an x-header by using EWS
<a name="bk_example1"> </a>

The following code example shows how to use the EWS [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) operation to create and send an email to provision a mailbox with an x-header. This is the XML request that is sent by the EWS Managed API when you [Provision an x-header by using the EWS Managed API](#bk_example1).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendOnly">
      <m:Items>
        <t:Message>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI DistinguishedPropertySetId="InternetHeaders"
                                PropertyName="X-Experimental"
                                PropertyType="String" />
            <t:Value>Provision X-Experimental Internet message header</t:Value>
          </t:ExtendedProperty>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>user@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

## Version differences
<a name="bk_example1"> </a>

The first time that you provision an x-header in Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange Server 2010, the value of a new custom x-header will not be written to the stored message. This is because the x-header must first be mapped to a named property in the user's mailbox. The mapping occurs upon the first request to add the named properties. When a subsequent request to create the named property occurs, the property and value are stored on the message. In Exchange 2007, the first time an x-header is written to a mailbox database, a mapping is created for the x-header to a named property across the mailbox database. When a subsequent request to create the named property occurs, the x-header is processed and stored for any mailbox in the Exchange 2007 database.
  
## Next steps
<a name="bk_example1"> </a>

This article shows you how to provision an x-header for a single mailbox by sending an email to a user. You can also provision an x-header for many users by [sending a batch email to a list of recipients](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md) in the caller's organization. 
  
## See also


- [Properties and extended properties in EWS in Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Exchange 2013: Provision custom X-headers programmatically](https://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [Named Properties, X-Headers, and You](https://blogs.technet.com/b/exchange/archive/2009/04/06/3407221.aspx)
    
- [Named Properties, Round 2: What lies Ahead](https://blogs.technet.com/b/exchange/archive/2009/06/12/3407672.aspx)
    
- [Header Firewall](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx)
    
- [EWS, MIME, and the missing Internet message headers](https://msdn.microsoft.com/library/office/hh545614%28v=exchg.140%29.aspx)
    
- [Process email messages in batches by using EWS in Exchange](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    

