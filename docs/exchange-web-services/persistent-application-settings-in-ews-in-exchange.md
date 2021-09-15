---
title: "Persistent application settings in EWS in Exchange"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: 394d4e70-8517-4073-809a-5b61780ff923
description: "Learn about the different options that your EWS Managed API or EWS application can use to create persistent custom application settings in Exchange."
---

# Persistent application settings in EWS in Exchange

Learn about the different options that your EWS Managed API or EWS application can use to create persistent custom application settings in Exchange.
  

  
The easiest way to keep custom client configurations in sync for a mailbox, or folders and items in a mailbox, is to store application settings on an Exchange server. You can ensure that those settings persist for a mailbox by using one of the following: 
  
- User configuration objects
    
- Extended properties
    
- Custom items
    
## What are my options for creating persistent application settings?
<a name="Options"> </a>

User configuration objects are your best option for storing configuration settings for your EWS client applications. You can also use extend properties or custom items, or a combination of all three. Choose your option based on the scope of your settings and whether your settings need to be available to other applications.
  
**Table 1. Recommended options for creating persistent application settings based on scope**

|**Setting scope**|**Use…**|**Accessed by**|
|:-----|:-----|:-----|
|Item  <br/> |An extended property on an existing item.  <br/> |Any EWS application. Only EWS clients that know the property identifier can access an extended property.  <br/> |
|Folder  <br/> |A user configuration object on the target folder. This is a good way to save view settings for a folder.  <br/> |Any EWS application.  <br/> |
|Mailbox  <br/> |A user configuration object on the default msgrootfolder folder.  <br/> |Any EWS application.  <br/> |
   
### User configuration objects
<a name="UserConfig"> </a>

User configuration objects are special items that are associated with folders in a mailbox. User configuration objects, also known as folder associated items, are typically the best option for persisting application settings, especially if the configuration information is associated with a folder or a mailbox. They typically are not surfaced to end users. Because they can natively store data streams and data dictionaries, they are ideal for storing configuration information. The best way to use user configuration objects is to store a set of configurations in an XML document and then save that information in one of the user configuration stream properties.
  
User configuration objects are accessed differently than the other item types stored in a mailbox. You can use the [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=EXCHG.80%29.aspx) EWS Managed API method or the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation to find all items, but you must use the **Associated** search traversal option to find user configuration objects. The **Associated** search traversal indicates that the search results should contain only user configuration objects. EWS includes a set of operations that are specific to user configuration objects. 
  
**Table 1. EWS operations and EWS Managed API methods for working with user configuration objects**

|**In order to…**|**Use this EWS operation**|**Use this EWS Managed API method**|
|:-----|:-----|:-----|
|Create a user configuration object  <br/> |[CreateUserConfiguration operation](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) <br/> |[UserConfiguration.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) <br/> |
|Get a user configuration object  <br/> |[GetUserConfiguration operation](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |[UserConfiguration.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> [UserConfiguration.Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.load%28v=exchg.80%29.aspx) <br/> |
|Update a user configuration object  <br/> |[UpdateUserConfiguration operation](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) <br/> |[UserConfiguration.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> |
|Delete a user configuration object  <br/> |[DeleteUserConfiguration operation](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |
   
> [!NOTE]
> User configuration objects created by using EWS have an [ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) prefix that starts with "IPM.Configuration.". The **ItemClass** of a user configuration object is the user configuration object prefix and your user configuration object name. You can use the [Item.ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS Managed API property or the **ItemClass** EWS element to search for user configuration objects that you've defined. 
  
### Extended properties
<a name="ExtendedProperties"> </a>

Use [Extended properties](properties-and-extended-properties-in-ews-in-exchange.md) if you want to store configuration information on items. EWS, unlike MAPI, does not return a property bag for items. This means that an EWS client must know the extended property identifier in order to find and access the extended property. If you need to store configuration information on items other than user configuration objects, using extended properties to create custom properties might be the solution for you. Extended properties enable you to access and store information on properties that are not part of the standard property set for an item. 
  
> [!IMPORTANT]
> The Exchange database schema has a finite number of properties. The maximum number of property identifiers for an Exchange database is 32,767. If you are using extended properties to store many settings, we suggest that you use a single extended property to store those settings so that you don't exceed this maximum. 
  
You can use the [Item.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=EXCHG.80%29.aspx) EWS Managed API method or the [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS operation to set extended properties on user configuration objects. 
  
### Custom items
<a name="CustomItems"> </a>

Custom items can also be used to store information. The existing item properties can be repurposed to contain configuration information. Or, you can use extended properties to define your own properties for you application. Using custom items to store configuration provides the following benefits: 
  
- They work for all versions of Exchange that support EWS.
    
- If you don't use extended properties on the item, the budget of Exchange properties is not charged.
    
## Where should I store my application settings?
<a name="ApplicationSettingsLocation"> </a>

Mailbox folders and the items within them are located in the root message folder. This folder is identified by the [WellKnownFolderName.msgfolderroot](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) value in the EWS Managed API. In MAPI terms, this is the equivalent of the IPM subtree of a mailbox. User configuration objects are often used to create UI-based settings, so that an application can render view settings based on the folder that a user is accessing. Folder-based view settings are usually set on a user configuration object that is associated with the folder. But sometimes, you might want to make your settings global to your application. In this case, you can store your settings in the root message folder. 
  
Most users are not aware of and typically don't access the root mailbox folder. This folder is identified by the [WellKnownFolderName.root](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) value in the EWS Managed API. In MAPI terms, this is the equivalent of the non-IPM subtree of a mailbox. Information that end users don't access directly is stored in the root mailbox folder. You might want to store your application setting in this folder because client applications do not typically access it. 
  
## Version differences
<a name="VersionDifferences"> </a>

User configuration objects are available on Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2010.
  
## See also


- [Manage persistent application settings by using EWS in Exchange](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    
- [EWS client design overview for Exchange](ews-client-design-overview-for-exchange.md)
    
- [Properties and extended properties in EWS in Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Work with folders by using EWS in Exchange](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [Work with Exchange mailbox items by using EWS in Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    

