---
title: Var, VarP Functions (Microsoft Access SQL)
keywords: jetsql40.chm5278829
f1_keywords:
- jetsql40.chm5278829
ms.prod: access
ms.assetid: 2cac402d-8384-0b33-c203-f493281a95f1
ms.date: 06/08/2017
---


# Var, VarP Functions (Microsoft Access SQL)

**Applies to:** Access 2013 | Access 2016

Return estimates of the variance for a population or a population sample represented as a set of values contained in a specified field on a query.

## Syntax
<a name="sectionSection0"> </a>

**Var(_expr_)**

**VarP(_expr_)**

The  _expr_ placeholder represents a string expression identifying the field that contains the numeric data you want to evaluate or an expression that performs a calculation using the data in that field. Operands in _expr_ can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).


## Remarks
<a name="sectionSection1"> </a>

The  **VarP** function evaluates a population, and the **Var** function evaluates a population sample.

If the underlying query contains fewer than two records, the  **Var** and **VarP** functions return a **Null** value, which indicates that a variance cannot be calculated.

You can use the  **Var** and **VarP** functions in a query expression or in an SQL statement.


## Example
<a name="sectionSection2"> </a>

This example uses the Orders table to estimate the variance of freight costs for orders shipped to the United Kingdom.

This example calls the EnumFields procedure, which you can find in the SELECT statement example.

```vb
Sub VarX() 
 
    Dim dbs As Database, rst As Recordset 
 
    ' Modify this line to include the path to Northwind 
    ' on your computer. 
    Set dbs = OpenDatabase("Northwind.mdb") 
 
    ' Calculate the variance of freight costs for  
    ' orders shipped to the United Kingdom.  
    Set rst = dbs.OpenRecordset("SELECT " _ 
        &; "Var(Freight) " _ 
        &; "AS [UK Freight Variance] " _ 
        &; "FROM Orders WHERE ShipCountry = 'UK';") 
 
    ' Populate the Recordset. 
    rst.MoveLast 
     
    ' Call EnumFields to print the contents of the  
    ' Recordset. Pass the Recordset object and desired 
    ' field width. 
    EnumFields rst, 20 
     
    Debug.Print 
     
    Set rst = dbs.OpenRecordset("SELECT " _ 
        &; "VarP(Freight) " _ 
        &; "AS [UK Freight VarianceP] " _ 
        &; "FROM Orders WHERE ShipCountry = 'UK';") 
 
    ' Populate the Recordset. 
    rst.MoveLast 
 
    ' Call EnumFields to print the contents of the  
    ' Recordset. Pass the Recordset object and desired 
    ' field width. 
    EnumFields rst, 20 
 
    dbs.Close 
 
End Sub 

```

## See also

- [Access for developers forum on MSDN](https://social.msdn.microsoft.com/Forums/office/en-US/home?forum=accessdev)
- [Access help on support.office.com](https://support.office.com/search/results?query=Access)
- [Access help on answers.microsoft.com](https://answers.microsoft.com/en-us/office/forum/access?page=1&;tab=question&;status=all&;auth=1)
- [Search for specific Access error codes on Bing](https://www.bing.com/)
- [Access forums on UtterAccess](https://www.utteraccess.com/forum/index.php?act=idx)
- [Access wiki on UtterAcess](https://www.utteraccess.com/forum/index.php?act=idx)
- [Access developer and VBA programming help center (FMS)](https://www.fmsinc.com/MicrosoftAccess/developer/)
- [Access posts on StackOverflow](https://stackoverflow.com/questions/tagged/ms-access)

