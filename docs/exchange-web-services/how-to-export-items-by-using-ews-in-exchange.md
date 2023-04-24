---
title: "Export items by using EWS in Exchange"
 
 
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
 
 
ms.assetid: e93ee68c-e134-4469-9070-fba404d46cb4
description: "Learn how to export appointments, emails, contacts, tasks, and other items by using the EWS Managed API or EWS in Exchange."
localization_priority: Priority
---

# Export items by using EWS in Exchange

Learn how to export appointments, emails, contacts, tasks, and other items by using the EWS Managed API or EWS in Exchange.
  
You can export items from Exchange by using the EWS Managed API or EWS in a number of different ways. The option you use depends on:
  
- The item type that is exported.
    
- The degree of fidelity that you want maintained between the item state in Exchange and the exported item.
    
- The format of the exported item.
    
- Any post-processing requirements.
    
- Whether you want to import the item back into Exchange.
    
This article shows you how to use each of the different options to export items. You can use any option to batch export items out of Exchange.
  
## Export an item into a custom format
<a name="bk_exportcustom"> </a>

You can use the results of an [Item.Bind](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) EWS Managed API method call or parse the results of a [GetItem](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) EWS operation into a format that works with your application requirements. Use this option when you are exporting items in order to import them into a database, .csv file, or another format or system. You can even save the item in the form of the item EWS XML, which can be useful because many systems have XML parsing capability. We recommend that you use the **Item.Bind** method or the **GetItem** operation (without the [Item.MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) property) because this option gives you control over which properties are exported. 
  
## Export items with full fidelity
<a name="bk_exportfullfidelity"> </a>

If you want to export items with full fidelity, you can use the [ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) EWS operation. The **ExportItems** operation exports each item as a data stream. This data stream is not for parsing, but can be used as an item-level backup that can be imported back into an Exchange mailbox. You can include many items in each **ExportItems** request, although we recommend that you include no more than 100 items in each call. Because the EWS Managed API does not implement the **ExportItems** operation, if you use the EWS Managed API, you'll need to write a routine to send the web requests. You can optionally use the [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method to get metadata about the item so that you can index and store information about the data stream. 
  
We recommend that you use the **ExportItems** operation to export items that you plan to import into an Exchange mailbox. 
  
The following example shows how to use the **ExportItems** operation. In this example, the item identifier is shortened for readability. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013"/>
  </soap:Header>
  <soap:Body>
    <m:ExportItems>
      <m:ItemIds>
        <t:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA="/>
      </m:ItemIds>
    </m:ExportItems>
  </soap:Body>
</soap:Envelope>
```

The server responds to the **ExportItems** request with an [ExportItemsResponse](https://msdn.microsoft.com/library/ef44354b-fbdb-4f7c-b6bd-b27f56a1d018%28Office.15%29.aspx) element that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the item was successfully exported. The response also includes the item ID of the exported item and the data stream that contains the exported content. The following example shows the SOAP body that contains the exported item.
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <m:ExportItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
    <m:ResponseMessages>
      <m:ExportItemsResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA=" ChangeKey="FwAAAA=="/>
        <m:Data>
          AQAAAAgAAAAAAAAALgBlAHgAdABlAHMAdAAuAG0AaQBjAHIAbwBzAG8AZgB0AC4A
          cgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUAeAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMA
          bwBmAHQALgBjAG8AbQAAAAMAADkAAAAAAwD+DwYAAAADAARAAwACQAMADkA=
        </m:Data>
      </m:ExportItemsResponseMessage>
     </m:ResponseMessages>
  </m:ExportItemsResponse>
</s:Body>
```

## Use the MIME stream to export into common file formats
<a name="bk_exportfullfidelity"> </a>

