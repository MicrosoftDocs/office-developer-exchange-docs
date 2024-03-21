---
title: "CChkSGFiles.ErrInit function"
manager: sethgros
ms.date: 1/22/2022
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- ErrInit
api_type:
- dllExport
ms.assetid: 61bb3af1-8b51-4bae-8e25-90a4dc1226c5
description: "Initializes the CChkSGFiles object by specifying the databases to be checked and the path and base name of the transaction log files to be checked."
---

# CChkSGFiles.ErrInit function
  
**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Initializes the **CChkSGFiles** object by specifying the databases to be checked and the path and base name of the transaction log files to be checked. Applications should call this function immediately after successfully calling the **New** function.
  
```cs
Vitual ERRErrInit  
(
    Const WCHAR  * const rgwszDb[],
    Const ULONGcDB,
    __in_z const WCHAR  * const wszLogPath,
    __in_z const WCHAR  * const wszBaseName,
    Const ULONGulFlags = NO_FLAGS
);

```

## Parameters

### rgwszDb[]
  
Input parameter. An array that specifies the databases to be checked. Each array element is a null-terminated Unicode string that contains the path and file name of a database to be checked.

### cDB
  
Input parameter. The number of valid database path elements in the **rgwszDb** array.

#### wszLogPath
  
Input parameter. The full path of the transaction log files to be checked, in the form of a null-terminated Unicode string.

### wszBaseName
  
Input parameter. The three-letter base name of the Exchange transaction log files, in the form of a null-terminated Unicode string.

### ulFlags
  
Optional input parameter. This value is reserved for future use. The value passed by this parameter should be 0 (zero).

## Return value

An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.
  
## Remarks

The **ErrInit** function registers the databases and log files that are to be checked. This function must be called after the **New** function is called but before any other **ChkSGFiles** function is called.
  
You must provide all the database names, the log file path, and the base name as null-terminated Unicode strings.
  
You can check only the database files, only the log files, or both the database and log files. However, when calling this function, the application must specify at least one entity to be checked. Passing 0 (zero) for **cDB** and NULL for **wszLogPath** will return an error.
  
If the value of **cDB** is other than 0 (zero), passing NULL for **rgwszDb** will result in an error. To check the database files, the application must provide the database names.
  
If NULL is passed for **wszBaseName** but  *wszLogPath** is not NULL, an error will be returned. A log file base name is always required when checking log files.
  
If you're using CHKSGFILES in a multithreaded application, you must call the **ErrInit** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.
  
## Requirements

Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.
  
The account that the application is running under must have read access permissions to the database and log files that are to be checked.
