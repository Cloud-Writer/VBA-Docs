---
title: Tab Object (Excel)
keywords: vbaxl10.chm722072
f1_keywords:
- vbaxl10.chm722072
ms.prod: excel
api_name:
- Excel.Tab
ms.assetid: c6555e96-b96e-54d8-b8c6-5ab13c256d97
ms.date: 06/08/2017
---


# Tab Object (Excel)

Represents a tab in a chart or a worksheet.


## Remarks

Use the  **[Tab](Excel.Chart.Tab.md)** property of the **[Chart](Excel.Chart(object).md)** object or **[Worksheet](Excel.Worksheet.md)** object to return a **Tab** object.

Once a  **Tab** object is returned, you can use the **[ColorIndex](Excel.Tab.ColorIndex.md)** property determine the settings of a tab for a chart or worksheet.


## Example

In the following example, Microsoft Excel determines if the worksheet's first tab color index is set to none and notifies the user.


```vb
Sub CheckTab() 
 
 ' Determine if color index of 1st tab is set to none. 
 If Worksheets(1).Tab.ColorIndex = xlColorIndexNone Then 
 MsgBox "The color index is set to none for the first " &; _ 
 "worksheet tab." 
 Else 
 MsgBox "The color index for the tab of the first worksheet " &; _ 
 "is not set none." 
 End If 
 
End Sub
```


## See also


[Excel Object Model Reference](./overview/Excel/object-model.md)