You can use the [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) EWS Managed API method or the [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS operation to get a MIME representation of an item. Because Exchange doesn't store the MIME content of each item, it has to convert the database representation of each item into the MIME stream. Because this conversion is costly, we do not recommend that you request the MIME stream for items on a large scale. Also note that the MIME stream contains a limited set of properties; you might have to consider other options if the property set doesn't contain the properties you need. 
  
### Use the EWS Managed API to export an email into an .eml and .mht file by using the MIME stream
<a name="bk_exportemailmime"> </a>

Outlook and other common email applications can open the EML (.eml) file format. The following example shows you how you can export an email by using the MIME stream, and use the MIME stream to create an EML and a MIME HTML (.mht) file. Many web browsers support the MIME HTML file format. This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server. 
  
```cs
private static void ExportMIMEEmail(ExchangeService service)
{
    Folder inbox = Folder.Bind(service, WellKnownFolderName.Inbox);
    ItemView view = new ItemView(1);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly);
    // This results in a FindItem call to EWS.
    FindItemsResults<Item> results = inbox.FindItems(view);
    foreach (var item in results)
    { 
        PropertySet props = new PropertySet(EmailMessageSchema.MimeContent);
        // This results in a GetItem call to EWS.
        var email = EmailMessage.Bind(service, item.Id, props);
                
        string emlFileName = @"C:\export\email.eml";
        string mhtFileName = @"C:\export\email.mht";
        // Save as .eml.
        using (FileStream fs = new FileStream(emlFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
        // Save as .mht.
        using (FileStream fs = new FileStream(mhtFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
    }
}
```

### Use the EWS Managed API to export an appointment into an iCal file by using the MIME stream
<a name="bk_exporticalmime"> </a>

Outlook and other common calendar applications can open the iCal (.ics) file format. The following example shows you how to export an appointment by using the MIME stream, and use the MIME stream to create an iCal file. Note that many properties are not exported with the MIME stream, including attendees and attachment-related properties. You can capture other properties from EWS by requesting them and saving them in the iCal file as private extensions. These private extensions are prefixed with "x-". 
  
This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server. This example also assumes that you have an appointment with the subject "2015 Financial Projections" in the calendar folder. 
  
```cs
private static void ExportMIMEAppointment(ExchangeService service)
{
    Folder inbox = Folder.Bind(service, WellKnownFolderName.Calendar);
    ItemView view = new ItemView(1);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly); 
    // This results in a FindItem call to EWS.
    FindItemsResults<Item> results = inbox.FindItems("subject:'2015 Financial Projections'", view);
    foreach (var item in results)
    {
        PropertySet props = new PropertySet(AppointmentSchema.MimeContent);
        // This results in a GetItem call to EWS.
        var email = Appointment.Bind(service, item.Id, props);
        string iCalFileName = @"C:\export\appointment.ics";
        // Save as .ics.
        using (FileStream fs = new FileStream(iCalFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
    }
}
```

### Use the EWS Managed API to export a contact into a vCard file by using the MIME stream
<a name="bk_exportvcardmime"> </a>

Outlook and other common contact management applications can open the vCard (.vcf) file format. The following example shows you how to export a contact by using the MIME stream, and use the MIME stream to create a vCard. You can capture other properties from EWS by requesting them and saving them in the . vCard as private extensions. These extensions are prefixed with "x-". 
  
This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server. 
  
```cs
private static void ExportMIMEContact(ExchangeService service)
{
    Folder inbox = Folder.Bind(service, WellKnownFolderName.Contacts);
    ItemView view = new ItemView(1);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly);
    // This results in a FindItem call to EWS.
    FindItemsResults<Item> results = inbox.FindItems(view);
    foreach (var item in results)
    {
        PropertySet props = new PropertySet(ContactSchema.MimeContent);
        // This results in a GetItem call to EWS.
        var email = Contact.Bind(service, item.Id, props);
        string vcfFileName = @"C:\export\contact.vcf";
        // Save as .vcf.
        using (FileStream fs = new FileStream(vcfFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
    }
}
```

> [!NOTE]
> You cannot import vCard files by using the **MimeContent** property. You can import contacts by using the [Contact.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) EWS Managed API method or the [CreateItem](https://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx) EWS operation. 
  
### Use EWS to export any item by using the MIME stream
<a name="bk_exportewsmime"> </a>

Use the **GetItem** operation to get the MIME stream of an item. The following **GetItem** request shows how to request the MIME content of an item. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkADEzYjJkLTYxMwB8GqYicWAAA=" ChangeKey="CQAAABzXv"/>
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

The following example shows the response to a request to get the MIME stream. The MIME stream has been shortened for readability.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="893" 
                         MinorBuildNumber="17" 
                         Version="V2_10" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:MimeContent CharacterSet="UTF-8">UmVjZ6IGZyb2b2suY29y5hMzgwZTA1YtDQo=</t:MimeContent>
              <t:ItemId Id="AAMkADEzYjJkLTYxMwB8GqYicWAAA=" ChangeKey="CQAAABzXv"/>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

 
<a name="bk_exportfullfidelity"> </a>

After exporting items, you might want to [import items into Exchange](how-to-import-items-by-using-ews-in-exchange.md).
  
## See also


- [Exporting and importing items by using EWS in Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [Import items by using EWS in Exchange](how-to-import-items-by-using-ews-in-exchange.md)
    
- [Folders and items in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [Mailbox synchronization and EWS in Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    

