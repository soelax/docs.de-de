---
title: ICorDebugDataTarget2::CreateVirtualUnwinder-Methode
ms.date: 03/30/2017
ms.assetid: 354c8b4c-7d23-45c6-a7d7-3be4c2a5b772
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f3782686f3caad6859aa81957f10e585265be340
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54585483"
---
# <a name="icordebugdatatarget2createvirtualunwinder-method"></a>ICorDebugDataTarget2::CreateVirtualUnwinder-Methode
Erstellt einen neuen Stapelentlader, der mit dem Entladen bei einem Anfangskontext beginnt (welcher nicht unbedingt das Blatt eines Threads ist).  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT CreateVirtualUnwinder(  
    [in] DWORD nativeThreadID,  
    [in] ULONG32 contextFlags,  
    [in] ULONG32 cbContext,  
    [in, size_is(cbContext)] BYTE initialContext[],  
    [out] ICorDebugVirtualUnwinder ** ppUnwinder);  
};  
```  
  
#### <a name="parameters"></a>Parameter  
 nativeThreadID  
 [in] Die systemeigene Thread-ID für den Thread, dessen Stapel entladen wird.  
  
 contextFlags  
 [in] Flags, die angeben, welche Teile des Kontexts in `initialContext` definiert sind.  
  
 cbContext  
 [in] Die Größe des `initialContext`.  
  
 initialContext  
 [in] Die Daten im Kontext.  
  
 ppUnwinder  
 [out] Ein Zeiger auf die Adresse eines ICorDebugVirtualUnwinder-Oberflächenobjekts.  
  
## <a name="return-value"></a>Rückgabewert  
 Bei Erfolg `S_OK`. Alle anderen `HRESULT` weisen auf Fehler hin. Alle fehlerhaften `HRESULT` von Mscordbi empfangenen als schwerwiegend und führt dazu, dass [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) Methoden zurückgeben `CORDBG_E_DATA_TARGET_ERROR`.  
  
## <a name="remarks"></a>Hinweise  
  
> [!NOTE]
>  Diese Methode ist nur mit .NET Native verfügbar.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** CorDebug.idl, CorDebug.h  
  
 **Bibliothek:** CorGuids.lib  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Siehe auch
- [ICorDebugDataTarget2-Schnittstelle](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-interface.md)
- [Debuggen von Schnittstellen](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
