---
title: "_byteswap_uint64、_byteswap_ulong、_byteswap_ushort | Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _byteswap_uint64
- _byteswap_ulong
- _byteswap_ushort
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-utility-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- byteswap_ulong
- _byteswap_ulong
- byteswap_uint64
- _byteswap_ushort
- _byteswap_uint64
- byteswap_ushort
dev_langs: C++
helpviewer_keywords:
- _byteswap_uint64 function
- byteswap_uint64 function
- swapping bytes
- byte swapping
- byteswap_ushort function
- _byteswap_ushort function
- bytes, swapping
- byteswap_ulong function
- _byteswap_ulong function
ms.assetid: 83bda211-f02f-4cf0-8a78-d6de1f175970
caps.latest.revision: "14"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 288747c372ddb01d293b6c702e8a91cc9acfc665
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="byteswapuint64-byteswapulong-byteswapushort"></a>_byteswap_uint64、_byteswap_ulong、_byteswap_ushort
颠倒整数中的字节顺序。  
  
## <a name="syntax"></a>语法  
  
```  
unsigned short _byteswap_ushort (  
   unsigned short val  
);  
unsigned long _byteswap_ulong (  
   unsigned long val  
);  
unsigned __int64 _byteswap_uint64 (  
   unsigned __int64 val  
);  
```  
  
#### <a name="parameters"></a>参数  
 `val`  
 要颠倒字节顺序的整数。  
  
## <a name="requirements"></a>惠?  
  
|例程所返回的值|必需的标头|  
|-------------|---------------------|  
|`_byteswap_ushort`|\<stdlib.h>|  
|`_byteswap_ulong`|\<stdlib.h>|  
|`_byteswap_uint64`|\<stdlib.h>|  
  
 有关更多兼容性信息，请参见“简介”中的 [兼容性](../../c-runtime-library/compatibility.md) 。  
  
## <a name="example"></a>示例  
  
```  
// crt_byteswap.c  
#include <stdlib.h>  
  
int main()  
{  
   unsigned __int64 u64 = 0x0102030405060708;  
   unsigned long ul = 0x01020304;  
  
   printf("byteswap of %I64x = %I64x\n", u64, _byteswap_uint64(u64));  
   printf("byteswap of %Ix = %Ix", ul, _byteswap_ulong(ul));  
}  
```  
  
```Output  
byteswap of 102030405060708 = 807060504030201  
byteswap of 1020304 = 4030201  
```  
  
## <a name="see-also"></a>请参阅  
 [按类别分的运行时例程](../../c-runtime-library/run-time-routines-by-category.md)