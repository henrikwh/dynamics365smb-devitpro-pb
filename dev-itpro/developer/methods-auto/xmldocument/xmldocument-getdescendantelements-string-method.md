---
title: "GetDescendantElements Method"
ms.author: solsen
ms.custom: na
ms.date: 11/02/2018
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
# GetDescendantElements Method
Gets a list containing the descendant elements for this document, in document order.

## Syntax
```
DescendantElements :=   XmlDocument.GetDescendantElements(Name: String)
```
## Parameters
*XmlDocument*  
&emsp;Type: [XmlDocument](xmldocument-data-type.md)  
An instance of the [XmlDocument](xmldocument-data-type.md) data type.  

*Name*  
&emsp;Type: [String](../string/string-data-type.md)  
The fully qualified name of the elements to retrieve.  


## Return Value
*DescendantElements*  
&emsp;Type: [XmlNodeList](../xmlnodelist/xmlnodelist-data-type.md)  
A list containing the descendant elements for this document, in document order.  


[//]: # (IMPORTANT: END>DO_NOT_EDIT)
## See Also
[XmlDocument Data Type](xmldocument-data-type.md)  
[Getting Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)