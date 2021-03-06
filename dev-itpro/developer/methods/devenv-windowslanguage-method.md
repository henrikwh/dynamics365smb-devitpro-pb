---
title: "WINDOWSLANGUAGE Method"
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.assetid: 07ed58f1-0fa9-47c4-97ef-10ebc52d4fe9
author: SusanneWindfeldPedersen
manager: edupont
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# WINDOWSLANGUAGE Method
Gets the current Windows language setting.  
  
## Syntax  
  
```  
  
LanguageID := WINDOWSLANGUAGE  
```  
  
## Property Value/Return Value  
 Type: Integer  
  
## Remarks  
 The *LanguageID* is a standard Windows language ID. The Windows Language virtual table contains a list of these IDs and the corresponding names and short names.  
  
 For more information, see [Multilanguage Development](../devenv-multilanguage-development.md).  
  
## See Also  
 [GLOBALLANGUAGE Method](devenv-GLOBALLANGUAGE-Method.md)