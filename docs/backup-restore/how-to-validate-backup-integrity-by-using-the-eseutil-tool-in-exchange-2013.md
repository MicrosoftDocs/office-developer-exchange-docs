---
title: "Validate backup integrity by using the Eseutil tool in Exchange 2013"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
ms.assetid: b0d325ba-4482-4ca2-9a69-c890f985b206
description: "Find out how to use the Eseutil command-line tool to validate a backup of the Exchange store."
---

# Validate backup integrity by using the Eseutil tool in Exchange 2013

Find out how to use the Eseutil command-line tool to validate a backup of the Exchange store.
  
**Applies to:** Exchange Server 2013
  
Because the Volume Shadow Copy Service (VSS) can create backups while Exchange continues to write to the database, the server does not touch all the pages and perform the necessary consistency checks. For this reason, any backup and restore application that uses VSS must verify snapshot consistency. Exchange Server 2013 supports the following two methods for checking snapshot consistency:
  
- The CHKSGFILES API

- The Eseutil command-line tool

We recommend that you use the CHKSGFILES API because it is easier for the backup application to detect, diagnose, and report errors that are found during the CHKSGFILES consistency check. For information about how to use the CHKSGFILES API, see [Validate backup integrity by using the CHKSGFILES API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md).
  
## Running the Eseutil tool

To check the snapshot consistency, run the eseutil command against the database and log files that are identified in the following table.
  
**Table 1. Eseutil.exe commands for each backup type**

|**File type/backup type**|**Full backup**|**Copy backup**|**Incremental backup**|**Differential backup**|
|:-----|:-----|:-----|:-----|:-----|
|.edb  <br/> |"eseutil /k /i"  <br/> |"eseutil /k /i"  <br/> |Not applicable  <br/> |Not applicable  <br/> |
|.log  <br/> |"eseutil /k" (1)  <br/> |"eseutil /k" (1)  <br/> |"eseutil /k" (2)  <br/> |"eseutil /k" (2)  <br/> |

> [!NOTE]
> You do not need to run the eseutil command against .stm and .chk files.
  
All the log files that have a log file generation number that is equal to or greater than the generation number of the checkpoint log file are required in order to recover a snapshot database. If it exists, the current log file (Enn.log) is also required for database recovery. If any of the required log files fail the consistency check, the requester must make sure that the status of the backup component is set to FALSE before it calls the [BackupComplete](/windows/win32/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) method. To identify the checkpoint log file, run Eseutil.exe against the snapshot checkpoint file and parse the output for "Checkpoint:." The following example shows how to run Eseutil.exe against a checkpoint file.
  
```cpp
c:\eseutil.exe /mk E01.chk
Checkpoint: (0x20, 9D, 187)
```

The second line in the example is the return value, where 0x20 is the hexadecimal log generation number of the checkpoint log file. In this example, any log files, including E01000020.log and greater, must not be corrupt in order to recover the snapshot database, even if the database itself has already passed the physical consistency check.
  
All log files in an incremental or differential backup set are required for database recovery. You can check the consistency of a log sequence by running Eseutil.exe against the log file prefix. The following example shows how to run consistency checks against all the files of the form E01xxxxx.log on a given path.
  
```cpp
c:\eseutil /k E01
```

## Checking the Eseutil.exe output

The requester must verify that all the exit ERRORLEVEL error values that are returned are nonnegative. For information about ERRORLEVEL values, see [Reference for Common Eseutil Errors](/previous-versions/office/exchange-server-2007/aa996759(v=exchg.80)). To see the ERRORLEVEL at the command line, type "echo %errorlevel%" after Eseutil.exe finishes running. A negative ERRORLEVEL indicates that one or more files is corrupted.
  
Before the requester calls the **BackupComplete** method, it must make sure that the status of the backup component reflects the result of the consistency check. If any corruption was found, the status will be FALSE; if no corruption was found, the status will be TRUE.
  
## See also

- [Validate backup integrity by using the CHKSGFILES API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
- [Build backup and restore applications for Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [CChkSGFiles class reference](cchksgfiles-class-reference.md)
- [Backup and restore concepts for Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
