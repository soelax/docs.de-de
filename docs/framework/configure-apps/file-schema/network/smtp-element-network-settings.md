---
title: <smtp>-Element (Netzwerkeinstellungen)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/mailSettings/smtp
- http://schemas.microsoft.com/.NetConfiguration/v2.0#smtp
helpviewer_keywords:
- <smtp> element
- smtp element
ms.assetid: 220b0329-e384-4e0c-86b4-0945ad17efd9
ms.openlocfilehash: ecd780da7224389685b61c39c796c7a80587709c
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2019
ms.locfileid: "55273581"
---
# <a name="smtp-element-network-settings"></a>\<SMTP >-Element (Netzwerkeinstellungen)
Konfiguriert das übermittlungsformat, die Übermittlungsmethode und die Absenderadresse zum Senden von e-Mails.  
  
 \<configuration>  
\<system.net>  
\<mailSettings>  
\<smtp>  
  
## <a name="syntax"></a>Syntax  
  
```xml  
<smtp  
  deliveryFormat="format"  
  deliveryMethod="method"  
  from="from address">
    <specifiedPickupDirectory>...</specifiedPickupDirectory>  
    <network>...</network>  
</smtp>  
```  
  
## <a name="attributes-and-elements"></a>Attribute und Elemente  
 In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.  
  
### <a name="attributes"></a>Attribute  
  
|Attribut|Beschreibung|  
|---------------|-----------------|  
|`deliveryFormat`|Gibt das übermittlungsformat für ausgehende e-Mails an. Zulässige Werte sind "SevenBit" und "International".|  
|`deliveryMethod`|Gibt die Übermittlungsmethode für e-Mails an. Zulässige Werte sind, Netzwerk, PickupDirectoryFromIis und "specifiedPickupDirectory".|  
|`from`|Gibt an, die Absenderadresse für ausgehende e-Mails.|  
  
### <a name="child-elements"></a>Untergeordnete Elemente  
  
|Attribut|Beschreibung|  
|---------------|-----------------|  
|`specifiedPickupDirectory`|Konfiguriert das lokale Verzeichnis für einen SMTP (Simple Mail Transport Protocol)-Server.|  
|`network`|Konfiguriert die Netzwerkoptionen für einen externen SMTP-Server.|  
  
### <a name="parent-elements"></a>Übergeordnete Elemente  
  
|**Element**|**Beschreibung**|  
|-----------------|---------------------|  
|[\<mailSettings>-Element (Netzwerkeinstellungen)](../../../../../docs/framework/configure-apps/file-schema/network/mailsettings-element-network-settings.md)|Konfiguriert E-Mail-Sendeoptionen.|  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel gibt die entsprechenden SMTP-Parameter zum Senden von e-Mails, die über die Standardanmeldeinformationen an.  
  
```xml  
<configuration>  
  <system.net>  
    <mailSettings>  
      <smtp deliveryMethod="Network" deliveryFormat="SevenBit"  from="ben@contoso.com">  
        <network  
          host="localhost"  
          port="25"  
          defaultCredentials="true"  
        />  
      </smtp>  
    </mailSettings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Net.Configuration.SmtpSection?displayProperty=nameWithType>
- <xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType>
- <xref:System.Net.Mail.SmtpDeliveryFormat>
- <xref:System.Net.Mail.SmtpDeliveryMethod>
- [Network Settings Schema (Schema für Netzwerkeinstellungen)](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
