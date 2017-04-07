---
title: "CTaskDialog 类 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CTaskDialog
- AFXTASKDIALOG/CTaskDialog
- AFXTASKDIALOG/CTaskDialog::CTaskDialog
- AFXTASKDIALOG/CTaskDialog::AddCommandControl
- AFXTASKDIALOG/CTaskDialog::AddRadioButton
- AFXTASKDIALOG/CTaskDialog::ClickCommandControl
- AFXTASKDIALOG/CTaskDialog::ClickRadioButton
- AFXTASKDIALOG/CTaskDialog::DoModal
- AFXTASKDIALOG/CTaskDialog::GetCommonButtonCount
- AFXTASKDIALOG/CTaskDialog::GetCommonButtonFlag
- AFXTASKDIALOG/CTaskDialog::GetCommonButtonId
- AFXTASKDIALOG/CTaskDialog::GetOptions
- AFXTASKDIALOG/CTaskDialog::GetSelectedCommandControlID
- AFXTASKDIALOG/CTaskDialog::GetSelectedRadioButtonID
- AFXTASKDIALOG/CTaskDialog::GetVerificationCheckboxState
- AFXTASKDIALOG/CTaskDialog::IsCommandControlEnabled
- AFXTASKDIALOG/CTaskDialog::IsRadioButtonEnabled
- AFXTASKDIALOG/CTaskDialog::IsSupported
- AFXTASKDIALOG/CTaskDialog::LoadCommandControls
- AFXTASKDIALOG/CTaskDialog::LoadRadioButtons
- AFXTASKDIALOG/CTaskDialog::NavigateTo
- AFXTASKDIALOG/CTaskDialog::OnCommandControlClick
- AFXTASKDIALOG/CTaskDialog::OnCreate
- AFXTASKDIALOG/CTaskDialog::OnDestroy
- AFXTASKDIALOG/CTaskDialog::OnExpandButtonClick
- AFXTASKDIALOG/CTaskDialog::OnHelp
- AFXTASKDIALOG/CTaskDialog::OnHyperlinkClick
- AFXTASKDIALOG/CTaskDialog::OnInit
- AFXTASKDIALOG/CTaskDialog::OnNavigatePage
- AFXTASKDIALOG/CTaskDialog::OnRadioButtonClick
- AFXTASKDIALOG/CTaskDialog::OnTimer
- AFXTASKDIALOG/CTaskDialog::OnVerificationCheckboxClick
- AFXTASKDIALOG/CTaskDialog::RemoveAllCommandControls
- AFXTASKDIALOG/CTaskDialog::RemoveAllRadioButtons
- AFXTASKDIALOG/CTaskDialog::SetCommandControlOptions
- AFXTASKDIALOG/CTaskDialog::SetCommonButtonOptions
- AFXTASKDIALOG/CTaskDialog::SetCommonButtons
- AFXTASKDIALOG/CTaskDialog::SetContent
- AFXTASKDIALOG/CTaskDialog::SetDefaultCommandControl
- AFXTASKDIALOG/CTaskDialog::SetDefaultRadioButton
- AFXTASKDIALOG/CTaskDialog::SetDialogWidth
- AFXTASKDIALOG/CTaskDialog::SetExpansionArea
- AFXTASKDIALOG/CTaskDialog::SetFooterIcon
- AFXTASKDIALOG/CTaskDialog::SetFooterText
- AFXTASKDIALOG/CTaskDialog::SetMainIcon
- AFXTASKDIALOG/CTaskDialog::SetMainInstruction
- AFXTASKDIALOG/CTaskDialog::SetOptions
- AFXTASKDIALOG/CTaskDialog::SetProgressBarMarquee
- AFXTASKDIALOG/CTaskDialog::SetProgressBarPosition
- AFXTASKDIALOG/CTaskDialog::SetProgressBarRange
- AFXTASKDIALOG/CTaskDialog::SetProgressBarState
- AFXTASKDIALOG/CTaskDialog::SetRadioButtonOptions
- AFXTASKDIALOG/CTaskDialog::SetVerificationCheckbox
- AFXTASKDIALOG/CTaskDialog::SetVerificationCheckboxText
- AFXTASKDIALOG/CTaskDialog::SetWindowTitle
- AFXTASKDIALOG/CTaskDialog::ShowDialog
- AFXTASKDIALOG/CTaskDialog::TaskDialogCallback
dev_langs:
- C++
helpviewer_keywords:
- CTaskDialog class
ms.assetid: 1991ec98-ae56-4483-958b-233809c8c559
caps.latest.revision: 29
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
translationtype: Machine Translation
ms.sourcegitcommit: 0e0c08ddc57d437c51872b5186ae3fc983bb0199
ms.openlocfilehash: 46de64825de9f824ce3d0a5d0c74b7cdc2352774
ms.lasthandoff: 02/24/2017

---
# <a name="ctaskdialog-class"></a>CTaskDialog Class
功能类似于消息框，但可向用户显示额外信息的弹出对话框。 `CTaskDialog` 还包括从用户那里收集信息的功能。  
  
## <a name="syntax"></a>语法  
  
```  
class CTaskDialog : public CObject  
```  
  
## <a name="members"></a>成员  
  
### <a name="constructors"></a>构造函数  
  
