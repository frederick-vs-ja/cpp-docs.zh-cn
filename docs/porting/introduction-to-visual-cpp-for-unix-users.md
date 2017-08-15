---
title: "Visual C++ 简介（针对 UNIX 用户）| Microsoft Docs"
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
- UNIX [C++]
ms.assetid: 36108b31-e7fa-49a8-a1f7-7077fcbec873
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
ms.sourcegitcommit: 3c1955bece0c8cdadb4a151ee06fa006402666a4
ms.openlocfilehash: 524be35ec1e1db511b7fd4c2ab2b87d83c54325c
ms.contentlocale: zh-cn
ms.lasthandoff: 06/08/2017

---
# <a name="introduction-to-visual-c-for-unix-users"></a>Visual C++ 简介（针对 UNIX 用户）
本主题为不熟悉 Visual C++ 并想要有效率的使用它的 UNIX 用户提供信息。  
  
## <a name="getting-started-on-the-command-line"></a>首先使用命令行  
 可按使用 UNIX 命令行环境的相似方式来使用命令行中的 Visual C++。 利用命令行 C 和 C++ 编译器 (CL.EXE) 以及 NMAKE.EXE、Microsoft 版本的 UNIX make 实用工具等工具从命令提示符中进行编译。  
  
 在 UNIX 中，命令安装在常用文件夹中，例如 /usr/bin。 在 Visual C++ 中，命令行工具安装在 VC\bin 的安装目录中（通常安装在 Program Files\Microsoft Visual Studio 8\VC\bin 中）。 若要使用命令行工具，请运行位于 Common7\Tools 的安装目录中的 vsvars32.bat。 这会将 bin 目录添加到路径中，并设置从命令行编译 Visual C++ 程序所必需的其他路径。 有关详细信息，请参阅[在命令行上生成](../build/building-on-the-command-line.md)和[演练：在命令行上编译本机 C++ 程序](../build/walkthrough-compiling-a-native-cpp-program-on-the-command-line.md)。  
  
> [!NOTE]
>  如果通过“开始”菜单中的“Visual Studio 命令行提示符”打开命令提示符，则运行 vsvars32.bat。  
  
 若要使用 Visual Studio 调试器、语句完成等更强大的功能，则需要使用开发环境。  
  
## <a name="debugging-your-code"></a>调试代码  
 如果使用命令行并在开发工作站上运行应用程序，则在代码遇到内存访问冲突、未处理的异常或其他不可恢复的错误时，将显示运行 [!INCLUDE[vsprvs](../assembler/masm/includes/vsprvs_md.md)] 调试器的对话框。 如果单击“确定”，将启动 Visual Studio 开发环境，并且在故障点之前调试器都将打开。 可按此方法调试应用程序，而且在这种情况下，只有在使用 [/Z7、/Zi、/ZI（调试信息格式）](../build/reference/z7-zi-zi-debug-information-format.md)交换机进行编译时，源代码才可用。 有关详细信息，请参阅[调试本机代码](/visualstudio/debugger/debugging-native-code)和[使用 Visual Studio IDE 进行 C++ 桌面开发](../ide/using-the-visual-studio-ide-for-cpp-desktop-development.md)。  
  
## <a name="using-the-development-environment"></a>使用开发环境  
 使用开发环境更容易在项目中编辑和生成源代码。 项目是指将编译到单个单元（如库或可执行文件）中的源文件和相关文件的集合。 项目还包括文件生成方式的相关信息。 项目的相关信息存储在扩展名为 .prj 的项目文件中。  
  
 单个解决方案中内含的多个项目中存储了包含多个库和可执行文件的应用程序，其中每个库或文件都可以一组不同的编译器选项，或甚至以不同语言生成。 解决方案是容器的抽象概念，用来将多个项目组合在一起。 解决方案的相关信息存储在扩展名为 .sln 的解决方案文件中。 有关详细信息，请参阅[Visual Studio 中的解决方案和项目](/visualstudio/ide/solutions-and-projects-in-visual-studio)和[使用 Visual Studio IDE 进行 C++ 桌面开发](../ide/using-the-visual-studio-ide-for-cpp-desktop-development.md)。  
  
## <a name="importing-your-existing-code"></a>导入现有代码  
 可借助 Visual C++ 来使用设置为用（不用）生成文件进行编译的现有代码，并将它放入 [!INCLUDE[vsprvs](../assembler/masm/includes/vsprvs_md.md)] 项目。 有关详细信息，请参阅**“从现有代码文件创建项目”向导**。 有关详细信息，请参阅[如何：通过现有代码创建 C++ 项目](../ide/how-to-create-a-cpp-project-from-existing-code.md)。  
  
## <a name="creating-a-new-project"></a>创建新项目  
 可在开发环境中创建新项目。 Visual C++ 提供了大量提供各种常见项目的标准代码的模板。 可使用应用程序向导为各种应用程序类型生成具有代码大纲的项目。  
  
 可以使用**“控制台应用程序 (Win32) 向导”**开始创建空项目。 选择“空项目”复选框。 然后稍后可将新的和现有文件添加到项目。  
  
 当创建项目时，必须对其进行命名。 默认情况下，项目名称即为动态链接库 (DLL) 或从此项目生成的可执行文件的名称。 有关详细信息，请参阅[创建解决方案和项目](/visualstudio/ide/creating-solutions-and-projects)。  
  
## <a name="microsoft-specific-modifiers"></a>Microsoft 专用的修饰符  
 Visual C++ 包含标准 C++ 编程语言的一些扩展。 这些扩展用于指定存储类特性、函数调用约定和基于寻址以及其他用途。 有关所有 Visual C++ 扩展的完整列表，请参阅 [Microsoft 专用的修饰符](../cpp/microsoft-specific-modifiers.md)。  
  
 可以使用 **/Za** 编译器选项禁用所有特定于 Microsoft 的 C++ 扩展。 如果希望编写可在多个平台上运行的代码，建议使用此选项。 有关 **/Za** 编译器选项的详细信息，请参阅 [/Za、/Ze（禁用语言扩展）](../build/reference/za-ze-disable-language-extensions.md)。 有关 Visual C++ 一致性的详细信息，请参阅[非标准行为](../cpp/nonstandard-behavior.md)。  
  
## <a name="precompiled-headers"></a>预编译标头  
 Microsoft C 和 C++ 编译器提供预编译任何 C 或 C++ 代码（包括内联代码）的选项。 使用此性能功能，可以编译稳定的代码正文，在文件中存储已编译的代码状态，并在后续编译过程中将预编译代码和仍在开发的代码合并在一起。 每个后续编译的速度都更快，因为无需重新编译稳定的代码。  
  
 默认情况下，所有预编译的代码均在文件 **stdafx.h** 和 **stdafx.cpp** 中进行指定。 “新建项目”向导将自动创建这些文件，除非取消选择“预编译标头”选项。 有关预编译标头的详细信息，请参阅[创建预编译标头文件](../build/reference/creating-precompiled-header-files.md)。  
  
## <a name="related-sections"></a>相关章节  
 有关详细信息，请参阅[从 UNIX 到 Win32 的迁移](../porting/porting-from-unix-to-win32.md)。  
  
## <a name="see-also"></a>另请参阅  
 [生成 C/C++ 程序](../build/building-c-cpp-programs.md)