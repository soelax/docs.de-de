---
title: In (generischer Modifizierer) (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.VarianceIn
helpviewer_keywords:
- contravariance, In keyword [Visual Basic]
- In keyword [Visual Basic]
ms.assetid: 59bb13c5-fe96-42b8-8286-86293d1661c5
ms.openlocfilehash: 4d5909e6ee7436b7e4f7baa30bfe81eb8ba5441e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54625748"
---
# <a name="in-generic-modifier-visual-basic"></a>In (generischer Modifizierer) (Visual Basic)
Das Schlüsselwort `In` gibt für generische Typparameter an, dass der Typparameter kontravariant ist.  
  
## <a name="remarks"></a>Hinweise  
 Kontravarianz ermöglicht Ihnen die Verwendung eines weniger stark abgeleiteten Typs als der durch den generischen Parameter angegebene. Dadurch wird eine implizite Konvertierung von Klassen berücksichtigt, die variante Schnittstellen und Konvertierung von Delegattypen implementiert.  
  
 Weitere Informationen finden Sie unter [Kovarianz und Kontravarianz](../../programming-guide/concepts/covariance-contravariance/index.md).  
  
## <a name="rules"></a>Regeln  
 Sie können das `In`-Schlüsselwort in generischen Schnittstellen und Delegaten verwenden.  
  
 Ein Typparameter kann als kontravariant in einer generischen Schnittstelle oder Delegaten deklariert werden, wenn er das nicht als Methodenrückgabetyp verwendet und nur als Typ von Methodenargumenten verwendet wird. `ByRef` Parameter nicht möglich, kovariant oder kontravariant.  
  
 Kovarianz und Kontravarianz werden für Verweistypen unterstützt und für Werttypen nicht unterstützt.  
  
 In Visual Basic können Sie Ereignisse in Schnittstellen mit kontravarianten deklarieren, ohne Typ des Delegaten angeben. Darüber hinaus kontravarianten Schnittstellen können keine Klassen, Enumerationen und Strukturen geschachtelte allerdings geschachtelte Schnittstellen.  
  
## <a name="behavior"></a>Verhalten  
 Mit einer Schnittstelle, die einen kontravarianten Typparameter hat, kann ihre Methode mehr abgeleitete Typen, als durch den Typparameter der Schnittstelle angegeben, akzeptieren. Da z.B. in .NET Framework 4 Typ T in der Schnittstelle <xref:System.Collections.Generic.IComparer%601> kontravariant ist, können Sie ein Objekt des `IComparer(Of Person)`-Typs an ein Objekt des `IComparer(Of Employee)`-Typs zuweisen, ohne besondere Konvertierungsmethoden zu verwenden, wenn `Person` von `Employee` erbt.  
  
 Ein kontravarianter Delegat kann einem anderen Delegaten desselben Typs zugewiesen werden, jedoch mit einem weniger stark abgeleiteten generischen Typparameter.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird gezeigt, wie Sie eine kontravariante generische Schnittstelle deklarieren, erweitern und implementieren können. Es wird auch gezeigt, wie Sie die implizite Konvertierung für Klassen verwenden können, die eine diese Schnittstelle implementieren können.  
  
 [!code-vb[vbVarianceKeywords#1](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/in-generic-modifier_1.vb)]  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt, wie Sie einen kontravarianten generischen Delegaten deklarieren, instanziieren und aufrufen. Es zeigt außerdem, wie Sie einen Delegattyp implizit konvertieren können.  
  
 [!code-vb[vbVarianceKeywords#2](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/in-generic-modifier_2.vb)]  
  
## <a name="see-also"></a>Siehe auch
- [Varianz in generischen Schnittstellen](../../programming-guide/concepts/covariance-contravariance/variance-in-generic-interfaces.md)
- [Out](../../../visual-basic/language-reference/modifiers/out-generic-modifier.md)
