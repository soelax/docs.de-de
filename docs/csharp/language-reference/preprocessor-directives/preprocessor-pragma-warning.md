---
title: '#pragma warning – C#-Referenz'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#pragma warning'
helpviewer_keywords:
- '#pragma warning [C#]'
ms.assetid: 723493d5-9753-4cec-babb-54e2b8eb36b6
ms.openlocfilehash: 7c664ee7d6e0e083eba958e6ee36a63009e13956
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54606607"
---
# <a name="pragma-warning-c-reference"></a>#pragma warning (C#-Referenz)
`#pragma warning` kann bestimmte Warnungen aktivieren oder deaktivieren.  
  
## <a name="syntax"></a>Syntax  
  
```csharp
#pragma warning disable warning-list  
#pragma warning restore warning-list  
```  
  
#### <a name="parameters"></a>Parameter  
 `warning-list`  
 Eine durch Trennzeichen getrennte Liste mit Warnzahlen. Das Präfix „CS“ ist optional.  
  
 Wenn keine Warnzahlen angegeben werden, deaktiviert `disable` alle Warnungen und `restore` aktiviert sie.  
  
> [!NOTE]
>  Um Warnzahlen in Visual Studio zu suchen, erstellen Sie Ihr Projekt und suchen Sie nach den Warnzahlen im Fenster **Ausgabe**.  
  
## <a name="example"></a>Beispiel  
  
```csharp
// pragma_warning.cs  
using System;  
  
#pragma warning disable 414, CS3021  
[CLSCompliant(false)]  
public class C  
{  
    int i = 1;  
    static void Main()  
    {  
    }  
}  
#pragma warning restore CS3021  
[CLSCompliant(false)]  // CS3021  
public class D  
{  
    int i = 1;  
    public static void F()  
    {  
    }  
}  
```  
  
## <a name="see-also"></a>Siehe auch

- [C#-Referenz](../../../csharp/language-reference/index.md)
- [C#-Programmierhandbuch](../../../csharp/programming-guide/index.md)
- [C#-Präprozessoranweisungen](../../../csharp/language-reference/preprocessor-directives/index.md)
- [C#-Compilerfehler](../../../csharp/language-reference/compiler-messages/index.md)
