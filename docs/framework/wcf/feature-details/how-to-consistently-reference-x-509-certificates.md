---
title: 'Vorgehensweise: Konsistent Verweis x. 509-Zertifikate'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- certificates [WCF], referencing X.509 certificates
ms.assetid: a6de1c63-e450-4640-ad08-ad7302dbfbfc
ms.openlocfilehash: 2468faabfbca57e7d905a592b6743c43cb2ccd56
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54731971"
---
# <a name="how-to-consistently-reference-x509-certificates"></a>Vorgehensweise: Konsistent Verweis x. 509-Zertifikate
Sie haben verschiedene Möglichkeiten, Zertifikate anzugeben: anhand des Hashwerts des Zertifikats, anhand des Ausstellers und der Seriennummer oder anhand der Schlüsselkennung des Antragstellers (Subject Key Identifier, SKI). Die Schlüsselkennung des Antragstellers gibt den öffentlichen Schlüssel des Zertifikatantagstellers eindeutig an. Sie wird häufig für digitale XML-Signaturen verwendet. Der SKI-Wert wird in der Regel Teil des x. 509-Zertifikats als ein *x. 509-zertifikaterweiterung*. Windows Communication Foundation (WCF) hat den Standardwert *verweisstil* , den Aussteller und die Seriennummer verwendet, wenn die SKI-Erweiterung aus dem Zertifikat nicht vorhanden ist. Enthält das Zertifikat die SKI-Erweiterung, verwendet der Standardverweis die Schlüsselkennung des Antragstellers, um auf das Zertifikat zu verweisen. Wenn zwischendurch durch die Entwicklung einer Anwendung, wird Sie von der Verwendung von Zertifikaten, die nicht die SKI-Erweiterung für Zertifikate verwenden, die die SKI-Erweiterung verwenden wechseln, ändert sich auch der verweisstil in generierten WCF Nachrichten verwendet.  
  
 Wenn unabhängig vom Vorhandensein einer SKI-Erweiterung ein einheitlicher Verweisstil erforderlich ist, kann der gewünschte Verweisstil wie im folgenden Code dargestellt konfiguriert werden.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein benutzerdefiniertes Sicherheitsbindungselement erstellt, das einen einzigen einheitlichen Verweisstil, den Namen des Ausstellers und die Seriennummer verwendet.  
  
 [!code-csharp[c_ReferencingCertificatesConsistently#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_referencingcertificatesconsistently/cs/source.cs#1)]
 [!code-vb[c_ReferencingCertificatesConsistently#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_referencingcertificatesconsistently/vb/source.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Die folgenden Namespaces sind zum Kompilieren des Codes erforderlich:  
  
-   <xref:System>  
  
-   <xref:System.ServiceModel>  
  
-   <xref:System.ServiceModel.Channels>  
  
-   <xref:System.ServiceModel.Security.Tokens>  
  
## <a name="see-also"></a>Siehe auch
- [Arbeiten mit Zertifikaten](../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
