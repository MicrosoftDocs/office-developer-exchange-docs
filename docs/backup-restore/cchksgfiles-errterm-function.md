---
title: "CChkSGFiles.ErrTerm function"
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- ErrTerm
api_type:
- dllExport
ms.assetid: eea20a55-4a2a-4209-ae79-dc1ee1cd631b
description: "Last modified: February 25, 2013"
---

# CChkSGFiles.ErrTerm function
  
**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Provides an overall status of the database and log verification, which indicates whether all the database pages and logs were successfully verified.
  
> [!IMPORTANT]
> Storage groups are not available in Exchange 2013. For backward compatibility with databases and storage groups in versions of Exchange earlier than Exchange Server 2010, the CHKSGFILES API enables you to specify storage groups. When you run CHKSGFILES against Exchange 2013 databases, you should set parameters that specify a storage group identifier to an empty string. 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## Parameters

### ulFlags
  
Optional input parameter. This value is reserved for future use. The value passed by this parameter should be 0 (zero).
    
## Return value

An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration. 
  
## Remarks

The **CChkSGFiles** object determines whether all the databases registered with the **ErrInit** function were actually checked. This object uses the **ErrCheckDbPages** function to verify that the same number of database pages identified by the **ErrCheckDbHeaders** function were actually verified. If the correct number of pages in each database are not successfully checked, the **ErrTerm** function returns an error. 
  
If the number of database pages checked with **ErrCheckDbPages** is less than that indicated by **ErrCheckDbHeaders**, this function creates an error in the Windows Event log, and **ErrTerm** returns an error. 
  
If the number of database pages checked with **ErrCheckDbPages** is greater than that indicated by **ErrCheckDbHeaders**, this function creates a warning in the Windows Event log to indicate that the application might be unnecessarily checking some database pages more than once. In this case, however, the **ErrTerm** function succeeds. 
  
The **CChkSGFiles** object also determines whether the log files registered with **ErrInit** were actually checked. If not all the logs were successfully checked, the **ErrTerm** function returns an error. 
  
When **ErrTerm** returns an error, it will be the first error it finds, even though it checks the verification status for all databases registered with **ErrInit**.
  
If you're using CHKSGFILES in a multithreaded application, you must call the **ErrTerm** function in the single-threaded portion of the application, and you can call it no more than once for each **CCheckSGFiles** object. 
  
## Requirements

Exchange 2013 only includes a 64-bit version of CHKSGFILES.
  
The account that the application is running under must have read access permissions to the database and log files that are to be checked.
  

