---
title: "CChkSGFiles.ErrCheckDbHeaders function"
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- ErrCheckDbHeaders
api_type:
- dllExport
ms.assetid: 75289cd2-35b1-4f75-a651-dce01f1ddda1
description: Validates the headers of the database files specified by the ErrInit function. This function also returns the page size and number of pages in each of the specified databases. 
---

# CChkSGFiles.ErrCheckDbHeaders function

**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013 
  
Validates the headers of the database files that were specified by the **ErrInit** function. This function also returns the page size and number of pages in each of the specified databases. 
  
```cs
Vitual ERRErrCheckDbHeaders  
(
        ULONG  * const pcbDbPageSize,
        ULONG  * const pcHeaderPagesPerDb,
        ULONG   const piDbErrorEncountered,
    Const ULONGulFlags = NO_FLAGS
);

```

## Parameters

### pcbDbPageSize 
  
Output parameter. The page size of each of the specified databases, in bytes.
    
### pcHeaderPagesPerDb 
  
Output parameter. The number of pages at the beginning of each specified database that are reserved by the database engine for internal use. Note that you should *not* pass header pages to the **ErrCheckDbPages** function for validation. 
    
### piDbErrorEncountered
  
Output parameter. If the return value of the function indicates an error, this parameter will be an index into the **rgwszDb[]** array passed to the **ErrInit** function. The indexed array element represents the database in which the error was encountered. If the function does not return an error value, this parameter value is invalid. 
    
### ulFlags 
  
Optional input parameter. This value is reserved for future use. The value passed should be 0 (zero).
    
## Return value

This function returns an error code from the [CChkSGFiles.ERR enumeration](cchksgfiles-err-enumeration.md).
  
## Remarks

**ErrCheckDbHeaders** verifies that all databases registered with **ErrInit** have the same log signature and database page size. You can also use the lowest **genMin** parameter value and the highest **genMax** parameter value to determine the set of log files that are necessary to bring all of the registered databases to a clean-shutdown state. 
  
The **piDbErrorEncountered** parameter is set only when an error is detected, as indicated by a non-zero **ErrCheckDbHeaders** return value. 
  
When an error occurs in this function, an error event will be added to the Windows Error event log.
  
You can call **ErrCheckDbHeaders** only after calling **ErrInit**, and you must call it before calling **ErrCheckDbPages** and **ErrCheckLogs**.
  
If you're using CHKSGFILES in a multithreaded application, you must call the **ErrCheckDbHeaders** function in the single-threaded portion, and you can call it only once for each **CCheckSGFiles** object. 
  
## Requirements

Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.
  
The account that the application is running under must have read access permissions to the database and log files that are to be checked.
  

