---
title: "编译器错误 C3036 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3036"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3036"
ms.assetid: 10c6993e-bc42-4a07-85c7-cdc34ac30906
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# 编译器错误 C3036
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

“operator”：OpenMP“reduction”子句中的运算符标记无效  
  
 未正确指定 [reduction](../../parallel/openmp/reference/reduction.md) 子句。  
  
 下面的示例生成 C3036：  
  
```  
// C3036.cpp // compile with: /openmp static float a[1000], b[1000], c[1000]; void test1(int first, int last) { static float dp = 0.0f; #pragma omp for nowait reduction(.:dp)   // C3036 // try the following line instead // #pragma omp for nowait reduction(+: dp) for (int i = first ; i <= last ; ++i) dp += a[i] * b[i]; }  
```