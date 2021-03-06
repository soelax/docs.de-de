---
title: 'Vorgehensweise: Lesen von Einstellungen zur Laufzeit mitC#'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], reading
- application settings [Windows Forms], run time
- application settings [Windows Forms], C#
ms.assetid: dbe8bf09-5e1c-49da-9192-154033d7240b
ms.openlocfilehash: d798b40e5e337ea7652c8e82cb7fa860a87528b9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521750"
---
# <a name="how-to-read-settings-at-run-time-with-c"></a>Vorgehensweise: Lesen von Einstellungen zur Laufzeit mitC# #
Über das Properties-Objekt können Sie zur Laufzeit anwendungsspezifische und benutzerspezifische Einstellungen auslesen. Das Properties-Objekt macht über den Properties.Settings.Default-Member alle Standardeinstellungen für des Projekt verfügbar.  
  
### <a name="to-read-settings-at-run-time-with-c"></a>So lesen Sie Einstellungen zur Laufzeit mit C#  
  
-   Greifen Sie über den Properties.Settings.Default-Member auf die geeignete Einstellung zu. Im folgenden Beispiel wird gezeigt, wie Sie einer BackColor-Eigenschaft eine Einstellung mit Namen `myColor` zuweisen. Dies setzt voraus, dass Sie zuvor eine Einstellungsdatei erstellt haben, die eine Einstellung mit Namen `myColor` vom Typ `System.Drawing.Color` enthält. Weitere Informationen zum Erstellen einer Datei, finden Sie unter [so wird's gemacht: Erstellen einer neuen Einstellung zur Entwurfszeit](../../../../docs/framework/winforms/advanced/how-to-create-a-new-setting-at-design-time.md).  
  
    ```  
    // C#  
    this.BackColor = Properties.Settings.Default.myColor;  
    ```  
  
## <a name="see-also"></a>Siehe auch
- [Verwenden von Anwendungseinstellungen und Benutzereinstellungen](../../../../docs/framework/winforms/advanced/using-application-settings-and-user-settings.md)
- [How To: Schreiben von Benutzereinstellungen zur Laufzeit mitC#](../../../../docs/framework/winforms/advanced/how-to-write-user-settings-at-run-time-with-csharp.md)
- [Übersicht über Anwendungseinstellungen](../../../../docs/framework/winforms/advanced/application-settings-overview.md)
