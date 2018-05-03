---
title: "Backup and restore for Exchange 2013"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 329902d9-0ecb-4cfb-86dd-5ce863deff3f
description: "Find information about creating backup and restore applications for Exchange 2013."
---

# Backup and restore for Exchange 2013

Find information about creating backup and restore applications for Exchange 2013.
  
 **Last modified:** September 17, 2015 
  
 * **Applies to:** Exchange Server 2013 * 
  
Exchange Server 2013 provides Database Availability Groups (DAGs), which help to keep stored data secure and available, and reduce the need for custom backup and restore applications. DAGs enable off-site data redundancy to help ensure that you won't lose data. However, many disaster recovery plans continue to include more traditional backup and restore methods and systems, including custom applications, for redundancy with the DAG. To help ensure data availability and redundancy in your organization, you can create custom applications that use Exchange Server and Windows Server operating system technologies to back up and restore your Exchange data.
  
## Backup technologies in Exchange 2013
<a name="bk_plugin"> </a>

Exchange 2013 includes a plug-in for Windows Server Backup that administrators can use to make VSS-based backups of Exchange data. Administrators can also use Windows Server Backup to back up and restore Exchange databases. If you are creating a backup and restore application for Exchange 2013, you need to create an Exchange-aware application that supports the VSS writer for Exchange 2013, and use the CHKSGFILES API to validate the consistency of that backup. For more information, see [How to: Validate backup integrity by using the CHKSGFILES API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013.md).
  
## VSS writer in Exchange 2013
<a name="bk_vsswriter"> </a>

Exchange 2013 introduces a significant change to the VSS writer architecture in Exchange Server 2010 and Exchange Server 2007. Exchange 2010 and Exchange 2007 include two VSS writers: one inside the Exchange Information Store service (store.exe) and one inside the Exchange Replication service (msexchangerepl.exe). In Exchange 2013, the VSS writer functionality is located in the Exchange Replication service. Your backup and restore application uses the new VSS writer, called the Microsoft Exchange Writer, to back up active and passive database copies, and to restore backed up database copies. Although the new VSS writer runs in the Exchange Replication service, the Exchange Information Store service must be running in order for the writer to be available. As a result, both services are required to back up or restore Exchange databases.
  
Although the VSS writer architecture was updated in Exchange 2013, the underlying functionality has not changed. If you created a backup and restore application for Exchange 2010, you do not need to make any changes to your application for Exchange 2013. Be sure to recompile your application with the latest files to ensure compatibility. For backup and restore applications created for Exchange 2007 or earlier versions, you will need to rewrite your code to use the latest CHKSGFILES API.
  
## What you need to know about VSS backup and restore
<a name="bk_vsswriter"> </a>

|**If you're wondering about…**|**Read this**|
|:-----|:-----|
|Application architectures  <br/> |Backup and restore applications that use VSS to back up Exchange databases typically consist of a background service that performs the backup, a scheduling service, and a Windows GUI application console that controls and configures the backup and restore system.  <br/> |
|Remote usage  <br/> |Applications that use VSS to back up Exchange servers must run on the Windows Server 2008 computer on which the Exchange store process is running. Because of the flexibility in large storage systems, the hardware hosting the storage volumes might not physically be part of the computer running Windows Server 2008.  <br/> |
|Languages and tools  <br/> |You can use any COM-compatible language to use VSS. It is most frequently used in applications written in C++. Because you have to take the Exchange store offline to create shadow copies, backup applications are typically time-sensitive, which in most cases makes using languages like Visual Basic or VBScript impractical.  <br/> |
|Managed implementation  <br/> |You can use the VSS APIs in a managed code environment via a COM Interop Assembly.  <br/> |
|Scriptable  <br/> |Yes, but not recommended.  <br/> |
|Available test and debug tools  <br/> |No special tools are required to debug applications that use the Windows VSS.  <br/> |
   
## In this section
<a name="bk_inthissection"> </a>

- [Backup and restore concepts for Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Build backup and restore applications for Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [CChkSGFiles class reference](cchksgfiles-class-reference.md)
    
## Additional resources
<a name="bk_addresources"> </a>

- [Volume Shadow Copy Service (Windows)](http://msdn.microsoft.com/en-us/library/windows/desktop/bb968832%28v=vs.85%29.aspx)
    
- [Explore the EWS Managed API, EWS, and web services in Exchange](http://msdn.microsoft.com/library/53553207-ff98-4fdb-8716-4ae02fee83bf%28Office.15%29.aspx)
    
- [Exchange Management Shell](http://msdn.microsoft.com/library/8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0%28Office.15%29.aspx)
    
- [Transport agents in Exchange 2013](http://msdn.microsoft.com/library/36d63aa6-1b72-4670-b5c3-da685f3017cb%28Office.15%29.aspx)
    

