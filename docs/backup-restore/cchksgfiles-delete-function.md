---
title: "CChkSGFiles.Delete function"
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- Delete
api_type:
- dllExport
ms.assetid: 869e927f-7df2-4247-88ef-b8b05b29a700
description: Destroys an existing instance of the CChkSGFiles class.
---

# CChkSGFiles.Delete function

**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Destroys an existing instance of the **CChkSGFiles** class. You must call this function after the application has finished working with the specified object. 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## Parameters

### pcchecksgfiles 
  
Input parameter. A pointer to an existing **CCheckSGFiles** object. The memory associated with the object will then be freed. 
    
## Return value

None.
  
## Remarks

The **Delete** function frees the memory associated with the **CCheckSGFiles** object. After you call **Delete**, the pointer passed in the  *pcchecksgfiles*  parameter will be invalid and no other operations can be performed on that object. 
  
If the application uses the **ErrCheckDbPages** function, the application must free the memory buffer manually; the **Delete** function will not free it. 
  
If you're using CHKSGFILES in a multithreaded application, you must call the **Delete** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object. 
  
## Requirements

Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.
  
The account that the application is running under must have read access permissions to the database and log files that are to be checked.
  