|||  
|-|-|  
|[CTaskDialog::CTaskDialog](#ctaskdialog)|构造 `CTaskDialog` 对象。|  
  
### <a name="methods"></a>方法  
  
|||  
|-|-|  
|[CTaskDialog::AddCommandControl](#addcommandcontrol)|添加到一个命令按钮控件`CTaskDialog`。|  
|[CTaskDialog::AddRadioButton](#addradiobutton)|将添加到单选按钮`CTaskDialog`。|  
|[CTaskDialog::ClickCommandControl](#clickcommandcontrol)|以编程方式单击命令按钮控件或常见的按钮。|  
|[CTaskDialog::ClickRadioButton](#clickradiobutton)|以编程方式单击单选按钮。|  
|[CTaskDialog::DoModal](#domodal)|显示`CTaskDialog`。|  
|[CTaskDialog::GetCommonButtonCount](#getcommonbuttoncount)|检索可用的常见按钮数。|  
|[CTaskDialog::GetCommonButtonFlag](#getcommonbuttonflag)|将转换为按钮的通用类型的 Windows 按钮与关联的标准`CTaskDialog`类。|  
|[CTaskDialog::GetCommonButtonId](#getcommonbuttonid)|将一个与相关联的常见按钮类型转换`CTaskDialog`类传递给标准的 Windows 按钮。|  
|[CTaskDialog::GetOptions](#getoptions)|返回此选项标志`CTaskDialog`。|  
|[CTaskDialog::GetSelectedCommandControlID](#getselectedcommandcontrolid)|返回所选的命令按钮控件。|  
|[CTaskDialog::GetSelectedRadioButtonID](#getselectedradiobuttonid)|返回选定的单选按钮。|  
|[CTaskDialog::GetVerificationCheckboxState](#getverificationcheckboxstate)|检索验证复选框的状态。|  
|[CTaskDialog::IsCommandControlEnabled](#iscommandcontrolenabled)|确定是否启用命令按钮控件或常见的按钮。|  
|[CTaskDialog::IsRadioButtonEnabled](#isradiobuttonenabled)|确定是否启用单选按钮。|  
|[CTaskDialog::IsSupported](#issupported)|确定是否正在运行该应用程序的计算机支持`CTaskDialog`。|  
|[CTaskDialog::LoadCommandControls](#loadcommandcontrols)|通过使用字符串表中的数据添加命令按钮控件。|  
|[CTaskDialog::LoadRadioButtons](#loadradiobuttons)|通过使用字符串表中的数据添加单选按钮。|  
|[CTaskDialog::NavigateTo](#navigateto)|将焦点转移到另一台`CTaskDialog`。|  
|[CTaskDialog::OnCommandControlClick](#oncommandcontrolclick)|在用户单击命令按钮控件时，框架将调用此方法。|  
|[CTaskDialog::OnCreate](#oncreate)|创建后，框架将调用此方法`CTaskDialog`。|  
|[CTaskDialog::OnDestroy](#ondestroy)|框架将调用此方法，它将销毁之前立即`CTaskDialog`。|  
|[CTaskDialog::OnExpandButtonClick](#onexpandbuttonclick)|当用户单击展开按钮时，框架将调用此方法。|  
|[CTaskDialog::OnHelp](#onhelp)|当用户请求帮助时，框架将调用此方法。|  
|[CTaskDialog::OnHyperlinkClick](#onhyperlinkclick)|在用户单击一个超链接时，框架将调用此方法。|  
|[CTaskDialog::OnInit](#oninit)|框架将调用此方法时`CTaskDialog`初始化。|  
|[CTaskDialog::OnNavigatePage](#onnavigatepage)|框架将调用此方法，当用户移动控件方面焦点`CTaskDialog`。|  
|[CTaskDialog::OnRadioButtonClick](#onradiobuttonclick)|当用户选择单选按钮控件时，框架将调用此方法。|  
|[CTaskDialog::OnTimer](#ontimer)|在计时器过期时，框架将调用此方法。|  
|[CTaskDialog::OnVerificationCheckboxClick](#onverificationcheckboxclick)|当用户单击验证复选框，框架将调用此方法。|  
|[CTaskDialog::RemoveAllCommandControls](#removeallcommandcontrols)|将移除所有的命令控件从`CTaskDialog`。|  
|[CTaskDialog::RemoveAllRadioButtons](#removeallradiobuttons)|删除从所有单选按钮`CTaskDialog`。|  
|[CTaskDialog::SetCommandControlOptions](#setcommandcontroloptions)|将更新命令按钮控件上`CTaskDialog`。|  
|[CTaskDialog::SetCommonButtonOptions](#setcommonbuttonoptions)|更新的常见按钮将启用，并且需要 UAC 提升的子集。|  
|[CTaskDialog::SetCommonButtons](#setcommonbuttons)|添加了对常见按钮`CTaskDialog`。|  
|[CTaskDialog::SetContent](#setcontent)|更新的内容`CTaskDialog`。|  
|[CTaskDialog::SetDefaultCommandControl](#setdefaultcommandcontrol)|指定的默认命令按钮控件。|  
|[CTaskDialog::SetDefaultRadioButton](#setdefaultradiobutton)|指定默认单选按钮。|  
|[CTaskDialog::SetDialogWidth](#setdialogwidth)|调整的宽度`CTaskDialog`。|  
|[CTaskDialog::SetExpansionArea](#setexpansionarea)|更新的扩展区域`CTaskDialog`。|  
|[CTaskDialog::SetFooterIcon](#setfootericon)|更新的页脚图标`CTaskDialog`。|  
|[CTaskDialog::SetFooterText](#setfootertext)|更新的脚注文本`CTaskDialog`。|  
|[CTaskDialog::SetMainIcon](#setmainicon)|更新主图标的`CTaskDialog`。|  
|[CTaskDialog::SetMainInstruction](#setmaininstruction)|更新的主指令`CTaskDialog`。|  
|[CTaskDialog::SetOptions](#setoptions)|为配置选项`CTaskDialog`。|  
|[CTaskDialog::SetProgressBarMarquee](#setprogressbarmarquee)|配置的字幕条`CTaskDialog`并将其添加到对话框。|  
|[CTaskDialog::SetProgressBarPosition](#setprogressbarposition)|调整进度条的位置。|  
|[CTaskDialog::SetProgressBarRange](#setprogressbarrange)|调整进度条的范围。|  
|[CTaskDialog::SetProgressBarState](#setprogressbarstate)|设置进度栏的状态，并将其显示在`CTaskDialog`。|  
|[CTaskDialog::SetRadioButtonOptions](#setradiobuttonoptions)|启用或禁用的单选按钮。|  
|[CTaskDialog::SetVerificationCheckbox](#setverificationcheckbox)|设置验证复选框的选中的状态。|  
|[CTaskDialog::SetVerificationCheckboxText](#setverificationcheckboxtext)|设置验证复选框右侧的文本。|  
|[CTaskDialog::SetWindowTitle](#setwindowtitle)|设置的标题`CTaskDialog`。|  
|[CTaskDialog::ShowDialog](#showdialog)|创建并显示`CTaskDialog`。|  
|[CTaskDialog::TaskDialogCallback](#taskdialogcallback)|框架将调用此以响应各种 Windows 消息。|  
  
### <a name="data-members"></a>数据成员  
  
|||  
|-|-|  
|`m_aButtons`|命令按钮控件，用于数组`CTaskDialog`。|  
|`m_aRadioButtons`|单选按钮控件，用于数组`CTaskDialog`。|  
|`m_bVerified`|`TRUE`指示已选中验证复选框;`FALSE`指示它不是。|  
|`m_footerIcon`|在页脚中的图标`CTaskDialog`。|  
|`m_hWnd`|为窗口的句柄`CTaskDialog`。|  
|`m_mainIcon`|主图标的`CTaskDialog`。|  
|`m_nButtonDisabled`|一个屏蔽，它表示常见按钮处于禁用状态。|  
|`m_nButtonElevation`|一个屏蔽，它表示常见按钮需要 UAC 提升。|  
|`m_nButtonId`|选定的命令按钮控件的 ID。|  
|`m_nCommonButton`|一个屏蔽，它指示哪些常见按钮显示在`CTaskDialog`。|  
|`m_nDefaultCommandControl`|命令按钮的 ID 控制何时选择`CTaskDialog`显示。|  
|`m_nDefaultRadioButton`|ID 为单选按钮控件时选择`CTaskDialog`显示。|  
|`m_nFlags`|一个屏蔽，它指示选项`CTaskDialog`。|  
|`m_nProgressPos`|进度栏的当前位置。  该值必须介于 `m_nProgressRangeMin` 和 `m_nProgressRangeMax` 之间。|  
|`m_nProgressRangeMax`|进度条的最大值。|  
|`m_nProgressRangeMin`|进度栏最小值。|  
|`m_nProgressState`|进度栏的状态。 有关详细信息，请参阅[CTaskDialog::SetProgressBarState](#setprogressbarstate)。|  
|`m_nRadioId`|选定的单选按钮控件的 ID。|  
|`m_nWidth`|宽度`CTaskDialog`以像素为单位。|  
|`m_strCollapse`|该字符串`CTaskDialog`隐藏展开的信息时，右侧的扩展框中显示。|  
|`m_strContent`|内容字符串`CTaskDialog`。|  
|`m_strExpand`|该字符串`CTaskDialog`显示展开的信息时，右侧的扩展框中显示。|  
|`m_strFooter`|页脚`CTaskDialog`。|  
|`m_strInformation`|为展开的信息`CTaskDialog`。|  
|`m_strMainInstruction`|主要指令`CTaskDialog`。|  
|`m_strTitle`|标题`CTaskDialog`。|  
|`m_strVerification`|该字符串，`CTaskDialog`右侧的验证复选框显示。|  
  
## <a name="remarks"></a>备注  
 `CTaskDialog`类替换标准 Windows 消息框，并具有额外功能，如用于从用户收集信息的新控件。 此类是在 MFC 库[!INCLUDE[vs_dev10_long](../../build/includes/vs_dev10_long_md.md)]。 `CTaskDialog`可用开头[!INCLUDE[wiprlhext](../../c-runtime-library/reference/includes/wiprlhext_md.md)]。 早期版本的 Windows 不能显示`CTaskDialog`对象。 使用`CTaskDialog::IsSupported`以在运行时确定当前用户是否可以显示任务对话框。 中仍支持标准 Windows 消息框[!INCLUDE[vs_dev10_long](../../build/includes/vs_dev10_long_md.md)]。  
  
 `CTaskDialog`可仅生成时您的应用程序通过使用 Unicode 库。  
  
 `CTaskDialog`具有两个不同的构造函数。 有一个构造函数可以指定两个命令按钮和最多包含六个常规按钮控件。 在创建后，可以添加更多命令按钮`CTaskDialog`。 第二个构造函数不支持任何命令按钮，但您可以添加任意的数量的常规按钮控件。 有关构造函数的详细信息，请参阅[CTaskDialog::CTaskDialog](#ctaskdialog)。  
  
 下图显示了一个示例`CTaskDialog`来说明的某些控件的位置。  
  
 ![CTaskDialog 示例](../../mfc/reference/media/ctaskdialogsample.png "ctaskdialogsample")  
CTaskDialog 示例  
  
## <a name="requirements"></a>要求  
 **最小值所需的操作系统︰**[!INCLUDE[wiprlhext](../../c-runtime-library/reference/includes/wiprlhext_md.md)]  
  
 **标头︰** afxtaskdialog.h  
  
##  <a name="addcommandcontrol"></a>CTaskDialog::AddCommandControl  
 添加到一个新命令按钮控件`CTaskDialog`。  
  
```  
void AddCommandControl(
    int nCommandControlID,  
    const CString& strCaption,  
    BOOL bEnabled = TRUE,  
    BOOL bRequiresElevation = FALSE);
```  
  
### <a name="parameters"></a>参数  
 [in] `nCommandControlID`  
 命令控件标识号。  
  
 [in] `strCaption`  
 该字符串，`CTaskDialog`向用户显示。 使用此字符串用于说明用途的命令。  
  
 [in] `bEnabled`  
 一个布尔型参数，该值指示是否新建按钮是启用还是禁用。  
  
 [in] `bRequiresElevation`  
 一个布尔型参数，该值指示命令是否需要提升。  
  
### <a name="remarks"></a>备注  
 `CTaskDialog Class`可显示无限的数量的命令按钮控件。 但是，如果`CTaskDialog`显示任何命令按钮控件，它还可以显示最多包含六个按钮。 如果`CTaskDialog`没有任何命令的按钮控件，它还可以显示无限的数量的按钮。  
  
 当用户选择命令按钮控件，`CTaskDialog`关闭。 如果您的应用程序显示对话框中，通过使用[CTaskDialog::DoModal](#domodal)，`DoModal`返回`nCommandControlID`的所选的命令按钮控件。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&2;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_1.cpp)]  
  
##  <a name="addradiobutton"></a>CTaskDialog::AddRadioButton  
 将添加到单选按钮`CTaskDialog`。  
  
```  
void CTaskDialog::AddRadioButton(
    int nRadioButtonID,  
    const CString& strCaption,  
    BOOL bEnabled = TRUE);
```  
  
### <a name="parameters"></a>参数  
 [in] `nRadioButtonID`  
 单选按钮的标识号。  
  
 [in] `strCaption`  
 该字符串，`CTaskDialog`显示旁边的单选按钮。  
  
 [in] `bEnabled`  
 一个布尔型参数，该值指示是否启用单选按钮。  
  
### <a name="remarks"></a>备注  
 单选按钮[CTaskDialog 类](../../mfc/reference/ctaskdialog-class.md)使您能够从用户收集的信息。 使用函数[CTaskDialog::GetSelectedRadioButtonID](#getselectedradiobuttonid)来确定选择哪个单选按钮。  
  
 `CTaskDialog`不要求`nRadioButtonID`参数都是唯一的每个单选按钮。 但是，可能会遇到意外的行为，如果不为每个单选按钮使用不同的标识符。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&3;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_2.cpp)]  
  
##  <a name="clickcommandcontrol"></a>CTaskDialog::ClickCommandControl  
 以编程方式单击命令按钮控件或常见的按钮。  
  
```  
protected:  
void ClickCommandControl(int nCommandControlID) const;  
```  
  
### <a name="parameters"></a>参数  
 [in] `nCommandControlID`  
 单击该控件的命令 ID。  
  
### <a name="remarks"></a>备注  
 此方法将生成的 windows 消息`TDM_CLICK_BUTTON`。  
  
##  <a name="clickradiobutton"></a>CTaskDialog::ClickRadioButton  
 以编程方式单击单选按钮。  
  
```  
protected:  
void ClickRadioButton(int nRadioButtonID) const;  
```  
  
### <a name="parameters"></a>参数  
 [in] `nRadioButtonID`  
 要单击的单选按钮的 ID。  
  
### <a name="remarks"></a>备注  
 此方法将生成的 windows 消息`TDM_CLICK_RADIO_BUTTON`。  
  
##  <a name="ctaskdialog"></a>CTaskDialog::CTaskDialog  
 创建的一个实例[CTaskDialog 类](../../mfc/reference/ctaskdialog-class.md)。  
  
```  
CTaskDialog(
    const CString& strContent,  
    const CString& strMainInstruction,  
    const CString& strTitle,  
    int nCommonButtons = TDCBF_OK_BUTTON | TDCBF_CANCEL_BUTTON,  
    int nTaskDialogOptions = TDF_ENABLE_HYPERLINKS | TDF_USE_COMMAND_LINKS,  
    const CString& strFooter = _T(""));

 
CTaskDialog(
    const CString& strContent,  
    const CString& strMainInstruction,  
    const CString& strTitle,  
    int nIDCommandControlsFirst,  
    int nIDCommandControlsLast,  
    int nCommonButtons,  
    int nTaskDialogOptions = TDF_ENABLE_HYPERLINKS | TDF_USE_COMMAND_LINKS,  
    const CString& strFooter = _T(""));
```  
  
### <a name="parameters"></a>参数  
 [in] `strContent`  
 要使用的内容的字符串`CTaskDialog`。  
  
 [in] `strMainInstruction`  
 主要指令`CTaskDialog`。  
  
 [in] `strTitle`  
 标题`CTaskDialog`。  
  
 [in] `nCommonButtons`  
 常见的按钮将添加到一个掩码`CTaskDialog`。  
  
 [in] `nTaskDialogOptions`  
 要使用的选项集`CTaskDialog`。  
  
 [in] `strFooter`  
 要用作页脚的字符串。  
  
 [in] `nIDCommandControlsFirst`  
 第一个命令字符串 ID。  
  
 [in] `nIDCommandControlsLast`  
 最后一个命令字符串 ID。  
  
### <a name="remarks"></a>备注  
 有两种方法可添加`CTaskDialog`到您的应用程序。 第一种方法是使用构造函数之一来创建`CTaskDialog`并将其使用显示[CTaskDialog::DoModal](#domodal)。 第二种方法是使用静态函数[CTaskDialog::ShowDialog](#showdialog)，这样您就可以显示`CTaskDialog`而无需显式创建`CTaskDialog`对象。  
  
 第二个构造函数通过使用您的应用程序的资源文件中的数据创建命令按钮控件。 资源文件中的字符串表具有与关联的字符串 Id 的多个字符串。 此方法之间的字符串表中添加每个有效项的命令按钮控件`nIDCommandControlsFirst`和`nCommandControlsLast`(含） 之间。 对于这些命令的按钮控件，该字符串表中的字符串是控件的标题和字符串 ID 是控件的 id。  
  
 请参阅[CTaskDialog::SetOptions](#setoptions)有关有效选项的列表。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&7;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_3.cpp)]  
  
##  <a name="domodal"></a>CTaskDialog::DoModal  
 显示`CTaskDialog`并使其成为模式。  
  
```  
INT_PTR DoModal (HWND hParent = ::GetActiveWindow());
```  
  
### <a name="parameters"></a>参数  
 [in] `hParent`  
 父窗口`CTaskDialog`。  
  
### <a name="return-value"></a>返回值  
 一个整数，对应于由用户所做的选择。  
  
### <a name="remarks"></a>备注  
 显示的此实例[CTaskDialog](../../mfc/reference/ctaskdialog-class.md)。 然后，应用程序等待用户关闭对话框。  
  
 `CTaskDialog`用户选择常见按钮，command link 控件，或关闭时，将关闭`CTaskDialog`。 返回值是指示用户如何关闭对话框中的标识符。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&7;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_3.cpp)]  
  
##  <a name="getcommonbuttoncount"></a>CTaskDialog::GetCommonButtonCount  
 检索常见按钮的数。  
  
```  
int GetCommonButtonCount() const;  
```  
  
### <a name="return-value"></a>返回值  
 可用的常见按钮数。  
  
### <a name="remarks"></a>备注  
 常见按钮是向您提供的默认按钮[CTaskDialog::CTaskDialog](#ctaskdialog)。 [CTaskDialog 类](../../mfc/reference/ctaskdialog-class.md)显示的对话框中底部的按钮。  
  
 CommCtrl.h 中提供的枚举的列表的按钮。  
  
##  <a name="getcommonbuttonflag"></a>CTaskDialog::GetCommonButtonFlag  
 将转换为按钮的通用类型的 Windows 按钮与关联的标准[CTaskDialog 类](../../mfc/reference/ctaskdialog-class.md)。  
  
```  
int GetCommonButtonFlag(int nButtonId) const;  
```  
  
### <a name="parameters"></a>参数  
 [in] `nButtonId`  
 标准 Windows 按钮值。  
  
### <a name="return-value"></a>返回值  
 相应的值`CTaskDialog`常见按钮。 如果没有相应的常见按钮，此方法将返回 0。  
  
##  <a name="getcommonbuttonid"></a>CTaskDialog::GetCommonButtonId  
 将一个与相关联的常见按钮类型转换[CTaskDialog 类](../../mfc/reference/ctaskdialog-class.md)到标准的 Windows 按钮。  
  
```  
int GetCommonButtonId(int nFlag);
```  
  
### <a name="parameters"></a>参数  
 [in] `nFlag`  
 与关联的常见按钮类型`CTaskDialog`类。  
  
### <a name="return-value"></a>返回值  
 相应的标准 Windows 按钮的值。 如果没有相应的 Windows 按钮，此方法将返回 0。  
  
##  <a name="getoptions"></a>CTaskDialog::GetOptions  
 返回此选项标志`CTaskDialog`。  
  
```  
int GetOptions() const;  
```  
  
### <a name="return-value"></a>返回值  
 标志`CTaskDialog`。  
  
### <a name="remarks"></a>备注  
 有关可用选项详细信息[CTaskDialog 类](../../mfc/reference/ctaskdialog-class.md)，请参阅[CTaskDialog::SetOptions](#setoptions)。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&7;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_3.cpp)]  
  
##  <a name="getselectedcommandcontrolid"></a>CTaskDialog::GetSelectedCommandControlID  
 返回所选的命令按钮控件。  
  
```  
int GetSelectedCommandControlID() const;  
```  
  
### <a name="return-value"></a>返回值  
 当前所选的命令按钮控件的 ID。  
  
### <a name="remarks"></a>备注  
 不需要使用此方法检索的用户选择命令按钮的 ID。 通过以下任一方法返回该 ID [CTaskDialog::DoModal](#domodal)或[CTaskDialog::ShowDialog](#showdialog)。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&2;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_1.cpp)]  
  
##  <a name="getselectedradiobuttonid"></a>CTaskDialog::GetSelectedRadioButtonID  
 返回选定的单选按钮。  
  
```  
int GetSelectedRadioButtonID() const;  
```  
  
### <a name="return-value"></a>返回值  
 选定的单选按钮的 ID。  
  
### <a name="remarks"></a>备注  
 用户关闭对话框检索选定的单选按钮后，可以使用此方法。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&3;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_2.cpp)]  
  
##  <a name="getverificationcheckboxstate"></a>CTaskDialog::GetVerificationCheckboxState  
 检索验证复选框的状态。  
  
```  
BOOL GetVerificationCheckboxState() const;  
```  
  
### <a name="return-value"></a>返回值  
 `TRUE`如果选中复选框，则`FALSE`如果不是。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&5;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_4.cpp)]  
  
##  <a name="iscommandcontrolenabled"></a>CTaskDialog::IsCommandControlEnabled  
 确定是否启用命令按钮控件或按钮。  
  
```  
BOOL IsCommandControlEnabled(int nCommandControlID) const;  
```  
  
### <a name="parameters"></a>参数  
 [in] `nCommandControlID`  
 若要测试的命令按钮控件或按钮 ID。  
  
### <a name="return-value"></a>返回值  
 `TRUE`如果已启用该控件，`FALSE`如果不是。  
  
### <a name="remarks"></a>备注  
 可以使用此方法来确定同时命令按钮控件的可用性以及的常见按钮`CTaskDialog Class`。  
  
 如果`nCommandControlID`不是有效的标识符，对于任何一种常见`CTaskDialog`按钮或命令按钮控件，此方法将引发异常。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&2;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_1.cpp)]  
  
##  <a name="isradiobuttonenabled"></a>CTaskDialog::IsRadioButtonEnabled  
 确定是否启用单选按钮。  
  
```  
BOOL IsRadioButtonEnabled(int nRadioButtonID) const;  
```  
  
### <a name="parameters"></a>参数  
 [in] `nRadioButtonID`  
 要测试的单选按钮的 ID。  
  
### <a name="return-value"></a>返回值  
 `TRUE`如果启用了单选按钮，`FALSE`不时。  
  
### <a name="remarks"></a>备注  
 如果`nRadioButtonID`不是有效标识符对于单选按钮，此方法将引发异常。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&3;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_2.cpp)]  
  
##  <a name="issupported"></a>CTaskDialog::IsSupported  
 确定是否正在运行该应用程序的计算机支持`CTaskDialog`。  
  
```  
static BOOL IsSupported();
```  
  
### <a name="return-value"></a>返回值  
 `TRUE`如果计算机支持`CTaskDialog`;`FALSE`否则为。  
  
### <a name="remarks"></a>备注  
 使用此函数可确定在运行时，如果正在运行您的应用程序的计算机支持`CTaskDialog Class`。 如果计算机不支持`CTaskDialog`，您应提供另一种方法的信息传达给用户。 如果它尝试使用您的应用程序将崩溃`CTaskDialog`不支持的计算机上`CTaskDialog`类。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&1;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_5.cpp)]  
  
##  <a name="loadcommandcontrols"></a>CTaskDialog::LoadCommandControls  
 通过使用字符串表中的数据添加命令按钮控件。  
  
```  
void LoadCommandControls(
    int nIDCommandControlsFirst,  
    int nIDCommandControlsLast);
```  
  
### <a name="parameters"></a>参数  
 [in] `nIDCommandControlsFirst`  
 第一个命令字符串 ID。  
  
 [in] `nIDCommandControlsLast`  
 最后一个命令字符串 ID。  
  
### <a name="remarks"></a>备注  
 此方法通过使用您的应用程序的资源文件中的数据来创建命令按钮控件。 资源文件中的字符串表具有与关联的字符串 Id 的多个字符串。 新的命令按钮控件添加通过使用此方法将字符串的控件的标题以及字符串 ID 用于控件的 id。 所选字符串的范围由`nIDCommandControlsFirst`和`nCommandControlsLast`(含） 之间。 如果在范围内的空的条目，该方法不会添加该条目的命令按钮控件。  
  
 默认情况下，新的命令按钮控件将启用，并且不需要提升。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&2;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_1.cpp)]  
  
##  <a name="loadradiobuttons"></a>CTaskDialog::LoadRadioButtons  
 通过使用字符串表中的数据添加单选按钮控件。  
  
```  
void LoadRadioButtons(
    int nIDRadioButtonsFirst,  
    int nIDRadioButtonsLast);
```  
  
### <a name="parameters"></a>参数  
 [in] `nIDRadioButtonsFirst`  
 第一个单选按钮的字符串 ID。  
  
 [in] `nIDRadioButtonsLast`  
 字符串 ID 的最后一个单选按钮。  
  
### <a name="remarks"></a>备注  
 此方法通过使用您的应用程序的资源文件中的数据来创建单选按钮。 资源文件中的字符串表具有与关联的字符串 Id 的多个字符串。 通过使用此方法添加的新单选按钮将字符串单选按钮的标题和字符串 ID 用于单选按钮的 id。 所选字符串的范围由`nIDRadioButtonsFirst`和`nRadioButtonsLast`(含） 之间。 如果在范围内的空的条目，该方法不会添加该条目的单选按钮。  
  
 默认情况下，会启用新的单选按钮。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&3;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_2.cpp)]  
  
##  <a name="navigateto"></a>CTaskDialog::NavigateTo  
 将焦点转移到另一台`CTaskDialog`。  
  
```  
protected:  
void NavigateTo(CTaskDialog& oTaskDialog) const;  
```  
  
### <a name="parameters"></a>参数  
 [in] `oTaskDialog`  
 `CTaskDialog`接收到焦点。  
  
### <a name="remarks"></a>备注  
 此方法会隐藏当前`CTaskDialog`当显示`oTaskDialog`。 `oTaskDialog`中当前所在的同一位置显示`CTaskDialog`。  
  
##  <a name="oncommandcontrolclick"></a>CTaskDialog::OnCommandControlClick  
 在用户单击命令按钮控件时，框架将调用此方法。  
  
```  
virtual HRESULT OnCommandControlClick(int nCommandControlID);
```  
  
### <a name="parameters"></a>参数  
 [in] `nCommandControlID`  
 在用户选择的命令按钮控件的 ID。  
  
### <a name="return-value"></a>返回值  
 默认实现返回 `S_OK`。  
  
### <a name="remarks"></a>备注  
 重写此方法在派生类来实现自定义行为。  
  
##  <a name="oncreate"></a>CTaskDialog::OnCreate  
 创建后，框架将调用此方法`CTaskDialog`。  
  
```  
virtual HRESULT OnCreate();
```  
  
### <a name="return-value"></a>返回值  
 默认实现返回 `S_OK`。  
  
### <a name="remarks"></a>备注  
 重写此方法在派生类来实现自定义行为。  
  
##  <a name="ondestroy"></a>CTaskDialog::OnDestroy  
 框架将调用此方法，它将销毁之前立即`CTaskDialog`。  
  
```  
virtual HRESULT OnDestroy();
```  
  
### <a name="return-value"></a>返回值  
 默认实现返回 `S_OK`。  
  
### <a name="remarks"></a>备注  
 重写此方法在派生类来实现自定义行为。  
  
##  <a name="onexpandbuttonclick"></a>CTaskDialog::OnExpandButtonClick  
 当用户单击展开按钮时，框架将调用此方法。  
  
```  
virtual HRESULT OnExpandButtonClicked(BOOL bExpanded);
```  
  
### <a name="parameters"></a>参数  
 [in] `bExpanded`  
 一个非零值指示显示额外信息;0 表示处于隐藏状态的附加信息。  
  
### <a name="return-value"></a>返回值  
 默认实现返回 `S_OK`。  
  
### <a name="remarks"></a>备注  
 重写此方法在派生类来实现自定义行为。  
  
##  <a name="onhelp"></a>CTaskDialog::OnHelp  
 当用户请求帮助时，框架将调用此方法。  
  
```  
virtual HRESULT OnHelp();
```  
  
### <a name="return-value"></a>返回值  
 默认实现返回 `S_OK`。  
  
### <a name="remarks"></a>备注  
 重写此方法在派生类来实现自定义行为。  
  
##  <a name="onhyperlinkclick"></a>CTaskDialog::OnHyperlinkClick  
 在用户单击一个超链接时，框架将调用此方法。  
  
```  
virtual HRESULT OnHyperlinkClick(const CString& strHref);
```  
  
### <a name="parameters"></a>参数  
 [in] `strHref`  
 表示该超链接的字符串。  
  
### <a name="return-value"></a>返回值  
 默认实现返回 `S_OK`。  
  
### <a name="remarks"></a>备注  
 此方法调用[ShellExecute](http://msdn.microsoft.com/library/windows/desktop/bb762153)它返回之前`S_OK`。  
  
 重写此方法在派生类来实现自定义行为。  
  
##  <a name="oninit"></a>CTaskDialog::OnInit  
 框架将调用此方法时`CTaskDialog`初始化。  
  
```  
virtual HRESULT OnInit();
```  
  
### <a name="return-value"></a>返回值  
 默认实现返回 `S_OK`。  
  
### <a name="remarks"></a>备注  
 重写此方法在派生类来实现自定义行为。  
  
##  <a name="onnavigatepage"></a>CTaskDialog::OnNavigatePage  
 框架将调用此方法以响应[CTaskDialog::NavigateTo](#navigateto)方法。  
  
```  
virtual HRESULT OnNavigatePage();
```  
  
### <a name="return-value"></a>返回值  
 默认实现返回 `S_OK`。  
  
### <a name="remarks"></a>备注  
 重写此方法在派生类来实现自定义行为。  
  
##  <a name="onradiobuttonclick"></a>CTaskDialog::OnRadioButtonClick  
 当用户选择单选按钮控件时，框架将调用此方法。  
  
```  
virtual HRESULT OnRadioButtonClick(int nRadioButtonID);
```  
  
### <a name="parameters"></a>参数  
 [in] `nRadioButtonID`  
 用户单击单选按钮控件的 ID。  
  
### <a name="return-value"></a>返回值  
 默认实现返回 `S_OK`。  
  
### <a name="remarks"></a>备注  
 重写此方法在派生类来实现自定义行为。  
  
##  <a name="ontimer"></a>CTaskDialog::OnTimer  
 在计时器过期时，框架将调用此方法。  
  
```  
virtual HRESULT OnTimer(long lTime);
```  
  
### <a name="parameters"></a>参数  
 [in] `lTime`  
 时间 （毫秒） 以来`CTaskDialog`已创建或重置计时器。  
  
### <a name="return-value"></a>返回值  
 默认实现返回 `S_OK`。  
  
### <a name="remarks"></a>备注  
 重写此方法在派生类来实现自定义行为。  
  
##  <a name="onverificationcheckboxclick"></a>CTaskDialog::OnVerificationCheckboxClick  
 当用户单击验证复选框，框架将调用此方法。  
  
```  
virtual HRESULT OnVerificationCheckboxClick(BOOL bChecked);
```  
  
### <a name="parameters"></a>参数  
 [in] `bChecked`  
 `TRUE`指示验证复选框处于选中状态，`FALSE`指示它不是。  
  
### <a name="return-value"></a>返回值  
 默认实现返回 `S_OK`。  
  
### <a name="remarks"></a>备注  
 重写此方法在派生类来实现自定义行为。  
  
##  <a name="removeallcommandcontrols"></a>CTaskDialog::RemoveAllCommandControls  
 删除所有命令按钮中的所有控件`CTaskDialog`。  
  
```  
void RemoveAllCommandControls();
```  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&2;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_1.cpp)]  
  
##  <a name="removeallradiobuttons"></a>CTaskDialog::RemoveAllRadioButtons  
 删除从所有单选按钮`CTaskDialog`。  
  
```  
void RemoveAllRadioButtons();
```  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&3;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_2.cpp)]  
  
##  <a name="setcommandcontroloptions"></a>CTaskDialog::SetCommandControlOptions  
 将更新命令按钮控件上`CTaskDialog`。  
  
```  
void SetCommandControlOptions(
    int nCommandControlID,  
    BOOL bEnabled,  
    BOOL bRequiresElevation = FALSE);
```  
  
### <a name="parameters"></a>参数  
 [in] `nCommandControlID`  
 要更新的命令控件的 ID。  
  
 [in] `bEnabled`  
 一个布尔型参数，该值指示是否指定的命令按钮控件是启用还是禁用。  
  
 [in] `bRequiresElevation`  
 一个布尔型参数，指示指定的命令按钮控件是否需要提升。  
  
### <a name="remarks"></a>备注  
 使用此方法来更改命令按钮控件启用还是添加到中之后需要提升`CTaskDialog Class`。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&2;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_1.cpp)]  
  
##  <a name="setcommonbuttonoptions"></a>CTaskDialog::SetCommonButtonOptions  
 更新常见按钮才可用，并要求 UAC 提升的子集。  
  
```  
void SetCommonButtonOptions(
    int nDisabledButtonMask,  
    int nElevationButtonMask = 0);
```  
  
### <a name="parameters"></a>参数  
 [in] `nDisabledButtonMask`  
 若要禁用的常见按钮操作的掩码。  
  
 [in] `nElevationButtonMask`  
 需要提升的常见按钮操作的掩码。  
  
### <a name="remarks"></a>备注  
 可以将可用的常见按钮设置为的一个实例[CTaskDialog 类](../../mfc/reference/ctaskdialog-class.md)使用构造函数[CTaskDialog::CTaskDialog](#ctaskdialog)和方法[CTaskDialog::SetCommonButtons](#setcommonbuttons)。 `CTaskDialog::SetCommonButtonOptions`不支持添加新的常见按钮。  
  
 如果使用此方法来禁用或提升不是可用于此的常见按钮`CTaskDialog`，此方法将引发异常，通过使用[确保](http://msdn.microsoft.com/library/738c4ccf-c29c-4c04-8d6c-f126bedf6e91)宏。  
  
 使用此方法可供任何按钮`CTaskDialog`但未在`nDisabledButtonMask`，即使它处于禁用状态。 此方法以类似方式处理提升︰ 记录为公共按钮是否可用，但并未包含在不需要提升的常见按钮`nElevationButtonMask`。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&6;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_6.cpp)]  
  
##  <a name="setcommonbuttons"></a>CTaskDialog::SetCommonButtons  
 添加了对常见按钮`CTaskDialog`。  
  
```  
void SetCommonButtons(
    int nButtonMask,  
    int nDisabledButtonMask = 0,  
    int nElevationButtonMask = 0);
```  
  
### <a name="parameters"></a>参数  
 [in] `nButtonMask`  
 要添加的按钮的掩码`CTaskDialog`。  
  
 [in] `nDisabledButtonMask`  
 要禁用的按钮的操作的掩码。  
  
 [in] `nElevationButtonMask`  
 需要提升的按钮操作的掩码。  
  
### <a name="remarks"></a>备注  
 不能后显示窗口中调用此方法的此实例的`CTaskDialog Class`创建。 否则，此方法将引发异常。  
  
 这些按钮指示`nButtonMask`重写以前添加到任何常见按钮`CTaskDialog`。 只有按钮所示`nButtonMask`可用。  
  
 如果任一`nDisabledButtonMask`或`nElevationButtonMask`包含不在一个按钮`nButtonMask`，此方法将引发异常，通过使用[确保](http://msdn.microsoft.com/library/738c4ccf-c29c-4c04-8d6c-f126bedf6e91)宏。  
  
 默认情况下，所有的常见按钮将启用，并且不需要提升。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&6;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_6.cpp)]  
  
##  <a name="setcontent"></a>CTaskDialog::SetContent  
 更新的内容`CTaskDialog`。  
  
```  
void SetContent(const CString& strContent);
```  
  
### <a name="parameters"></a>参数  
 [in] `strContent`  
 要向用户显示的字符串。  
  
### <a name="remarks"></a>备注  
 内容`CTaskDialog Class`是向对话框中的主要部分中的用户显示的文本。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&7;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_3.cpp)]  
  
##  <a name="setdefaultcommandcontrol"></a>CTaskDialog::SetDefaultCommandControl  
 指定的默认命令按钮控件。  
  
```  
void SetDefaultCommandControl(int nCommandControlID);
```  
  
### <a name="parameters"></a>参数  
 [in] `nCommandControlID`  
 要为默认值的命令按钮控件的 ID。  
  
### <a name="remarks"></a>备注  
 默认值的命令按钮控件是为该控件时选择`CTaskDialog`第一次显示给用户。  
  
 此方法将引发异常，如果它找不到指定的命令按钮控件`nCommandControlID`。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&2;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_1.cpp)]  
  
##  <a name="setdefaultradiobutton"></a>CTaskDialog::SetDefaultRadioButton  
 指定默认单选按钮。  
  
```  
void SetDefaultRadioButton(int nRadioButtonID);
```  
  
### <a name="parameters"></a>参数  
 [in] `nRadioButtonID`  
 要为默认值单选按钮的 ID。  
  
### <a name="remarks"></a>备注  
 默认单选按钮为是按钮时选择`CTaskDialog`第一次显示给用户。  
  
 此方法将引发异常，如果它找不到指定的单选按钮`nRadioButtonID`。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&3;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_2.cpp)]  
  
##  <a name="setdialogwidth"></a>CTaskDialog::SetDialogWidth  
 调整的宽度`CTaskDialog`。  
  
```  
void SetDialogWidth(int nWidth = 0);
```  
  
### <a name="parameters"></a>参数  
 [in] `nWidth`  
 对话框中，以像素为单位的宽度。  
  
### <a name="remarks"></a>备注  
 该参数`nWidth`必须大于或等于 0。 否则，此方法将引发异常。  
  
 如果`nWidth`设置为 0，此方法将设置为默认大小的对话框。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&7;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_3.cpp)]  
  
##  <a name="setexpansionarea"></a>CTaskDialog::SetExpansionArea  
 更新的扩展区域`CTaskDialog`。  
  
```  
void SetExpansionArea(
    const CString& strExpandedInformation,  
    const CString& strCollapsedLabel = _T(""),  
    const CString& strExpandedLabel = _T(""));
```  
  
### <a name="parameters"></a>参数  
 [in] `strExpandedInformation`  
 该字符串，`CTaskDialog`显示在对话框中的主要部分中，当用户单击展开按钮。  
  
 [in] `strCollapsedLabel`  
 该字符串，`CTaskDialog`时扩展的区域处于折叠状态显示扩展按钮旁边。  
  
 [in] `strExpandedLabel`  
 该字符串，`CTaskDialog`时显示的扩展区域扩展按钮旁边显示。  
  
### <a name="remarks"></a>备注  
 扩展区域`CTaskDialog Class`使您可以向用户提供的其他信息。 扩展区域中的主要部分是`CTaskDialog`位于正下方的标题和内容的字符串。  
  
 当`CTaskDialog`第一次显示，不会显示展开的信息并将放`strCollapsedLabel`扩展按钮旁边。 当用户单击展开按钮`CTaskDialog`显示`strExpandedInformation`并更改标签到`strExpandedLabel`。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&7;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_3.cpp)]  
  
##  <a name="setfootericon"></a>CTaskDialog::SetFooterIcon  
 更新的页脚图标`CTaskDialog`。  
  
```  
void SetFooterIcon(HICON hFooterIcon);  
void SetFooterIcon(LPCWSTR lpszFooterIcon);
```  
  
### <a name="parameters"></a>参数  
 [in] `hFooterIcon`  
 为新建图标`CTaskDialog`。  
  
 [in] `lpszFooterIcon`  
 为新建图标`CTaskDialog`。  
  
### <a name="remarks"></a>备注  
 页脚图标显示在底部[CTaskDialog 类](../../mfc/reference/ctaskdialog-class.md)。 它可以具有关联的页脚文本。 您可以更改页脚文本与[CTaskDialog::SetFooterText](#setfootertext)。  
  
 此方法将引发的异常，而且[确保](http://msdn.microsoft.com/library/738c4ccf-c29c-4c04-8d6c-f126bedf6e91)宏如果`CTaskDialog`显示或输入的参数是`NULL`。  
  
 一个`CTaskDialog`只能接受`HICON`或`LPCWSTR`为页脚图标。 这通过设置选项配置`TDF_USE_HICON_FOOTER`构造函数中或[CTaskDialog::SetOptions](#setoptions)。 默认情况下，`CTaskDialog`被配置为使用`LPCWSTR`作为页脚图标的输入类型。 如果您尝试设置所使用的不适当类型的图标，则此方法将引发异常。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&7;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_3.cpp)]  
  
##  <a name="setfootertext"></a>CTaskDialog::SetFooterText  
 更新的脚注文本`CTaskDialog`。  
  
```  
void SetFooterText(const CString& strFooterText);
```  
  
### <a name="parameters"></a>参数  
 [in] `strFooterText`  
 新的表尾的文本。  
  
### <a name="remarks"></a>备注  
 在底部的页脚文本旁边显示的页脚图标`CTaskDialog`。 您可以更改与页脚图标[CTaskDialog::SetFooterIcon](#setfootericon)。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&7;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_3.cpp)]  
  
##  <a name="setmainicon"></a>CTaskDialog::SetMainIcon  
 更新主图标的`CTaskDialog`。  
  
```  
void SetMainIcon(HICON hMainIcon);  
void SetMainIcon(LPCWSTR lpszMainIcon);
```  
  
### <a name="parameters"></a>参数  
 [in] `hMainIcon`  
 新建图标。  
  
 [in] `lpszMainIcon`  
 新建图标。  
  
### <a name="remarks"></a>备注  
 此方法将引发的异常，而且[确保](http://msdn.microsoft.com/library/738c4ccf-c29c-4c04-8d6c-f126bedf6e91)宏如果`CTaskDialog`显示或输入的参数是`NULL`。  
  
 一个`CTaskDialog`只能接受`HICON`或`LPCWSTR`作为主图标。 您可以通过设置配置此`TDF_USE_HICON_MAIN`选项构造函数中或在[CTaskDialog::SetOptions](#setoptions)方法。 默认情况下，`CTaskDialog`被配置为使用`LPCWSTR`作为主图标的输入类型。 如果您尝试设置所使用的不适当类型的图标，则此方法将引发异常。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&7;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_3.cpp)]  
  
##  <a name="setmaininstruction"></a>CTaskDialog::SetMainInstruction  
 更新的主指令`CTaskDialog`。  
  
```  
void SetMainInstruction(const CString& strInstructions);
```  
  
### <a name="parameters"></a>参数  
 [in] `strInstructions`  
 新的主要说明。  
  
### <a name="remarks"></a>备注  
 主要指令`CTaskDialog Class`是在向用户显示较大的加粗字体的文本。 位于在标题栏下的对话框。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&7;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_3.cpp)]  
  
##  <a name="setoptions"></a>CTaskDialog::SetOptions  
 为配置选项`CTaskDialog`。  
  
```  
void SetOptions(int nOptionFlag);
```  
  
### <a name="parameters"></a>参数  
 [in] `nOptionFlag`  
 一组标志用于`CTaskDialog`。  
  
### <a name="remarks"></a>备注  
 此方法会清除所有的当前选项`CTaskDialog`。 若要保留当前的选项，你必须检索它们首先与[CTaskDialog::GetOptions](#getoptions)并将其合并与你想要设置的选项。  
  
 下表列出了所有有效的选项。  
  
 `TDF_ENABLE_HYPERLINKS`  
 启用中的超链接`CTaskDialog`。  
  
 `TDF_USE_HICON_MAIN`  
 配置`CTaskDialog`使用`HICON`主图标。 替代方法是使用`LPCWSTR`。  
  
 `TDF_USE_HICON_FOOTER`  
 配置`CTaskDialog`使用`HICON`页脚图标。 替代方法是使用`LPCWSTR`。  
  
 `TDF_ALLOW_DIALOG_CANCELLATION`  
 使用户能够关闭`CTaskDialog`使用键盘或使用中的对话框中，右上角的图标即使**取消**按钮未启用。 如果未设置此标志和**取消**按钮未启用，用户不能通过使用 Alt + F4，Esc 键关闭对话框中或标题栏的关闭按钮。  
  
 `TDF_USE_COMMAND_LINKS`  
 配置`CTaskDialog`若要使用命令按钮控件。  
  
 `TDF_USE_COMMAND_LINKS_NO_ICON`  
 配置`CTaskDialog`若要使用命令按钮控件，而不会显示在控件旁边的图标。 `TDF_USE_COMMAND_LINKS` 重写 `TDF_USE_COMMAND_LINKS_NO_ICON`。  
  
 `TDF_EXPAND_FOOTER_AREA`  
 指示当前已展开的扩展区域。  
  
 `TDF_EXPANDED_BY_DEFAULT`  
 确定是否默认情况下展开的扩展区域。  
  
 `TDF_VERIFICATION_FLAG_CHECKED`  
 指示当前所选验证复选框。  
  
 `TDF_SHOW_PROGRESS_BAR`  
 配置`CTaskDialog`以显示一个进度栏。  
  
 `TDF_SHOW_MARQUEE_PROGRESS_BAR`  
 配置进度条为字幕进度条。 如果启用此选项，则必须设置`TDF_SHOW_PROGRESS_BAR`具有预期的行为。  
  
 `TDF_CALLBACK_TIMER`  
 指示`CTaskDialog`回调间隔设置为大约 200 毫秒。  
  
 `TDF_POSITION_RELATIVE_TO_WINDOW`  
 配置`CTaskDialog`相对于父窗口居中对齐。 如果未启用此标志，`CTaskDialog`处于居中位置相对于监视器。  
  
 `TDF_RTL_LAYOUT`  
 配置`CTaskDialog`实现从右到左阅读的布局。  
  
 `TDF_NO_DEFAULT_RADIO_BUTTON`  
 指示没有单选按钮处于选中状态时`CTaskDialog`出现。  
  
 `TDF_CAN_BE_MINIMIZED`  
 使用户能够最大程度减少`CTaskDialog`。 若要支持此选项，`CTaskDialog`不能为模式。 MFC 不支持此选项，因为 MFC 不支持无模式`CTaskDialog`。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&7;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_3.cpp)]  
  
##  <a name="setprogressbarmarquee"></a>CTaskDialog::SetProgressBarMarquee  
 配置的字幕条`CTaskDialog`并将其添加到对话框。  
  
```  
void SetProgressBarMarquee(
    BOOL bEnabled = TRUE,  
    int nMarqueeSpeed = 0);
```  
  
### <a name="parameters"></a>参数  
 [in] `bEnabled`  
 `TRUE`若要启用的字幕条;`FALSE`禁用字幕栏并将其从删除`CTaskDialog`。  
  
 [in] `nMarqueeSpeed`  
 一个整数，指示字幕条的速度。  
  
### <a name="remarks"></a>备注  
 主文本的下方会显示对字幕条`CTaskDialog Class`。  
  
 使用`nMarqueeSpeed`来设置该字幕条; 速度较大的值指示较慢的速度。 值为 0，`nMarqueeSpeed`这将使在默认的速度移动字幕栏[!INCLUDE[wiprlhext](../../c-runtime-library/reference/includes/wiprlhext_md.md)]。  
  
 此方法将引发的异常，而且[确保](http://msdn.microsoft.com/library/738c4ccf-c29c-4c04-8d6c-f126bedf6e91)宏如果`nMarqueeSpeed`小于 0。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&4;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_7.cpp)]  
  
##  <a name="setprogressbarposition"></a>CTaskDialog::SetProgressBarPosition  
 调整进度条的位置。  
  
```  
void SetProgressBarPosition(int nProgressPos);
```  
  
### <a name="parameters"></a>参数  
 [in] `nProgressPos`  
 进度条的位置。  
  
### <a name="remarks"></a>备注  
 此方法将引发的异常，而且[确保](http://msdn.microsoft.com/library/738c4ccf-c29c-4c04-8d6c-f126bedf6e91)宏如果`nProgressPos`不在进度栏范围内。 您可以更改与进度栏范围[CTaskDialog::SetProgressBarRange](#setprogressbarrange)。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&4;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_7.cpp)]  
  
##  <a name="setprogressbarrange"></a>CTaskDialog::SetProgressBarRange  
 调整进度条的范围。  
  
```  
void SetProgressBarRange(
    int nRangeMin,  
    int nRangeMax);
```  
  
### <a name="parameters"></a>参数  
 [in] `nRangeMin`  
 进度栏的下限。  
  
 [in] `nRangeMax`  
 进度栏的上限。  
  
### <a name="remarks"></a>备注  
 进度条的位置是相对于`nRangeMin`和`nRangeMax`。 例如，如果`nRangeMin`为 50 和`nRangeMax`为 100、 75 的位置为偶数进度条交叉。 使用[CTaskDialog::SetProgressBarPosition](#setprogressbarposition)设置进度栏的位置。  
  
 若要显示进度栏选项`TDF_SHOW_PROGRESS_BAR`必须启用和`TDF_SHOW_MARQUEE_PROGRESS_BAR`不能启用。 此方法将自动设置`TDF_SHOW_PROGRESS_BAR`并清除`TDF_SHOW_MARQUEE_PROGRESS_BAR`。 使用[CTaskDialog::SetOptions](#setoptions)以手动更改此实例的选项[CTaskDialog 类](../../mfc/reference/ctaskdialog-class.md)。  
  
 此方法将引发的异常，而且[确保](http://msdn.microsoft.com/library/738c4ccf-c29c-4c04-8d6c-f126bedf6e91)宏如果`nRangeMin`是不小于`nRangeMax`。 此方法也会引发异常如果`CTaskDialog`尚未显示，并且具有字幕进度条。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&4;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_7.cpp)]  
  
##  <a name="setprogressbarstate"></a>CTaskDialog::SetProgressBarState  
 设置进度栏的状态，并将其显示在`CTaskDialog`。  
  
```  
void SetProgressBarState(int nState = PBST_NORMAL);
```  
  
### <a name="parameters"></a>参数  
 [in] `nState`  
 进度栏的状态。 请参阅备注部分中有关可能的值。  
  
### <a name="remarks"></a>备注  
 此方法将引发的异常，而且[确保](http://msdn.microsoft.com/library/738c4ccf-c29c-4c04-8d6c-f126bedf6e91)宏如果`CTaskDialog`尚未显示，并且具有字幕进度条。  
  
 下表列出的可能值`nState`。 在所有这些情况下，进度条将填充常规彩色直到其达到指定的位位置。 此时，将会更改基于状态的颜色。  
  
 PBST_NORMAL  
 后进度条填满，则`CTaskDialog`不会更改则条形的颜色。 默认情况下，正则颜色为绿色。  
  
 PBST_ERROR  
 后进度条填满，则`CTaskDialog`则条形的颜色更改为错误颜色。 默认情况下，这为红色。  
  
 PBST_PAUSED  
 后进度条填满，则`CTaskDialog`则条形的颜色更改为暂停颜色。 默认情况下，这为黄色。  
  
 您可以设置与进度栏的停止位置[CTaskDialog::SetProgressBarPosition](#setprogressbarposition)。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&4;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_7.cpp)]  
  
##  <a name="setradiobuttonoptions"></a>CTaskDialog::SetRadioButtonOptions  
 启用或禁用的单选按钮。  
  
```  
void SetRadioButtonOptions(
    int nRadioButtonID,  
    BOOL bEnabled);
```  
  
### <a name="parameters"></a>参数  
 [in] `nRadioButtonID`  
 单选按钮控件的 ID。  
  
 [in] `bEnabled`  
 `TRUE`若要启用的单选按钮;`FALSE`若要禁用的单选按钮。  
  
### <a name="remarks"></a>备注  
 此方法将引发的异常，而且[确保](http://msdn.microsoft.com/library/738c4ccf-c29c-4c04-8d6c-f126bedf6e91)宏如果`nRadioButtonID`不单选按钮是有效 ID。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&3;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_2.cpp)]  
  
##  <a name="setverificationcheckbox"></a>CTaskDialog::SetVerificationCheckbox  
 设置验证复选框的选中的状态。  
  
```  
void SetVerificationCheckbox(BOOL bChecked);
```  
  
### <a name="parameters"></a>参数  
 [in] `bChecked`  
 `TRUE`要验证已选中复选框时`CTaskDialog`会显示出来;`FALSE`能够验证复选框处于未选中状态时`CTaskDialog`显示。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&5;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_4.cpp)]  
  
##  <a name="setverificationcheckboxtext"></a>CTaskDialog::SetVerificationCheckboxText  
 设置验证复选框的右侧会显示的文本。  
  
```  
void SetVerificationCheckboxText(CString& strVerificationText);
```  
  
### <a name="parameters"></a>参数  
 [in] `strVerificationText`  
 此方法显示验证复选框旁边的文本。  
  
### <a name="remarks"></a>备注  
 此方法将引发的异常，而且[确保](http://msdn.microsoft.com/library/738c4ccf-c29c-4c04-8d6c-f126bedf6e91)宏如果此实例`CTaskDialog Class`尚未显示。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&5;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_4.cpp)]  
  
##  <a name="setwindowtitle"></a>CTaskDialog::SetWindowTitle  
 设置的标题`CTaskDialog`。  
  
```  
void SetWindowTitle(CString& strWindowTitle);
```  
  
### <a name="parameters"></a>参数  
 [in] `strWindowTitle`  
 为新的标题`CTaskDialog`。  
  
### <a name="remarks"></a>备注  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&7;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_3.cpp)]  
  
##  <a name="showdialog"></a>CTaskDialog::ShowDialog  
 创建并显示`CTaskDialog`。  
  
```  
static INT_PTR ShowDialog(
    const CString& strContent,  
    const CString& strMainInstruction,  
    const CString& strTitle,  
    int nIDCommandControlsFirst,  
    int nIDCommandControlsLast,  
    int nCommonButtons = TDCBF_YES_BUTTON | TDCBF_NO_BUTTON,  
    int nTaskDialogOptions = TDF_ENABLE_HYPERLINKS | TDF_USE_COMMAND_LINKS,  
    const CString& strFooter = _T(""));
```  
  
### <a name="parameters"></a>参数  
 [in] `strContent`  
 要使用的内容的字符串`CTaskDialog`。  
  
 [in] `strMainInstruction`  
 主要指令`CTaskDialog`。  
  
 [in] `strTitle`  
 标题`CTaskDialog`。  
  
 [in] `nIDCommandControlsFirst`  
 第一个命令字符串 ID。  
  
 [in] `nIDCommandControlsLast`  
 最后一个命令字符串 ID。  
  
 [in] `nCommonButtons`  
 要添加的按钮的掩码`CTaskDialog`。  
  
 [in] `nTaskDialogOptions`  
 要使用的选项集`CTaskDialog`。  
  
 [in] `strFooter`  
 要用作页脚的字符串。  
  
### <a name="return-value"></a>返回值  
 一个整数，对应于由用户所做的选择。  
  
### <a name="remarks"></a>备注  
 此静态方法可以创建的实例`CTaskDialog Class`而无需显式创建`CTaskDialog`在代码中的对象。 因为没有任何`CTaskDialog`对象时，不能调用任何其他方法的`CTaskDialog`如果使用此方法以显示`CTaskDialog`给用户。  
  
 此方法通过使用您的应用程序的资源文件中的数据来创建命令按钮控件。 资源文件中的字符串表具有与关联的字符串 Id 的多个字符串。 此方法之间的字符串表中添加每个有效项的命令按钮控件`nIDCommandControlsFirst`和`nCommandControlsLast`(含） 之间。 对于这些命令的按钮控件，该字符串表中的字符串是控件的标题和字符串 ID 是控件的 id。  
  
 请参阅[CTaskDialog::SetOptions](#setoptions)有关有效选项的列表。  
  
 `CTaskDialog`用户选择常见按钮，command link 控件，或关闭时，将关闭`CTaskDialog`。 返回值是指示用户如何关闭对话框中的标识符。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFC_CTaskDialog #&1;](../../mfc/reference/codesnippet/cpp/ctaskdialog-class_5.cpp)]  
  
##  <a name="taskdialogcallback"></a>CTaskDialog::TaskDialogCallback  
 框架将调用此方法以响应各种 Windows 消息。  
  
```  
friend:  
HRESULT TaskDialogCallback(
    HWND hWnd,  
    UINT uNotification,  
    WPARAM wParam,  
    LPARAM lParam,  
    LONG_PTR dwRefData);
```  
  
### <a name="parameters"></a>参数  
 [in] `hwnd`  
 句柄`m_hWnd`结构`CTaskDialog`。  
  
 [in] `uNotification`  
 用于指定所生成的消息的通知代码。  
  
 [in] `wParam`  
 有关消息的详细信息。  
  
 [in] `lParam`  
 有关消息的详细信息。  
  
 [in] `dwRefData`  
 一个指向`CTaskDialog`回调消息适用于的对象。  
  
### <a name="return-value"></a>返回值  
 取决于特定的通知代码。 有关详细信息，请参阅备注部分。  
  
### <a name="remarks"></a>备注  
 默认实现`TaskDialogCallback`处理特定消息，然后调用相应方法[CTaskDialog 类](../../mfc/reference/ctaskdialog-class.md)。 例如，在响应`TDN_BUTTON_CLICKED`消息，`TaskDialogCallback`调用[CTaskDialog::OnCommandControlClick](#oncommandcontrolclick)。  
  
 值`wParam`和`lParam`取决于特定生成的消息。 它有可能一种或两个值为空。 下表列出了支持的默认通知和的值`wParam`和`lParam`表示。 如果重写此方法在派生类中的，应在下表中实现的每条消息的回调代码。  
  
|通知消息|`wParam` 值|`lParam` 值|  
|--------------------------|--------------------|--------------------|  
|`TDN_CREATED`|未使用。|未使用。|  
|`TDN_NAVIGATED`|未使用。|未使用。|  
|`TDN_BUTTON_CLICKED`|命令按钮控件 id。|未使用。|  
|`TDN_HYPERLINK_CLICKED`|未使用。|一个[LPCWSTR](http://msdn.microsoft.com/library/windows/desktop/aa383751)结构，它包含的链接。|  
|`TDN_TIMER`|时间 （毫秒） 以来`CTaskDialog`已创建或重置计时器。|未使用。|  
|`TDN_DESTROYED`|未使用。|未使用。|  
|`TDN_RADIO_BUTTON_CLICKED`|单选按钮 id。|未使用。|  
|`TDN_DIALOG_CONSTRUCTED`|未使用。|未使用。|  
|`TDN_VERIFICATION_CLICKED`|1 如果选中此复选框，如果它不为 0。|未使用。|  
|`TDN_HELP`|未使用。|未使用。|  
|`TDN_EXPANDO_BUTTON_CLICKED`|扩展区域处于折叠状态; 如果为&0;如果扩展文本显示非零。|未使用。|  
  
## <a name="see-also"></a>另请参阅  
 [类](../../mfc/reference/mfc-classes.md)   
 [CObject 类](../../mfc/reference/cobject-class.md)   
 [层次结构图](../../mfc/hierarchy-chart.md)   
 [演练︰ 向应用程序添加 CTaskDialog](../../mfc/walkthrough-adding-a-ctaskdialog-to-an-application.md)



