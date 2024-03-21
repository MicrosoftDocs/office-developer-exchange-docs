---
title: "CChkSGFiles.ERR enumeration"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- ERR
api_type:
- dllExport
ms.assetid: f0efe195-91c3-4f3a-8c7d-e5dba336465a
description: "Last modified: March 09, 2015"
---

# CChkSGFiles.ERR enumeration 
  
**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Indicates the results of the called function. This enumeration is returned by many functions of the **CCheckSGFiles** class. 
  
```cs
Enum ERR  
{
        errSuccess = 0,
        errTaskDropped = -106,
        errRequiredLogFilesMissing = -543,
        errInvalidParameter = -1003,
        errOutOfMemory = -1011,
        errReadVerifyFailure = -1018,
        errTooManyActiveUsers = -1059,
        errDatabaseCorrupted = -1206
}

```

## Values

|**Member name**|**Value**|**Description**|
|:-----|:-----|:-----|
|errSuccess  <br/> |0  <br/> |The function completed without any errors.  <br/> |
|errTaskDropped  <br/> |-106  <br/> |Returned by the **ErrTerm** function to indicate that not all database pages and transaction log files were checked, or that errors were encountered during the verification.  <br/> |
|errRequiredLogFilesMissing  <br/> |-543  <br/> |One or more log files that are required to bring the database to a clean-shutdown state was not found in the log file path, or did not have the specified three-letter base name.  <br/> |
|errInvalidParameter  <br/> |-1003  <br/> |One or more parameters that were passed to the function were invalid.  <br/> |
|errOutOfMemory  <br/> |-1011  <br/> |Insufficient memory was available to complete the requested operation.  <br/> |
|errReadVerifyFailure  <br/> |-1018  <br/> |The checksum that is stored on a database page does not match its expected checksum.  <br/> |
|errTooManyActiveUsers  <br/> |-1059  <br/> |The **ErrTerm** function was called while the object was still being used. This can occur if **ErrTerm** is called before **ErrCheckDbPages** or **ErrCheckLogFiles** has returned.  <br/> |
   
## Requirements

Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.
  
The account that the application is running under must have read access permissions to the database and log files that are to be checked.
  

