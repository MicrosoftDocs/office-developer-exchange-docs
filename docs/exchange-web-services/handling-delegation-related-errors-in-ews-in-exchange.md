---
title: "Handling delegation-related errors in EWS in Exchange"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: 631d364f-e324-4838-a92c-820286f771f8
description: "Find out how to handle delegation-related errors in applications that you develop by using the EWS Managed API or EWS in Exchange."
---

# Handling delegation-related errors in EWS in Exchange

Find out how to handle delegation-related errors in applications that you develop by using the EWS Managed API or EWS in Exchange.
  
If your application uses delegation or adds or removes delegates, you might have to handle delegation-related errors. You can handle these errors at runtime, or while you are developing your EWS application. These errors are defined by the EWS Managed API [ServiceError](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) enumeration and the EWS [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element. 
  
## Delegation-related errors

|**Error**|**Occurs when you try to…**|**Handle it by…**|
|:-----|:-----|:-----|
|ErrorItemNotFound  <br/> ErrorFolderNotFound  <br/> |Perform an operation on a mailbox, folder, or item that you do not have access to.  <br/> |Updating the delegate's permissions to enable them to access the folder or item by calling the [UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) EWS Managed API method or the [UpdateDelegate](https://msdn.microsoft.com/library/03f618ac-ad1a-4772-9b81-c5bb0f12d6ab%28Office.15%29.aspx) EWS operation, and then retrying the request.  <br/> |
|ErrorAccessDenied  <br/> |Modify an item that you do not have sufficient privileges to modify.  <br/> |Updating your delegate permissions by calling the **UpdateDelegate** EWS Managed API method or the **UpdateDelegate** EWS operation, and then retrying the request.  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |Attempt to add the mailbox owner as a delegate to their own mailbox.  <br/> |[Adding a different user as a delegate](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md), not the mailbox owner.  <br/> |
|ErrorDelegateAlreadyExists  <br/> |Add the delegate when the delegate already exists.  <br/> |Doing nothing, because the delegate already exists for the mailbox owner. Or, if you're trying to change the permissions of an existing delegate, then use the **UpdateDelegates** method or the **UpdateDelegate** operation.  <br/> |
|ErrorNotDelegate  <br/> |Modify delegate permissions for a user who has no delegate permissions for the mailbox.  <br/> |[Adding the user as a delegate](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) for the mailbox before attempting to update or remove their permissions.  <br/> |
|ErrorDelegateNoUser  <br/> |Modify delegate permissions for a user who is not in Active Directory Domain Service (AD DS).  <br/> |Creating the user in AD DS, or correcting the delegate information in the request.  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |Use a delegate to subscribe to notifications on behalf of the mailbox owner.  <br/> |Subscribing to notifications as the mailbox owner.  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |Make a request from a delegate that has a different server version than the principal's mailbox server.  <br/> |Using a delegate or adding a delegate whose mailbox has the same server version as the mailbox owner.  <br/> |
|ErrorMissingEmailAddress  <br/> |Make a request using a delegate account that does not have a mailbox.  <br/> |Adding a mailbox to the delegate's account.  <br/> |
   
## See also


- [Delegate access and EWS in Exchange](delegate-access-and-ews-in-exchange.md)
    
- [Tools and resources for troubleshooting EWS applications for Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

