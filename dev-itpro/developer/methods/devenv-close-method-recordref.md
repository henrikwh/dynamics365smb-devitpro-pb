---
title: "CLOSE Method (RecordRef)"
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.assetid: 4726d978-e289-45ce-96b2-a666078bc71c
author: SusanneWindfeldPedersen
manager: edupont
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# CLOSE Method (RecordRef)
Closes the current page or table.  
  
## Syntax  
  
```  
  
RecordRef.CLOSE  
```  
  
#### Parameters  
 *RecordRef*  
 Type: RecordRef  
  
 The RecordRef of a record in the table that you want to close.  
  
## Remarks  
 You must use this method if you have several recordrefs defined as variables because these will be maintained until the variable gets out of scope.  
  
## Example  
 The following example opens tables 3 through 10 as a Recordref variable that is named MyRecordRef. For each table that is open, the [CAPTION Method \(RecordRef\)](devenv-CAPTION-Method-RecordRef.md) retrieves the caption of the table and displays the table number and the caption in a messages box. After each caption is displayed, the CLOSE method closes the table before the next table is open. This example requires that you create the following global variables and text constants.  
  
|Variable name|DataType|  
|-------------------|--------------|  
|MyRecordRef|RecordRef|  
|varCaption|Text|  
|i|Integer|  
  
|Text constant name|DataType|ENU value|  
|------------------------|--------------|---------------|  
|Text000|Text|Table No: %1 Caption: %2|  
  
```  
FOR i := 3 TO 10 DO BEGIN  
MyRecordRef.OPEN(i);  
varCaption := MyRecordRef.CAPTION;  
MESSAGE(Text000, i, varCaption);  
MyRecordRef.CLOSE;  
END;  
```  
  
## See Also  
 [RecordRef Data Type](../datatypes/devenv-RecordRef-Data-Type.md)