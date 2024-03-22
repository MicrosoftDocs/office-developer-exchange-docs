---
title: "CChkSGFiles.ErrCheckDbPages function"
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- ErrCheckDbPages
api_type:
- dllExport
ms.assetid: 5e981a7c-28cd-470c-b7eb-606463e9dd05
description: Validates a range of pages in a specified database. 
---

# CChkSGFiles.ErrCheckDbPages function

**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Validates a range of pages in a specified database. 
  
```cs
Vitual ERRErrCheckDbPages  
(
    Const ULONGiDb,
    Const VOID  * const pvPageBuffer,
    Const ULONGcbPageBuffer,
    PAGE_INFOrgPageInfo[],
    Const ULONGcPageInfo,
    Const ULONGulFlags = NO_FLAGS
);

```

## Parameters

### iDb
  
Input parameter. An index into the array of databases specified in the **rgwszDb[]** parameter to the **ErrInit** function. The database indexed by this parameter will be checked. 
    
### pvPageBuffer 
  
Input parameter. A pointer to a buffer containing one or more database pages to be checked. The size of the buffer must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function. The calling application must fill the buffer with the database page contents before calling **ErrCheckDbPages**.
    
### cbPageBuffer
  
Input parameter. The size of the **pvPageBuffer** parameter, in bytes. This value must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function. 
    
### rgPageInfo[] 
  
Input/output parameter. An array of **PAGE\_INFO** structures that **ErrCheckDbPages** fills with detailed results of each database page that is checked. The array must have one element for each database page passed in the **pvPageBuffer** parameter, and the **ulPgno** field in each **PAGE\_INFO** structure must be set to the logical page number that corresponds to the database page. For more information, see "Remarks" later in this topic. 
    
### cPageInfo
  
Input parameter. The number of entries in the **rgPageInfo[]** array. This value must be equal to the number of database pages passed in the **pvPageBuffer** parameter. 
    
### ulFlags 
  
Optional input parameter. This value is reserved for future use. The value passed in this parameter should be 0 (zero).
    
## Return value

An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration. 
  
## Remarks

Note that you need to have specified the database in the array of databases passed to the **ErrInit** function. Also, **ErrCheckDbHeaders** must be called before **ErrCheckDbPages**.
  
The calling application must allocate a memory buffer that is large enough to hold the database pages to be checked. The application is responsible for filling the buffer with the contents of one or more such database pages. 
  
The calling application must call **ErrCheckDbHeaders** before calling **ErrCheckDbPages**. This function can be called as many times as necessary to cover all the pages in all database files that are to be checked.
  
In the **rgPageInfo[]** parameter, each element returned contains information about the database page in a **PAGE\_INFO** structure. If the **ErrCheckDbPages** function returns an error, the application should check each **PAGE\_INFO** structure to determine on which page the error was found. For example, comparing the **checksumActual** and **checksumExpected** values will indicate whether a checksum error was detected on that database page. 
  
If **ErrCheckDbPages** detects any errors in the database content, it will create a Windows Error event log entry. 
  
The **CChkSGFiles** object determines whether all the databases registered with the **ErrInit** function were actually checked. Specifically, **CChkSGFiles** uses the **ErrCheckDbPages** function to determine whether the same number of database pages indicated by **ErrCheckDbHeaders** were actually verified. If the correct number of pages in each database were not successfully checked, the **ErrTerm** function returns an error. 
  
If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckDbPages** function in the multithreaded portion of the application. Note that **ErrCheckDbPages** is typically called multiple times for each database that is checked. 
  
## Requirements

Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.
  
The account that the application is running under must have read permissions to the database and log files that are to be checked.
  

