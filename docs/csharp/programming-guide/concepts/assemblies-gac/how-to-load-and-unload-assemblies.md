---
title: 'Vorgehensweise: Laden und Entladen von Assemblys (C#)'
ms.date: 07/20/2015
ms.assetid: 6a4f490f-3576-471f-9533-003737cad4a3
ms.openlocfilehash: eadab1d0e5ddd22fb5c0e92f45162548c9bfd76c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54509349"
---
# <a name="how-to-load-and-unload-assemblies-c"></a>Vorgehensweise: Laden und Entladen von Assemblys (C#)
Assemblys, auf die das Programm verweist, werden automatisch zur Buildzeit geladen. Es ist jedoch ebenfalls möglich, bestimmte Assemblys zur Laufzeit in die aktuelle Anwendungsdomäne zu laden. Weitere Informationen finden Sie unter [Vorgehensweise: Laden von Assemblys in eine Anwendungsdomäne](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md).  
  
 Es gibt keine Möglichkeit, eine einzelne Assembly zu entladen, ohne alle Anwendungsdomänen zu entladen, die diese Assembly enthalten. Selbst wenn sich die Assembly außerhalb des gültigen Bereichs befindet, bleibt die entsprechende Assemblydatei geladen, bis alle Anwendungsdomänen entladen sind, in denen sie enthalten ist.  
  
 Wenn Sie nur einige Assemblys entladen möchten, können Sie eine neue Anwendungsdomäne erstellen, darin den Code ausführen und diese Anwendungsdomäne dann entladen. Weitere Informationen finden Sie unter [Vorgehensweise: Entladen einer Anwendungsdomäne](../../../../framework/app-domains/how-to-unload-an-application-domain.md).  
  
### <a name="to-load-an-assembly-into-an-application-domain"></a>So laden Sie eine Assembly in eine Anwendungsdomäne  
  
1.  Verwenden Sie eine der Load-Methoden in den <xref:System.AppDomain>-Klassen und in den <xref:System.Reflection>-Klassen. Weitere Informationen finden Sie unter [Vorgehensweise: Laden von Assemblys in eine Anwendungsdomäne](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md).  
  
### <a name="to-unload-an-application-domain"></a>So entladen Sie eine Anwendungsdomäne  
  
1.  Es gibt keine Möglichkeit, eine einzelne Assembly zu entladen, ohne alle Anwendungsdomänen zu entladen, die diese Assembly enthalten. Verwenden Sie die `Unload`-Methode von <xref:System.AppDomain>, um die Anwendungsdomänen zu entladen. Weitere Informationen finden Sie unter [Vorgehensweise: Entladen einer Anwendungsdomäne](../../../../framework/app-domains/how-to-unload-an-application-domain.md).  
  
## <a name="see-also"></a>Siehe auch

- [C#-Programmierhandbuch](../../../../csharp/programming-guide/index.md)
- [Assemblys und der globale Assemblycache (C#)](../../../../csharp/programming-guide/concepts/assemblies-gac/index.md)
- [Vorgehensweise: Laden von Assemblys in eine Anwendungsdomäne](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md)
