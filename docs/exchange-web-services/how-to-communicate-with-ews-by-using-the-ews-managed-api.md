---
title: "Communicate with EWS by using the EWS Managed API"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: d1b78293-da02-413a-875c-681e99146af3
description: "Find information about how to use the EWS Managed API to communicate with EWS in Exchange."
localization_priority: Priority
---

# Communicate with EWS by using the EWS Managed API

Find information about how to use the EWS Managed API to communicate with EWS in Exchange.

> [!NOTE]
> We’re removing the ability to use Basic authentication in Exchange Online for EWS beginning October 2022 [Deprecation of Basic authentication in Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). You should use OAuth authentication instead. [Authenticate an EWS application by using OAuth](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth)
  
The [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) class in the EWS Managed API contains the methods and properties that you use to set user credentials, identify the EWS endpoint, send and receive SOAP messages, and configure the binding to communicate with EWS. Before you can use the EWS Managed API to perform any task, you have to create an instance of the **ExchangeService** class and bind it to EWS.
  
After you set up an [ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx) object with user credentials and the EWS endpoint, any mailbox object that references the [ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx) object can use the following method types to communicate with EWS:
  
- ExchangeService object methods — All the methods on the **ExchangeService** object that are not inherited from the base **Object** type make calls to EWS.
- Exchange mailbox item and folder type methods.

**Table 1. Mailbox item and folder type methods that communicate with EWS**

|Method|What it does|Operations that it calls|
|:-----|:-----|:-----|
|[Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.load%28v=exchg.80%29.aspx) <br/> |Gets properties on an item, attachment, or user configuration object.  <br/> |[GetItem operation](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/><br/> [GetAttachment operation](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) <br/><br/> [GetUserConfiguration operation](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |
|[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |Populates a new item on the client with information from an existing item on the server.  <br/> |[GetItem operation](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|[Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) <br/> |Saves the copy of the client item on the server.  <br/> |[UpdateItem operation](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/> [UpdateFolder operation](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/><br/>[CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/><br/>[CreateFolder operation](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|[Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> |Updates the server with the changes made on the client.<br/><br/>For items and folders, the **Update** method uses the [UpdateItem operation](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) and the [UpdateFolder operation](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx).  <br/> |[UpdateItem operation](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/>[UpdateFolder operation](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|[Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> |Deletes an item on the server.<br/><br/>For items and folders, the **Delete** method uses the and the [DeleteFolder operation](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx).  <br/> |[DeleteItem operation](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/><br/> [DeleteFolder operation](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
|[Copy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> |Creates a copy of the item or folders on the server.  <br/> |[CopyItem operation](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/><br/> [CopyFolder operation](https://msdn.microsoft.com/library/c7ea0d68-9793-4144-b378-d99536776db9%28Office.15%29.aspx) <br/> |
|[Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> |Moves items or folders on the server.  <br/> |[MoveItem operation](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/><br/> [MoveFolder operation](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |

## To use the EWS Managed API to communicate with EWS

1. Instantiate the **ExchangeService** class.

   ```csharp
    ExchangeService service = new ExchangeService();
   ```

   > [!NOTE]
   > Instantiating **ExchangeService** with an empty constructor will create an instance that is bound to the latest known version of Exchange. Alternatively, you can target a specific version of Exchange by specifying version as a parameter. `ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);`
  
2. Set the credentials of the user who sends requests to the Exchange server. If you want to connect to EWS from a computer that is logged on to the domain, using the credentials of the authenticated user, set the **UseDefaultCredentials** property on the **ExchangeService** object to **true**.

   ```cs
    // Connect by using the default credentials of the authenticated user.
    service.UseDefaultCredentials = true;
   ```

   If you do not want to connect by using the default user credentials, set the **Credentials** property on the **ExchangeService** object to explicitly specify the credentials of a different user. If you are using Exchange Online or Exchange Online as part of Office 365, you'll use basic authentication, with just a user name and password. A domain name is required for NTLM authentication.

   ```cs
    // Connect by using the credentials of user1 at contoso.com.
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

   You can also specify the credentials of the user by using the user's domain name and password.

   ```cs
    // Connect by using the credentials of contoso/user1.
    service.Credentials = new WebCredentials("user1", "password", "contoso");
   ```

   > [!NOTE]
   > If the **UseDefaultCredentials** property is set to **true**, the value of the **Credentials** property is ignored.
  
3. Set the URL of the EWS endpoint. This URL locates the exchange.asmx file on Client Access server.

   ```cs
    // Use Autodiscover to set the URL endpoint.
    service.AutodiscoverUrl("user1@contoso.com");
   ```

   > [!NOTE]
   >  Although you can explicitly set the **Url** property of the **ExchangeService** to a hardcoded value, we recommend that you use the Autodiscover service instead, for the following reasons:
   >
   >  - Autodiscover determines the best endpoint for a given user (the endpoint that is closest to the user's Mailbox server).
   >  - The EWS URL might change if new Client Access servers are deployed. In this scenario, using [Autodiscover](autodiscover-for-exchange.md) means no code changes are necessary. 
   >  - You should either set the URL explicitly or call **AutodiscoverUrl**, but you should not do both.
  
## See also

- [Get started with EWS Managed API client applications](get-started-with-ews-managed-api-client-applications.md)
- [Use Autodiscover to find connection points](how-to-use-autodiscover-to-find-connection-points.md)
- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)
