---
title: <remove>-Element für <listeners> für <trace>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/trace/listeners/remove
helpviewer_keywords:
- remove element
- <remove> element
ms.assetid: 9a5cd1b5-be1a-485f-8f0c-2890ad3ef3e0
ms.openlocfilehash: 5a6b94756cb1b451d40229674dd887dd9f84676b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2019
ms.locfileid: "55267065"
---
# <a name="remove-element-for-listeners-for-trace"></a>\<Entfernen Sie >-Element für \<Listener > für \<Ablaufverfolgung >
Entfernt einen Listener aus der **Listener** Auflistung.  
  
 \<configuration>  
\<system.diagnostics>  
\<trace>  
\<listeners>  
\<remove>  
  
## <a name="syntax"></a>Syntax  
  
```xml  
<remove name="listener name" />  
```  
  
## <a name="attributes-and-elements"></a>Attribute und Elemente  
 In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.  
  
### <a name="attributes"></a>Attribute  
  
|Attribut|Beschreibung|  
|---------------|-----------------|  
|**name**|Erforderliches Attribut.<br /><br /> Der Name des Listeners, Aufheben der **Listener** Auflistung.|  
  
### <a name="child-elements"></a>Untergeordnete Elemente  
 Keine  
  
### <a name="parent-elements"></a>Übergeordnete Elemente  
  
|Element|Beschreibung|  
|-------------|-----------------|  
|`configuration`|Das Stammelement in jeder von den Common Language Runtime- und .NET Framework-Anwendungen verwendeten Konfigurationsdatei.|  
|`listeners`|Gibt an, einen Listener, der sammelt, speichert, und leitet Nachrichten. Listener leiten die Ablaufverfolgungsausgabe an ein entsprechendes Ziel.|  
|`system.diagnostics`|Gibt Ablaufverfolgungslistener an, die Meldungen sammeln, speichern und weiterleiten sowie die Ebene, für die ein Ablaufverfolgungsschalter festgelegt ist.|  
|`trace`|Konfiguriert den ASP.NET-Ablaufverfolgungsdienst.|  
  
## <a name="remarks"></a>Hinweise  
  
> [!NOTE]
>  Entfernen der <xref:System.Diagnostics.DefaultTraceListener> aus der `Listeners` Auflistung ändert das Sitzungsverhalten, sodass die <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=nameWithType>, und <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=nameWithType> Methoden. Aufrufen einer `Assert` oder `Fail` -Methode führt normalerweise in der Anzeige eines Meldungsfelds, aber das Feld nicht angezeigt wird der <xref:System.Diagnostics.DefaultTraceListener> befindet sich nicht in der `Listeners` Auflistung.  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt, wie Sie den standardmäßigen Ablaufverfolgungslistener aus der Ablaufverfolgung entfernen **Listener** Auflistung.  
  
```xml  
<configuration>  
   <system.diagnostics>  
      <trace autoflush="true" indentsize="0">  
         <listeners>  
            <remove name="Default" />  
         </listeners>  
      </trace>  
   </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Diagnostics.TraceListener>
- <xref:System.Diagnostics.DefaultTraceListener>
- <xref:System.Diagnostics.TextWriterTraceListener>
- <xref:System.Diagnostics.EventLogTraceListener>
- [Trace and Debug Settings Schema (Schema für Ablaufverfolgungs- und Debugeinstellungen)](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
