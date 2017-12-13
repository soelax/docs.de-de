---
title: "Ausführen, Verwalten und Überwachen von Docker-Produktionsumgebungen"
description: Lebenszyklus von Docker-Containeranwendungen mit der Microsoft-Plattform und Tools
keywords: Docker, Microservices, ASP.NET, Container
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: e377a5ec4b34a1ae25246747cf652a22064b8ffd
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="run-manage-and-monitor-docker-production-environments"></a><span data-ttu-id="d60f7-104">Ausführen, Verwalten und Überwachen von Docker-Produktionsumgebungen</span><span class="sxs-lookup"><span data-stu-id="d60f7-104">Run, manage, and monitor Docker production environments</span></span>

<span data-ttu-id="d60f7-105">Vision: Unternehmensanwendungen müssen hochverfügbar und hochgradig skalierbar sein, und die operative IT muss in der Lage sein, die Umgebungen und Anwendungen selbst zu verwalten und zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="d60f7-105">Vision: Enterprise applications need to run with high availability and high scalability; IT operations need to be able to manage and monitor the environments and the applications themselves.</span></span>

<span data-ttu-id="d60f7-106">Dieser letzte Eckpfeiler im Lebenszyklus der containerisierten Docker-Anwendungen ist darauf ausgerichtet, wie Sie Ihre Anwendungen in skalierbaren, hochverfügbaren Produktionsumgebungen (HA) betreiben, verwalten und überwachen können.</span><span class="sxs-lookup"><span data-stu-id="d60f7-106">This last pillar in the containerized Docker applications life cycle is centered on how you can run, manage, and monitor your applications in scalable, high availability (HA) production environments.</span></span>

<span data-ttu-id="d60f7-107">Wie Sie Ihre containerisierten Anwendungen in der Produktion ausführen (Infrastrukturarchitektur und Plattformtechnologien), besitzt ebenfalls einen großen Bezug zu und basiert vollständig auf den gewählten Architektur- und Entwicklungsplattformen, die wir in Kapitel 1 dieses E-Books untersucht haben.</span><span class="sxs-lookup"><span data-stu-id="d60f7-107">How you run your containerized applications in production (infrastructure architecture and platform technologies) is also very much related and completely founded on the chosen architecture and development platforms that we looked at in the Chapter 1 of this e-book.</span></span> <span data-ttu-id="d60f7-108">In diesem Kapitel werden spezifische Produkte und Technologien von Microsoft und anderen Anbietern untersucht, mit denen Sie hochgradig skalierbare, HA-verteilte Anwendungen effektiv ausführen können, und wie Sie diese aus IT-Perspektive verwalten und überwachen können.</span><span class="sxs-lookup"><span data-stu-id="d60f7-108">This chapter examines specific products and technologies from Microsoft and other vendors that you can use to effectively run highly scalable, HA distributed applications plus how you can manage and monitor them from the IT perspective.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="d60f7-109">[Vorheriger] (../docker-devops-workflow/docker-application-outer-loop-devops-workflow.md) [Nächster] (run-microservices-based-applications-in-production.md)</span><span class="sxs-lookup"><span data-stu-id="d60f7-109">[Previous] (../docker-devops-workflow/docker-application-outer-loop-devops-workflow.md) [Next] (run-microservices-based-applications-in-production.md)</span></span>