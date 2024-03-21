---
title: "CChkSGFiles.NO_FLAGS enumeration"
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- NO_FLAGS
api_type:
- dllExport
ms.assetid: 6b18b645-fec4-429a-9900-62ad0f19bf96
description: Serves as a placeholder value for the ulFlags parameters that are accepted by most CCheckSGFiles class functions. 
---

# CChkSGFiles.NO_FLAGS enumeration

**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Serves as a placeholder value for the **ulFlags** parameters that are accepted by most **CCheckSGFiles** class functions. 
  
```cs
Enum { NO_FLAGS = 0 }

```

## Requirements

Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.
  
The account that the application is running under must have read access permissions to the database and log files that are to be checked.
  

