---
title: "ResolveNames"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: c85207e1-1315-443b-94ec-2b58f405076b
description: "The ResolveNames element defines a request to resolve ambiguous names."
---

# ResolveNames

The **ResolveNames** element defines a request to resolve ambiguous names. 
  
```XML
<ResolveNames ReturnFullContactData="" SearchScope="" ContactDataShape="">
   <ParentFolderIds/>
   <UnresolvedEntry/>
</ResolveNames>
```

 **ResolveNamesType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ReturnFullContactData** <br/> |Describes whether the full contact details for public contacts for a resolved name are returned in the response. This attribute is required for public contacts. This value does not affect private contacts and private distribution lists, for which [ItemId](itemid.md) is always returned.  <br/> |
|**SearchScope** <br/> |Identifies the order and scope for a ResolveNames search.  <br/> |
|ContactDataShape  <br/> |Identifies the property set returned for contacts. This attribute was introduced in Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
   
#### ReturnFullContactData attribute values

|**Value**|**Description**|
|:-----|:-----|
|True  <br/> |Full contact details for public contacts are returned.  <br/> |
|False  <br/> |Full contact details for public contacts are not returned.  <br/> |
   
#### SearchScope attribute values

|**Value**|**Description**|
|:-----|:-----|
|ActiveDirectory  <br/> |Only the Active Directory directory service is searched.  <br/> |
|ActiveDirectoryContacts  <br/> |Active Directory is searched first, and then the contact folders that are specified in the [ParentFolderIds](parentfolderids.md) property are searched.  <br/> |
|Contacts  <br/> |Only the contact folders that are identified by the [ParentFolderIds](parentfolderids.md) property are searched.  <br/> |
|ContactsActiveDirectory  <br/> |Contact folders that are identified by the [ParentFolderIds](parentfolderids.md) property are searched first and then Active Directory is searched.  <br/> |
   
#### ContactDataShape attribute values

|**Value**|**Description**|
|:-----|:-----|
|IdOnly  <br/> |The contact item identifier property is returned.  <br/> |
|Default  <br/> |The Default set of contact item properties is returned. For more information, see [Response shapes in EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).  <br/> |
|AllProperties  <br/> |The AllProperties set of contact item properties are returned. For more information, see [Response shapes in EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).  <br/> |
   
### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ParentFolderIds](parentfolderids.md) <br/> |Contains an array of contact folder identifiers that would be searched if the **SearchScope** attribute is set to ActiveDirectoryContacts, Contacts, or ContactsActiveDirectory. The ParentFolderIds array can only contain a single contact folder identifier. If the **ParentFolderIds** element is not present, the default Contacts folder is searched.  <br/> The folder identifier can be used for delegate access.  <br/> Active Directory searches are performed by using access control lists (ACLs). Some users might not have the rights to see some Active Directory objects.  <br/> This element is optional.  <br/> |
|[UnresolvedEntry](unresolvedentry.md) <br/> |Contains the name of a contact or distribution list to resolve.  <br/> |
   
### Parent elements

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
## Element information

|**Name**|**Value**|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema name  <br/> |Messages schema  <br/> |
|Validation file  <br/> |Messages.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

- [ResolveNames operation](resolvenames-operation.md)
  
- [ResolveNamesType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesType.aspx)
  
- [ResolveNamesSearchScopeType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesSearchScopeType.aspx)

- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

- [Using Name Resolution](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)
