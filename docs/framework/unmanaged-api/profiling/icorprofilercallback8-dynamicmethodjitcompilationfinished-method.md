---
title: ICorProfilerCallback8::DynamicMethodJITCompilationFinished-Methode
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback8.DynamicMethodJITCompilationFinished
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: addaf6333914c9f0ea36d67e3eb96577fef79e1e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54497917"
---
# <a name="icorprofilercallback8dynamicmethodjitcompilationfinished-method"></a>ICorProfilerCallback8::DynamicMethodJITCompilationFinished-Methode
[Wird nur in der .NET Framework 4.7 und höheren Versionen unterstützt]  
  
Benachrichtigt den Profiler an, wenn JIT-Kompilierung einer dynamischen Methode abgeschlossen wurde.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT DynamicMethodJITCompilationFinished(  
     [in]  FunctionID  functionId,   
     [in]  BOOL        hrStatus,   
     [in]  BOOL        fIsSafeToBlock   
);  
```  
  
#### <a name="parameters"></a>Parameter  
[in] `functionId`  
Der Bezeichner der in-Memory-Funktion, die für die JIT-Kompilierung gestartet wird.   

[in] `hrStatus`   
Ein Wert, der angibt, ob die JIT-Kompilierung erfolgreich war.

[in] `fIsSafeToBlock`   
`true` um anzugeben, das blockieren die Laufzeit zu warten, bis der aufrufende Thread von diesem Rückruf zurück zur Folge haben. `false` um anzugeben, dass die Blockierung der Vorgang der Laufzeit nicht beeinflusst wird.  

## <a name="remarks"></a>Hinweise  

Dieser Rückruf wird immer dann ausgelöst, wenn JIT-Kompilierung einer dynamischen Methode abgeschlossen ist. Dies umfasst verschiedene IL-Stubs und LCG-Methoden. Das Ziel ist, die Profiler-Schreiber genügend Informationen zum Identifizieren der kompilierten Methode für Benutzer bereitstellen.

> [!NOTE]
> `functionId` Werte können nicht zum Auflösen in ihren Metadatentoken verwendet werden, da dynamische Methoden keine Metadaten haben.

## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** CorProf.idl, CorProf.h  
  
 **Bibliothek:** CorGuids.lib  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  
  
## <a name="see-also"></a>Siehe auch
- [DynamicMethodJITCompilationStarted-Methode](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [ICorProfilerCallback8-Schnittstelle](icorprofilercallback8-interface.md)
