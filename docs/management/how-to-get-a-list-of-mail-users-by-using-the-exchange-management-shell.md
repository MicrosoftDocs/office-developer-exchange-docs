---
title: "Get a list of mail users by using the Exchange Management Shell"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.assetid: 8b790dc8-5c4f-4acf-bbe7-63523395fbe7
description: "Learn how to use Exchange Management Shell cmdlets to create a tool that returns a list of Exchange mailbox users."
localization_priority: Priority
---

# Get a list of mail users by using the Exchange Management Shell

Learn how to use Exchange Management Shell cmdlets to create a tool that returns a list of Exchange mailbox users.
  
**Applies to:** Exchange Online | Exchange Server 2013 | Office 365
  
Getting a list of users from Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013 by using a managed tool that calls an Exchange Management Shell cmdlet is a two-step process. First, you establish a remote runspace on an Exchange server; then, you run the cmdlet to retrieve the user information in the remote runspace.

To connect to the remote runspace, you have to authenticate with the Exchange server by using the authentication scheme that meets the security requirements of your organization.

This article provides code examples that you can use to set up a remote runspace and run an Exchange Management Shell cmdlet to get a list of users from an Exchange server.

## Prerequisites for getting a list of mailbox users

To perform this task, you need a reference to the following namespaces:
  
- **System.Collections.ObjectModel**
- **System.Management.Automation**
- **System.Management.Automation.Remoting**
- **System.Management.Automation.Runspaces**

> [!NOTE]
> When you are using Visual Studio to create an application, you must add a reference to the System.Management.Automation.dll assembly to the project. The assembly can be found in one of the following locations:
>
> - For Windows XP and Windows Vista operating systems, the Windows PowerShell installation directory ($PSHOME).
> - For the Windows 7 and Windows 8 operating systems, the following folder: Windows\assembly\GAC_MSIL\System.Management.Automation.
  
Do not load the Exchange 2013 Management snap-in into the runspace on computers that are running applications that automate Exchange Management Shell cmdlets. The application should instead create a remote runspace, as described later in this article.

## Connect to a remote runspace on an Exchange server

The method that you use to connect to a remote runspace to use an Exchange Management Shell cmdlet varies based on the authentication scheme that you are using. This section provides code examples that show how to connect to a remote runspace when you are using an authentication method listed in the following table.
  
