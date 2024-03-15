---
title: "Use the Exchange Management Shell cmdlet response"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.service: exchange
ms.localizationpriority: medium
ms.assetid: dac8e526-11c6-4c2e-b9a2-f016b1fc738a
description: "Learn how to use the response from an Exchange Management Shell cmdlet in your Exchange managed application."
---

# Use the Exchange Management Shell cmdlet response

Learn how to use the response from an Exchange Management Shell cmdlet in your Exchange managed application.
  
**Applies to:** Exchange Online | Exchange Server 2013 | Office 365
  
Each Exchange Management Shell cmdlet returns one or more [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) instances that provide a consistent view of any object in the Exchange Management Shell environment. This article provides information about how to use the properties of a **PSObject** instance to return the property values of the underlying Exchange Server 2013 API object. 
  
## Prerequisites for using cmdlet responses
<a name="prerequisites_bk"> </a>

To use cmdlet responses, you need a reference to the **System.Automation.Management** namespace. 
  
> [!NOTE]
>  When you are using Visual Studio to create an application, you must add a reference to the System.Mangagement.Automation.dll assembly to the project. You can find the assembly in one of the following locations: 
> - For Windows XP and Windows Vista operating systems, the Windows PowerShell installation directory ($PSHOME). 
> - For the Windows 7 and Windows 8 operating systems, the following folder: Windows\assembly\GAC_MSIL\System.Management.Automation. 
  
## Windows PowerShell remote runspace
<a name="usingremoterunspace_bk"> </a>

The Exchange Management Shell uses remote Windows PowerShell features for all commands, even commands that are run on the local server. As a result, all responses from Exchange Management Shell cmdlets are serialized XML. This means that although the response object indicates the Exchange object type that was used to generate the response, the response object cannot be cast to the Exchange object type; instead, you must use the property bag that is exposed by the response object to obtain the values from the Exchange object type.
  
The property bag in the response object contains a key/value pair for each public property or method in the Exchange object type. The response object contains the name of the underlying Exchange object type; you can use this name to determine the Exchange object type that is represented by the response object so that you can extract the appropriate property. Each value in the property bag also includes type information so that you can cast the property value to the appropriate managed type.
  
## Use the cmdlet response
<a name="usingPSObject_bk"> </a>

The [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) class exposes the following three public properties that contain the values of the underlying Exchange 2013 API object: [Properties](https://msdn.microsoft.com/library/system.management.automation.psobject.properties%28VS.85%29.aspx), [Methods](https://msdn.microsoft.com/library/system.management.automation.psobject.methods%28VS.85%29.aspx), and [Members](https://msdn.microsoft.com/library/system.management.automation.psobject.members%28VS.85%29.aspx). Each property that is exposed by the Exchange 2013 API object has a corresponding key/value pair in the **Properties** and **Members** properties. Your application can index the **Properties** collection by the name of a property to retrieve the value of the property. 
  
You can use the **TypeNames** property of the **PSObject** instance to determine the type of the underlying Exchange object that is encapsulated by the **PSObject** instance. The **TypeNames** property is a collection of strings that contains the object hierarchy of the represented type. You can use these names to determine the object that is represented by the **PSObject** instance so that you can extract the appropriate property. 
  
The following code example uses the cmdlet response to print the contents of the **Properties** collection of a **PSObject** instance on the console. The code example requires a reference to the **System.Automation.Management** namespace. 
  
```cs
foreach (PSPropertyInfo propertyInfo in psObject.Properties)
{
    Console.WriteLine(string.Format("{0}: {1}",
        propertyInfo.Name, propertyInfo.Value);
}
```

<br/>

```vb
For Each PropertyInfo As PSProperty In ObjectInfo.Properties
    Console.WriteLine(String.Format("{0}: {1}", PropertyInfo.Name, PropertyInfo.Value))
Next

```

## See also

- [Create Exchange Management Shell tools](create-exchange-management-shell-tools.md)   
- [Get a list of mail users by using the Exchange Management Shell](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

