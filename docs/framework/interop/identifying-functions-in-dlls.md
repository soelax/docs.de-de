---
title: Identifizieren von Funktionen in DLLs
ms.date: 03/30/2017
helpviewer_keywords:
- platform invoke, identifying functions
- COM interop, DLL functions
- unmanaged functions
- COM interop, platform invoke
- interoperation with unmanaged code, DLL functions
- interoperation with unmanaged code, platform invoke
- identifying DLL functions
- DLL functions
ms.assetid: 3e3f6780-6d90-4413-bad7-ba641220364d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: eb1aba9e794928b0eb905722e2a5d7df84100ea4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54729209"
---
# <a name="identifying-functions-in-dlls"></a>Identifizieren von Funktionen in DLLs
Die Identität einer DLL-Funktion besteht aus den folgenden Elementen:  
  
-   Funktionsname oder Ordinalzahl  
  
-   Name der DLL-Datei, in der die Implementierung gefunden werden kann  
  
 Die Angabe der **MessageBox**-Funktion in der „User32.dll“ gibt beispielsweise die Funktion (**MessageBox**) und deren Speicherort (User32.dll, User32 oder user32) an. Die Microsoft Windows-Anwendungsprogrammierschnittstelle (Win32-API) kann zwei Versionen jeder Funktion enthalten, die Zeichen und Zeichenfolgen behandelt: eine ANSI-Version mit 1-Byte-Zeichen und eine Unicode-Version mit 2-Byte-Zeichen. Ohne Angabe wird der Zeichensatz, der durch das <xref:System.Runtime.InteropServices.DllImportAttribute.CharSet>-Feld dargestellt wird, standardmäßig auf ANSI festgelegt. Einige Funktionen können über mehr als zwei Versionen verfügen.  
  
 **MessageBoxA** ist der ANSI-Einstiegspunkt für die **MessageBox**-Funktion. **MessageBoxW** ist die Unicode-Version. Sie können Funktionsnamen für eine bestimmte DLL-Datei, z.B. „User32.dll“, auflisten, indem Sie eine Vielzahl von Befehlszeilentools ausführen. Beispielsweise können Sie `dumpbin /exports user32.dll` oder `link /dump /exports user32.dll` verwenden, um Funktionsnamen abzurufen.  
  
 Sie können eine nicht verwaltete Funktion innerhalb des Codes beliebig umbenennen, solange Sie den neuen Namen für den ursprünglichen Einstiegspunkt in der DLL zuordnen. Anweisungen zur Umbenennung einer nicht verwalteten DLL-Funktion in verwaltetem Quellcode finden Sie unter [Angeben eines Einstiegspunktes](../../../docs/framework/interop/specifying-an-entry-point.md).  
  
 Durch einen Plattformaufruf können Sie einen beträchtlichen Teil des Betriebssystems durch Aufrufen von Funktionen in der Win32-API und anderen DLLs steuern. Zusätzlich zur Win32-API stehen Ihnen über Ihren Plattformaufruf zahlreiche andere APIs und DLLs zur Verfügung.  
  
 Die folgende Tabelle beschreibt einige häufig verwendete DLLs in der Win32-API.  
  
|DLL|Inhaltsbeschreibung|  
|---------|-----------------------------|  
|GDI32.dll|Funktionen für Graphics Device Interface (GDI) für Geräteausgaben, wie z.B. die für die Verwaltung der Zeichnung und Schriftart.|  
|Kernel32.dll|Betriebssystemfunktionen auf niedriger Ebene für die Verwaltung des Arbeitsspeichers und Ressourcenbehandlung.|  
|User32.dll|Windows-Verwaltungsfunktionen für Meldungsbehandlung, Timer, Menüs und Kommunikation.|  
  
 Eine vollständige Dokumentation für die Win32-API finden Sie im Plattform SDK. Beispiele für die Vorgehensweise beim Erstellen von .NET-basierten Deklarationen, die mit dem Plattformaufruf verwendet werden können, finden Sie unter [Marshaling Data with Platform Invoke (Marshallen von Daten mit Plattformaufruf)](../../../docs/framework/interop/marshaling-data-with-platform-invoke.md).  
  
## <a name="see-also"></a>Siehe auch
- [Verwenden nicht verwalteter DLL-Funktionen](../../../docs/framework/interop/consuming-unmanaged-dll-functions.md)
- [Angeben eines Einstiegspunktes](../../../docs/framework/interop/specifying-an-entry-point.md)
- [Erstellen einer Klasse zum Halten von DLL-Funktionen](../../../docs/framework/interop/creating-a-class-to-hold-dll-functions.md)
- [Creating Prototypes in Managed Code (Erstellen von Prototypen in verwaltetem Code)](../../../docs/framework/interop/creating-prototypes-in-managed-code.md)
- [Calling a DLL Function (Aufrufen einer DLL-Funktion)](../../../docs/framework/interop/calling-a-dll-function.md)
