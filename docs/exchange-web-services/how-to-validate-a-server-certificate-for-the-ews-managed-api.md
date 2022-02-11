---
title: "Validate a server certificate for the EWS Managed API"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 1fe0b215-8340-4bc8-a6ce-4f591ca9e353
description: "Learn how to create and reference a certificate validation callback method so that you can make EWS Managed API requests to an Exchange server."
localization_priority: Priority
---

# Validate a server certificate for the EWS Managed API

Learn how to create and reference a certificate validation callback method so that you can make EWS Managed API requests to an Exchange server.
  
By default, versions of Exchange starting with Exchange 2007 SP1 use self-signed X509 certificates to authenticate calls from EWS. When you are using the EWS Managed API, you need to create a certificate validation callback method; otherwise, EWS Managed API requests will fail. If you are using the Autodiscover service, the call to the EWS Managed API Autodiscover method will fail with an **AutodiscoverLocalException** error. If you are using a web-generated web service proxy, you might also have to create a validation callback method, depending on how the proxy is created.
  
## Prerequisites for creating a validation callback method

<a name="bk_prereq"> </a>

To set up to validate a server certificate, ensure that the following are true:
  
- Your Exchange server is using a self-signed certificate for EWS. If the administrator has installed a valid certificate that traces to a root certificate, you do not need to create a validation callback method.

- You are creating a managed application that includes a reference to the following required .NET Framework namespaces:

  - **System.Net**
  - **System.Net.Security**
  - **System.Security.Cryptography.X509Certificates**

## Example: Callback method to validate a server certificate for the EWS Managed API

<a name="bk_example"> </a>

The following code example shows how to create an X509 certificate validation callback method for the EWS Managed API. This method will validate an X509 certificate and only return true when either of the following criteria are met:
  
- The certificate is valid and traces back to a valid root certificate.
- The certificate is valid and is self-signed by the server that returned it.

> [!IMPORTANT]
> The certificate validation callback method in this example provides sufficient security for development and testing of EWS Managed API applications. However, it might not provide sufficient security for your deployed application. You should always make sure that the certificate validation callback method that you use meets the security requirements of your organization.
  
```cs
      private static bool CertificateValidationCallBack(
         object sender,
         System.Security.Cryptography.X509Certificates.X509Certificate certificate,
         System.Security.Cryptography.X509Certificates.X509Chain chain,
         System.Net.Security.SslPolicyErrors sslPolicyErrors)
    {
      // If the certificate is a valid, signed certificate, return true.
      if (sslPolicyErrors == System.Net.Security.SslPolicyErrors.None)
      {
        return true;
      }
      // If there are errors in the certificate chain, look at each error to determine the cause.
      if ((sslPolicyErrors &amp; System.Net.Security.SslPolicyErrors.RemoteCertificateChainErrors) != 0)
      {
        if (chain != null &amp;&amp; chain.ChainStatus != null)
        {
          foreach (System.Security.Cryptography.X509Certificates.X509ChainStatus status in chain.ChainStatus)
          {
            if ((certificate.Subject == certificate.Issuer) &amp;&amp;
               (status.Status == System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.UntrustedRoot))
            {
              // Self-signed certificates with an untrusted root are valid. 
              continue;
            }
            else
            {
              if (status.Status != System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.NoError)
              {
                // If there are any other errors in the certificate chain, the certificate is invalid,
             // so the method returns false.
                return false;
              }
            }
          }
        }
        // When processing reaches this line, the only errors in the certificate chain are 
    // untrusted root errors for self-signed certificates. These certificates are valid
    // for default Exchange server installations, so return true.
        return true;
      }
      else
      {
     // In all other cases, return false.
        return false;
      }
    }

```

You use the **ServicePointManager** class in the .NET **System.Net** namespace to hook up a validation callback method by setting the **ServerCertificateValidationCallback** property. You can use code similar to the following code example to set the **ServerCertificateValidationCallback** property.
  
```cs
ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;

```

## Next steps

<a name="bk_example"> </a>

After you have created the validation callback method for the EWS Managed API, you can use the Autodiscover service to get connection points and user and domain settings from an Exchange server. For more information, see the following articles:
  
- [Use Autodiscover to find connection points](how-to-use-autodiscover-to-find-connection-points.md)

- [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)

- [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)

- [Get domain settings from an Exchange server](how-to-get-domain-settings-from-an-exchange-server.md)

## See also

- [Setting up your EWS application](setting-up-your-ews-application.md)  
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
