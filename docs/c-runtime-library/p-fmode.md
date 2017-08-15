---
title: "__p__fmode |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- __p__fmode
apilocation:
- msvcr80.dll
- msvcr120.dll
- msvcr90.dll
- msvcrt.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr100.dll
apitype: DLLExport
f1_keywords:
- __p__fmode
dev_langs:
- C++
helpviewer_keywords:
- __p__fmode
ms.assetid: 1daa1394-81eb-43aa-a71b-4cc6acf3207b
caps.latest.revision: 3
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Human Translation
ms.sourcegitcommit: d6eb43b2e77b11f4c85f6cf7e563fe743d2a7093
ms.openlocfilehash: 56f18d9d1912465161cb62b9d95e1c3a477a739d
ms.contentlocale: zh-cn
ms.lasthandoff: 05/18/2017

---
# <a name="pfmode"></a>__p__fmode
指向 `_fmode` 全局变量，该变量为文件 I/O 操作指定默认的*文件转换模式*。  
  
## <a name="syntax"></a>语法  
  
```cpp  
int* __p__fmode(  
   );  
```  
  
## <a name="return-value"></a>返回值  
 指向 `_fmode` 全局变量的指针。  
  
## <a name="remarks"></a>备注  
 `__p__fmode` 函数仅供内部使用，且不应从用户代码调用它。  
  
 文件转换模式为 [_open](../c-runtime-library/reference/open-wopen.md) 和 [_pipe](../c-runtime-library/reference/pipe.md) I/O 操作指定 `binary` 或 `text` 转换。 有关详细信息，请参阅 [_fmode](../c-runtime-library/fmode.md)。  
  
## <a name="requirements"></a>要求  
  
|例程|必需的标头|  
|-------------|---------------------|  
|__p\__fmode|stdlib.h|