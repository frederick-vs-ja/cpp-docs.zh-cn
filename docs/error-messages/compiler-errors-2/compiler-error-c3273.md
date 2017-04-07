---
title: "编译器错误 C3273 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3273"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3273"
ms.assetid: 1d2ce9d9-222b-4cab-94e2-d2c1a9f5ebe0
caps.latest.revision: 5
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 5
---
# 编译器错误 C3273
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

\_\_finally 不能用于非托管代码中的异常块。  
  
 下面的示例生成 C3273：  
  
```  
// C3273.cpp // compile with: /GX int main() { try { } catch (int) { } __finally   // C3273, remove __finally clause { } }  
```