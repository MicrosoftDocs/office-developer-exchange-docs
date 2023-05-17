---
title: "FindFolder operation" 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- FindFolder
api_type:
- schema
ms.assetid: 7a9855aa-06cc-45ba-ad2a-645c15b7d031
description: "The FindFolder operation uses Exchange Web Services to find subfolders of an identified folder and returns a set of properties that describe the set of subfolders."
---

# FindFolder operation

The **FindFolder** operation uses Exchange Web Services to find subfolders of an identified folder and returns a set of properties that describe the set of subfolders.
  
FindFolder returns only the first 512 bytes of any streamable property. For Unicode, it returns the first 255 characters by using a null-terminated Unicode string.
  
Deep traversal queries cannot be performed on public folders.
  
Restrictions are permitted and should use only the folder properties, not the item properties. Sorting functionality is not available for **FindFolder** responses. Grouped queries are not available for **FindFolder** queries.
  
> [!NOTE}
> The **FindFolder** operation is also used to find managed folders.
  
## SOAP Headers

The **FindFolder** operation can use the SOAP headers that are listed and described in the following table.
  
|**Header**|**Element**|**Description**|
|:-----|:-----|:-----|
|Impersonation |[ExchangeImpersonation](exchangeimpersonation.md) |Identifies the user whom the client application is impersonating. |
|MailboxCulture |[MailboxCulture](mailboxculture.md) |Identifies the RFC3066 culture to be used to access the mailbox. |
|RequestVersion |[RequestServerVersion](requestserverversion.md) |Identifies the schema version for the operation request. |
|ServerVersion |[ServerVersionInfo](serverversioninfo.md) |Identifies the version of the server that responded to the request. |
|TimeZoneContext |[TimeZoneContext](timezonecontext.md) |Identifies the time zone to be used for all responses from the server. |
  
## FindFolder request example

The following example of a **FindFolder** request shows how to form a request to find all the folders located in an Inbox.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

Using the Default value for the [BaseShape](baseshape.md), the response returns the folder name, the folder ID, the number of subfolders, the number of child folders found in the folder, and the count of unread items.
  
### FindFolder request elements

This **FindFolder** request includes the following elements:
  
- [FindFolder](findfolder.md)
- [FolderShape](foldershape.md)
- [BaseShape](baseshape.md)
- [ParentFolderIds](parentfolderids.md)
- [DistinguishedFolderId](distinguishedfolderid.md)

 For additional **FindFolder** request elements, see the schema.
  
## FindFolder response example

The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **FindFolder** request. The response contains the elements that are returned when the Default value for the [BaseShape](baseshape.md) is used.
  
> [!NOTE]
> The folder ID and the change key have been shortened to preserve readability.

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Folders>
              <t:Folder>
                <t:FolderId Id="AQAnAH" ChangeKey="AQAAABY" />
                <t:DisplayName>TestFolder</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </FindFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### FindFolder response elements

The properties that are returned in the response are determined by the [BaseShape](baseshape.md) and the [AdditionalProperties](additionalproperties.md) if they are used. A successful **FindFolder** response includes the following elements:
  
- [ServerVersionInfo](serverversioninfo.md)
- [FindFolderResponse](findfolderresponse.md)
- [ResponseMessages](responsemessages.md)
- [FindFolderResponseMessage](findfolderresponsemessage.md)
- [ResponseCode](responsecode.md)
- [RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md)
- [Folders](folders-ex15websvcsotherref.md)
- [Folder](folder.md)
- [FolderId](folderid.md)
- [DisplayName (string)](displayname-string.md)
- [TotalCount](totalcount.md)
- [ChildFolderCount](childfoldercount.md)
- [UnreadCount](unreadcount.md)
  
**FindFolder** responses to a request with the **AllProperties** response shape will not return the [TotalCount](totalcount.md) and [UnreadCount](unreadcount.md) elements for public folder searches.
  
## FindFolder Error response example

The following SOAP body example shows an error response that occurs when you search for a folder that is identified by a malformed folder identifier.
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </FindFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### FindFolder error response elements

The **FindFolder** error response includes the following elements:
  
- [FindFolderResponse](findfolderresponse.md)
- [ResponseMessages](responsemessages.md)
- [MessageText](messagetext.md)
- [ResponseCode](responsecode.md)
- [DescriptiveLinkKey](descriptivelinkkey.md)
  
## Additional Information

- The folder [DisplayName (string)](displayname-string.md) element is always included in the default shape.
- The [UnreadCount](unreadcount.md) element is included in Tasks and Notes folders.
- Use the **PropertyTag** value of 0x672D with a property type of **Integer** to identify a managed folder by using the [ExtendedFieldURI](extendedfielduri.md) element.
  
## See also

[Finding Folders](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
