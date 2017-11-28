---
title: "ICorDebugValue 接口 1"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugValue
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugValue
helpviewer_keywords: ICorDebugValue interface [.NET Framework debugging]
ms.assetid: b2f7007f-c446-4b18-aed1-a25cff8aee31
topic_type: apiref
caps.latest.revision: "17"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 01c94df1d8e6ddef0110268461a2b28f594201b6
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugvalue-interface1"></a><span data-ttu-id="a1ddc-102">ICorDebugValue 接口 1</span><span class="sxs-lookup"><span data-stu-id="a1ddc-102">ICorDebugValue Interface1</span></span>
<span data-ttu-id="a1ddc-103">表示正在调试的进程中的值。</span><span class="sxs-lookup"><span data-stu-id="a1ddc-103">Represents a value in the process being debugged.</span></span> <span data-ttu-id="a1ddc-104">值可以是读取或写入值。</span><span class="sxs-lookup"><span data-stu-id="a1ddc-104">The value can be a read or a write value.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a1ddc-105">方法</span><span class="sxs-lookup"><span data-stu-id="a1ddc-105">Methods</span></span>  
  
|<span data-ttu-id="a1ddc-106">方法</span><span class="sxs-lookup"><span data-stu-id="a1ddc-106">Method</span></span>|<span data-ttu-id="a1ddc-107">描述</span><span class="sxs-lookup"><span data-stu-id="a1ddc-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a1ddc-108">CreateBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="a1ddc-108">CreateBreakpoint Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-createbreakpoint-method.md)|<span data-ttu-id="a1ddc-109">当前未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="a1ddc-109">This method is not currently implemented.</span></span>|  
|[<span data-ttu-id="a1ddc-110">GetAddress 方法</span><span class="sxs-lookup"><span data-stu-id="a1ddc-110">GetAddress Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getaddress-method.md)|<span data-ttu-id="a1ddc-111">获取此地址`ICorDebugValue`对象，它是正在调试的过程中。</span><span class="sxs-lookup"><span data-stu-id="a1ddc-111">Gets the address of this `ICorDebugValue` object, which is in the process of being debugged.</span></span>|  
|[<span data-ttu-id="a1ddc-112">GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="a1ddc-112">GetSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getsize-method.md)|<span data-ttu-id="a1ddc-113">获取以字节为单位，此大小，`ICorDebugValue`对象。</span><span class="sxs-lookup"><span data-stu-id="a1ddc-113">Gets the size, in bytes, of this `ICorDebugValue` object.</span></span>|  
|[<span data-ttu-id="a1ddc-114">GetType 方法</span><span class="sxs-lookup"><span data-stu-id="a1ddc-114">GetType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-gettype-method.md)|<span data-ttu-id="a1ddc-115">获取此的基元类型`ICorDebugValue`对象。</span><span class="sxs-lookup"><span data-stu-id="a1ddc-115">Gets the primitive type of this `ICorDebugValue` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a1ddc-116">备注</span><span class="sxs-lookup"><span data-stu-id="a1ddc-116">Remarks</span></span>  
 <span data-ttu-id="a1ddc-117">一般情况下，它返回时，被传递值对象的所有权。</span><span class="sxs-lookup"><span data-stu-id="a1ddc-117">In general, ownership of a value object is passed when it is returned.</span></span> <span data-ttu-id="a1ddc-118">接收方负责完成与对象从对象中移除引用。</span><span class="sxs-lookup"><span data-stu-id="a1ddc-118">The recipient is responsible for removing a reference from the object when it is finished with the object.</span></span>  
  
 <span data-ttu-id="a1ddc-119">具体取决于其中的值从检索，值可能不会保持有效后恢复进程。</span><span class="sxs-lookup"><span data-stu-id="a1ddc-119">Depending on where the value was retrieved from, the value may not remain valid after the process is resumed.</span></span> <span data-ttu-id="a1ddc-120">因此，一般情况下，保持的值不应在的调用[icordebugcontroller:: Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="a1ddc-120">So, in general, the value shouldn't be held across a call of the [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a1ddc-121">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="a1ddc-121">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a1ddc-122">要求</span><span class="sxs-lookup"><span data-stu-id="a1ddc-122">Requirements</span></span>  
 <span data-ttu-id="a1ddc-123">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a1ddc-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1ddc-124">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a1ddc-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a1ddc-125">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a1ddc-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a1ddc-126">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a1ddc-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1ddc-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a1ddc-127">See Also</span></span>  
    
    
    
    
 [<span data-ttu-id="a1ddc-128">ICorDebugValue3 接口</span><span class="sxs-lookup"><span data-stu-id="a1ddc-128">ICorDebugValue3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md)  
 [<span data-ttu-id="a1ddc-129">调试接口</span><span class="sxs-lookup"><span data-stu-id="a1ddc-129">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)