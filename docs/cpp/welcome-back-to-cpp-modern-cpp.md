---
title: "欢迎回到 C++（现代 C++） | Microsoft Docs"
ms.custom: ""
ms.date: "12/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
ms.assetid: 1cb1b849-ed9c-4721-a972-fd8f3dab42e2
caps.latest.revision: 23
caps.handback.revision: 23
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 欢迎回到 C++（现代 C++）
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

C\+\+ 是世界上最常用的编程语言之一。  正确编写的 C\+\+ 程序快速、高效。  该语言比其他语言更加灵活，因为你可以使用它来创建各种应用，包括有趣刺激的游戏、高性能科学软件、设备驱动程序、嵌入式程序和 Windows 客户端应用。  20 多年来，C\+\+ 已用于解决此类问题和许多其他问题。  你可能不知道，越来越多的 C\+\+ 程序员已经抛弃过时的 C 样式编程，改为使用先进的 C\+\+。  
  
 C\+\+ 的原始要求之一是与 C 语言向后兼容。  从那时起，C\+\+ 经历了几次迭代演变，从带有类的 C 语言发展到原始的 C\+\+ 语言规范，然后又发展到后来的许多增强版本。  由于有此继承，C\+\+ 通常称为多范例编程语言。  在 C\+\+ 中，可进行纯程序性 C 样式编程，此类编程涉及原始指针、数组、以 NULL 结尾的字符串、自定义数据结构，以及可实现卓越性能同时也可能产生 Bug 和复杂性的其他功能。  由于 C 样式编程充满此类风险，因此 C\+\+ 的一个目标就是使程序既类型安全，又更易于编写、扩展和维护。  在早期，C\+\+ 接受面向对象的编程等编程范例。  多年来，此语言中已加入功能并结合了经过高度测试的标准数据结构和算法库。  正是这些新增功能使得实现现代 C\+\+ 样式成为可能。  
  
 现代 C\+\+ 强调：  
  
-   基于堆栈的范围，而非堆或静态全局范围。  
  
-   自动类型推理，而非显式类型名称。  
  
-   智能指针，而非原始指针。  
  
-   `std::string` 和 `std::wstring` 类型（请参见 [\<string\>](../standard-library/string.md)），而非原始 `char[]` 数组。  
  
-   [标准模板库](../standard-library/cpp-standard-library-header-files.md) \(STL\) 容器（例如 `vector`、`list` 和 `map`），而非原始数组或自定义容器。  请参见[\<vector\>](../standard-library/vector.md)、[\<list\>](../standard-library/list.md)和[\< 映射 \>](../standard-library/map.md)。  
  
-   [STL 算法](../standard-library/algorithm.md)，而非手动编码的算法。  
  
-   异常，可报告和处理错误条件。  
  
-   使用 STL `std::atomic<>`（请参见 [\<atomic\>](../standard-library/atomic.md)），而非其他线程间通信机制的无锁线程间通信。  
  
-   内联 [lambda 函数](../cpp/lambda-expressions-in-cpp.md)，而非单独实现的小函数。  
  
-   基于范围的 for 循环，编写以 `for ( for-range-declaration : expression )` 形式使用数组、STL 容器和 [!INCLUDE[wrt](../atl/reference/includes/wrt_md.md)]集合的更可靠循环。  这是核心语言支持的一部分。  有关详细信息，请参阅[基于范围的 for 语句 \(C\+\+\)](../cpp/range-based-for-statement-cpp.md)。  
  
 C\+\+ 语言本身也有所发展。  比较以下代码片段。  下面显示了过去 C\+\+ 的代码片段：  
  
```cpp  
  
// circle and shape are user-defined types  
circle* p = new circle( 42 );   
vector<shape*> v = load_shapes();  
  
for( vector<circle*>::iterator i = v.begin(); i != v.end(); ++i ) {  
    if( *i && **i == *p )  
        cout << **i << “ is a match\n”;  
}  
  
for( vector<circle*>::iterator i = v.begin();  
        i != v.end(); ++i ) {  
    delete *i; // not exception safe  
}  
  
delete p;  
  
```  
  
 以下是用现代 C\+\+ 完成同一操作的代码片段：  
  
