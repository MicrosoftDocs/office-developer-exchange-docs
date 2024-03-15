---
title: "CChkSGFiles.New function"
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- New
api_type:
- dllExport
ms.assetid: 588d8c74-c9ce-4d5e-8a79-a2a68676e858
description: Creates a new instance of the CChkSGFiles class.
---

# CChkSGFiles.New function

**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Creates a new instance of the **CChkSGFiles** class. You must call this function before you can specify the storage group and databases to be checked. 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## Parameters

None.
  
## Return value

A reference (pointer) to the newly created object.
  
## Remarks

The **New** function creates a **CCheckSGFiles** object and returns to the caller a reference (pointer) to that object. You must call this function before it calls any of the other functions in the **CCheckSGFiles** class. 
  
If you're using CHKSGFILES in a multithreaded application, you must call the **New** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object. 
  
## Requirements

Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.
  
The account that the application is running under must have read access permissions to the database and log files that are to be checked.
  

