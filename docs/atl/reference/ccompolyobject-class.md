---
title: "CComPolyObject 类 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CComPolyObject
- ATLCOM/ATL::CComPolyObject
- ATLCOM/ATL::CComPolyObject::CComPolyObject
- ATLCOM/ATL::CComPolyObject::AddRef
- ATLCOM/ATL::CComPolyObject::CreateInstance
- ATLCOM/ATL::CComPolyObject::FinalConstruct
- ATLCOM/ATL::CComPolyObject::FinalRelease
- ATLCOM/ATL::CComPolyObject::QueryInterface
- ATLCOM/ATL::CComPolyObject::Release
- ATLCOM/ATL::CComPolyObject::m_contained
dev_langs:
- C++
helpviewer_keywords:
- aggregate objects [C++], in ATL
- aggregation [C++], ATL objects
- CComPolyObject class
ms.assetid: eaf67c18-e855-48ca-9b15-f1df3106121b
caps.latest.revision: 19
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
ms.openlocfilehash: 37be4c985983cb760246a4a2450c27d175d1f440
ms.lasthandoff: 02/24/2017

---
# <a name="ccompolyobject-class"></a>CComPolyObject 类
此类实现**IUnknown**聚合或非聚合对象。  
  
## <a name="syntax"></a>语法  
  
```
template<class contained>  
class CComPolyObject : public IUnknown,
      public CComObjectRootEx<contained::_ThreadModel::ThreadModelNoCS>
```  
  
#### <a name="parameters"></a>参数  
 `contained`  
 您的类，派生自[CComObjectRoot](../../atl/reference/ccomobjectroot-class.md)或[CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)，如你想要在对象上支持任何其他接口也一样。  
  
## <a name="members"></a>成员  
  
### <a name="public-constructors"></a>公共构造函数  
  
