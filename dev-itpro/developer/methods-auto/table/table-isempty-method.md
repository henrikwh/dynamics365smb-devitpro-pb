---
title: "IsEmpty Method"
ms.author: solsen
ms.custom: na
ms.date: 11/06/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: "dynamics365-business-central"
author: solsen
---
[//]: # (START>DO_NOT_EDIT)
[//]: # (IMPORTANT:Do not edit any of the content between here and the END>DO_NOT_EDIT.)
[//]: # (Any modifications should be made in the .xml files in the ModernDev repo.)
# IsEmpty Method
Determines whether a table or a filtered set of records is empty.

## Syntax
```
Empty :=   Table.IsEmpty()
```
> [!NOTE]  
> This method can be invoked using property access syntax.  

## Parameters
*Table*  
&emsp;Type: [Table](table-data-type.md)  
An instance of the [Table](table-data-type.md) data type.  

## Return Value
*Empty*  
&emsp;Type: [Boolean](../boolean/boolean-data-type.md)  
  


[//]: # (IMPORTANT: END>DO_NOT_EDIT)

## Remarks  
 **True** if the record or table is empty; otherwise, **false**. If you have applied filters, the method determines whether the filtered set of records is empty. The number of filters that you have applied to the records affects the speed of the **ISEMPTY** method. The fewer the number of filters, the faster the operation is performed.  
  
 When you are using SQL Server, this method is faster than using the [COUNT Method \(Record\)](../../methods/devenv-count-method-record.md) and then testing the result for zero.  
  
## Example  
 The following code example uses a record from the **Customer** table to determine whether the table has any records. The **ISEMPTY** method uses the CustomerRec variable to determine whether the **Customer** table is empty, stores the return value in the varIsEmpty variable, and displays the value in a message box. The value of the varIsEmpty variable is **false** because the **Customer** table has records \(that is, not empty\). The method then uses the PrinterSelec variable, which is a record from the **Printer Selection** table to check whether the **Printer Selection** table has any records and stores the return value in the varIsEmpty variable. The value of **true** is displayed in the message box because the **Printer Selection** table has no records \(that is, empty\). This example requires that you create the following global variables.  
  
|Variable name|Data Type|Subtype|  
|-------------------|---------------|-------------|  
|CustomerRec|Record|Customer|  
|PrinterSelec|Record|Printer Selection|  
|varIsEmpty|Boolean|Not applicable|  
  
```  
varIsEmpty := CustomerRec.ISEMPTY;  
MESSAGE('Is the Customer table empty?: %1', varIsEmpty);  
varIsEmpty := PrinterSelec.ISEMPTY;  
MESSAGE('Is the Printer Selection table empty?: %1', varIsEmpty);  
```  
  

## See Also
[Table Data Type](table-data-type.md)  
[Getting Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)