---
title: "CChkSGFiles class reference"
ms.author: null
author: null
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9347d5f6-95bb-4045-9c86-0dc0ded24fe8
description: "Find reference information for the CHKSGFILES API in Exchange 2013."
---

# CChkSGFiles class reference

Find reference information for the CHKSGFILES API in Exchange 2013.
  
 **Last modified:** September 17, 2015 
  
 * **Applies to:** Exchange Server 2013 * 
  
The CHKSGFILES API enables backup and restore applications to verify the integrity of Exchange Server 2013 transaction log files and databases programmatically. You can use this API in backup and restore applications that use the Volume Shadow Copy Service (VSS).
  
> [!NOTE]
> Storage groups are not available in Exchange 2013. Support for storage groups was removed from versions of Exchange starting with Exchange Server 2010. For backward compatibility with databases and storage groups in versions of Exchange earlier than Exchange 2010, the CHKSGFILES API enables you to specify storage groups. When you run CHKSGFILES against Exchange 2013 databases, you should set parameters that specify a storage group identifier to an empty string. 
  
## File location
<a name="bk_fileslocation"> </a>

The CHKSGFILES API ships as part of Exchange 2013. You can use this API on a computer that has the Mailbox server role installed. 
  
By default, the CHKSGFILES DLL is installed in the C:\Program Files\Microsoft\Exchange\V15\Bin directory.
  
Exchange 2013 includes only a 64-bit (amd64) version of the CHKSGFILES API. 
  
You can download a .zip file that includes the CHKSGFILE.lib library and CHKSGFILES.hxx header files for use in your custom application from the [Microsoft Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=36802).
  
## Development languages
<a name="bk_developmentlanguages"> </a>

The CHKSGFILES API is intended for use with versions of Visual Studio starting with Visual Studio 2005 in native C/C++. The CHKSGFILES API is not intended for use in managed code. Although you can create a COM Interop assembly with CHKSGFILES, we do not ship a supported COM Interop assembly with Exchange 2013.
  
## In this section
<a name="bk_inthissection"> </a>

- [CChkSGFiles.CMaxDbPerSG function](cchksgfiles-cmaxdbpersg-function.md)
    
- [CChkSGFiles.Delete function](cchksgfiles-delete-function.md)
    
- [CChkSGFiles.ERR enumeration](cchksgfiles-err-enumeration.md)
    
- [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md)
    
- [CChkSGFiles.ErrCheckDbPages function](cchksgfiles-errcheckdbpages-function.md)
    
- [CChkSGFiles.ErrCheckLogs function](cchksgfiles-errchecklogs-function.md)
    
- [CChkSGFiles.ErrGetHeader function (reserved)](cchksgfiles-errgetheader-function-reserved.md)
    
- [CChkSGFiles.ErrInit function](cchksgfiles-errinit-function.md)
    
- [CChkSGFiles.ErrTerm function](cchksgfiles-errterm-function.md)
    
- [CChkSGFiles.iDbInvalid enumeration](cchksgfiles-idbinvalid-enumeration.md)
    
- [CChkSGFiles.New function](cchksgfiles-new-function.md)
    
- [CChkSGFiles.NO_FLAGS enumeration](cchksgfiles-no_flags-enumeration.md)
    
- [CChkSGFiles.PAGE_INFO struct](cchksgfiles-page_info-struct.md)
    
- [CChkSGFiles.PgnoFromFileOffset function](cchksgfiles-pgnofromfileoffset-function.md)
    
## Additional resources
<a name="bk_addresources"> </a>

- [Exchange Online and Exchange 2013 development](http://msdn.microsoft.com/library/f33d1093-75ba-4ff2-8d15-b0bf73a401bf%28Office.15%29.aspx)
    
- [Backup, Restore, and Disaster Recovery](http://technet.microsoft.com/en-us/library/dd876874)
    

