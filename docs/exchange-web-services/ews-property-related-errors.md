---
title: "EWS property-related errors"
 
 
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
 
 
ms.localizationpriority: medium
ms.assetid: 1c4c5969-7bdd-4021-be0e-cae99e86cf2c
description: "Find out how to handle property-related errors in your EWS application."
---

# EWS property-related errors

Find out how to handle property-related errors in your EWS application.
  
Most EWS client applications will use properties, which means that you will have to handle property-related errors. You can handle these errors at runtime, or while you are developing your EWS application.
  
**Table 1: Property-related errors and how to handle them**

|**Error**|**Caused by an attempt to…**|**Handle it by…**|
|:-----|:-----|:-----|
|ErrorDataSizeLimitExceeded  <br/> |Set a property with a value that exceeds the maximum size for the property or the property does not support streaming, such as folder properties.  <br/> |Limiting the size of data you set on the property.  <br/> |
|ErrorFolderPropertRequestFailed  <br/> |Get a property that could not be retrieved.  <br/> |Indicating that the property cannot be retrieved.  <br/> |
|ErrorInvalidExtendedProperty  <br/> |Set an invalid combination of extended property values or results in an invalid extended property Uniform Resource Identifier (URI).  <br/> |Checking the extended property value.  <br/> |
|ErrorInvalidExtendedPropertyValue  <br/> |Set an extended property value that does not match the specified type  <br/> |Updating your code to check for matching types.  <br/> |
|ErrorInvalidFolderId  <br/> |Set the structure of a folder identifier to an invalid form.  <br/> |Only using identifiers returned by EWS.  <br/> |
|ErrorInvalidId  <br/> |Set the structure of an identifier and/or change key to an invalid form.  <br/> |Only using identifiers returned by EWS.  <br/> |
|ErrorInvalidIdEmpty  <br/> |Set an empty an identifier.  <br/> |Setting the identifier with a valid item or folder identifier.  <br/> |
|ErrorInvalidIdMalformed  <br/> |Set the structure of an identifier and/or change key to an invalid form.  <br/> |Only using identifiers returned by EWS.  <br/> |
|ErrorInvalidPropertyAppend  <br/> |Append a property that does not support appending.  <br/> |Updating your code so that it only attempts to append values to the recipient collection properties (To, Cc, Bcc), Attendee collection properties (Required, Optional, Resources), Body property, and the ReplyTo property.  <br/> |
|ErrorInvalidPropertyDelete  <br/> |Delete a property that does not support deleting.  <br/> |Updating your code to not try to delete the property. For example, the folder and item identifiers cannot be deleted.  <br/> |
|ErrorInvalidPropertyForExists  <br/> |Set an existential based search restriction on a flag-based property.  <br/> |Updating your code to not use flag-based properties in an existential based search restriction. Flag-based properties are IsDraft, IsSubmitted, IsUnmodified, IsResend, and IsFromMe.  <br/> |
|ErrorInvalidPropertyForOperation  <br/> |Act on a property of an item or folder that is not supported by the operation.  <br/> |Updating your code to not access the property with the operation that caused the error.  <br/> |
|ErrorInvalidPropertyRequest  <br/> |Specify a property in the request that is not supported for the item type.  <br/> |Updating your code to not try to access the property with the operation.  <br/> |
|ErrorInvalidPropertySet  <br/> |Set a read-only property.  <br/> |Updating your code to not try to set the property.  <br/> |
|ErrorInvalidValueForProperty  <br/> |Compare a property value in a search restriction where the comparison value does not match the property type.  <br/> |Updating your code to check for property type mismatch.  <br/> |
|ErrorItemSavePropertyError  <br/> |Save an item or folder with invalid property values.  <br/> |Checking the property values and types before submitting them in a request.  <br/> |
|ErrorNoFolderClassOverride  <br/> |Set the folder class on a new folder that is not the base folder type.  <br/> |Using a generic folder type to set the folder class.  <br/> |
|ErrorNoPropertyTagForCustomProperties  <br/> |Reference a custom extended property by its property tag.  <br/> |Updating your code to reference the custom extended property by property set identifier and either the property name or property dispatch identifier.  <br/> |
|ErrorObjectTypeChanged  <br/> |Set or update the item class on an item that doesn't match with its schema type.  <br/> |Updating your code so that item class matches the item schema type.  <br/> |
|ErrorPropertyUpdate  <br/> |Update a property with an invalid property value.  <br/> |Checking the property value before submitting it in an [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) request.  <br/> |
|ErrorRequiredPropertyMissing  <br/> |Send a CreateAttachment request that is missing a required property.  <br/> |Updating your code to set the missing property as specified by the property path returned in the response.  <br/> |
|ErrorUnsupportedMapiPropertyType  <br/> |Use extended property types of type object, object array, error or null.  <br/> |Updating your code to not use the restricted extended property types.  <br/> |
|ErrorUnsupportedPathForQuery  <br/> |Use an unsupported property path in a search restriction.  <br/> |Changing the search restriction to exclude the unsupported property path.  <br/> |
|ErrorUnsupportedPathForSortGroup  <br/> |Use an unsupported property path in a sorted or grouped search request.  <br/> |Changing the search restriction to exclude the unsupported property path.  <br/> |
|ErrorUnsupportedTypeForConversion  <br/> |Request a property type that cannot be converted to XML for EWS to return in a response.  <br/> |Updating your code to not request the unsupported property.  <br/> |
|ErrorUpdatePropertyMismatch  <br/> |Update an item or folder the change description for which doesn't match the property that is specified to be updated.  <br/> |Changing your code so that the change description matches the item or folder type that is being updated.  <br/> |
   
## See also


- [Properties and extended properties in EWS in Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [Develop web service clients for Exchange](develop-web-service-clients-for-exchange.md)
    

