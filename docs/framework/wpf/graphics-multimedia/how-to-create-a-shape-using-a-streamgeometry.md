---
title: 'Vorgehensweise: Erstellen eines Shapes mit einer StreamGeometry'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], shapes
- shapes [WPF], creating with StreamGeometry class
ms.assetid: 08f7c8ce-074b-49cd-9aba-cc9592d4ee51
ms.openlocfilehash: 94e7683d22b685c95f9f70612bc0aacef06e23bd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54554204"
---
# <a name="how-to-create-a-shape-using-a-streamgeometry"></a>Vorgehensweise: Erstellen eines Shapes mit einer StreamGeometry
<xref:System.Windows.Media.StreamGeometry> stellt einfache Alternative zu <xref:System.Windows.Media.PathGeometry> zum Erstellen geometrischer Formen. Verwenden einer <xref:System.Windows.Media.StreamGeometry> Wenn Sie eine komplexe Geometrie beschreiben müssen jedoch nicht den Mehraufwand für die Unterstützung von Datenbindung, Animation oder Änderung möchten. Beispielsweise aufgrund ihrer Effizienz der <xref:System.Windows.Media.StreamGeometry> Klasse ist eine gute Wahl zum Beschreiben von Adornern.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird eine Attributsyntax eine dreieckige erstellen <xref:System.Windows.Media.StreamGeometry> in [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)].  
  
 [!code-xaml[GeometriesMiscSnippets_snip#StreamGeometryTriangleExampleWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/GeometriesMiscSnippets_snip/XAML/StreamGeometryExample.xaml#streamgeometrytriangleexamplewholepage)]  
  
 Weitere Informationen zu <xref:System.Windows.Media.StreamGeometry> Attributsyntax, finden Sie unter den [Pfadmarkupsyntax](../../../../docs/framework/wpf/graphics-multimedia/path-markup-syntax.md) Seite.  
  
## <a name="example"></a>Beispiel  
 Im nächsten Beispiel wird eine <xref:System.Windows.Media.StreamGeometry> ein Dreieck im Code definiert. Zunächst das Beispiel erstellt eine <xref:System.Windows.Media.StreamGeometry>, erhält dann eine <xref:System.Windows.Media.StreamGeometryContext> und wird verwendet, um das Dreieck zu beschreiben.  
  
 [!code-csharp[GeometriesMiscSnippets_procedural_snip#StreamGeometryTriangleExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometriesMiscSnippets_procedural_snip/CSharp/StreamGeometryTriangleExample.cs#streamgeometrytriangleexamplewholepage)]
 [!code-vb[GeometriesMiscSnippets_procedural_snip#StreamGeometryTriangleExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/GeometriesMiscSnippets_procedural_snip/visualbasic/streamgeometrytriangleexample.vb#streamgeometrytriangleexamplewholepage)]  
  
## <a name="example"></a>Beispiel  
 Im nächste Beispiel erstellt eine Methode, verwendet eine <xref:System.Windows.Media.StreamGeometry> und <xref:System.Windows.Media.StreamGeometryContext> eine geometrische Form, die basierend auf den angegebenen Parametern definiert.  
  
 [!code-csharp[GeometriesMiscSnippets_procedural_snip#StreamGeometryExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometriesMiscSnippets_procedural_snip/CSharp/StreamGeometryExample.cs#streamgeometryexamplewholepage)]
 [!code-vb[GeometriesMiscSnippets_procedural_snip#StreamGeometryExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/GeometriesMiscSnippets_procedural_snip/visualbasic/streamgeometryexample.vb#streamgeometryexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Windows.Media.PathGeometry>
- <xref:System.Windows.Media.StreamGeometry>
- <xref:System.Windows.Media.StreamGeometryContext>
- [Erstellen einer Form mithilfe von PathGeometry](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-shape-by-using-a-pathgeometry.md)
- [Übersicht über Geometrien](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md)
