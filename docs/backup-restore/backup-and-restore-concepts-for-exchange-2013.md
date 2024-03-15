---
title: "Backup and restore concepts for Exchange 2013"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
ms.assetid: 9a1c4709-9313-4ccf-9f8a-673a51d51f23
description: "Find information about Exchange databases that will help you create your backup and restore applications for Exchange 2013."
---

# Backup and restore concepts for Exchange 2013

Find information about Exchange databases that will help you create your backup and restore applications for Exchange 2013.
  
Before you create backup and restore applications for Exchange Server 2013, you should be familiar with the Exchange database file structure. By using the Exchange store database files, you can back up the data in your store and restore it at a later time as needed. If you are limited on disk space, your administrator might implement circular logging, and this will affect your ability to back up the database. You can also take advantage of the database mobility feature in Exchange 2013 to back up and restore Exchange data. Database mobility, in combination with your backup and restore application, is a good measure of redundancy for disaster recovery.

<a name="bk_exchangedatabases"> </a>

## Exchange store database files

Exchange 2013 includes support for up to 100 databases. Each Exchange 2013 database contains the files listed in the following table. 
  
**Table 1. Exchange 2013 database files**

|File type|Extension|Description|
|:-----|:-----|:-----|
|Database file  <br/> |\*.edb  <br/> |Records all the changes that have been committed to the in-memory database.  <br/> |
|Transaction log stream  <br/> |\*.log  <br/> |Records operations, such as the creation or modification of a message, that will be committed to the database. Limited in size to 1 MB each.  <br/> |
|Checkpoint file  <br/> |\*.chk  <br/> |Records which logged transactions have been written to the on-disk database files.  <br/> |
   
Exchange 2013 maintains a single set of transaction log files for each database. The transaction logs are important for backup and recovery operations. When you create a backup and restore application that uses the Volume Shadow Copy Service (VSS), you must ensure that you handle these logs correctly. For more information, see [Transaction logs and checkpoint files for backup and restore in Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md). To back up a database and its log stream, you must back up the entire volume that contains the database and logs. Log truncation will occur only after a successful completion of a full backup of a volume or folders that contain an Exchange database.
  
On each Exchange server, you can mount only one recovery database at a time. You can access the recovery database by using Exchange Management Shell cmdlets such as **New-MailboxRestoreRequest**. For more information about Exchange recovery databases, see [Recovery Databases](https://technet.microsoft.com/library/dd876954%28v=exchg.150%29.aspx) on TechNet. For more information about Exchange Management Shell cmdlets, see [Exchange 2013 Cmdlets](https://technet.microsoft.com/library/bb124413.aspx) on TechNet. 
  
## Circular logging
<a name="bk_circularlogging"> </a>

If storage capacity is an issue, your administrator might enable circular logging. When circular logging is enabled, Exchange writes transaction logs as usual, but when a checkpoint file is advanced, the inactive portion of the transaction log is truncated. Your administrator should not configure Exchange 2013 databases to use circular logging if you also plan to use VSS to enable your custom backup and restore operations. Circular logging creates the following restrictions: 
  
- If enabled during the backup operation or the recovery operation, you cannot restore individual databases.
    
- Only point-in-time recovery operations are possible. When circular logging is enabled, you can delete transaction logs in the same directory when a database is restored, although those logs might be part of a different Exchange 2013 database. 
    
- You cannot perform incremental or differential backup operations. For more information about these types of backups, see [Types of backup operations for Exchange 2013](types-of-backup-operations-for-exchange-2013.md).
    
If circular logging is enables, your administrator should disable it as soon as possible to ensure that your VSS backups don't fail. For more information, check out the blog post [Exchange Circular Logging and VSS Backups](https://blogs.technet.com/b/exchange/archive/2010/08/18/3410672.aspx). 
  
## Exchange database mobility
<a name="bk_exchangedatabasemobility"> </a>

Exchange 2013 allows for database mobility to improve mailbox reliability and availability. Database mobility enables you to make copies of your Exchange store database, disconnect the database from the server, and store it on another server. In an Exchange 2013 Database Availability Group (DAG), multiple copies of the database are stored on different computers. When one or more copies of the database are lost due to hardware or other system failure, information from the other copies can be used to reseed the database via normal replication operations.
  
For backup operations, if the Exchange 2013 databases that are to be backed up are configured in a DAG, the backup application can better prevent interference between the snapshot and the active server's performance by taking the snapshot on one of the inactive database copies. Because the database copies are for the most part synchronized, the backup application can take snapshots from different copies of the database, and later reconstruct it from the pieces.
  
The only supported method of restoring DAG databases from backup data is to restore all copies of the database by using the same backup data. Because the database log files might be slightly different between the copies, restoring individual database copies using different data can cause the database to become unmountable.
  
## In this section
<a name="bk_inthissection"> </a>

- [Transaction logs and checkpoint files for backup and restore in Exchange 2013](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Exchange writer in Exchange 2013](exchange-writer-in-exchange-2013.md)
    
## See also

- [Exchange Online and Exchange development](../exchange-server-development.md) 
- [Types of backup operations for Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
- [Restoring Exchange 2013 databases](restoring-exchange-2013-databases.md)
    

