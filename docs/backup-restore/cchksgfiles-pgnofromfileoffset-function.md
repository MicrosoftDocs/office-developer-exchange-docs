---
title: "CChkSGFiles.PgnoFromFileOffset function"
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- PgnoFromFileOffset
api_type:
- dllExport
ms.assetid: 3d69ca6d-5ed1-4038-859e-106e776eeec1
description: Returns the logical database page number that corresponds to the specified byte index in the physical database file.
---

# CChkSGFiles.PgnoFromFileOffset function

**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Returns the logical database page number that corresponds to the specified byte index in the physical database file. If the file offset is invalid, or if the **ErrCheckDbHeaders** function has not been called for the databases, this function returns 0 (zero). 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## Parameters

### ibFileOffset
  
Input parameter. The offset into a database file, in bytes.
    
## Return value

The database file's logical page number that includes the specified offset.
  
## Remarks

If the **ibFileOffset** parameter is invalid, the **PgnoFromFileOffset** function returns 0 (zero). 
  
**PgnoFromFileOffset** also returns 0 (zero) if you haven't called the **ErrCheckDbHeaders** function on the **CCheckSGFiles** instance. You must call **ErrCheckDbHeaders** to initialize the database page size and number of pages allocated to database headers. 
  
You should use **PgnoFromFileOffset** to fill in the **PAGE\_INFO** structure elements in preparation for calling **ErrCheckDbPages**. The **rgPageInfo** parameter to **ErrCheckDbPages** requires that each element in the array be a **PAGE_INFO** structure, with the **ulPgno** member values correctly initialized. 
  
If you're using CHKSGFILES in a multithreaded application, you can call the **PgnoFromFileOffset** function in the multithreaded portion of the application. Note that you would typically call this function multiple times for each database being checked. 
  
## Requirements

Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.
  
The account that the application is running under must have read permission to the database and log files that are to be checked.
  

