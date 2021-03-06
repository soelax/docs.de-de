---
title: Logische und bitweise Operatoren in Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- short-circuiting
- Boolean expressions
- logical operators [Visual Basic], Boolean expressions
- operators [Visual Basic], logical
- AndAlso operator [Visual Basic]
- Not operator [Visual Basic], Boolean expressions
- Xor operator [Visual Basic], Boolean expressions
- And operator [Visual Basic], logical operators
- logical operators [Visual Basic]
- expressions [Visual Basic], Boolean
- Or operator [Visual Basic], logical operators
- Visual Basic code, operators
- short-circuiting [Visual Basic], logical operators
- logical operators [Visual Basic], short-circuiting
- Visual Basic code, expressions
- logical operators [Visual Basic], binary
- OrElse operator [Visual Basic]
- logical operators [Visual Basic], unary
ms.assetid: ca474e13-567d-4b1d-a18b-301433705e57
ms.openlocfilehash: 6dd71a01aeb56a6805689b6e898ab9c2c404959b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54640757"
---
# <a name="logical-and-bitwise-operators-in-visual-basic"></a>Logische und bitweise Operatoren in Visual Basic
Logische Operatoren vergleichen `Boolean` Ausdrücke und Rückgabe einer `Boolean` Ergebnis. Die `And`, `Or`, `AndAlso`, `OrElse`, und `Xor` Operatoren sind *binäre* , da sie zwei Operanden in Anspruch nehmen, während er sich die `Not` Operator *unäre* , da die kann eines einzelnen Operanden aus. Einige dieser Operatoren können auch die bitweise logische Operationen für ganzzahlige Werte ausführen.  
  
