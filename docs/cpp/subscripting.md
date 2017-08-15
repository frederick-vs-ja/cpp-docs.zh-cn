---
title: "下标 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "数组 [C++], 下标 "
  - "运算符重载, 示例"
  - "运算符 [C++], 重载"
  - "下标运算符"
  - "下标运算符, 重载的"
  - "下标 "
ms.assetid: eb151281-6733-401d-9787-39ab6754c62c
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 8
---
# 下标
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

下标运算符 \(**\[ \]**\)（如函数调用运算符）被视为二元运算符。  下标运算符必须是采用单个参数的非静态成员函数。  此参数可以是任何类型，并指定所需的数组下标。  
  
## 示例  
 以下示例演示如何创建用于实现边界检查的 `int` 类型的矢量：  
  
```  
// subscripting.cpp  
// compile with: /EHsc  
#include <iostream>  
  
using namespace std;  
class IntVector {  
public:  
   IntVector( int cElements );  
   ~IntVector() { delete [] _iElements; }  
   int& operator[](int nSubscript);  
private:  
   int *_iElements;  
   int _iUpperBound;  
};  
  
// Construct an IntVector.  
IntVector::IntVector( int cElements ) {  
   _iElements = new int[cElements];  
   _iUpperBound = cElements;  
}  
  
// Subscript operator for IntVector.  
int& IntVector::operator[](int nSubscript) {  
   static int iErr = -1;  
  
   if( nSubscript >= 0 && nSubscript < _iUpperBound )  
      return _iElements[nSubscript];  
   else {  
      clog << "Array bounds violation." << endl;  
      return iErr;  
   }  
}  
  
// Test the IntVector class.  
int main() {  
   IntVector v( 10 );  
   int i;  
  
   for( i = 0; i <= 10; ++i )  
      v[i] = i;  
  
   v[3] = v[9];  
  
   for ( i = 0; i <= 10; ++i )  
      cout << "Element: [" << i << "] = " << v[i] << endl;  
}  
```  
  
  **Array bounds violation.**  
**Element: \[0\] \= 0**  
**Element: \[1\] \= 1**  
**Element: \[2\] \= 2**  
**Element: \[3\] \= 9**  
**Element: \[4\] \= 4**  
**Element: \[5\] \= 5**  
**Element: \[6\] \= 6**  
**Element: \[7\] \= 7**  
**Element: \[8\] \= 8**  
**Element: \[9\] \= 9**  
**Array bounds violation.**  
**Element: \[10\] \= 10**   
## 注释  
 当 `i` 在前一个程序中达到 10 时，`operator[]` 将检测是否在使用超出边界的下标并发出错误消息。  
  
 请注意，函数 `operator[]` 将返回引用类型。  这会使它成为左值，从而使您可以在赋值运算符的任何一侧使用下标表达式。  
  
## 请参阅  
 [运算符重载](../cpp/operator-overloading.md)