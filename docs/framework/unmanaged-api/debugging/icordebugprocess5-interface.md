---
title: ICorDebugProcess5-Schnittstelle
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugProcess5
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugProcess5
helpviewer_keywords: ICorDebugProcess5 interface [.NET Framework debugging]
ms.assetid: 30a39d79-1f10-4328-9c5d-094ed824e2ba
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 0f0a46e18121a222ee62fec207dde938d1e967b5
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugprocess5-interface"></a>ICorDebugProcess5-Schnittstelle
ICorDebugProcess-Schnittstelle, um Zugriff auf den verwalteten Heap an, um Informationen zum Garbagecollection verwalteten Objekte bereitzustellen unterstützen erweitert, und lädt bestimmen, ob ein Debugger Bilder vom lokalen systemeigenen Imagecache von Anwendung.  
  
## <a name="methods"></a>Methoden  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[EnableNGenPolicy-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enablengenpolicy-method.md)|Legt einen Wert, der bestimmt, wie eine Anwendung während der Ausführung unter einem verwalteten Debugger systemeigene Abbilder lädt.|  
|[EnumerateGCReferences-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerategcreferences-method.md)|Ruft einen Enumerator für alle Objekte, die in einem Prozess speicherbereinigt werden soll.|  
|[EnumerateHandles-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumeratehandles-method.md)|Ruft einen Enumerator für die Objekt-Handles in einem Prozess ab.|  
|[EnumerateHeap-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerateheap-method.md)|Ruft einen Enumerator für Objekte im verwalteten Heap.|  
|[EnumerateHeapRegions-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerateheapregions-method.md)|Ruft einen Enumerator für die Regionen des verwalteten Heaps.|  
|[GetArrayLayout-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-getarraylayout-method.md)|Ruft Informationen zum Layout eines Arrays im Arbeitsspeicher ab.|  
|[GetGCHeapInformation-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-getgcheapinformation-method.md)|Ruft einen Zeiger auf eine [COR_HEAPINFO](../../../../docs/framework/unmanaged-api/debugging/cor-heapinfo-structure.md) -Struktur, die Informationen zu Objekten enthält, die Garbage Collection auf dem verwalteten Heap werden sollen.|  
|[GetObject-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-getobject-method.md)|Ruft einen Zeiger auf ein Objekt ab, auf dem verwalteten Heap.|  
|[GetTypeFields-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-gettypefields-method.md)|Ruft einen Zeiger auf ein Array, das Feldinformationen für einen Typ auf Grundlage seines Bezeichners Typ enthält.|  
|[GetTypeForTypeID-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-gettypefortypeid-method.md)|Ruft ein Objekt vom Typ, der Informationen zu einem Objekt basierend auf seiner Typenbezeichnern bereitstellt.|  
|[GetTypeID-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-gettypeid-method.md)|Ruft die Typ-ID für das Objekt an einer angegebenen Adresse an.|  
|[GetTypeLayout-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-gettypelayout-method.md)|Ruft Informationen zum Layout eines Objekts im Arbeitsspeicher auf Grundlage seines Bezeichners Typ ab.|  
  
## <a name="remarks"></a>Hinweise  
 Diese Schnittstelle erweitert logisch die ICorDebugProcess ICorDebugProcess2, und [ICorDebugProcess3](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess3-interface.md) Schnittstellen.  
  
> [!NOTE]
>  Diese Schnittstelle unterstützt keine Remote aufgerufen werden, von einem anderen Computer oder einem anderen Prozess.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** CorDebug.idl, CorDebug.h  
  
 **Bibliothek:** CorGuids.lib  
  
 **.NET Framework-Versionen:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch  
 [Debugschnittstellen](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [Debuggen](../../../../docs/framework/unmanaged-api/debugging/index.md)