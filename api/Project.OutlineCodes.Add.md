---
title: OutlineCodes.Add Method (Project)
ms.prod: project-server
api_name:
- Project.OutlineCodes.Add
ms.assetid: e33dcb6b-90a3-e52c-099a-f0a901b3f3f7
ms.date: 06/08/2017
---


# OutlineCodes.Add Method (Project)

Adds an  **OutlineCode** object to an **OutlineCodes** collection.


## Syntax

 _expression_. `Add`( ` _FieldID_`, ` _Name_` )

 _expression_ A variable that represents an 'OutlineCodes' object.


### Parameters



|**Name**|**Required/Optional**|**Data Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _FieldID_|Required|**Long**| Specifies the type of custom field for the outline code. Can be one of the **[PjCustomField](Project.PjCustomField.md)** constants.|
| _Name_|Required|**String**|The name of the outline code to add.|

### Return Value

 **OutlineCode**


## See also


[OutlineCodes Collection Object](Project.outlinecodes(object).md)
