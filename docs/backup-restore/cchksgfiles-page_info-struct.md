---
title: "CChkSGFiles.PAGE_INFO struct"
manager: sethgros
ms.date: 1/22/2022
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
api_name:
- PAGE_INFO
api_type:
- dllExport
ms.assetid: 408335e1-6977-441f-bfad-ede791d1630c
description: "Last modified: January 22, 2022"
---

# CChkSGFiles.PAGE_INFO struct

**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Holds information for an Exchange database page. This structure is used with the **ErrCheckDbPages** function.
  
```cs
Struct PAGE_INFO  
{
        ULONGulPgno;
        BOOLfPageIsInitialized : 1;
        BOOLfCorrectableError : 1;
        ULONGLONGchecksumActual;
        ULONGLONGchecksumExpected;
        ULONGLONGdbTime;
        ULONGLONGchecksumPageStructure;
        ULONGLONGulFlags;
}

```

## Members

### ulPgNo
  
Unsigned Long. Logical page number of the database page to be checked. This value must be set before calling **ErrCheckDbPages**. If the application is reading the file based on file offsets, and must therefore map those file offsets to logical page numbers, you will find the **PgnoFromFileOffset** method useful to determine the value for this field. **ErrCheckDbPages** does not modify this value.

### fPageIsInitialized
  
Boolean. A value of TRUE indicates that the database page contains data. A value of FALSE indicates that the page contains only zeros. **ErrCheckDbPages** sets this value.

### fCorrectableError
  
Boolean. A value of TRUE indicates that there was a checksum mismatch detected in the database page, but that it is a correctable error. **ErrCheckDbPages** sets this value.

### checksumActual
  
Unsigned 64-bit integer. Indicates the checksum value stored in the database for this logical page. **ErrCheckDbPages** sets this value.

### checksumExpected
  
Unsigned 64-bit integer. This is the expected checksum value that is calculated for the database page; it is set by **ErrCheckDbPages**. If this value is different from that stored on the database page (that is, the value returned in **checksumActual**), **ErrCheckDbPages** will indicate that an error was found on this database page.

### dbTime
  
Unsigned 64-bit integer. **ErrCheckDbPages** sets this member to the timestamp on the database page.

### checksumPageStructure
  
Unsigned 64-bt integer. **ErrCheckDbPages** sets this member to the calculated checksum value of the contents of the page excluding data which is unnecessary when determining the logical page equivalence. For example, it is unnecessary to consider the data values in unused database page space. This member is only valid if the **checksumActual** and **checksumExpected** values are equal to each other.

### ulFlags
  
Unsigned 64-bit integer. Reserved for future use. The value of this field must be set to 0 (zero) before calling **ErrCheckDbPages**.

## Remarks

When calling the **ErrCheckDbPages** function, the **rgPageInfo** parameter is an array of **PAGE\_INFO** structures. There must be one **PAGE\_INFO** structure for each database page to be checked.
  
The application must set the **ulPgno** member to the proper value, and must also set the **ulFlags** member to 0 (zero) before calling **ErrCheckDbPages**.
  
## Requirements

Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.
  
The account that the application is running under must have read access permissions to the database and log files that are to be checked.
  