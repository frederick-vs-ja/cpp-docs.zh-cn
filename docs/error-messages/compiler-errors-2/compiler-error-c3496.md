---
title: "编译器错误 C3496 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C3496
dev_langs: C++
helpviewer_keywords: C3496
ms.assetid: e19885f2-677f-4c1e-bc69-e35852262dc3
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: e8e5e441011c69e2b50b4565981d89a7730d542f
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3496"></a>编译器错误 C3496
“this”始终按值捕获: 已忽略“&”  
  
 不能按引用捕获 `this` 指针。  
  
### <a name="to-correct-this-error"></a>更正此错误  
  
-   按值捕获 `this` 指针。  
  
## <a name="example"></a>示例  
 下面的示例将生成 C3496，因为 lambda 表达式的捕获列表中出现了对 `this` 指针的引用：  
  
```  
// C3496.cpp  
// compile with: /c  
  
class C  
{  
   void f()  
   {  
      [&this] {}(); // C3496  
   }  
};  
```  
  
## <a name="see-also"></a>请参阅  
 [Lambda 表达式](../../cpp/lambda-expressions-in-cpp.md)