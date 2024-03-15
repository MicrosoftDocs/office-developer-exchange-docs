---
title: "Transaction logs and checkpoint files for backup and restore in Exchange"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
ms.assetid: 80e04b9f-87c7-4acf-89b1-aa66ffaf7e53
description: "Find information about transaction logs and checkpoint files and how they are used to back up and restore Exchange 2013 data."
---

# Transaction logs and checkpoint files for backup and restore in Exchange

Find information about transaction logs and checkpoint files and how they are used to back up and restore Exchange 2013 data.
  
**Applies to:** Exchange Server 2013 
  
This article describes how Exchange Server 2013 uses transaction logs and checkpoint files to help prevent data loss. It is important to be aware of this information when you develop backup and restore applications that use the Volume Shadow Copy Service (VSS) in versions of Windows Server starting with Windows Server 2008.
  
## Transaction logs in Exchange 2013

Exchange 2013 maintains a single set of transaction log files for each database. A transaction is defined as any operation that changes the state or contents of the database. The transaction log files for an individual database record all the transactions performed on the database. Records of the transactions are written to the transaction logs before they are made in the database itself, to ensure that all committed transactions can be recovered in the event of a database failure. Exchange 2013 database transaction logs are stored on disk before the transactions are committed to the database file. 
  
The recording of the transactions before the database is updated is called write-ahead logging. To help ensure that the database is correctly brought back to the proper state, Exchange 2013 writes data into the database files by using page-based writes and checkpoints. During regular operations, the Exchange store first records database changes in the transaction logs, and then makes those changes on an in-memory copy of the database. The transaction logs record the beginning and end of each transaction. This ensures that sufficient information is available to later undo or roll back operations in the database.
  
When recovering from errors in which the database file on disk is damaged, but the transaction logs are intact, your restore application must first restore a known good copy of the database file.
  
The Exchange store replays the transactions from the previously backed up transaction logs, and then replays any remaining transactions from the on-disk transaction log files. Note that sometimes transactions can be lost if the system fails between when the transactions are recorded in the transaction logs, and when they are actually written to the database files. 
  
Periodically, the Exchange store checks the in-memory database image, and then determines which pages have changed. The Exchange store combines the pending changes, and then writes those pages to the database file on disk.
  
## Checkpoint files in Exchange 2013

A checkpoint file records which logged transactions have been written to the on-disk database files. The checkpoint is advanced when all the database pages that have been modified by entries in the transaction logs are successfully written to disk. Because the checkpoint file records which transactions are already in the on-disk database image, the Exchange store only needs to replay transactions that occurred after the checkpoint. Depending on the time period between backups, this can greatly decrease the number of transactions that must be replayed into the database if a system failure occurs.
  
## See also

- [Backup and restore concepts for Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
- [Types of backup operations for Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
- [Restoring Exchange 2013 databases](restoring-exchange-2013-databases.md)
    

