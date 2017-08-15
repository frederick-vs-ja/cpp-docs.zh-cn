---
title: "使用数目可变的参数调用 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- arguments [C++], function
- arguments [C++], variable number of
- VARARGS.H
- ellipses (...), variable number of arguments
- STDARGS.H
- function calls, arguments
- '... ellipsis'
- function calls, variable number of arguments
ms.assetid: 8808fb26-4822-42f5-aba3-ac64b54e151b
caps.latest.revision: 7
author: mikeblome
ms.author: mblome
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Human Translation
ms.sourcegitcommit: d6eb43b2e77b11f4c85f6cf7e563fe743d2a7093
ms.openlocfilehash: 8b6b922ecbbeafe1f97025861ae9e8b933a9226c
ms.contentlocale: zh-cn
ms.lasthandoff: 05/18/2017

---
# <a name="calls-with-a-variable-number-of-arguments"></a>使用数目可变的自变量调用
部分参数列表可由省略号表示法（一个逗号后跟三个句点 (, ...) 终止，以指示可能有多个自变量传递给函数，但没有有关这些自变量的详细信息。 对此类自变量不执行类型检查。 省略号表示法前面必须至少有一个参数，并且省略号表示法必须是参数列表中的最后一个标记。 如果没有省略号表示法，当函数收到除参数列表中声明的参数以外的参数时，该函数的行为是不确定的。  
  
 若要调用具有可变数量的参数的函数，只需在函数调用中指定任意数量的参数即可。 一个示例是 C 运行库中的 `printf` 函数。 函数调用必须包含参数列表或参数类型列表中声明的每个类型名称的一个参数。  
  
 除非指定 `__fastcall` 调用约定，否则函数调用中指定的所有参数都将位于堆栈上。 为函数声明的形参的数量决定了从堆栈获取和分配给形参的实参的数量。 您负责从堆栈中检索任何其他参数和确定应存在的参数数量。 STDARG.H 文件包含 ANSI 样式宏，该宏用于访问采用可变数量的参数的函数的参数。 此外，VARARGS.H 中的 XENIX 样式宏仍受支持。  
  
 以下示例声明用于调用可变数量的自变量的函数：  
  
```  
int average( int first, ...);  
```  
  
## <a name="see-also"></a>另请参阅  
 [函数调用](../c-language/function-calls.md)