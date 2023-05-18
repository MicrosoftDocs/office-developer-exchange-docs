---
title: "ExtendedFieldURI"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.service: office-online-server
ms.technology: ews
ms.localizationpriority: medium
api_name:
- ExtendedFieldURI
api_type:
- schema
ms.assetid: b3c6ea3a-9ead-44b9-9d99-64ecf12bde23
description: "The ExtendedFieldURI element identifies an extended MAPI property."
---

# ExtendedFieldURI

The **ExtendedFieldURI** element identifies an extended MAPI property. 
  
```xml
<ExtendedFieldURI DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" />
```

**PathToExtendedFieldType**

## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**DistinguishedPropertySetId** <br/> |Defines the well-known property set IDs for extended MAPI properties.<br/><br/>If this attribute is used, the **PropertySetId** and **PropertyTag** attributes cannot be used. This attribute must be used with either the **PropertyId** or **PropertyName** attribute, and the **PropertyType** attribute.<br/><br/>The **DistinguishedPropertySetId** Attribute table later in this topic lists the possible values for this attribute.<br/><br/>This attribute is optional.  <br/> |
|**PropertySetId** <br/> |Identifies a MAPI extended property set or namespace by its identifying GUID.<br/><br/>If this attribute is used, the **DistinguishedPropertySetId** and **PropertyTag** attribute cannot be used. This attribute must be used with either the **PropertyId** or **PropertyName** attribute, and the **PropertyType** attribute.<br/><br/>This attribute is optional.  <br/> |
|**PropertyTag** <br/> |Identifies the property tag without the type part of the tag. The **PropertyTag** can be represented as either a hexadecimal or a short integer.<br/><br/>The range between 0x8000 and 0xFFFE represents the custom range of properties. When a mailbox database encounters a custom property for the first time, it assigns that custom property a property tag within the custom property range of 0x8000-0xFFFE. A given custom property tag will most likely differ across databases. Therefore, a custom property request by property tag can return different properties on different databases. The use of the **PropertyTag** attribute is prohibited for custom properties. Instead, use the **PropertySetId** attribute and the **PropertyName** or **PropertyId** attribute.<br/><br/>**IMPORTANT**: Access any custom property between 0x8000 and 0xFFFE by using the GUID + name/ID. If the **PropertyTag** attribute is used, the **DistinguishedPropertySetId**, **PropertySetId**, **PropertyName**, and **PropertyId** attributes cannot be used.<br/><br/>This attribute is optional.<br/><br/>**NOTE**: You cannot use a property tag attribute for properties within the custom range 0x8000-0xFFFE. You must use a named property in this case.           |
|**PropertyName** <br/> |Identifies an extended property by its name. This property must be coupled with either **DistinguishedPropertySetId** or **PropertySetId**.<br/><br/>If this attribute is used, the **PropertyId** and **PropertyTag** attributes cannot be used.<br/><br/>This attribute is optional.  <br/> |
|**PropertyId** <br/> |Identifies an extended property by its dispatch ID. The dispatch ID can be identified in either decimal or hexadecimal formats. This property must be coupled with either **DistinguishedPropertySetId** or **PropertySetId**.<br/><br/>If this attribute is used, the **PropertyName** and **PropertyTag** attributes cannot be used.<br/><br/>This attribute is optional.  <br/> |
|**PropertyType** <br/> |Represents the property type of a property tag. This corresponds to the least significant word in a property tag.<br/><br/>The PropertyType Attribute table later in this topic contains the possible values for this attribute.<br/><br/>This attribute is required.  <br/> |
   
#### DistinguishedPropertySetId Attribute

|**Value**|**Description**|
|:-----|:-----|
|Address  <br/> |Identifies the address property set ID by name.  <br/> |
|Appointment  <br/> |Identifies the appointment property set ID by name.  <br/> |
|CalendarAssistant  <br/> |Identifies the calendar assistant property set ID by name.  <br/> |
|Common  <br/> |Identifies the common property set ID by name.  <br/> |
|InternetHeaders  <br/> |Identifies the Internet headers property set ID by name.  <br/> |
|Meeting  <br/> |Identifies the meeting property set ID by name.  <br/> |
|Sharing  <br/> | <br/> |
|PublicStrings  <br/> |Identifies the public strings property set ID by name.  <br/> |
|Task  <br/> |Identifies the task property set ID by name.  <br/> |
|UnifiedMessaging  <br/> |Identifies the unified messaging property set ID by name.  <br/> |
   
#### PropertyType Attribute

