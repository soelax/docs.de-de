---
title: 'Vorgehensweise: Zurückgeben eines Werts aus einer Prozedur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], returning from
- procedures [Visual Basic], returning a value
ms.assetid: 4bcc4724-2b4e-4df8-9b4b-16054607f87d
ms.openlocfilehash: 38b0673f5725077eec9253021eec4216e66504a2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54615248"
---
# <a name="how-to-return-a-value-from-a-procedure-visual-basic"></a>Vorgehensweise: Zurückgeben eines Werts aus einer Prozedur (Visual Basic)
Ein `Function` Prozedur gibt einen Wert zurück an den aufrufenden Code entweder durch Ausführen einer `Return` Anweisung oder durch Auftreten einer `Exit Function` oder `End Function` Anweisung.  
  
### <a name="to-return-a-value-using-the-return-statement"></a>Zum Zurückgeben eines Werts, der mithilfe der Return-Anweisung  
  
1.  Einfügen einer `Return` Anweisung, an dem Punkt, in dem die Aufgabe der Prozedur abgeschlossen ist.  
  
2.  Führen Sie die `Return` Schlüsselwort mit einem Ausdruck, der den Wert ergibt, an den aufrufenden Code zurückgegeben werden sollen.  
  
3.  Es können sich mehrere `Return`-Anweisungen in derselben Prozedur befinden.  
  
     Die folgenden `Function` Prozedur berechnet die längste Seite, die Hypotenuse eines rechtwinkligen Dreiecks, und wird an den aufrufenden Code zurückgegeben.  
  
     [!code-vb[VbVbcnProcedures#1](./codesnippet/VisualBasic/how-to-return-a-value-from-a-procedure_1.vb)]  
  
     Das folgende Beispiel zeigt einen typischen Aufruf von `hypotenuse`, das den zurückgegebenen Wert speichert.  
  
     [!code-vb[VbVbcnProcedures#6](./codesnippet/VisualBasic/how-to-return-a-value-from-a-procedure_2.vb)]  
  
### <a name="to-return-a-value-using-exit-function-or-end-function"></a>Zum Zurückgeben eines Werts, der mit der Funktion "Exit" oder eine End-Funktion  
  
1.  In mindestens einer zentralen Stelle in der `Function` Verfahren, weisen Sie einen Wert, der Name der Prozedur.  
  
2.  Beim Ausführen einer `Exit Function` oder `End Function` -Anweisung, Visual Basic gibt den Wert der Name der Prozedur zuletzt zugewiesen wurde.  
  
3.  Es können sich mehrere `Exit Function`-Anweisungen in derselben Prozedur befinden. Außerdem können sich sowohl `Return`- als auch `Exit Function`-Anweisungen in derselben Prozedur befinden.  
  
4.  Sie haben nur eine `End Function` -Anweisung in einem `Function` Verfahren.  
  
     Weitere Informationen und ein Beispiel finden Sie unter "Rückgabewert" in [Function-Anweisung](../../../../visual-basic/language-reference/statements/function-statement.md).  
  
## <a name="see-also"></a>Siehe auch
- [Verfahren](./index.md)
- [Sub-Prozeduren](./sub-procedures.md)
- [Eigenschaftenprozeduren](./property-procedures.md)
- [Operatorprozeduren](./operator-procedures.md)
- [Parameter und Argumente von Prozeduren](./procedure-parameters-and-arguments.md)
- [Function-Anweisung](../../../../visual-basic/language-reference/statements/function-statement.md)
- [Return-Anweisung](../../../../visual-basic/language-reference/statements/return-statement.md)
- [Vorgehensweise: Erstellen Sie eine Prozedur, die einen Wert zurückgibt.](./how-to-create-a-procedure-that-returns-a-value.md)
- [Vorgehensweise: Aufrufen einer Prozedur, die einen Wert zurückgibt.](./how-to-call-a-procedure-that-returns-a-value.md)
