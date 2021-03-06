---
title: Key (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.AnonymousKey
helpviewer_keywords:
- anonymous types [Visual Basic], key
- Key [Visual Basic]
- Key keyword [Visual Basic]
ms.assetid: 7697a928-7d14-4430-a72a-c9e96e8d6c11
ms.openlocfilehash: 695f356f44bfd6ea5ad3c0a977ec31ddfbea2b05
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54668222"
---
# <a name="key-visual-basic"></a>Key (Visual Basic)
Die `Key` Schlüsselwort können Sie Verhalten für Eigenschaften anonymer Typen anzugeben. Nur Eigenschaften bestimmen Sie, wie Tests für Gleichheit zwischen Instanzen eines anonymen Typs oder eine Berechnung des Code-Hashwerte Schlüsseleigenschaften teilnehmen. Die Werte der Eigenschaften können nicht geändert werden.  
  
 Eine Eigenschaft eines anonymen Typs wird als Schlüsseleigenschaft gekennzeichnet, indem Sie das Schlüsselwort `Key` vor ihrer Deklaration in der Initialisierungsliste. Im folgenden Beispiel `Airline` und `FlightNo` sind Schlüsseleigenschaften, aber `Gate` nicht.  
  
 [!code-vb[VbVbalrAnonymousTypes#26](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/key_1.vb)]  
  
 Wenn ein neuer anonymer Typ erstellt wird, erbt direkt von <xref:System.Object>. Der Compiler überschreibt drei geerbte Member: <xref:System.Object.Equals%2A>, <xref:System.Object.GetHashCode%2A>, und <xref:System.Object.ToString%2A>. Der überschreibende Code, der für die erzeugt wird <xref:System.Object.Equals%2A> und <xref:System.Object.GetHashCode%2A> basiert auf Eigenschaften. Wenn keine Eigenschaften vorhanden, geben Sie in das sind <xref:System.Object.GetHashCode%2A> und <xref:System.Object.Equals%2A> nicht überschrieben werden.  
  
## <a name="equality"></a>Gleichheit  
 Wenn sie Instanzen des gleichen Typs sind und die Werte der Eigenschaften, die ihren Schlüssel gleich sind, werden die zwei Instanzen eines anonymen Typs gleich sind. In den folgenden Beispielen `flight2` gleich `flight1` aus dem vorherigen Beispiel, da sie Instanzen desselben anonymen sind Typ und sie haben übereinstimmende Werte für ihre Haupteigenschaften. Allerdings `flight3` ist nicht gleich `flight1` da sie einen anderen Wert für eine Schlüsseleigenschaft verfügt `FlightNo`. Instanz `flight4` ist nicht der gleiche Typ wie `flight1` , da sie andere Eigenschaften als Schlüsseleigenschaften festlegen.  
  
 [!code-vb[VbVbalrAnonymousTypes#27](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/key_2.vb)]  
  
 Wenn zwei Instanzen mit nur nicht schlüsselbezogene Eigenschaften Name, Datentyp, Reihenfolge und Wert identisch deklariert werden, sind die beiden Instanzen nicht gleich. Eine Instanz ohne Schlüsseleigenschaften entspricht nur sich selbst zur Verfügung.  
  
 Weitere Informationen zu den Bedingungen, unter dem sind zwei Instanzen eines anonymen Typs Instanzen desselben anonymen Typs, finden Sie unter [anonyme Typen](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md).  
  
## <a name="hash-code-calculation"></a>Hash-Code-Berechnung  
 Wie <xref:System.Object.Equals%2A>, die Hashfunktion, die in definierten <xref:System.Object.GetHashCode%2A> für ein anonymer Typ, auf die wichtigsten Eigenschaften des Typs basiert. Die folgenden Beispiele zeigen die Interaktion zwischen Eigenschaften und Hash Codewerte.  
  
 Instanzen eines anonymen Typs, die die gleichen Werte für alle Schlüsseleigenschaften haben den gleichen Hashcodewert aus, auch wenn nicht schlüsselbezogene Eigenschaften keine übereinstimmenden Werte. Die folgende Anweisung gibt `True`.  
  
 [!code-vb[VbVbalrAnonymousTypes#37](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/key_3.vb)]  
  
 Instanzen eines anonymen Typs, die unterschiedliche für eine oder mehrere wichtige Eigenschaften Werte haben unterschiedliche Hashwerte für Code. Die folgende Anweisung gibt `False`.  
  
 [!code-vb[VbVbalrAnonymousTypes#38](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/key_4.vb)]  
  
 Instanzen von anonymen Typen, die verschiedene Eigenschaften als Eigenschaften festlegen, sind keine Instanzen desselben Typs. Sie weisen die Werte der anderen Hash-Code, selbst, wenn die Namen und Werte aller Eigenschaften identisch sind. Die folgende Anweisung gibt `False`.  
  
 [!code-vb[VbVbalrAnonymousTypes#39](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/key_5.vb)]  
  
## <a name="read-only-values"></a>Schreibgeschützte Werte  
 Die Werte der Eigenschaften können nicht geändert werden. Z. B. in `flight1` in den vorherigen Beispielen die `Airline` und `FlightNo` Felder sind schreibgeschützt, aber `Gate` kann geändert werden.  
  
 [!code-vb[VbVbalrAnonymousTypes#28](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/key_6.vb)]  
  
## <a name="see-also"></a>Siehe auch
- [Definition von anonymen Typen](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-type-definition.md)
- [Vorgehensweise: Ableiten von Eigenschaftennamen und Typen in Deklarationen von anonymen Typen](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-infer-property-names-and-types-in-anonymous-type-declarations.md)
- [Anonyme Typen](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)
