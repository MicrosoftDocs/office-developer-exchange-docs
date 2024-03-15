---
title: "CChkSGFiles.ErrGetHeader function (reserved)"
manager: sethgros
ms.date: 02/11/2022
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- ErrGetHeader
api_type:
- dllExport
ms.assetid: eed4d88b-8ac5-4c03-9ed9-e529e6072450
description: "Do not call CChkSGFiles.ErrGetHeader function; reserved for future use."
---

# CChkSGFiles.ErrGetHeader function (reserved)

**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Reserved for future use, and not implemented. Do not call this function.
  
```cs
Vitual ERRErrGetHeader  
(
    __in_z const WCHAR  * const wszFile,
        VOID  * const pvResult,
    Const ULONGcbMax,
    Const ULONGulFlags = NO_FLAGS
);

```

## Parameters

### wszFile
  
Reserved for future use; do not use.

### pvResult
  
Reserved for future use; do not use.

### cbMax
  
Reserved for future use; do not use.

### ulFlags
  
Reserved for future use; do not use.

## Return value

None.
  
## Remarks

None.
  
## Requirements

Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.
