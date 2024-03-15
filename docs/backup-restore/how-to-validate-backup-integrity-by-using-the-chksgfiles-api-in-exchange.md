---
title: "Validate backup integrity by using the CHKSGFILES API in Exchange 2013"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
ms.assetid: 607cbeb9-0a02-4079-8a4d-34bdeb560224
description: "Find out how to use the CHKSGFILES API to validate a backup of the Exchange store in Exchange 2013."
---

# Validate backup integrity by using the CHKSGFILES API in Exchange 2013

Find out how to use the CHKSGFILES API to validate a backup of the Exchange store in Exchange 2013.
  
**Applies to:** Exchange Server 2013 
  
During backup operations managed by the Volume Shadow Copy Service (VSS), Exchange Server 2013 cannot read each database file in its entirety and verify its checksum integrity. Therefore, you might want your backup application to verify database and transaction log file integrity. We recommend that your backup application verify the physical consistency of the shadow copy set prior to informing the Exchange writer that the backup is complete. After a successful backup, the Exchange store updates the headers of the backed-up databases to reflect the last successful backup times and removes transaction logs from the server that are no longer required to roll forward from the last successful backup.
  
## Prerequisites for validating backup integrity

Before your application can validate the integrity of your backup, you must have access to the following:
  
- Files from your Exchange store backup.
- A version of Visual Studio starting with Visual Studio 2010.
- The CHKSGFILES library and header files. You can download the library and header files from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=36802).
    
## Validate backup integrity

The following procedure describes how to validate data integrity in your backup and restore application.
  
### To validate backup integrity

1. Create a new instance of the **CChkSGFiles** class. 
   
   ```cpp
   CCheckSGFiles::ERRerr = CCheckSGFiles::errSuccess;
   ULONGiDbError = (ULONG)CCheckSGFiles::iDbInvalid;
   CCheckSGFiles * const pcchecksgfiles = CCheckSGFiles::New();
   if ( NULL == pcchecksgfiles )
   {
     err = CCheckSGFiles::errOutOfMemory;
     printf( "ERROR: Could not allocate CCheckSGFiles object.\n" );
     goto HandleError;
   }
   ```

   The first lines of code create an error object and set its initial value to success, and create an object that checks the validity of the database. Then, the [CChkSGFiles.New function](cchksgfiles-new-function.md) creates a new instance of the **CChkSGFiles** class. A quick check of the new object indicates whether any issues occurred when the new instance was created. 
    
2. Initialize the **CChkSGFiles** object. 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   For more information about the parameters, see [CChkSGFiles.ErrInit function](cchksgfiles-errinit-function.md).
   
3. Use the [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md) to validate database integrity by checking the database headers.
   
   ```cpp
   err = pcchecksgfiles->ErrCheckDbHeaders(
   &amp;cbDbPageSize,
   &amp;cDbHeaderPages,
   &amp;iDbError );
   if ( CCheckSGFiles::errSuccess != err )
   {
   if ( CCheckSGFiles::iDbInvalid != iDbError )
   {
   printf(
   "ERROR: Database header validation for '%S' failed with error %d (0x%x)\n",
   rgwszDb[ iDbError ],
   err,
   err );
   }
   goto HandleError;
   }
   ```
   
   For more information about the parameters, see [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md).
   
4. Handle errors, and use the [CChkSGFiles.Delete function](cchksgfiles-delete-function.md) to remove the **CChkSGFiles** class from memory. 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## See also

- [CChkSGFiles class reference](cchksgfiles-class-reference.md)
- [Build backup and restore applications for Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
- [Backup and restore concepts for Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    

