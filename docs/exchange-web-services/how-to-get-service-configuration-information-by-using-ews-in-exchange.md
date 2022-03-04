---
title: "Get service configuration information by using EWS in Exchange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9379740a-96e1-490d-a229-0f9937c548d2
description: "Find out how to get service configuration information for UM, policy nudges, mail tips, and protection rules from EWS in Exchange."
---

# Get service configuration information by using EWS in Exchange

Find out how to get service configuration information for UM, policy nudges, mail tips, and protection rules from EWS in Exchange.
  
Does your EWS application work with Unified Messaging (UM), policy nudges, mail tips, or protection rules? If so, your application will need to call the [GetServiceConfiguration operation](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to get the service configuration information that it needs. The **GetServiceConfiguration** operation returns configuration information that is specific to each of these EWS features. 
  
> [!NOTE]
> The EWS Managed API does not implement this functionality. 
  
**Table 1. Configuration information that the GetServiceConfiguration operation returns**

|EWS feature|GetServiceConfiguration operation returns…|
|:-----|:-----|
|UM  <br/> | <ul><li>A value that indicates whether UM is enabled.</li><li>A value that indicates whether play on phone is enabled.</li><li>The play on phone dial string.</li></ul> |
|Policy nudges  <br/> | <ul><li>Policy nudges for display in your client.</li></ul> |
|Mail tips  <br/> | <ul><li>A value that indicates whether mail tips are enabled.</li><li>The maximum number of recipients per request.</li><li>The maximum message size.</li><li>The large audience threshold.</li><li>A value that indicates whether the number of external recipients is shown.</li><li>A list of internal domains.</li><li>A value that indicates whether policy tips are enabled.</li><li>The large audience cap threshold for indicating whether your mail is considered to have a large number of recipients.  </li></ul>|
|Protection rules  <br/> | <ul><li>Protection rules setup for your client.</li><li>A list of domains that are internal to your organization.  </li></ul> |
   
## Code example: Get service configuration information for mail tips by using EWS

The following code example uses the [GetServiceConfiguration operation](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to request service configuration information for mail tips. You can request additional service configuration information by adding more [ConfigurationName](https://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) elements with different values. 
  
```cs
private static void GetServiceConfiguration(ExchangeService service, NetworkCredential creds)
{ 
  // XML for the GetServiceConfiguration request SOAP envelope for mail tips configuration information.
  const string getServiceConfigurationRequest = 
    "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
    "<soap:Envelope xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\"\n" +
    "               xmlns:m=\"http://schemas.microsoft.com/exchange/services/2006/messages\"\n" +
    "               xmlns:t=\"http://schemas.microsoft.com/exchange/services/2006/types\" \n" +
    "               xmlns:soap=\"http://schemas.xmlsoap.org/soap/envelope/\"\n" +
    "               xmlns:xs=\"http://www.w3.org/2001/XMLSchema\">\n" +
    "  <soap:Header>\n" +
    "    <t:RequestServerVersion Version=\"Exchange2013\" />\n" +
    "  </soap:Header>\n" +
    "  <soap:Body>\n" +
    "    <m:GetServiceConfiguration>\n" +
    "      <m:ActingAs>\n" +
    "        <t:EmailAddress>user1@contoso.com</t:EmailAddress>\n" +
    "        <t:RoutingType>SMTP</t:RoutingType>\n" +
    "      </m:ActingAs>\n" +
    "      <m:RequestedConfiguration>\n" +
    "        <m:ConfigurationName>MailTips</m:ConfigurationName>\n" +
    "      </m:RequestedConfiguration>\n" +
    "    </m:GetServiceConfiguration>\n" +
    "  </soap:Body>\n" +
    "</soap:Envelope>";
  // Encoded GetServiceConfiguration operation request.
  byte[] payload = System.Text.Encoding.UTF8.GetBytes(getServiceConfigurationRequest);
  try
  {
    HttpWebRequest request = (HttpWebRequest)WebRequest.Create(service.Url);
    request.AllowAutoRedirect = false;
    request.Credentials = creds;
    request.Method = "POST";
    request.ContentType = "text/xml";
    Stream requestStream = request.GetRequestStream();
    requestStream.Write(payload, 0, payload.Length);
    requestStream.Close();
    HttpWebResponse response = (HttpWebResponse)request.GetResponse();
    if (response.StatusCode == HttpStatusCode.OK)
    {
      Stream responseStream = response.GetResponseStream();
      StreamReader reader = new StreamReader(responseStream);
      string responseFromServer = reader.ReadToEnd();
      Console.WriteLine("You will need to parse this response to get the configuration information:\n\n" + responseFromServer);
      reader.Close();
      responseStream.Close();
    }
    else
      throw new WebException(response.StatusDescription);
          
  }
  catch (WebException e)
  {
    Console.WriteLine(e.Message);
  }
}

```

## Next steps

After you request service configuration information, use the [XmlDocument class](https://msdn.microsoft.com/library/system.xml.xmldocument.aspx) to load the response XML so that you can parse it. Then, depending on your scenario, you can do one of the following: 
  
- Use the [GetMailTips operation](https://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) to get mail tips for client applications to display to users. 
    
- If UM is enabled, [learn about how to play mailbox items](https://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) over your phone. 
    
## See also

- [Configuration options for EWS in Exchange](configuration-options-for-ews-in-exchange.md)    
- [Setting up your EWS application](setting-up-your-ews-application.md)    
- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)
    

