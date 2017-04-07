---
title: "CRgn 类 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CRgn
- AFXWIN/CRgn
- AFXWIN/CRgn::CRgn
- AFXWIN/CRgn::CombineRgn
- AFXWIN/CRgn::CopyRgn
- AFXWIN/CRgn::CreateEllipticRgn
- AFXWIN/CRgn::CreateEllipticRgnIndirect
- AFXWIN/CRgn::CreateFromData
- AFXWIN/CRgn::CreateFromPath
- AFXWIN/CRgn::CreatePolygonRgn
- AFXWIN/CRgn::CreatePolyPolygonRgn
- AFXWIN/CRgn::CreateRectRgn
- AFXWIN/CRgn::CreateRectRgnIndirect
- AFXWIN/CRgn::CreateRoundRectRgn
- AFXWIN/CRgn::EqualRgn
- AFXWIN/CRgn::FromHandle
- AFXWIN/CRgn::GetRegionData
- AFXWIN/CRgn::GetRgnBox
- AFXWIN/CRgn::OffsetRgn
- AFXWIN/CRgn::PtInRegion
- AFXWIN/CRgn::RectInRegion
- AFXWIN/CRgn::SetRectRgn
dev_langs:
- C++
helpviewer_keywords:
- HRGN
- CRgn class
- regions, MFC
ms.assetid: d904da84-76aa-481e-8780-b09485f49e64
caps.latest.revision: 23
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
ms.openlocfilehash: 9ec2634a2495d301e09b483d60db8838be0b14ab
ms.lasthandoff: 02/24/2017

---
# <a name="crgn-class"></a>CRgn 类
封装一个 Windows 图形设备接口 (GDI) 区域。  
  
## <a name="syntax"></a>语法  
  
```  
class CRgn : public CGdiObject  
```  
  
## <a name="members"></a>成员  
  
### <a name="public-constructors"></a>公共构造函数  
  
