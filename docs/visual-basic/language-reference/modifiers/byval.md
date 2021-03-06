---
title: ByVal (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.ByVal
- ByVal
helpviewer_keywords:
- ByVal keyword [Visual Basic], contexts
- ByVal keyword [Visual Basic]
ms.assetid: 1eaf4e58-b305-4785-9e3d-e416b9c75598
ms.openlocfilehash: 6fa87db4fbab961dd1aa526e2ac8ff15b031005b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54650079"
---
# <a name="byval-visual-basic"></a>ByVal (Visual Basic)
Gibt an, dass ein Argument so übergeben wird, dass die aufgerufene Prozedur oder Eigenschaft den Wert einer Variablen mit dem zugrunde liegenden Arguments im aufrufenden Code nicht ändern kann.  
  
## <a name="remarks"></a>Hinweise  
 Der `ByVal`-Modifizierer kann in folgenden Kontexten verwendet werden:  
  
 [Declare-Anweisung](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [Function-Anweisung](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Operator-Anweisung](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
 [Property-Anweisung](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Sub-Anweisung](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt die Verwendung der `ByVal` Mechanismus, mit einem Verweis Typargument übergeben von Parametern. Im Beispiel ist das Argument ist `c1`, eine Instanz der Klasse `Class1`. `ByVal` verhindert, dass den Code in den Verfahren ändern den zugrunde liegenden Wert des Arguments Verweis `c1`, aber nicht die verfügbare Felder und Eigenschaften der schützt `c1`.  
  
 [!code-vb[VbVbalrKeywords#10](../../../visual-basic/language-reference/codesnippet/VisualBasic/byval_1.vb)]  
  
## <a name="see-also"></a>Siehe auch
- [Schlüsselwörter](../../../visual-basic/language-reference/keywords/index.md)
- [Übergeben von Argumenten als Wert und als Verweis](../../../visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
