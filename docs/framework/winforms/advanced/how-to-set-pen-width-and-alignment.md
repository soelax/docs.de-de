---
title: 'Vorgehensweise: Festlegen von Stiftbreite und-Ausrichtung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- pens [Windows Forms], setting width
- pens [Windows Forms], setting alignment
ms.assetid: a202af36-4d31-4401-a126-b232f51db581
ms.openlocfilehash: d1a465fb7c1cd6d4064a077e592daefebf590714
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564824"
---
# <a name="how-to-set-pen-width-and-alignment"></a>Vorgehensweise: Festlegen von Stiftbreite und-Ausrichtung
Bei der Erstellung einer <xref:System.Drawing.Pen>, Sie können die Stiftbreite als eines der Argumente an den Konstruktor bereitstellen. Sie können auch die Stiftbreite mit Ändern der <xref:System.Drawing.Pen.Width%2A> Eigenschaft der <xref:System.Drawing.Pen> Klasse.  
  
 Eine theoretische Linie hat es sich um eine Breite von 0. Wenn Sie eine Linie, die 1-Pixel breit ist zeichnen, werden die Pixel auf der theoretischen Linie zentriert. Wenn Sie eine Linie, die mehr als einem Pixel Breite ist zeichnen, wird die Pixel werden entweder auf der theoretischen Linie zentriert oder werden auf einer Seite von der theoretischen Linie. Sie können festlegen, die Stiftausrichtungseigenschaft, der eine <xref:System.Drawing.Pen> um zu bestimmen, wie die mit diesem Stift gezeichneten Pixel relativ zur theoretischen Linien positioniert werden.  
  
 Die Werte <xref:System.Drawing.Drawing2D.PenAlignment.Center>, <xref:System.Drawing.Drawing2D.PenAlignment.Outset>, und <xref:System.Drawing.Drawing2D.PenAlignment.Inset> , angezeigt werden, in der folgenden Codebeispiele sind Mitglieder der <xref:System.Drawing.Drawing2D.PenAlignment> Enumeration.  
  
 Im folgenden Codebeispiel wird zeichnet eine Linie zweimal: einmal mit einem schwarzen Stift der Breite 1 und einmal mit einem grünen Stift der Breite 10.  
  
### <a name="to-vary-the-width-of-a-pen"></a>Um die Breite des Stifts zu variieren.  
  
-   Legen Sie den Wert, der die <xref:System.Drawing.Pen.Alignment%2A> Eigenschaft <xref:System.Drawing.Drawing2D.PenAlignment.Center> (Standard), um anzugeben, dass mit dem grünen Stift gezeichneten Pixel auf der theoretischen Linie zentriert werden soll. Die folgende Abbildung zeigt die resultierende Linie.  
  
     ![Stifte](../../../../docs/framework/winforms/advanced/media/pens1a.gif "pens1A")  
  
     Im folgenden Codebeispiel wird zeichnet ein Rechteck zweimal: einmal mit einem schwarzen Stift der Breite 1 und einmal mit einem grünen Stift der Breite 10.  
  
     [!code-csharp[System.Drawing.UsingAPen#41](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#41)]
     [!code-vb[System.Drawing.UsingAPen#41](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#41)]  
  
### <a name="to-change-the-alignment-of-a-pen"></a>So ändern Sie die Ausrichtung eines Stifts  
  
-   Legen Sie den Wert von der <xref:System.Drawing.Pen.Alignment%2A> Eigenschaft <xref:System.Drawing.Drawing2D.PenAlignment.Center> um anzugeben, dass die mit dem grünen Stift gezeichneten Pixel soll, auf die Begrenzung des Rechtecks zentriert werden.  
  
     Die folgende Abbildung zeigt das sich ergebende Rechteck.  
  
     ![Stifte](../../../../docs/framework/winforms/advanced/media/pens2.gif "pens2")  
  
     [!code-csharp[System.Drawing.UsingAPen#42](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#42)]
     [!code-vb[System.Drawing.UsingAPen#42](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#42)]  
  
### <a name="to-create-an-inset-pen"></a>Ein abgesenkter Stift erstellen  
  
-   Ändern Sie den grünen Stift-Ausrichtung, indem Sie im obigen Codebeispiel wird die dritte Anweisung wie folgt ändern:  
  
     [!code-csharp[System.Drawing.UsingAPen#43](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#43)]
     [!code-vb[System.Drawing.UsingAPen#43](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#43)]  
  
     Jetzt werden die Pixel in der breiten grünen Linie innerhalb des Rechtecks angezeigt, wie in der folgenden Abbildung dargestellt.  
  
     ![Stifte](../../../../docs/framework/winforms/advanced/media/pens3.gif "pens3")  
  
## <a name="see-also"></a>Siehe auch
- [Verwenden eines Stifts zum Zeichnen von Linien und Formen](../../../../docs/framework/winforms/advanced/using-a-pen-to-draw-lines-and-shapes.md)
- [Grafik und Zeichnen in Windows Forms](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)
