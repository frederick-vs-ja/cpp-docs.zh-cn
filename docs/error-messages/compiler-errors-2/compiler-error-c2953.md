---
title: "编译器错误 C2953 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C2953"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2953"
ms.assetid: 8dbcfa24-8296-4e40-bdc4-5526c07d8892
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# 编译器错误 C2953
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

“identifier”：类模板已经定义  
  
 检查源文件并包含其他定义的文件。  
  
 以下示例生成 C2953：  
  
```  
// C2953.cpp // compile with: /c template <class T>  class A {}; template <class T>  class A {};   // C2953 template <class T>  class B {};   // OK  
```