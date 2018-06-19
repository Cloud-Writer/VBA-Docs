---
title: Areas.Creator Property (Excel)
keywords: vbaxl10.chm196074
f1_keywords:
- vbaxl10.chm196074
ms.prod: excel
api_name:
- Excel.Areas.Creator
ms.assetid: 0a612f3d-437c-95f2-ea15-042017ba941b
ms.date: 06/08/2017
---


# Areas.Creator Property (Excel)

Returns a 32-bit integer that indicates the application in which this object was created. Read-only  **Long** .


## Syntax

 _expression_ . **Creator**

 _expression_ A variable that represents an **Areas** object.


## Remarks

If the object was created in Microsoft Excel, this property returns the string XCEL, which is equivalent to the hexadecimal number 5843454C. The  **Creator** property is designed to be used in Microsoft Excel for the Macintosh, where each application has a four-character creator code. For example, Microsoft Excel has the creator code XCEL.


## See also


[Areas Collection](Excel.Areas.md)
