---
title: "编译器错误 C2892 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2892
dev_langs: C++
helpviewer_keywords: C2892
ms.assetid: c22a5084-2f50-42c2-a56b-6dfe5442edc9
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 371305a8137b169caad9649b2f78d77663013a5e
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2892"></a>编译器错误 C2892
局部类不应具有成员模板  
  
 模板化成员函数不是有效的类中定义的函数中的。  
  
 下面的示例生成 C2892:  
  
```  
// C2892.cpp  
int main() {  
   struct local {  
      template<class T>   // C2892  
      void f() {}  
   };  
}  
```