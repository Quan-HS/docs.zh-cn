---
title: ICorDebugModule::IsInMemory 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.IsInMemory
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::IsInMemory
helpviewer_keywords:
- IsInMemory method [.NET Framework debugging]
- ICorDebugModule::IsInMemory method [.NET Framework debugging]
ms.assetid: 89940711-98e7-4aa6-bffc-5e39e91e1b7d
topic_type:
- apiref
ms.openlocfilehash: c5fa55a84ed8907a5072f6099c3bf02cd6d78683
ms.sourcegitcommit: 488aced39b5f374bc0a139a4993616a54d15baf0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2020
ms.locfileid: "83213122"
---
# <a name="icordebugmoduleisinmemory-method"></a>ICorDebugModule::IsInMemory 方法
获取一个值，该值指示此模块是否仅存在于内存中。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT IsInMemory(  
    [out] BOOL *pInMemory  
);  
```  
  
## <a name="parameters"></a>参数  
 `pInMemory`  
 [out] `true`如果此模块仅存在于内存中，则为;否则为 `false` 。  
  
## <a name="remarks"></a>备注  
 公共语言运行时（CLR）支持从原始字节流加载模块。 此类模块称为*内存中模块*，不存在于磁盘上。  
  
## <a name="requirements"></a>要求  
 **平台：** 请参阅[系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅
