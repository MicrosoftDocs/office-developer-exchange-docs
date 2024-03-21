---
title: "Exchange writer in Exchange 2013"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
ms.assetid: ec126433-9f0a-46ec-a685-ff4af2f97bc1
description: "Find information about the Exchange writer in Exchange 2013 for backup and restore operations."
---

# Exchange writer in Exchange 2013

Find information about the Exchange writer in Exchange 2013 for backup and restore operations. 
  
**Applies to:** Exchange Server 2013 
  
The Exchange writer is responsible for the backup and restore of active Exchange Server 2013 databases. The Exchange writer also supports backup functionality for a selected database where the shadow copy is taken against the replicated instance of the database and transaction log files. 
  
## Overview of the Exchange writer
<a name="bk_Overview"> </a>

Exchange 2013 includes database mobility features, which enable databases to be replicated among different Exchange servers to improve database availability and site resilience. The other database copies in a Database Availability Group (DAG) provide a valuable opportunity for Exchange backups to use the extra resources that are available at the copy location. In addition, because the copy instead of the active database master is backed up, the copy can be unavailable during the backup for a longer period of time. 
  
The Exchange writer coordinates with the Exchange services (operating on behalf of the requester) to prepare the database files for backups, freeze the IO activity resulting from Exchange transactions before backing up the database, and then unfreeze and truncate log files after the backup is complete.
  
During a restore, your backup and restore application instructs the Exchange writer to coordinate with the Exchange store (operating on behalf of the requester) to verify the restore targets, rename the database file if necessary, and then replay the transaction logs as needed. The Exchange writer supports both backups and restores.
  
The Exchange writer is available on any Exchange server that has the Mailbox server role installed. 
  
## Exchange writer configuration settings
<a name="bk_ExchangeWriterConfig"> </a>

The Exchange writer for VSS uses a variety of settings and values that must be set correctly and preserved during backup and restore operations. These configuration settings are stored in the Exchange writer metadata document. If your backup application does not preserve these settings, you might experience unexpected errors when you attempt to back up your Exchange databases. 
  
The following table lists the VSS interfaces that expose metadata about the components of your database backup. These interfaces are required to get the Exchange writer metadata document that is used to perform a backup of the Exchange store.
  
**Table 1. VSS interfaces**

|**VSS interface**|**Description**|
|:-----|:-----|
|IVssWMComponent  <br/> |Allows access to component information stored in the Exchange writer.  <br/> |
|IVssExamineWriterMetadata  <br/> |Allows the requesting backup and restore application to examine the metadata of the Exchange writer. The Exchange writer metadata document contains Exchange 2013-specific values and parameters that the requesting backup and restore application requires so that it can correctly specify the appropriate components for backup.  <br/> |
|IVssComponent  <br/> |Contains methods for examining and modifying information about components contained in a requester's Backup Components Document. Objects can only be obtained for those components that have been explicitly added to this document by the [IVssBackupComponents::AddComponent](https://msdn.microsoft.com/library/windows/desktop/aa382646%28v=vs.85%29.aspx) method.  <br/> |
|IVssBackupComponents  <br/> |Used by the requesting backup and restore application to poll the Exchange writer about file status and to run backup and restore operations. The [IVssBackupComponents::SetBackupState ](https://msdn.microsoft.com/library/windows/desktop/aa382833%28v=vs.85%29.aspx) method defines whether the backup operation is a full, copy, incremental, or differential backup. The [IVssBackupComponents::AddRestoreSubcomponent](https://msdn.microsoft.com/library/windows/desktop/aa382649%28v=vs.85%29.aspx) method defines the subcomponents of an Exchange 2013 database that can be selected for a restore operation.  <br/> |
   
Within the Windows Server file system, an Exchange 2013 database is stored as a single database file with an extension *.edb. The Exchange writer exposes the *.edb as the database component, while transaction logs (*.log) and checkpoint files (*.chk) are combined into a single component, referred to as the log component. For more information about Exchange database files, see [Backup and restore concepts for Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md).
  
## Interactions between the Exchange writer, VSS, and VSS requesters
<a name="bk_interactions"> </a>

The high-level interaction between the VSS, the Exchange writer, and Exchange 2013 during backup operations is as follows:
  
1. The backup program (or agent) runs a scheduled job. 
    
2. The VSS requester in the backup and restore application sends a command to VSS to take a shadow copy of the selected Exchange 2013 databases. 
    
3. VSS communicates with the Exchange writer to prepare for a snapshot backup. Exchange 2013 prohibits administrative actions against the databases, checks volume dependencies, and suspends all write operations to selected instance of the database and transaction log files while allowing read-only access. 
    
4. VSS communicates with the appropriate storage provider to create a shadow copy of the storage volume that contains the Exchange 2013 databases. 
    
5. VSS releases Exchange 2013 to resume ordinary operations. 
    
6. The VSS requester verifies the physical consistency of the backup set prior to signaling that the backup was successful. Exchange 2013 truncates the transaction logs (if the database is part of a DAG, log truncation is replicated among all the copies) and records the time of the last backup for the database.
    
VSS serializes requesters' interaction with the Exchange writer starting with the [OnPrepareBackup](https://msdn.microsoft.com/library/windows/desktop/aa381571%28v=vs.85%29.aspx) method and ending with the [OnPostSnapshot](https://msdn.microsoft.com/library/windows/desktop/aa381568%28v=vs.85%29.aspx) method. Typically, the majority of time the Exchange writer spends working with the shadow copy occurs after the **OnPostSnapshot** method, when the consistency of the shadow copy is verified prior to completion of the backups. The Exchange writer supports parallel backups between **OnPostSnapshot** and [OnBackupComplete](https://msdn.microsoft.com/library/windows/desktop/aa381557%28v=vs.85%29.aspx).
  
Exchange 2013 does not allow concurrent backups of the same database. Only one backup job can run against a given database at one time. When the backup is running, the Exchange store puts the database in a backup-in-progress state. This in-memory state is cleared either at the completion of the backup process or when the service is restarted. The in-memory backup-in-progress state and its associated data are lost when the service that hosts the Exchange writer is restarted, when the operating system is restarted, or when a cluster failover occurs. Any of these events will cause the backup job to fail.
  
Backup-initiated transaction log file truncation is triggered based on the type of backup to be performed. In non-DAG configurations, the Exchange writer will truncate the transaction log files at the completion of successful full or incremental backups. In DAG replicated configurations, log truncation will be delayed by the replication service until all necessary log files are replayed into all other copies. The replication service will delete the backed up log files both from the active and the copy log file paths after it verifies that the log files have successfully been applied to the copy database and both active database and the database copies checkpoint has passed the log files to be deleted.
  
## See also

- [Transaction logs and checkpoint files for backup and restore in Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Backup and restore concepts for Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

