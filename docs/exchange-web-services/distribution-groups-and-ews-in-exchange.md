---
title: "Distribution groups and EWS in Exchange"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: fe08c2e3-92a0-43ec-bc61-69b14caee8fe
description: "Learn about the different types of distribution groups that are available in Exchange and how you can manage them in your EWS Managed API or EWS application."
---

# Distribution groups and EWS in Exchange

Learn about the different types of distribution groups that are available in Exchange and how you can manage them in your EWS Managed API or EWS application.
  
A distribution group is a collection of email addresses that are associated with a single alias or email address. Distribution groups (also sometimes called distribution lists) enable a user to send email to multiple people by using a single recipient address. Because distribution group membership, and therefore the message recipients, can be managed outside of individual email threads, distribution groups provide an excellent way to enable the distribution of mail to a group of users. You can programmatically create and manage distribution groups by using the EWS Managed API, EWS, and the Exchange Management Shell. Before you start programming, let's explore the different types of distribution groups that are available and your options for managing them.
  
## Types of distribution groups

Exchange supports three types of distribution groups:
  
- [Universal distribution groups](distribution-groups-and-ews-in-exchange.md#bk_DistributionGroup) — Active Directory universal distribution group objects that are mail-enabled. Universal distribution groups are used to distribute messages to a group of recipients. 
    
- [Security groups](distribution-groups-and-ews-in-exchange.md#bk_SecurityGroup) — Active Directory objects that are mail-enabled; also known as universal security groups. Security groups are used to assign access permissions to resources in Active Directory Domain Services (AD DS) as well as to distribute messages. 
    
- [Contact groups](distribution-groups-and-ews-in-exchange.md#bk_ContactGroup) — Private distribution groups that are located in a user's mailbox. 
    
The type of distribution group that you choose will depend on where you plan to store the distribution group, who will use it, and what it will be used for.

<a name="bk_DistributionGroup"> </a>

### Universal distribution groups

You can use universal distribution groups to consolidate groups of recipients into a single alias or email address. Because universal distribution groups are stored in AD DS, anyone can use them to send email, including users outside your organization. You can use the EWS Managed API or EWS to expand a distribution group, but to create and manage distribution groups, you'll need to use [Exchange Management Shell cmdlets](#bk_UsingEMS).
  
You can also use universal distribution groups to contain a collection of rooms; for example, to make it easier for users to find a conference room for a meeting. Users can add a room list — a universal distribution group that contains room resource mailboxes — to a meeting request to find an available room without having to add each room individually.
  
You can create a static universal distribution group that stays the same until you to update the membership, or you can create a dynamic universal distribution group. A dynamic universal distribution group queries Active Directory mail-enabled objects and builds the group membership based on the results. The group membership is recalculated whenever an email message is sent to the group. 

<a name="bk_SecurityGroup"> </a>

### Security groups

Universal distribution groups and security groups are identical in most ways. However, unlike universal distribution groups, you can use security groups to assign permissions to network resources in AD DS. You cannot use the EWS Managed API or EWS to create and manage security groups; instead, you use [Exchange Management Shell cmdlets](#bk_UsingEMS). But, just like universal distribution groups, you can use the EWS Managed API or EWS to expand security groups.

<a name="bk_ContactGroup"> </a>

### Contact groups

If you don't want to give every user administrative access to the server to create distribution groups, but you want to enable them to send a single message to a large collection of people, you can do this by using contact groups. A contact group does not have an email address associated with it, and it exists only in one user's mailbox; other users won't have access to it. You can [use the EWS Managed API or EWS to create contact groups](how-to-create-contact-groups-by-using-ews-in-exchange.md).
  
## Managing distribution groups by using the EWS Managed API or EWS

You can use the EWS Managed API or EWS to expand a universal distribution group or security group and to control the creation and management of a contact group; however, you cannot use these technologies to create or edit the members of those groups. 
  
**Table 1. EWS Managed API methods and EWS operations for managing distribution groups**

|**EWS Managed API method**|**EWS operation**|**Use to…**|
|:-----|:-----|:-----|
|[ContactGroup class](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) methods  <br/> |[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |Create a contact group in the Exchange store.<br/><br/>**NOTE**: You cannot create a universal distribution group or security group by using EWS Managed API or EWS.           |
|[ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) <br/> |[ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) <br/> |Expand a universal distribution group, security group, or contact group by retrieving a list of its members.  <br/> |
|[FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |Search for contact groups in the mailbox.  <br/> |
|[GetRooms](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) <br/> |[GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) <br/> |Retrieve a collection of all rooms in a specified room list in an organization. A room list is a distribution group that only contains room resource mailboxes.  <br/> |
|[ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |Search for and return possible candidates to match an ambiguous name. The candidates can be distribution groups.  <br/> |
   
You can use the information returned by the [ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) method or the [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) operation to determine what types of members are in the group. The member types are defined by the [MailboxType](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.mailboxtype%28v=exchg.80%29.aspx) EWS Managed API enumeration and the [MailboxType](https://msdn.microsoft.com/library/696e5fdb-d8c5-40f0-9e79-885eae65dfa4%28Office.15%29.aspx) EWS element. 
  
**Table 2. Distribution group member types**

|**MailboxType enumeration value**|**MailboxType element value**|**Description**|
|:-----|:-----|:-----|
|Mailbox  <br/> |Mailbox  <br/> |A mail-enabled Active Directory object.  <br/> |
|PublicGroup  <br/> |PublicDL  <br/> |A distribution group contained within the group you just expanded. To get a full list of members, expand this group as well.  <br/> |
|ContactGroup  <br/> |PrivateDL  <br/> |A group of contacts that is located in the mailbox and is only available to users of that mailbox.  <br/> |
|Contact  <br/> |Contact  <br/> |An Exchange database contact or Active Directory mail contact.  <br/> |

<a name="bk_UsingEMS"> </a>

## Managing distribution groups by using the Exchange Management Shell

You can [use Exchange Management Shell cmdlets](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx) to create and manage universal distribution groups and security groups in your code. 
  
> [!NOTE]
> You cannot use Exchange Management Shell cmdlets to manage contact groups. 
  
**Table 3. Exchange Management Shell cmdlets for working with distribution groups**

|**Cmdlet**|**Use to…**|
|:-----|:-----|
|[Disable-DistributionGroup](https://technet.microsoft.com/library/aa997942%28v=exchg.150%29.aspx) <br/> |Remove mail capabilities from a mail-enabled distribution group.  <br/> |
|[Enable-DistributionGroup](https://technet.microsoft.com/library/aa998916%28v=exchg.150%29.aspx) <br/> |Mail-enable an existing universal group.  <br/> |
|[Get-DistributionGroup](https://technet.microsoft.com/library/bb124755%28v=exchg.150%29.aspx) <br/> |Query for existing distribution groups.  <br/> |
|[New-DistributionGroup](https://technet.microsoft.com/library/aa998856%28v=exchg.150%29.aspx) <br/> |Create a distribution group.  <br/> |
|[Remove-DistributionGroup](https://technet.microsoft.com/library/aa997627%28v=exchg.150%29.aspx) <br/> |Delete an existing distribution group from AD DS.  <br/> |
|[Set-DistributionGroup](https://technet.microsoft.com/library/bb124955%28v=exchg.150%29.aspx) <br/> |Modify the settings of an existing distribution group.  <br/> |
|[Add-DistributionGroupMember](https://technet.microsoft.com/library/bb124340%28v=exchg.150%29.aspx) <br/> |Add a recipient to a distribution group.  <br/> |
|[Get-DistributionGroupMember](https://technet.microsoft.com/library/aa996367%28v=exchg.150%29.aspx) <br/> |Find existing distribution group members.  <br/> |
|[Remove-DistributionGroupMember](https://technet.microsoft.com/library/aa998016%28v=exchg.150%29.aspx) <br/> |Remove an existing recipient from a distribution group.  <br/> |
|[Update-DistributionGroupMember](https://technet.microsoft.com/library/dd335049%28v=exchg.150%29.aspx) <br/> |Update a member of a specified distribution group.  <br/> |
|[Get-DynamicDistributionGroup](https://technet.microsoft.com/library/bb124762%28v=exchg.150%29.aspx) <br/> |Retrieve the settings on an existing dynamic distribution group.  <br/> |
|[New-DynamicDistributionGroup](https://technet.microsoft.com/library/bb125127%28v=exchg.150%29.aspx) <br/> |Create a dynamic distribution group.  <br/> |
|[Remove-DynamicDistributionGroup](https://technet.microsoft.com/library/bb125038%28v=exchg.150%29.aspx) <br/> |Delete an existing dynamic distribution group. This cmdlet removes the dynamic distribution group from AD DS.  <br/> |
|[Set-DynamicDistributionGroup](https://technet.microsoft.com/library/bb123796%28v=exchg.150%29.aspx) <br/> |Modify the settings of an existing dynamic distribution group.  <br/> |

<a name="bk_UsingEMS"> </a>

## In this section

- [Create contact groups by using EWS in Exchange](how-to-create-contact-groups-by-using-ews-in-exchange.md)   
- [Expand distribution groups by using EWS in Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    
## See also

- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)   
- [Calling Exchange Management Shell Cmdlets from Managed Code](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx)
    

