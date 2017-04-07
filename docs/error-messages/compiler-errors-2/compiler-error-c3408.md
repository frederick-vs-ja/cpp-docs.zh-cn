---
title: "编译器错误 C3408 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3408"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3408"
ms.assetid: 1f5ea979-fb1e-4214-b310-6fd6ca8249b1
caps.latest.revision: 12
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 12
---
# 编译器错误 C3408
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

“attribute”：模板定义中不允许使用特性  
  
 特性不能应用于模板定义。  
  
## 示例  
 以下示例生成 C3408。  
  
```  
// C3408.cpp // compile with: /c template <class T> struct PTS { enum { IsPointer = 0, IsPointerToDataMember = 0 }; }; template <class T> [coclass]   // C3408 struct PTS<T*> { enum { IsPointer = 1, IsPointerToDataMember = 0 }; }; template <class T, class U> struct PTS<T U::*> { enum { IsPointer = 1, IsPointerToDataMember = 1 }; }; struct S{}; extern "C" int printf(const char*,...); int main() { S s, *pS; int S::*ptm; printf("PTS<S>::IsPointer == %d PTS<S>::IsPointerToDataMember == %d\n", PTS<S>::IsPointer, PTS<S>:: IsPointerToDataMember); printf("PTS<S*>::IsPointer == %d PTS<S*>::IsPointerToDataMember == %d\n", PTS<S*>::IsPointer, PTS<S*>:: IsPointerToDataMember); printf("PTS<int S::*>::IsPointer == %d PTS<int S::*>::IsPointerToDataMember == %d\n", PTS<int S::*>::IsPointer, PTS<int S::*>:: IsPointerToDataMember); }  
```