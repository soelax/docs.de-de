---
title: 'Vorgehensweise: Übergeben von Argumenten an eine Prozedur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- arguments [Visual Basic], passing to procedures
- procedures [Visual Basic], arguments
- procedures [Visual Basic], parameters
- procedure arguments
- Visual Basic code, procedures
- procedure parameters
- procedures [Visual Basic], calling
- argument passing [Visual Basic], procedures
ms.assetid: 08723588-3890-4ddc-8249-79e049e0f241
ms.openlocfilehash: 6d9daf47b8d9300e9de8add1423fa1824fc62d5d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54691228"
---
# <a name="how-to-pass-arguments-to-a-procedure-visual-basic"></a>Vorgehensweise: Übergeben von Argumenten an eine Prozedur (Visual Basic)
Wenn Sie eine Prozedur aufrufen, verwenden Sie den Namen der Prozedur mit einer Argumentliste in Klammern angegeben. Sie geben Sie ein Argument für alle erforderlichen Parameter, die die Prozedur definiert, und geben Sie optional die Argumente, die `Optional` Parameter. Wenn Sie keinen angeben einer `Optional` Parameter im Aufruf, müssen Sie ein Komma, um seine Position in der Argumentliste zu markieren, wenn Sie alle nachfolgenden Argumente angeben einschließen.  
  
 Wenn Sie beabsichtigen, ein Argument eines Datentyps unterscheidet, von der entsprechenden Parameter, wie z. B. übergeben werden `Byte` zu `String`, Sie können festlegen, dass den Switch-typüberprüfung ([Option Strict-Anweisung](../../../../visual-basic/language-reference/statements/option-strict-statement.md)) zu `Off`. Wenn `Option Strict` ist `On`, verwenden Sie entweder erweiternde Konvertierungen oder explizite Konvertierungsschlüsselwörter. Weitere Informationen finden Sie unter [Widening and Narrowing Conversions](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md) und [Typkonvertierungsfunktionen](../../../../visual-basic/language-reference/functions/type-conversion-functions.md).  
  
 Weitere Informationen finden Sie unter [Prozedurparameter und Argumente](./procedure-parameters-and-arguments.md).  
  
### <a name="to-pass-one-or-more-arguments-to-a-procedure"></a>Um ein oder mehrere Argumente an eine Prozedur übergeben.  
  
1.  Führen Sie den Namen der Prozedur mit Klammern, in der aufrufenden Anweisung.  
  
2.  Fügen Sie in den Klammern einer Argumentliste aus. Fügen Sie ein Argument für die einzelnen erforderlichen Parameter an, dass die Prozedur definiert, und trennen Sie die Argumente durch Kommas.  
  
3.  Stellen Sie sicher, dass jedes Argument ist, dass ein gültiger Ausdruck, der einen Daten-Typ konvertierbar sein in den Typ der Prozedur ergibt für den entsprechenden Parameter definiert.  
  
4.  Wenn ein Parameter, als definiert ist [Optional](../../../../visual-basic/language-reference/modifiers/optional.md), Sie können in der Argumentliste einfügen oder ihn auslassen. Wenn Sie ihn weglassen, verwendet die Prozedur den für diesen Parameter definierten Standardwert ein.  
  
5.  Wenn Sie weglassen, dass ein Argument für eine `Optional` Parameter ist ein weiterer Parameter nach ihm in der Parameterliste, Sie können den Platz von das ausgelassene Argument markieren, indem ein zusätzliches Komma in der Argumentliste.  
  
     Im folgenden Beispiel wird die Visual Basic <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> Funktion.  
  
     [!code-vb[VbVbcnProcedures#34](./codesnippet/VisualBasic/how-to-pass-arguments-to-a-procedure_1.vb)]  
  
     Im vorherige Beispiel stellt das erforderliche erste-Argument, das wird von die Meldungszeichenfolge, die angezeigt werden. Sie lässt es sich um ein Argument für den optionalen zweiten Parameter, der angibt, die Schaltflächen im Meldungsfeld angezeigt werden. Da der Aufruf einen Wert nicht angegeben wird `MsgBox` verwendet den Standardwert `MsgBoxStyle.OKOnly`, wird angezeigt, die nur eine **OK** Schaltfläche.  
  
     Das zweite Komma in der Argumentliste markiert die Stelle des zweiten Arguments nicht angegeben, und die letzte Zeichenfolge übergeben wird, auf dem dritten optionalen Parameter der `MsgBox`, d.h., dass der Text, der in der Titelleiste angezeigt werden.  
  
## <a name="see-also"></a>Siehe auch

- [Sub-Prozeduren](./sub-procedures.md)
- [Function-Prozeduren](./function-procedures.md)
- [Eigenschaftenprozeduren](./property-procedures.md)
- [Operatorprozeduren](./operator-procedures.md)
- [Vorgehensweise: Definieren eines Parameters für eine Prozedur](./how-to-define-a-parameter-for-a-procedure.md)
- [Übergeben von Argumenten als Wert und als Verweis](./passing-arguments-by-value-and-by-reference.md)
- [Rekursive Prozeduren](./recursive-procedures.md)
- [Prozedurüberladung](./procedure-overloading.md)
- [Objekte und Klassen](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
- [Objektorientierte Programmierung (Visual Basic)](../../concepts/object-oriented-programming.md)