|名称|说明|  
|----------|-----------------|  
|[CComPolyObject::CComPolyObject](#ccompolyobject)|构造函数。|  
|[CComPolyObject:: ~ CComPolyObject](#dtor)|析构函数。|  
  
### <a name="public-methods"></a>公共方法  
  
|名称|描述|  
|----------|-----------------|  
|[CComPolyObject::AddRef](#addref)|递增该对象的引用计数。|  
|[CComPolyObject::CreateInstance](#createinstance)|（静态）允许您创建一个新**CComPolyObject** `contained` ** > **对象而不需要的开销[CoCreateInstance](http://msdn.microsoft.com/library/windows/desktop/ms686615)。|  
|[CComPolyObject::FinalConstruct](#finalconstruct)|执行的最后一个初始化`m_contained`。|  
|[CComPolyObject::FinalRelease](#finalrelease)|执行最终销毁`m_contained`。|  
|[CComPolyObject::QueryInterface](#queryinterface)|检索指向所请求的接口的指针。|  
|[CComPolyObject::Release](#release)|递减对象的引用计数。|  
  
### <a name="public-data-members"></a>公共数据成员  
  
|名称|说明|  
|----------|-----------------|  
|[CComPolyObject::m_contained](#m_contained)|委托**IUnknown**如果该对象进行了聚合或未知的外部对象中调用**IUnknown**如果对象未聚合的对象。|  
  
## <a name="remarks"></a>备注  
 `CComPolyObject`实现[IUnknown](http://msdn.microsoft.com/library/windows/desktop/ms680509)聚合或非聚合对象。  
  
 实例时`CComPolyObject`创建的外部值检查未知。 如果它是**NULL**， **IUnknown**对于非聚合对象的实现。 如果不是未知的外部对象**NULL**， **IUnknown**聚合对象实现。  
  
 使用的优点`CComPolyObject`是避免同时[CComAggObject](../../atl/reference/ccomaggobject-class.md)和[CComObject](../../atl/reference/ccomobject-class.md)模块来处理聚合的和非聚合情况中。 单个`CComPolyObject`对象处理这两种情况。 这意味着只有一份 vtable 和函数的一个副本存在于您的模块。 如果您 vtable 很大，这可以显著减少模块大小。 但是，如果您 vtable 很小，则使用`CComPolyObject`可能会导致稍大一些的模块的大小，因为它不优化聚合或非聚合对象，允许进行`CComAggObject`和`CComObject`。  
  
 如果`DECLARE_POLY_AGGREGATABLE`中对象的类定义中，指定宏`CComPolyObject`将用于创建您的对象。 `DECLARE_POLY_AGGREGATABLE`将自动声明如果使用 ATL 项目向导来创建完全控制或 Internet 资源管理器控件。  
  
 如果聚合，`CComPolyObject`对象都具有其自己**IUnknown**、 独立于外部对象**IUnknown**，并保留其自身的引用计数。 `CComPolyObject`使用[CComContainedObject](../../atl/reference/ccomcontainedobject-class.md)委托给未知的外部对象。  
  
 有关聚合的详细信息，请参阅文章[ATL COM 对象的基础知识](../../atl/fundamentals-of-atl-com-objects.md)。  
  
## <a name="inheritance-hierarchy"></a>继承层次结构  
 `CComObjectRootBase`  
  
 [CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)  
  
 `IUnknown`  
  
 `CComPolyObject`  
  
## <a name="requirements"></a>要求  
 **标头︰** atlcom.h  
  
##  <a name="addref"></a>CComPolyObject::AddRef  
 递增对对象的引用计数。  
  
```
STDMETHOD_(ULONG, AddRef)();
```  
  
### <a name="return-value"></a>返回值  
 可能是有用的诊断或测试一个值。  
  
##  <a name="ccompolyobject"></a>CComPolyObject::CComPolyObject  
 构造函数。  
  
```
CComPolyObject(void* pv);
```  
  
### <a name="parameters"></a>参数  
 `pv`  
 [in]一个指向未知的外部对象的对象是否进行聚合，或**NULL**如果对象未聚合的对象。  
  
### <a name="remarks"></a>备注  
 初始化`CComContainedObject`数据成员[m_contained](#m_contained)，和模块锁计数递增&1;。  
  
 析构函数递减模块锁计数。  
  
##  <a name="dtor"></a>CComPolyObject:: ~ CComPolyObject  
 析构函数。  
  
```
~CComPolyObject();
```  
  
### <a name="remarks"></a>备注  
 释放所有已分配的资源，调用[FinalRelease](#finalrelease)，并减少模块锁计数。  
  
##  <a name="createinstance"></a>CComPolyObject::CreateInstance  
 允许您创建一个新**CComPolyObject** `contained` ** > **对象而不需要的开销[CoCreateInstance](http://msdn.microsoft.com/library/windows/desktop/ms686615)。  
  
```
static HRESULT WINAPI CreateInstance(  
    LPUNKNOWN pUnkOuter, 
    CComPolyObject<contained>** pp);
```  
  
### <a name="parameters"></a>参数  
 `pp`  
 [out]一个指向**CComPolyObject** `contained` ** > **指针。 如果`CreateInstance`不成功，`pp`设置为**NULL**。  
  
### <a name="return-value"></a>返回值  
 标准 `HRESULT` 值。  
  
### <a name="remarks"></a>备注  
 返回的对象具有引用计数为零，因此请调用`AddRef`立即，然后使用**版本**以完成后释放对对象指针的引用。  
  
 如果您不需要直接访问对象，但仍想要创建新的对象，而不需要的开销`CoCreateInstance`，使用[CComCoClass::CreateInstance](../../atl/reference/ccomcoclass-class.md#createinstance)相反。  
  
##  <a name="finalconstruct"></a>CComPolyObject::FinalConstruct  
 调用对象构造的最后阶段，此方法对中执行任何最终初始化[m_contained](#m_contained)数据成员。  
  
```
HRESULT FinalConstruct();
```  
  
### <a name="return-value"></a>返回值  
 标准 `HRESULT` 值。  
  
##  <a name="finalrelease"></a>CComPolyObject::FinalRelease  
 在对象销毁过程中调用，此方法释放[m_contained](#m_contained)数据成员。  
  
```
void FinalRelease();
```  
  
##  <a name="m_contained"></a>CComPolyObject::m_contained  
 一个[CComContainedObject](../../atl/reference/ccomcontainedobject-class.md)从您的类派生的对象。  
  
```
CComContainedObject<contained> m_contained;
```  
  
### <a name="parameters"></a>参数  
 `contained`  
 [in]您的类，派生自[CComObjectRoot](../../atl/reference/ccomobjectroot-class.md)或[CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)，如你想要在对象上支持任何其他接口也一样。  
  
### <a name="remarks"></a>备注  
 **IUnknown**调用通过`m_contained`都委托给未知的外部对象中，如果该对象进行了聚合，或**IUnknown**此对象，如果对象不聚合。  
  
##  <a name="queryinterface"></a>CComPolyObject::QueryInterface  
 检索指向所请求的接口的指针。  
  
```
STDMETHOD(QueryInterface)(REFIID iid, void** ppvObject);
template <class Q>  
HRESULT QueryInterface(Q** pp);
```  
  
### <a name="parameters"></a>参数  
 `Q`  
 COM 接口中。  
  
 `iid`  
 [in]正在请求的接口的标识符。  
  
 `ppvObject`  
 [out]指向由标识的接口指针的指针`iid`。 如果该对象不支持此接口，`ppvObject`设置为**NULL**。  
  
 `pp`  
 [out]指向由所标识的接口的指针**__uuidof(Q)**。  
  
### <a name="return-value"></a>返回值  
 标准 `HRESULT` 值。  
  
### <a name="remarks"></a>备注  
 对于聚合对象，如果所请求的接口是**IUnknown**，`QueryInterface`返回指向聚合对象本身的指针**IUnknown**和递增引用计数。 否则，此方法通过接口会询问`CComContainedObject`数据成员[m_contained](#m_contained)。  
  
##  <a name="release"></a>CComPolyObject::Release  
 递减引用计数对象。  
  
```
STDMETHOD_(ULONG, Release)();
```  
  
### <a name="return-value"></a>返回值  
 在调试版本中**版本**返回一个值，可能是有用的诊断或测试。 在非调试生成中，**版本**始终返回 0。  
  
## <a name="see-also"></a>另请参阅  
 [CComObjectRootEx 类](../../atl/reference/ccomobjectrootex-class.md)   
 [DECLARE_POLY_AGGREGATABLE](http://msdn.microsoft.com/library/7569e738-cfbc-4404-ba1d-78dcefa3bdb3)   
 [类概述](../../atl/atl-class-overview.md)
