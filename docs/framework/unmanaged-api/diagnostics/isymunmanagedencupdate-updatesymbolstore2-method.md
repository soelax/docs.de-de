---
title: ISymUnmanagedENCUpdate::UpdateSymbolStore2-Methode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.UpdateSymbolStore2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::UpdateSymbolStore2
helpviewer_keywords:
- ISymUnmanagedENCUpdate::UpdateSymbolStore2 method [.NET Framework debugging]
- UpdateSymbolStore2 method [.NET Framework debugging]
ms.assetid: 35588317-6184-485c-ab41-4b15fc1765d9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b5a7d678d03435aa483ae4a4102672df504199d6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54550616"
---
# <a name="isymunmanagedencupdateupdatesymbolstore2-method"></a>ISymUnmanagedENCUpdate::UpdateSymbolStore2-Methode
Ermöglicht es einen Compiler, um Funktionen, die nicht aus dem Stream Programm Programmdatenbankdatei (PDB) geändert wurden zu unterdrücken, sofern die Zeileninformationen die Anforderungen erfüllt. Die richtige Zeileninformationen kann mit der alten Zeileninformationen für die PDB-Datei und einem Delta für alle Zeilen in der Funktion bestimmt werden.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT UpdateSymbolStore2(  
    [in]  IStream      *pIStream,  
    [in]  SYMLINEDELTA* pDeltaLines,  
    [in]  ULONG         cDeltaLines);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pIStream`  
 [in] Ein Zeiger auf ein [IStream](/windows/desktop/api/objidl/nn-objidl-istream) , das die Zeileninformationen enthält.  
  
 `pDeltaLines`  
 [in] Ein Zeiger auf eine [SYMLINEDELTA](../../../../docs/framework/unmanaged-api/diagnostics/symlinedelta-structure.md) Struktur, die die Zeilen enthält, die geändert wurden.  
  
 `cDeltaLines`  
 [in] Ein `ULONG` , die die Anzahl der Zeilen, die geändert wurden.  
  
## <a name="return-value"></a>Rückgabewert  
 S_OK, wenn die Methode erfolgreich ist; andernfalls E_FAIL oder einen anderen Fehlercode.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Siehe auch
- [ISymUnmanagedENCUpdate-Schnittstelle](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)