```cpp  
  
#include <memory>  
#include <vector>  
// ...  
// circle and shape are user-defined types  
auto p = make_shared<circle>( 42 );  
vector<shared_ptr<shape>> v = load_shapes();  
  
for_each( begin(v), end(v), [&](const shared_ptr<shape>& s) {  
    if( s && *s == *p )  
        cout << *s << " is a match\n";  
} );  
  
```  
  
 在现代 C\+\+ 中，不必使用 new\/delete 或显式异常处理，因为可以使用智能指针来替代。  使用 `auto` 类型推导和 [lambda 函数](../cpp/lambda-expressions-in-cpp.md)时，可以更快地编写代码、加强代码并更好地了解代码。  `for_each` 比 `for` 循环更整洁和易于使用，并且不容易发生意外错误。  可以使用样本和最少行数的代码来编写应用。  你可以确保代码异常安全和内存安全，并且没有要处理的分配\/解除分配或错误代码。  
  
 现代 C\+\+ 整合两种多态性：编译时（通过模板）和运行时（通过继承和虚拟化）。  可以混合使用这两种多态性以增强效果。  STL 模板 `shared_ptr` 使用内部虚拟方法极为轻松地完成类型抹除。  但是，当模板是更好的选择时，请勿过度使用多态性的虚拟化。  模板可以非常强大。  
  
 如果从其他语言（尤其是托管语言，其中大多数类型为引用类型，极少类型为值类型）转换到 C\+\+，请注意 C\+\+ 类在默认情况下是值类型。  但是，你可以将这些 C\+\+ 类指定为引用类型，从而实现多态行为以支持面向对象的编程。  有帮助的观点：值类型与内存和布局控制更相关，而引用类型与支持多态性的基类和虚拟函数更相关。  默认情况下，值类型可以复制，每个值类型都具有一个复制构造函数和一个复制赋值运算符。  指定引用类型时，请将类设为不可复制（禁用复制构造函数和复制赋值运算符），并使用支持多态性的虚拟析构函数。  值类型还与内容有关，复制时，这将提供可单独修改的两个独立值。  但引用类型与标识（即对象类型）有关，因此有时称为多态类型。  
  
 C\+\+ 又一次兴起，因为功能再次占据首要位置。  当程序员的工作效率很重要时，Java 和 C\# 等语言是很好的选择，但当功能和性能至关重要时，此类语言就暴露出了自身限制。  要实现高效率和强大功能，特别是在硬件有限的设备上，现代 C\+\+ 无可匹敌。  
  
 不仅语言现代，开发工具也很现代。  [!INCLUDE[vsprvs](../assembler/masm/includes/vsprvs_md.md)] 可让开发周期的各个部分高效可靠。  开发周期包括应用程序生命周期管理 \(ALM\) 工具、IntelliSense 等 IDE 增强功能、XAML 等工具友好机制，以及生成、调试和许多其他工具。  
  
 此部分文档中的文章提供了有关在编写现代 C\+\+ 程序时最重要的功能和技术的深入指导与最佳做法。  
  
-   [支持 C\+\+11\/14\/17 功能](../cpp/support-for-cpp11-14-17-features-modern-cpp.md)  
  
-   [C\+\+ 类型系统](../cpp/cpp-type-system-modern-cpp.md)  
  
-   [统一安装和委派构造函数](../cpp/uniform-initialization-and-delegating-constructors.md)  
  
-   [对象生存期和资源管理](../cpp/object-lifetime-and-resource-management-modern-cpp.md)  
  
-   [对象所有资源 \(RAII\)](../cpp/objects-own-resources-raii.md)  
  
-   [智能指针](../cpp/smart-pointers-modern-cpp.md)  
  
-   [用于编译时封装的 Pimpl](../cpp/pimpl-for-compile-time-encapsulation-modern-cpp.md)  
  
-   [容器](../cpp/containers-modern-cpp.md)  
  
-   [算法](../cpp/algorithms-modern-cpp.md)  
  
-   [字符串和 I\/O 格式化](../cpp/string-and-i-o-formatting-modern-cpp.md)  
  
-   [错误和异常处理](../cpp/errors-and-exception-handling-modern-cpp.md)  
  
-   [ABI 边界处的可移植性](../cpp/portability-at-abi-boundaries-modern-cpp.md)  
  
 有关详细信息，请参阅 StackOverflow 文章 [C\+\+11 中弃用了哪些 C\+\+ 术语](http://go.microsoft.com/fwlink/?LinkId=402836)  
  
## 请参阅  
 [C\+\+ 语言参考](../cpp/cpp-language-reference.md)   
 [lambda 表达式](../cpp/lambda-expressions-in-cpp.md)   
 [C\+\+ 标准库](../standard-library/cpp-standard-library-reference.md)