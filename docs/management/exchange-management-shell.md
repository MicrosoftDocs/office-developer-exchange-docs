---
title: "Exchange Management Shell"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0
description: "Find information about how to use the Exchange Management Shell to develop tools for Exchange server administration."
---

# Exchange Management Shell

Find information about how to use the Exchange Management Shell to develop tools for Exchange server administration.
  
**Applies to:** Exchange Online | Exchange Server 2013 | Office 365
  
The Exchange Management Shell provides a rich set of commands, based on the Windows PowerShell platform, for managing Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013. You can use the Exchange Management Shell to create two kinds of tools: command-line scripts that work within the Windows PowerShell environment, and tools that use the Exchange Management Shell cmdlets through a managed interface. You can use managed applications to create a standard Windows or web-based UI to administer an Exchange server. 
  
## What you need to know about the Exchange Management Shell

|If you're wondering about|Read this|
|:-----|:-----|
|Availability  <br/> |Exchange Management Shell commands are installed on all servers running versions of Exchange starting with Exchange 2007.<br/>Client applications can be deployed on any computer running Windows PowerShell 2.0.<br/> For information about accessing the shell, see [Exchange Server PowerShell (Exchange Management Shell)](/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).  <br/> |
|Languages and tools  <br/> |You can create Exchange Management Shell scripts in any text editor.<br/>You can use one of many third-party tools for creating Windows PowerShell scripts that can be used with the Exchange Management Shell.  <br/> The [Exchange Management Shell object model](exchange-management-shell-namespaces.md) is based on the .NET Framework.<br/>You can use any .NET language to develop Exchange Management Shell applications.  <br/> |
|Available test and debug tools  <br/> |You can use one of many third-party applications to test and debug Exchange Management Shell scripts.  <br/> You can use Visual Studio and third-party tools to test and debug managed Exchange Management Shell applications.  <br/> |
|Server platform requirements  <br/> |You can use the Exchange Management Shell on any Exchange server that has Windows PowerShell 2.0 installed.  <br/> |
|Client platform requirements  <br/> |Exchange Management Shell client applications require Windows PowerShell 2.0.  <br/> |
|Permissions  <br/> |Running an Exchange Management Shell application requires that the user have role-based access control rights to the affected data on the Exchange store.<br/>For more information about role-based access control, see [Understanding Role Based Access Control](https://technet.microsoft.com/library/dd298183.aspx).  <br/> |
   
The articles in this section describe Exchange Management Shell features that are important for creating Exchange management tools. For information about planning, configuring, or maintaining Exchange, see the [Exchange](/exchange/) site.
  
## In this section

- [Create Exchange Management Shell tools](create-exchange-management-shell-tools.md)
    
- [Exchange Management Shell namespaces](exchange-management-shell-namespaces.md)
    
## See also
  
- [Windows PowerShell documentation](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-6)
- [PowerShell scripting](/powershell/scripting/overview?view=powershell-7.2)