|名称|说明|  
|----------|-----------------|  
|[CRgn::CRgn](#crgn)|构造 `CRgn` 对象。|  
  
### <a name="public-methods"></a>公共方法  
  
|名称|说明|  
|----------|-----------------|  
|[CRgn::CombineRgn](#combinergn)|集`CRgn`对象，以便让它相当于两个指定的联合`CRgn`对象。|  
|[CRgn::CopyRgn](#copyrgn)|集`CRgn`对象，以便让它是指定的副本`CRgn`对象。|  
|[CRgn::CreateEllipticRgn](#createellipticrgn)|初始化`CRgn`具有椭圆区域的对象。|  
|[CRgn::CreateEllipticRgnIndirect](#createellipticrgnindirect)|初始化`CRgn`对象具有定义的椭圆区域[RECT](../../mfc/reference/rect-structure1.md)结构。|  
|[CRgn::CreateFromData](#createfromdata)|从给定的区域和转换数据创建一个区域。|  
|[CRgn::CreateFromPath](#createfrompath)|选入给定的设备上下文的路径中创建一个区域。|  
|[CRgn::CreatePolygonRgn](#createpolygonrgn)|初始化`CRgn`与多边形区域的对象。 系统多边形将自动关闭，如有必要，通过从最后一个顶点与第一个绘制的线。|  
|[CRgn::CreatePolyPolygonRgn](#createpolypolygonrgn)|初始化`CRgn`带有一系列闭合的多边形组成的区域的对象。 多边形可能是不相互连接，或者它们可能会重叠。|  
|[CRgn::CreateRectRgn](#createrectrgn)|初始化`CRgn`对象的矩形区域。|  
|[CRgn::CreateRectRgnIndirect](#createrectrgnindirect)|初始化`CRgn`对象定义的矩形区域[RECT](../../mfc/reference/rect-structure1.md)结构。|  
|[CRgn::CreateRoundRectRgn](#createroundrectrgn)|初始化`CRgn`具有带圆角矩形区域的对象。|  
|[CRgn::EqualRgn](#equalrgn)|检查两个`CRgn`对象来确定它们是否等效。|  
|[CRgn::FromHandle](#fromhandle)|返回一个指向`CRgn`对象时提供给 Windows 区域的句柄。|  
|[CRgn::GetRegionData](#getregiondata)|描述给定的区域的数据填充指定的缓冲区。|  
|[CRgn::GetRgnBox](#getrgnbox)|检索的绑定矩形的坐标`CRgn`对象。|  
|[CRgn::OffsetRgn](#offsetrgn)|将移动`CRgn`对象指定的偏移量。|  
|[CRgn::PtInRegion](#ptinregion)|确定指定的点是否在区域中。|  
|[CRgn::RectInRegion](#rectinregion)|确定指定的任何的矩形部分是否为该区域的边界内。|  
|[CRgn::SetRectRgn](#setrectrgn)|集`CRgn`对象传递给指定的矩形区域。|  
  
### <a name="public-operators"></a>公共运算符  
  
|名称|说明|  
|----------|-----------------|  
|[CRgn::operator HRGN](#operator_hrgn)|返回中包含的 Windows 句柄`CRgn`对象。|  
  
## <a name="remarks"></a>备注  
 区域是一个窗口内的一个椭圆或多边形区域。 若要使用的区域，您可以使用类的成员函数`CRgn`这两个剪辑函数定义为类的成员`CDC`。  
  
 成员函数`CRgn`创建、 更改和检索有关区域对象调用它们的信息。  
  
 有关详细信息使用`CRgn`，请参阅[图形对象](../../mfc/graphic-objects.md)。  
  
## <a name="inheritance-hierarchy"></a>继承层次结构  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CGdiObject](../../mfc/reference/cgdiobject-class.md)  
  
 `CRgn`  
  
## <a name="requirements"></a>要求  
 **标头:** afxwin.h  
  
##  <a name="combinergn"></a>CRgn::CombineRgn  
 通过组合两个现有区域来创建一个新的 GDI 区域。  
  
```  
int CombineRgn(
    CRgn* pRgn1,  
    CRgn* pRgn2,  
    int nCombineMode);
```  
  
### <a name="parameters"></a>参数  
 `pRgn1`  
 标识现有区域。  
  
 `pRgn2`  
 标识现有区域。  
  
 `nCombineMode`  
 指定要组合两个源区域时执行的操作。 它可以是下列值之一︰  
  
- **RGN_AND**使用的两个区域 （交点） 重叠区域。  
  
- **RGN_COPY**会创建一份地区 1 (由标识`pRgn1`)。  
  
- **RGN_DIFF**创建区域包含的区域的区域 1 (由标识`pRgn1`)，不是区域 2 的一部分 (由标识`pRgn2`)。  
  
- **RGN_OR**将其作为一个整体 （联合） 这两个地区的组合。  
  
- **RGN_XOR**组合两个区域，但将删除重叠区域。  
  
### <a name="return-value"></a>返回值  
 指定所生成的区域的类型。 它可以是下列值之一︰  
  
- **COMPLEXREGION**新区域有重叠的边框。  
  
- **错误**创建任何新区域。  
  
- **NULLREGION**新的区域为空。  
  
- **SIMPLEREGION**新区域具有不重叠的边框。  
  
### <a name="remarks"></a>备注  
 区域组合所指定的`nCombineMode`。  
  
 两个指定的区域结合使用，并生成区域句柄存储在`CRgn`对象。 因此，任何区域存储在`CRgn`对象被替换的组合的区域。  
  
 区域的大小被限制为 32767 的 32767 的逻辑单元或 64k 的内存，两者中较小。  
  
 使用[CopyRgn](#copyrgn)简单地将一个区域复制到另一个区域。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFCDocView #&144;](../../mfc/codesnippet/cpp/crgn-class_1.cpp)]  
  
##  <a name="copyrgn"></a>CRgn::CopyRgn  
 将所定义的区域复制`pRgnSrc`到`CRgn`对象。  
  
```  
int CopyRgn(CRgn* pRgnSrc);
```  
  
### <a name="parameters"></a>参数  
 `pRgnSrc`  
 标识现有区域。  
  
### <a name="return-value"></a>返回值  
 指定所生成的区域的类型。 它可以是下列值之一︰  
  
- **COMPLEXREGION**新区域有重叠的边框。  
  
- **错误**创建任何新区域。  
  
- **NULLREGION**新的区域为空。  
  
- **SIMPLEREGION**新区域具有不重叠的边框。  
  
### <a name="remarks"></a>备注  
 新的区域将替换以前存储在区域`CRgn`对象。 此函数是一种特殊情况的[CombineRgn](#combinergn)成员函数。  
  
### <a name="example"></a>示例  
  请参阅示例[CRgn::CreateEllipticRgn](#createellipticrgn)。  
  
##  <a name="createellipticrgn"></a>CRgn::CreateEllipticRgn  
 创建椭圆区域。  
  
```  
BOOL CreateEllipticRgn(
    int x1,  
    int y1,  
    int x2,  
    int y2);
```  
  
### <a name="parameters"></a>参数  
 `x1`  
 指定的椭圆的边框的左上角的逻辑 x 坐标。  
  
 `y1`  
 指定的椭圆的边框的左上角的逻辑 y 坐标。  
  
 `x2`  
 指定的椭圆的边框的右下角的逻辑 x 坐标。  
  
 `y2`  
 指定的椭圆的边框的右下角的逻辑 y 坐标。  
  
### <a name="return-value"></a>返回值  
 如果该操作成功，则非零值否则为 0。  
  
### <a name="remarks"></a>备注  
 该区域定义的由指定的绑定矩形`x1`， `y1`， `x2`，和`y2`。 该区域存储在`CRgn`对象。  
  
 区域的大小被限制为 32767 的 32767 的逻辑单元或 64k 的内存，两者中较小。  
  
 当它已完成使用区域创建`CreateEllipticRgn`函数，应用程序应选择的设备上下文和使用的区域出`DeleteObject`函数以将其删除。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFCDocView #&145;](../../mfc/codesnippet/cpp/crgn-class_2.cpp)]  
  
##  <a name="createellipticrgnindirect"></a>CRgn::CreateEllipticRgnIndirect  
 创建椭圆区域。  
  
```  
BOOL CreateEllipticRgnIndirect(LPCRECT lpRect);
```  
  
### <a name="parameters"></a>参数  
 `lpRect`  
 指向`RECT`结构或`CRect`对象，其中包含椭圆的边框的左上角和右下角中的逻辑坐标。  
  
### <a name="return-value"></a>返回值  
 如果该操作成功，则非零值否则为 0。  
  
### <a name="remarks"></a>备注  
 该区域定义的结构或指向的对象`lpRect`并存储在`CRgn`对象。  
  
 区域的大小被限制为 32767 的 32767 的逻辑单元或 64k 的内存，两者中较小。  
  
 当它已完成使用区域创建`CreateEllipticRgnIndirect`函数，应用程序应选择的设备上下文和使用的区域出`DeleteObject`函数以将其删除。  
  
### <a name="example"></a>示例  
  请参阅示例[CRgn::CreateRectRgnIndirect](#createrectrgnindirect)。  
  
##  <a name="createfromdata"></a>CRgn::CreateFromData  
 从给定的区域和转换数据创建一个区域。  
  
```  
BOOL CreateFromData(
    const XFORM* lpXForm,  
    int nCount,  
    const RGNDATA* pRgnData);
```  
  
### <a name="parameters"></a>参数  
 *lpXForm*  
 指向[XFORM](../../mfc/reference/xform-structure.md)数据结构，它定义要在区域上执行的转换。 如果此指针为**NULL**，用于标识转换。  
  
 `nCount`  
 指定所指向的字节数`pRgnData`。  
  
 `pRgnData`  
 指向[RGNDATA](../../mfc/reference/rgndata-structure.md)包含区域数据的数据结构。  
  
### <a name="return-value"></a>返回值  
 如果该函数成功，则为非 0；否则为 0。  
  
### <a name="remarks"></a>备注  
 应用程序可以通过调用来检索区域的数据`CRgn::GetRegionData`函数。  
  
##  <a name="createfrompath"></a>CRgn::CreateFromPath  
 选入给定的设备上下文的路径中创建一个区域。  
  
```  
BOOL CreateFromPath(CDC* pDC);
```  
  
### <a name="parameters"></a>参数  
 `pDC`  
 标识包含封闭的路径的设备上下文。  
  
### <a name="return-value"></a>返回值  
 如果该函数成功，则为非 0；否则为 0。  
  
### <a name="remarks"></a>备注  
 通过标识的设备上下文`pDC`参数必须包含封闭的路径。 之后`CreateFromPath`将为的路径的区域中，Windows 将丢弃从设备上下文已关闭的路径。  
  
##  <a name="createpolygonrgn"></a>CRgn::CreatePolygonRgn  
 创建一个多边形的区域。  
  
```  
BOOL CreatePolygonRgn(
    LPPOINT lpPoints,  
    int nCount,  
    int nMode);
```  
  
### <a name="parameters"></a>参数  
 `lpPoints`  
 指向数组的**点**结构或一组`CPoint`对象。 每个结构指定的 x 坐标和 y 坐标的多边形的一个顶点。 **点**结构具有以下形式︰  
  
 `typedef struct tagPOINT {`  
  
 `int x;`  
  
 `int y;`  
  
 `} POINT;`  
  
 `nCount`  
 指定的数**点**结构或`CPoint`指向数组中的对象`lpPoints`。  
  
 `nMode`  
 指定区域的填充模式。 此参数可能是**备用**或**缠绕**。  
  
### <a name="return-value"></a>返回值  
 如果该操作成功，则非零值否则为 0。  
  
### <a name="remarks"></a>备注  
 系统多边形将自动关闭，如有必要，通过从最后一个顶点与第一个绘制的线。 所生成的区域存储在`CRgn`对象。  
  
 区域的大小被限制为 32767 的 32767 的逻辑单元或 64k 的内存，两者中较小。  
  
 多边形填充模式时**备用**，系统填充每个扫描线上的奇数和偶数个多边形边之间的区域。 也就是说，系统填充的区域之间的第一个和第二个一侧，之间的第三个和第四个端，依次类推。  
  
 多边形填充模式时**缠绕**，系统将使用一个数字绘制来确定是否填充的区域的方向。 将以顺时针或逆时针方向绘制多边形内的每个直线线段。 每当从封闭区域到图的外部绘制的虚线通过顺时针方向的直线线段时，计数将递增。 当在行通过逆时针旋转直线线段时，计数会递减。 如果计数不为零的曲线到达图外部时，填充区域。  
  
 当应用程序已完成使用区域创建`CreatePolygonRgn`函数，它应选择的设备上下文和使用的区域出`DeleteObject`函数以将其删除。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFCDocView #&146;](../../mfc/codesnippet/cpp/crgn-class_3.cpp)]  
  
##  <a name="createpolypolygonrgn"></a>CRgn::CreatePolyPolygonRgn  
 创建一系列闭合的多边形组成的区域。  
  
```  
BOOL CreatePolyPolygonRgn(
    LPPOINT lpPoints,  
    LPINT lpPolyCounts,  
    int nCount,  
    int nPolyFillMode);
```  
  
### <a name="parameters"></a>参数  
 `lpPoints`  
 指向数组的**点**结构或一组`CPoint`定义多边形顶点的对象。 必须显式关闭每个多边形，因为系统不会自动关闭它们。 多边形是连续指定。 **点**结构具有以下形式︰  
  
 `typedef struct tagPOINT {`  
  
 `int x;`  
  
 `int y;`  
  
 `} POINT;`  
  
 `lpPolyCounts`  
 指向整数的数组。 第一个整数指定中第一个多边形的顶点的数量`lpPoints`数组，第二个整数指定的顶点数中的第二个多边形，依次类推。  
  
 `nCount`  
 指定在整数的总数`lpPolyCounts`数组。  
  
 `nPolyFillMode`  
 指定的多边形填充模式。 此值可能**备用**或**缠绕**。  
  
### <a name="return-value"></a>返回值  
 如果该操作成功，则非零值否则为 0。  
  
### <a name="remarks"></a>备注  
 所生成的区域存储在`CRgn`对象。  
  
 多边形可能是不相互连接，或者它们可能会重叠。  
  
 区域的大小被限制为 32767 的 32767 的逻辑单元或 64k 的内存，两者中较小。  
  
 多边形填充模式时**备用**，系统填充每个扫描线上的奇数和偶数个多边形边之间的区域。 也就是说，系统填充的区域之间的第一个和第二个一侧，之间的第三个和第四个端，依次类推。  
  
 多边形填充模式时**缠绕**，系统将使用一个数字绘制来确定是否填充的区域的方向。 将以顺时针或逆时针方向绘制多边形内的每个直线线段。 每当从封闭区域到图的外部绘制的虚线通过顺时针方向的直线线段时，计数将递增。 当在行通过逆时针旋转直线线段时，计数会递减。 如果计数不为零的曲线到达图外部时，填充区域。  
  
 当应用程序已完成使用区域创建`CreatePolyPolygonRgn`函数，它应选择的设备上下文和使用的区域出[CGDIObject::DeleteObject](../../mfc/reference/cgdiobject-class.md#deleteobject)成员函数以将其删除。  
  
##  <a name="createrectrgn"></a>CRgn::CreateRectRgn  
 创建存储在一个矩形区域`CRgn`对象。  
  
```  
BOOL CreateRectRgn(
    int x1,  
    int y1,  
    int x2,  
    int y2);
```  
  
### <a name="parameters"></a>参数  
 `x1`  
 指定区域的左上角的逻辑 x 坐标。  
  
 `y1`  
 指定区域的左上角的逻辑 y 坐标。  
  
 `x2`  
 指定区域的右下角的逻辑 x 坐标。  
  
 `y2`  
 指定区域的右下角的逻辑 y 坐标。  
  
### <a name="return-value"></a>返回值  
 如果该操作成功，则非零值否则为 0。  
  
### <a name="remarks"></a>备注  
 区域的大小被限制为 32767 的 32767 的逻辑单元或 64k 的内存，两者中较小。  
  
 当它已完成使用创建的区域`CreateRectRgn`，应用程序应使用[CGDIObject::DeleteObject](../../mfc/reference/cgdiobject-class.md#deleteobject)成员函数来删除该区域。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFCDocView #&147;](../../mfc/codesnippet/cpp/crgn-class_4.cpp)]  
  
 有关其他示例，请参阅[CRgn::CombineRgn](#combinergn)。  
  
##  <a name="createrectrgnindirect"></a>CRgn::CreateRectRgnIndirect  
 创建存储在一个矩形区域`CRgn`对象。  
  
```  
BOOL CreateRectRgnIndirect(LPCRECT lpRect);
```  
  
### <a name="parameters"></a>参数  
 `lpRect`  
 指向`RECT`结构或`CRect`对象，其中包含该区域的左上角和右下角中的逻辑坐标。 `RECT`结构具有以下形式︰  
  
 `typedef struct tagRECT {`  
  
 `int left;`  
  
 `int top;`  
  
 `int right;`  
  
 `int bottom;`  
  
 `} RECT;`  
  
### <a name="return-value"></a>返回值  
 如果该操作成功，则非零值否则为 0。  
  
### <a name="remarks"></a>备注  
 区域的大小被限制为 32767 的 32767 的逻辑单元或 64k 的内存，两者中较小。  
  
 当它已完成使用创建的区域`CreateRectRgnIndirect`，应用程序应使用[CGDIObject::DeleteObject](../../mfc/reference/cgdiobject-class.md#deleteobject)成员函数来删除该区域。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFCDocView #&148;](../../mfc/codesnippet/cpp/crgn-class_5.cpp)]  
  
##  <a name="createroundrectrgn"></a>CRgn::CreateRoundRectRgn  
 创建存储中的圆角矩形区域`CRgn`对象。  
  
```  
BOOL CreateRoundRectRgn(
    int x1,  
    int y1,  
    int x2,  
    int y2,  
    int x3,  
    int y3);
```  
  
### <a name="parameters"></a>参数  
 `x1`  
 指定区域的左上角的逻辑 x 坐标。  
  
 `y1`  
 指定区域的左上角的逻辑 y 坐标。  
  
 `x2`  
 指定区域的右下角的逻辑 x 坐标。  
  
 `y2`  
 指定区域的右下角的逻辑 y 坐标。  
  
 *x3*  
 指定用于创建圆的角的椭圆的宽度。  
  
 `y3`  
 指定用于创建圆的角的椭圆的高度。  
  
### <a name="return-value"></a>返回值  
 如果该操作成功，则非零值否则为 0。  
  
### <a name="remarks"></a>备注  
 区域的大小被限制为 32767 的 32767 的逻辑单元或 64k 的内存，两者中较小。  
  
 当应用程序已完成使用区域创建`CreateRoundRectRgn`函数，它应选择的设备上下文和使用的区域出[CGDIObject::DeleteObject](../../mfc/reference/cgdiobject-class.md#deleteobject)成员函数以将其删除。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFCDocView #&149;](../../mfc/codesnippet/cpp/crgn-class_6.cpp)]  
  
##  <a name="crgn"></a>CRgn::CRgn  
 构造 `CRgn` 对象。  
  
```  
CRgn();
```  
  
### <a name="remarks"></a>备注  
 `m_hObject`数据成员不包含有效的 Windows GDI 区域之前初始化对象，一个或多个其他`CRgn`成员函数。  
  
### <a name="example"></a>示例  
  请参阅示例[CRgn::CreateRoundRectRgn](#createroundrectrgn)。  
  
##  <a name="equalrgn"></a>CRgn::EqualRgn  
 确定给定的区域是否等效于存储在区域`CRgn`对象。  
  
```  
BOOL EqualRgn(CRgn* pRgn) const;  
```  
  
### <a name="parameters"></a>参数  
 `pRgn`  
 标识某个区域。  
  
### <a name="return-value"></a>返回值  
 如果两个区域相等，则非零值否则为 0。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFCDocView #&150;](../../mfc/codesnippet/cpp/crgn-class_7.cpp)]  
  
##  <a name="fromhandle"></a>CRgn::FromHandle  
 返回一个指向`CRgn`对象时提供给 Windows 区域的句柄。  
  
```  
static CRgn* PASCAL FromHandle(HRGN hRgn);
```  
  
### <a name="parameters"></a>参数  
 `hRgn`  
 指定一个 Windows 区域的句柄。  
  
### <a name="return-value"></a>返回值  
 一个指向`CRgn`对象。 如果函数未成功完成，返回值是**NULL**。  
  
### <a name="remarks"></a>备注  
 如果`CRgn`对象尚未附加到该句柄，一种临时`CRgn`创建对象并将其连接。 此临时`CRgn`对象是否有效，仅直到下一次应用程序在其事件循环内有空闲时间，在该时间所有临时图形对象会被删除。 另一种说法是一个窗口消息处理过程才有效临时对象。  
  
##  <a name="getregiondata"></a>CRgn::GetRegionData  
 描述该区域的数据填充指定的缓冲区。  
  
```  
int GetRegionData(
    LPRGNDATA lpRgnData,  
    int nCount) const;  
```  
  
### <a name="parameters"></a>参数  
 `lpRgnData`  
 指向[RGNDATA](../../mfc/reference/rgndata-structure.md)数据结构，它接收的信息。 如果此参数为**NULL**，返回值将包含所需的区域数据的字节数。  
  
 `nCount`  
 指定的大小，以字节为单位，`lpRgnData`缓冲区。  
  
### <a name="return-value"></a>返回值  
 如果函数成功和`nCount`指定足够数量的字节，返回值也始终`nCount`。 如果函数失败，或者如果`nCount`指定小于比足够数量的字节数，返回值为 0 （错误）。  
  
### <a name="remarks"></a>备注  
 此数据包括构成该区域的矩形的尺寸。 结合使用此函数`CRgn::CreateFromData`函数。  
  
##  <a name="getrgnbox"></a>CRgn::GetRgnBox  
 检索的绑定矩形的坐标`CRgn`对象。  
  
```  
int GetRgnBox(LPRECT lpRect) const;  
```  
  
### <a name="parameters"></a>参数  
 `lpRect`  
 指向`RECT`结构或`CRect`对象以便接收的边框的坐标。 `RECT`结构具有以下形式︰  
  
 `typedef struct tagRECT {`  
  
 `int left;`  
  
 `int top;`  
  
 `int right;`  
  
 `int bottom;`  
  
 `} RECT;`  
  
### <a name="return-value"></a>返回值  
 指定区域的类型。 它可以是任何以下值︰  
  
- **COMPLEXREGION**区域有重叠的边框。  
  
- **NULLREGION**区域为空。  
  
- **错误**`CRgn`对象未指定有效的区域。  
  
- **SIMPLEREGION**区域具有不重叠的边框。  
  
### <a name="example"></a>示例  
  请参阅示例[CRgn::CreatePolygonRgn](#createpolygonrgn)。  
  
##  <a name="offsetrgn"></a>CRgn::OffsetRgn  
 移动存储在区域`CRgn`对象指定的偏移量。  
  
```  
int OffsetRgn(
    int x,  
    int y);  
  
int OffsetRgn(POINT point);
```  
  
### <a name="parameters"></a>参数  
 *x*  
 指定要向左移动或向右的单位数。  
  
 *y*  
 指定要上移或下移的单位数。  
  
 `point`  
 X 坐标`point`指定左移或向右的单位数。 Y 坐标`point`指定要上移或下移的单位数。 `point`参数可能**点**结构或`CPoint`对象。  
  
### <a name="return-value"></a>返回值  
 新的区域类型。 它可以是下列值之一︰  
  
- **COMPLEXREGION**区域有重叠的边框。  
  
- **错误**区域句柄无效。  
  
- **NULLREGION**区域为空。  
  
- **SIMPLEREGION**区域具有不重叠的边框。  
  
### <a name="remarks"></a>备注  
 该函数将移动区域*x*沿 x 轴单位并*y*沿 y 轴的单位。  
  
 一个区域的坐标值必须小于或等于 32767 且大于或等于-32768。 *X*和*y*参数必须仔细选择，以防止无效的区域坐标。  
  
### <a name="example"></a>示例  
  请参阅示例[CRgn::CreateEllipticRgn](#createellipticrgn)。  
  
##  <a name="operator_hrgn"></a>CRgn::operator HRGN  
 使用此运算符将获得附加的 Windows GDI 句柄的`CRgn`对象。  
  
```  
operator HRGN() const;  
```  
  
### <a name="return-value"></a>返回值  
 如果成功，Windows GDI 对象的句柄由表示`CRgn`对象; 否则为**NULL**。  
  
### <a name="remarks"></a>备注  
 此运算符被强制转换运算符，它支持直接使用**HRGN**对象。  
  
 有关使用图形对象的详细信息，请参阅文章[图形对象](http://msdn.microsoft.com/library/windows/desktop/dd144962)中[!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]。  
  
##  <a name="ptinregion"></a>CRgn::PtInRegion  
 检查是否由给定的点*x*和*y*存储在区域中`CRgn`对象。  
  
```  
BOOL PtInRegion(
    int x,  
    int y) const;  
  
BOOL PtInRegion(POINT point) const;  
```  
  
### <a name="parameters"></a>参数  
 *x*  
 指定要测试的点的逻辑 x 坐标。  
  
 *y*  
 指定要测试的点的逻辑 y 坐标。  
  
 `point`  
 X 和 y 坐标`point`指定要测试的值的点 x 和 y 坐标。 `point`参数可以是**点**结构或`CPoint`对象。  
  
### <a name="return-value"></a>返回值  
 非零，如果该点位于该区域;否则为 0。  
  
##  <a name="rectinregion"></a>CRgn::RectInRegion  
 确定指定的矩形的任何部分`lpRect`中存储的区域的边界内`CRgn`对象。  
  
```  
BOOL RectInRegion(LPCRECT lpRect) const;  
```  
  
### <a name="parameters"></a>参数  
 `lpRect`  
 指向`RECT`结构或`CRect`对象。 `RECT`结构具有以下形式︰  
  
 `typedef struct tagRECT {`  
  
 `int left;`  
  
 `int top;`  
  
 `int right;`  
  
 `int bottom;`  
  
 `} RECT;`  
  
### <a name="return-value"></a>返回值  
 非零，如果指定的任何的矩形部分存在于区域的边界内否则为 0。  
  
##  <a name="setrectrgn"></a>CRgn::SetRectRgn  
 创建一个矩形区域。  
  
```  
void SetRectRgn(
    int x1,  
    int y1,  
    int x2,  
    int y2);  
  
void SetRectRgn(LPCRECT lpRect);
```  
  
### <a name="parameters"></a>参数  
 `x1`  
 指定的矩形区域的左上角的 x 坐标。  
  
 `y1`  
 指定的矩形区域的左上角的 y 坐标。  
  
 `x2`  
 指定的矩形区域的右下角的 x 坐标。  
  
 `y2`  
 指定的矩形区域的右下角的 y 坐标。  
  
 `lpRect`  
 指定的矩形区域。 可以是到指针`RECT`结构或`CRect`对象。  
  
### <a name="remarks"></a>备注  
 与不同[CreateRectRgn](#createrectrgn)，但是，它不会分配任何额外的内存从本地 Windows 应用程序堆。 相反，它使用为该区域存储在分配的空间`CRgn`对象。 这意味着，`CRgn`对象必须具有已初始化与有效的 Windows 区域之前，先调用`SetRectRgn`。 由给定的点`x1`， `y1`， `x2`，和`y2`指定已分配空间的最小大小。  
  
 使用此函数，而不是`CreateRectRgn`成员函数，以避免对本地内存管理器调用。  
  
## <a name="see-also"></a>另请参阅  
 [CWnd 类](../../mfc/reference/cwnd-class.md)   
 [层次结构图](../../mfc/hierarchy-chart.md)