|**Value**|**Description**|
|:-----|:-----|
|ApplicationTime  <br/> |A double value that is interpreted as a date and time. The integer part is the date and the fraction part is the time.  <br/> |
|ApplicationTimeArray  <br/> |An array of double values that are interpreted as a date and time.  <br/> |
|Binary  <br/> |A Base64-encoded binary value.  <br/> |
|BinaryArray  <br/> |An array of Base64-encoded binary values.  <br/> |
|Boolean  <br/> |A Boolean **true** or **false**.  <br/> |
|CLSID  <br/> |A GUID string.  <br/> |
|CLSIDArray  <br/> |An array of GUID strings.  <br/> |
|Currency  <br/> |A 64-bit integer that is interpreted as the number of cents.  <br/> |
|CurrencyArray  <br/> |An array of 64-bit integers that are interpreted as the number of cents.  <br/> |
|Double  <br/> |A 64-bit floating-point value.  <br/> |
|DoubleArray  <br/> |An array of 64-bit floating-point values.  <br/> |
|Error  <br/> |SCODE value; 32-bit unsigned integer.  <br/> Not used for restrictions or for getting/setting values. This exists only for reporting.  <br/> |
|Float  <br/> |A 32-bit floating-point value.  <br/> |
|FloatArray  <br/> |An array of 32-bit floating-point values.  <br/> |
|Integer  <br/> |A signed 32-bit (Int32) integer.  <br/> |
|IntegerArray  <br/> |An array of signed 32-bit (Int32) integers.  <br/> |
|Long  <br/> |A signed or unsigned 64-bit (Int64) integer.  <br/> |
|LongArray  <br/> |An array of signed or unsigned 64-bit (Int64) integers.  <br/> |
|Null  <br/> |Indicates no property value.  <br/> Not used for restrictions or for getting/setting values. This exists only for reporting.  <br/> |
|Object  <br/> |A pointer to an object that implements the IUnknown interface.  <br/> Not used for restrictions or for getting/setting values. This exists only for reporting.  <br/> |
|ObjectArray  <br/> |An array of pointers to objects that implement the IUnknown interface.  <br/> Not used for restrictions or for getting/setting values. This exists only for reporting.  <br/> |
|Short  <br/> |A signed 16-bit integer.  <br/> |
|ShortArray  <br/> |An array of signed 16-bit integers.  <br/> |
|SystemTime  <br/> |A 64-bit integer data and time value in the form of a FILETIME structure.  <br/> |
|SystemTimeArray  <br/> |An array of 64-bit integer data and time values in the form of a FILETIME structure.  <br/> |
|String  <br/> |A Unicode string.  <br/> |
|StringArray  <br/> |An array of Unicode strings.  <br/> |
   
### Child elements

None.
  
### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ExtendedProperty](extendedproperty.md) <br/> |Identifies extended properties on folders and items.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> | Identifies additional properties.<br/><br/>The following are the XPath expressions to this element:<br/><br/>`/FindFolder/FolderShape/AdditionalProperties` <br/>  `/GetFolder/FolderShape/AdditionalProperties` <br/>  `/SyncFolderHierarchy/FolderShape/AdditionalProperties` <br/>  `/GetItem/ItemShape/AdditionalProperties` <br/>  `/FindItem/ItemShape/AdditionalProperties` <br/>  `/SyncFolderItems/ItemShape/AdditionalProperties` <br/>  `/GetAttachment/AttachmentShape/AdditionalProperties` <br/> |
|[SetItemField](setitemfield.md) <br/> |Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |Represents a delete operation for deleting a given property from an item during an [UpdateItem operation](updateitem-operation.md).  <br/> |
|[DeleteFolderField](deletefolderfield.md) <br/> |Represents a delete operation for deleting a given property from a folder during an UpdateFolder call.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).  <br/> |
|[AppendToFolderField](appendtofolderfield.md) <br/> |Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).  <br/> |
|[Exists](exists.md) <br/> |Represents a search expression that returns **true** if the supplied property exists on an item.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Represents either a property or a constant value to be used when comparing with another property.  <br/> |
|[IsEqualTo](isequalto.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and evaluates to **true** if they are equal.  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater.  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than or equal to the second.  <br/> |
|[IsLessThan](islessthan.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than the second.  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than the second.  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |Represents a search expression that compares a property with either a constant value or another property and returns **true** if the values are not the same.  <br/> |
|[Excludes](excludes.md) <br/> |Performs a bitwise mask of the properties.  <br/> |
|[Contains](contains.md) <br/> |Represents a search expression that determines whether a given property contains the supplied constant string value.  <br/> |
|[FieldOrder](fieldorder.md) <br/> |Represents a single field by which to sort results and indicates the direction for the sort.  <br/> |
   
## Remarks

Some attributes cannot be used in combination with other attributes. Any request that comes in with an invalid combination of extended property attributes will generate an error message.
  
The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
> [!NOTE]
> In Microsoft .NET, a Long is a 64-bit signed integer, while in MAPI and COM, a Long is a 32-bit integer. Most developers will use the Microsoft.NET Framework to develop Exchange Web Services client applications. Therefore, the .NET naming is used instead of the MAPI naming.
> 
> For example, the PR_MESSAGE_FLAGS MAPI property, 0x0E07, is a PT\_LONG type. In .NET, this is considered an integer. An extended property for PR_MESSAGE_FLAGS is defined as `<t:ExtendedFieldURI PropertyTag="0x0E07" PropertyType="Integer"/>`. 
  
## Example

The following example of a request creates an item that has two custom properties. The first custom property is named **IsMyHouse** with a Boolean value set to **true**. The second custom extended property is named **HousePrices**. It contains an array of Currency values. 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
    MessageDisposition="SaveOnly">
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </SavedItemFolderId>
      <Items>
        <t:Item>
          <t:ItemClass>IPM.Note</t:ItemClass>
          <t:Subject>Create an extended property</t:Subject>
          <t:Body BodyType="Text">Added info to extended props</t:Body>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI DistinguishedPropertySetId="PublicStrings" 
                                PropertyName="IsMyHouse" 
                                PropertyType="Boolean"/>
            <t:Value>true</t:Value>
          </t:ExtendedProperty>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI DistinguishedPropertySetId="PublicStrings" 
                                PropertyName="HousePrices" 
                                PropertyType="CurrencyArray"/>
            <t:Values>
              <t:Value>30000000</t:Value>
              <t:Value>40000000</t:Value>
              <t:Value>50000000</t:Value>
            </t:Values>
          </t:ExtendedProperty>
        </t:Item>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

## Element information

|Element|Example|
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

- [FieldURI](fielduri.md)
- [IndexedFieldURI](indexedfielduri.md)
- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

