---
title: "C 杂注 | Microsoft Docs"
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
- pragmas, C/C++
ms.assetid: 3d6d36b4-d565-4632-a4cd-e39aeaded5ad
caps.latest.revision: 13
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
ms.openlocfilehash: b511f6f1d7f9fab0b45f345e39e1251df520624f
ms.contentlocale: zh-cn
ms.lasthandoff: 05/18/2017

---
# <a name="c-pragmas"></a>C 杂注
**Microsoft 专用**  
  
 “杂注”指示编译器在编译时执行特定操作。 杂注随编译器的不同而不同。 例如，可以使用 optimize 杂注来设置要在程序中执行的优化。 Microsoft C 杂注为：  
  
|||||  
|-|-|-|-|  
|**alloc_text**|**data_seg**|**inline_recursion**|**setlocale**|  
|**auto_inline**|**函数**|**intrinsic**|**warning**|  
|**check_stack**|**hdrstop**|**message**||  
|**code_seg**|**include_alias**|**optimize**||  
|**comment**|**inline_depth**|**pack**||  
  
 有关 Microsoft C 编译器杂注的说明，请参阅《预处理器参考》*中的* [Pragma 指令和 __Pragma 关键字](../preprocessor/pragma-directives-and-the-pragma-keyword.md)。  
  
 **结束 Microsoft 专用**  
  
## <a name="see-also"></a>另请参阅  
 [源文件和源程序](../c-language/source-files-and-source-programs.md)