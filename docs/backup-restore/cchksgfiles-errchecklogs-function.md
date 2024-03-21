---
title: "CChkSGFiles.ErrCheckLogs function"
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- ErrCheckLogs
api_type:
- dllExport
ms.assetid: cec0df4b-4679-4682-bacf-69b4f4aef343
description: Validates the log files of all the database files specified in the ErrInit function.
---

# CChkSGFiles.ErrCheckLogs function

**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Validates the log files of all the database files that were specified in the **ErrInit** function. The validated logs are those that exist in the path, and that have the three-letter base log file name passed to **ErrInit**.
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## Parameters

### pfOnlyUnnecessaryLogsCorrupt
  
Output parameter. When **true**, this parameter indicates that errors were found in the transaction log files, but those errors were all found in log files that are not needed to bring the database to a clean-shutdown state without data loss. A **true** value returned in this parameter is valid only when **ErrCheckLogs** returns **errSuccess**.

### ulFlags
  
Optional input parameter. This value is reserved for future use. The value passed by this parameter should be 0 (zero).

## Return value

An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.
  
It's important to remember that this function can return **errSuccess** even when errors are found in the log files. Therefore, when **ErrCheckLogs** returns **errSuccess**, the application should also check the **pfOnlyUnnecessaryLogsCorrupt** return parameter. If **pfOnlyUnnecessaryLogsCorrupts** is **true** when **ErrCheckLogs** returns **errSuccess**, this indicates that one or more errors were found, but only in log files not needed to bring the database up-to-date.
  
## Remarks

The **ErrCheckDbHeaders** function must be called before the **ErrCheckLogs** function can be called.
  
When Exchange database transaction log files are being checked, some of the log files will be necessary to bring the databases in the storage group to a clean-shutdown state without data loss, whereas other log files might not be needed. The **ErrCheckLogs** function determines both the oldest and the newest log files that are needed to bring the databases up to date.
  
The **ErrCheckLogs** function verifies all the log files in the specified paths that also have the specified three-letter base file name, as passed to the **ErrInit** function.
  
If no errors are found in the log files, **ErrCheckLogs** returns **errSuccess**.
  
If any of the required log files are found to be corrupted, **ErrCheckLogs** returns an error.
  
If errors are found only in log files that are older than the earliest ones needed, the function returns **errSuccess** and sets the return parameter **pfOnlyUnnecessaryLogCorrupt** to **true**. The application should recognize that there are errors in some of those old log files, and if so, it will possibly alert the user. In any case, those errors should not affect the overall integrity of the database or affect whether playing the logs forward will succeed.
  
If errors are found in any log file created after the earliest log that **ErrCheckLogs** determines is needed, the function returns an error. The error will be returned even if the log file error was found in a log file that was generated later than what is needed to bring the database up to date. Although it would be possible to bring the databases to a clean-shutdown state by using the identified log files, transactions specified in the later corrupted log files would not be applied, resulting in data loss when the database is restored.
  
The **CChkSGFiles** object determines whether all of the log files registered with the **ErrInit** function were actually checked. If not all of the logs were not successfully checked, the **ErrTerm** function returns an error.
  
If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckLogs** function in the multithreaded portion of the application, but you can call it only once for each **CCheckSGFiles** object.
  
## Requirements

Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.
  
The account that the application is running under must have read access permissions to the database and log files that are to be checked.
  
