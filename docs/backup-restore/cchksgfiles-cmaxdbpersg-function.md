---
title: "CChkSGFiles.CMaxDbPerSG function"
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- CMaxDbPerSG
api_type:
- dllExport
ms.assetid: 5871988b-a5d7-42cc-9b83-8fededb5072f
description: "CChkSGFiles.CMaxDbPerSG function returns the maximum number of databases allowed in a single Exchange server storage group."
---

# CChkSGFiles.CMaxDbPerSG function

**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Returns the maximum number of databases allowed in a single Exchange server storage group.
  
```cs
Static ULONG __stdcall CMaxDbPerSG  ();

```

## Parameters

None.
  
## Return value

The maximum number of databases that the specified Exchange server allows per storage group. Because storage groups are not part of Exchange 2013, this function returns 1.
  
## Remarks

You can use the **CCheckSGFiles** object to validate databases (and transaction log files) in only one storage group, so the value returned by the **CMaxDbPerSG** function also represents the maximum number of databases that you can check by using an instance of the **CCheckSGFiles** class.
  
Note that by default, Exchange Server 2003 and Exchange Server 2007 allow a maximum of five databases per storage group.
  
## Requirements

Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.
  
The account that the application is running under must have read access permissions to the database and log files that are to be checked.
 