## <a name="unary-logical-operator"></a>Unärer logischer Operator  
 Die [Not-Operator](../../../../visual-basic/language-reference/operators/not-operator.md) führt logische *Negation* auf eine `Boolean` Ausdruck. Er stellt das logische Gegenteil des Operanden. Wenn der Ausdruck ergibt `True`, klicken Sie dann `Not` gibt `False`; Wenn der Ausdruck ergibt `False`, klicken Sie dann `Not` gibt `True`. Dies wird anhand des folgenden Beispiels veranschaulicht.  
  
 [!code-vb[VbVbalrOperators#77](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/logical-and-bitwise-operators_1.vb)]  
  
## <a name="binary-logical-operators"></a>Binären logischen Operatoren  
 Die [und Operator](../../../../visual-basic/language-reference/operators/and-operator.md) führt logische *zusammen* für zwei `Boolean` Ausdrücke. Wenn beide Ausdrücke `True`, klicken Sie dann `And` gibt `True`. Wenn mindestens einer der Ausdrücke ergibt `False`, klicken Sie dann `And` gibt `False`.  
  
 Die [oder-Operator](../../../../visual-basic/language-reference/operators/or-operator.md) führt logische *Disjunktion* oder *Aufnahme* für zwei `Boolean` Ausdrücke. Wenn die beiden Ausdrücke ist `True`, oder beide auswerten `True`, klicken Sie dann `Or` gibt `True`. Wenn kein Ausdruck ergibt `True`, `Or` gibt `False`.  
  
 Die [Xor-Operator](../../../../visual-basic/language-reference/operators/xor-operator.md) führt logische *Ausschluss* für zwei `Boolean` Ausdrücke. Wenn genau ein Ausdruck ergibt `True`, aber nicht beide `Xor` gibt `True`. Wenn beide Ausdrücke `True` oder beide auswerten `False`, `Xor` gibt `False`.  
  
 Das folgende Beispiel veranschaulicht die `And`, `Or`, und `Xor` Operatoren.  
  
 [!code-vb[VbVbalrOperators#78](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/logical-and-bitwise-operators_2.vb)]  
  
## <a name="short-circuiting-logical-operations"></a>Kurzschließen von logischen Operationen  
 Die [AndAlso-Operator](../../../../visual-basic/language-reference/operators/andalso-operator.md) ähnelt sehr der `And` -Operator, da er führt auch logischen Konjunktion für zwei `Boolean` Ausdrücke. Der Hauptunterschied zwischen den beiden ist, `AndAlso` weist *kurzschließen* Verhalten. Wenn der erste Ausdruck in einer `AndAlso` Ausdruck wird zu `False`, und klicken Sie dann der zweite Ausdruck nicht ausgewertet, weil es das endgültige Ergebnis, alter kann nicht und `AndAlso` gibt `False`.  
  
 Auf ähnliche Weise die [OrElse-Operator](../../../../visual-basic/language-reference/operators/orelse-operator.md) führt eine verkürzte logischen Disjunktion für zwei `Boolean` Ausdrücke. Wenn der erste Ausdruck in einer `OrElse` Ausdruck wird zu `True`, und klicken Sie dann der zweite Ausdruck nicht ausgewertet, weil es das endgültige Ergebnis, alter kann nicht und `OrElse` gibt `True`.  
  
### <a name="short-circuiting-trade-offs"></a>Verkürzte vor-und Nachteile  
 Verkürzte kann die Leistung erhöht nicht die Auswertung eines Ausdrucks, das das Ergebnis der logischen Operation nicht ändern kann. Allerdings, wenn dieser Ausdruck zusätzliche Aktionen ausführt, überspringt das kurzschließen dieser Aktionen. Wenn der Ausdruck einen Aufruf von enthält z. B. eine `Function` Prozedur, die, dass die Prozedur nicht aufgerufen wird, wenn des Ausdrucks kurzgeschlossen, und keinen zusätzlicher Code innerhalb der `Function` wird nicht ausgeführt. Aus diesem Grund wird die Funktion kann nur gelegentlich ausgeführt werden und möglicherweise nicht ordnungsgemäß getestet werden. Die Logik des Programm kann der Code in abhängig sind oder die `Function`.  
  
 Das folgende Beispiel veranschaulicht den Unterschied zwischen `And`, `Or`, und ihren entsprechenden Kurzschlussoperatoren.  
  
 [!code-vb[VbVbalrOperators#81](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/logical-and-bitwise-operators_3.vb)]  
  
 [!code-vb[VbVbalrOperators#80](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/logical-and-bitwise-operators_4.vb)]  
  
 [!code-vb[VbVbalrOperators#79](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/logical-and-bitwise-operators_5.vb)]  
  
 Im vorherigen Beispiel beachten Sie, dass wichtiger Code in `checkIfValid()` wird nicht ausgeführt werden, wenn der Aufruf kurzgeschlossen wird. Die erste `If` Anweisung ruft `checkIfValid()` , obwohl `12 > 45` gibt `False`, da `And` keinen Kurzschluss ausführt. Die zweite `If` Anweisung ruft nicht `checkIfValid()`, da beim `12 > 45` gibt `False`, `AndAlso` wird verkürzt den zweiten Ausdruck. Die dritte `If` Anweisung ruft `checkIfValid()` , obwohl `12 < 45` gibt `True`, da `Or` keinen Kurzschluss ausführt. Der vierte `If` Anweisung ruft nicht `checkIfValid()`, da beim `12 < 45` gibt `True`, `OrElse` wird verkürzt den zweiten Ausdruck.  
  
## <a name="bitwise-operations"></a>Bitweise Operationen  
 Bitweise Operationen ausgewertet werden zwei ganzzahlige Werte im binären (Basis 2)-Format. Sie vergleichen die Bits an den entsprechenden Positionen und weisen Sie dann Werte, die auf Basis des Vergleichs. Das folgende Beispiel veranschaulicht die `And` Operator.  
  
 [!code-vb[VbVbalrConcepts#2](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/codesnippet/VisualBasic/logical-and-bitwise-operators_6.vb)]  
  
 Im vorherigen Beispiel wird den Wert des `x` auf 1. In diesem Fall den folgenden Gründen:  
  
-   Die Werte werden als Binärdatei behandelt:  
  
     3 in binärer Form 011 =  
  
     5 in binärer Form = 101  
  
-   Die `And` Operator vergleicht die binären Darstellungen, die eine binäre Position (Bit) zu einem Zeitpunkt. Wenn beide Bits an einer bestimmten Position 1 sind, wird dann an dieser Position im Resultset 1 platziert. Wenn jedes Bit 0 ist, wird eine 0 in dieser Position im Resultset platziert. Im vorherigen Beispiel funktioniert dies wie folgt:  
  
     011 (3 in binärer Form)  
  
     101 (5 in binärer Form)  
  
     001 (Ergebnis in binärer Form)  
  
-   Das Ergebnis wird als Dezimalzahl behandelt. Der Wert 001 ist die binäre Darstellung von 1, also `x` = 1.  
  
 Der bitweise `Or` Vorgang ist ähnlich, außer dass das Ergebnisbit 1 zugewiesen wird, wenn eine oder beide der verglichenen Bits ist 1. `Xor` weist 1, der dem Ergebnisbit, wenn genau eines der Bits im Vergleich (nicht beide) 1 ist. `Not` akzeptiert einen einzelnen Operanden aus und kehrt alle Bits, einschließlich des Vorzeichenbits und weist diesen Wert auf das Ergebnis. Dies bedeutet, dass für positive Zahlen mit Vorzeichen `Not` gibt immer einen negativen Wert zurück, und für negative Zahlen `Not` gibt immer eine positive Zahl oder 0 (null) zurück.  
  
 Die `AndAlso` und `OrElse` Operatoren bitweise Operationen nicht unterstützt.  
  
> [!NOTE]
>  Bitweise Operationen können nur für ganzzahlige Typen ausgeführt werden. Gleitkommazahlen-Punktwerte müssen in ganzzahlige Typen konvertiert werden, bevor bitweise Operation fortgesetzt werden kann.  
  
## <a name="see-also"></a>Siehe auch
- [Logische/bitweise Operatoren (Visual Basic)](../../../../visual-basic/language-reference/operators/logical-bitwise-operators.md)
- [Boolesche Ausdrücke](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/boolean-expressions.md)
- [Arithmetische Operatoren in Visual Basic](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
- [Vergleichsoperatoren in Visual Basic](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)
- [Verkettungsoperatoren in Visual Basic](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/concatenation-operators.md)
- [Effiziente Kombination von Operatoren](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/efficient-combination-of-operators.md)