|**Authentication method**|**Applies to**|**URI**|
|:-----|:-----|:-----|
|[Connect to a remote runspace on Exchange Online by using basic authentication](#connect-to-a-remote-runspace-on-exchange-online-by-using-basic-authentication) |Exchange Online servers |`https://outlook.office365.com/PowerShell-LiveID` <br/>`https://<server>/PowerShell-LiveID` |
|[Connect to a remote runspace by using certificate authentication](#connect-to-a-remote-runspace-by-using-certificate-authentication) |Exchange Online and Exchange on-premises servers |`https://outlook.office365.com/PowerShell` <br/>`https://<server>/PowerShell` <br/>`http://<server>/PowerShell` |
|[Connect to a remote runspace on an Exchange server by using Kerberos authentication](#connect-to-a-remote-runspace-on-an-exchange-server-by-using-kerberos-authentication) |Exchange Online and Exchange on-premises servers  |`https://<server>/PowerShell` <br/>`http://<server>/PowerShell` |

### Connect to a remote runspace on Exchange Online by using basic authentication

The following code example defines the **GetUsersUsingBasicAuth** method, which creates an Exchange Management Shell runspace on a remote Exchange Online server by using basic authentication. The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#get-a-list-of-mailbox-users-from-a-remote-runspace), to return a list of users on the remote server.
  
This method requires the following parameters:
  
- **liveIDConnectionUri** &ndash; A string that contains the URI of the Exchange Online server that will authenticate the application. If Exchange Online is running in Office 365, the URI is `https://outlook.office365.com/PowerShell-LiveID`; otherwise, the URI is `https://<servername>/PowerShell-LiveID`.
- **schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema. The schema URI is `https://schemas.microsoft.com/powershell/Microsoft.Exchange`.
- **credentials** &ndash; A [PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) object that contains the credentials of the user who is running the application.
- **count** &ndash; The number of Exchange mailbox users to return.

```cs
public Collection<PSObject> GetUsersUsingBasicAuth(
    string liveIDConnectionUri, string schemaUri, PSCredential credentials, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(liveIDConnectionUri),
        schemaUri, credentials);
    connectionInfo.AuthenticationMechanism = AuthenticationMechanism.Basic;
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```

```vb
  Function GetUsersUsingBasicAuth( _
    ByVal LiveIDConnectionUri As String, ByVal ScehmaUri As String, _
    ByVal Credentials As PSCredential, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo = _
        New WSManConnectionInfo(New Uri(LiveIDConnectionUri), ScehmaUri, Credentials)
    ConnectionInfo.AuthenticationMechanism = AuthenticationMechanism.Basic
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

### Connect to a remote runspace by using certificate authentication

The following code example defines the **GetUsersUsingCertificate** method, which creates an Exchange Management Shell runspace on a remote server by using a certificate. The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#get-a-list-of-mailbox-users-from-a-remote-runspace), to return a list of users on the remote server.
  
This method requires the following parameters:
  
- **thumbprint** &ndash; A string that contains the thumbprint of the certificate that is used to authenticate the application.
- **certConnectionUri** &ndash; A string that contains the URI of the server that will authenticate the certificate. The URI will be one of those listed in the following table.

    **Table 1. certConnectionUri URIs**

    |**Server**|**URI**|
    |:-----|:-----|
    |Exchange server without using SSL|`http://<servername>/PowerShell` |
    |Exchange server using SSL |`https://<servername>/PowerShell` |
    |Exchange Online as part of Office 365 |`https://outlook.office365.com/PowerShell` |

- **schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema. The schema URI is [https://schemas.microsoft.com/powershell/Microsoft.Exchange](https://schemas.microsoft.com/powershell/Microsoft.Exchange).
- **count** &ndash; The number of Exchange mailbox users to return.

```cs
public Collection<PSObject> GetUsersUsingCertificate(
    string thumbprint, string certConnectionUri, string schemaUri, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(certConnectionUri),
        schemaUri,
        thumbprint)
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```

```vb
  Function GetUsersUsingCertificate( _
    ByVal Thumbprint As String, ByVal CertConnectionUri As String, _
    ByVal SchemaUri As String, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo
    ConnectionInfo = New WSManConnectionInfo(New Uri(CertConnectionUri), SchemaUri, Thumbprint)
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

### Connect to a remote runspace on an Exchange server by using Kerberos authentication

The following code example defines the **GetUsersUsingKerberos** method, which creates an Exchange Management Shell runspace on a remote server by using Kerberos authentication. The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#get-a-list-of-mailbox-users-from-a-remote-runspace), to return a list of users on the remote server.
  
This method requires the following parameters:
  
- **kerberosUri** &ndash; A string that contains the URI of the Kerberos server that will authenticate the application. The URI will be one of those listed in the following table.

    **Table 2. kerberosUri URIs**

    |**Server**|**URI**|
    |:-----|:-----|
    |Exchange server without using SSL|`http://<servername>/PowerShell` |
    |Exchange server using SSL |`https://<servername>/PowerShell` |

- **schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema. The schema URI is [https://schemas.microsoft.com/powershell/Microsoft.Exchange](https://schemas.microsoft.com/powershell/Microsoft.Exchange).
- **credentials** &ndash; A [PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) object that contains the credentials of the user who is running the application.
- **count** &ndash; The number of Exchange mailbox users to return.

```cs
public Collection<PSObject> GetUsersUsingKerberos(
    string kerberosUri, string schemaUri, PSCredential credentials, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(kerberosUri),
        schemaUri, credentials);
    connectionInfo.AuthenticationMechanism = AuthenticationMechanism.Kerberos;
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```

```vb
  Function GetUsersUsingKerberos( _
    ByVal KerberosUri As String, ByVal ScehmaUri As String, _
    ByVal Credentials As PSCredential, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo = _
        New WSManConnectionInfo(New Uri(KerberosUri), ScehmaUri, Credentials)
    ConnectionInfo.AuthenticationMechanism = AuthenticationMechanism.Kerberos
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

## Get a list of mailbox users from a remote runspace

The following code example defines the **GetUserInformation** method, which returns a collection of [PSObject](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) instances that represent Exchange mailbox users. This method is called by the **GetUsersUsingBasicAuth**, **GetUsersUsingCertificate**, and **GetUsersUsingKerberos** methods to return the list of users from the remote server.
  
This method requires the following parameters:
  
- **count** &ndash; The number of Exchange mailbox users to return.
- **runspace** &ndash; The remote runspace that is established for the remote Exchange server.

```cs
public Collection<PSObject> GetUserInformation(int count, Runspace runspace)
{
    using (PowerShell powershell = PowerShell.Create())
    {
        powershell.AddCommand("Get-Users");
        powershell.AddParameter("ResultSize", count);
        runspace.Open();
        powershell.Runspace = runspace;
        return powershell.Invoke();
    }
}
```

```vb
Function GetUserInformation(ByVal Count As Integer, ByVal RemoteRunspace As Runspace) As Collection(Of PSObject)
    Dim RemotePowerShell As PowerShell = PowerShell.Create
    RemotePowerShell.AddCommand("Get-Users")
    RemotePowerShell.AddParameter("ResultSize", Count)
    ' Open the remote runspace on the server.
    RemoteRunspace.Open()
    ' Associate the runspace with the Exchange Management Shell.
    RemotePowerShell.Runspace = RemoteRunspace
    ' Invoke the Exchange Management Shell to run the command.
    Return RemotePowerShell.Invoke
End Function

```

The **GetUserInformation** method will return no more than _count_ mailbox users. To simplify the code for this example, the method does not filter or otherwise limit the mailbox users that are returned.
  
## See also

- [Create Exchange Management Shell tools](create-exchange-management-shell-tools.md)  
- [Use the Exchange Management Shell cmdlet response](how-to-use-the-exchange-management-shell-cmdlet-response.md)
