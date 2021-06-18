---
title: Voorgestelde resources beoordelen
description: Dit onderwerp bevat informatie over hoe u projectresources kunt voorstellen.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000745"
---
# <a name="review-proposed-resources"></a>Voorgestelde resources beoordelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Resourcemanagers kunnen een resource voorstellen aan de projectmanager door middel van een resourceaanvraag.

1. Selecteer in het aanvraagraster of in de aanvraag zelf **Resources zoeken**.
2. Selecteer op de pagina **Planningsassistent** de resource en selecteer vervolgens in het deelvenster **Resourceboeking maken** in het veld **Boekingsstatus** de optie **Boeken**.

De volgende statusupdates worden uitgevoerd:

- Op de pagina **Planningsassistent** worden de statusindicatoren bijgewerkt om aan te geven dat de boeking wordt voorgesteld en niet hard geboekt is.
- Op de resourceaanvraag wordt de status gewijzigd in **Moet worden geëvalueerd**.
- Op het tabblad **Team** van het project wordt de **Aanvraagstatus** van het algemene teamlid gewijzigd in **Moet worden geëvalueerd**.

De projectmanager kan het voorstel accepteren of afwijzen.

Wanneer resourcemanagers resourceaanvragen verwerken, kunnen ze een van de volgende benaderingen gebruiken:

- Stel meerdere resources voor om aan de vraag te voldoen, als er niet een enkele resource beschikbaar is om de vereiste uren te vervullen. Voorgestelde uren worden vervolgens verdeeld over meerdere resources, die kunnen voldoen aan de vereiste uren. In dit scenario kunnen de uren niet overlappen.
- Stel minder resources voor dan nodig is. In dit scenario is de voorgestelde resourcecapaciteit minder dan de vereiste uren die de aanvrager heeft opgegeven. Wanneer de aanvrager de voorgestelde resources accepteert, wordt er daarom een niet-vervulde resourcevereiste gemaakt om de overblijvende vraag vast te leggen.
- Boek meerdere resources om aan de vraag te voldoen, als er niet één enkele resource beschikbaar is om het werk te voltooien.
- Boek minder resources dan vereist. In dit scenario zijn de geboekte uren minder dan de vereiste uren. Het systeem begeleidt u bij het voorstellen van resources in plaats van boekingen, zodat de aanvrager de resterende vraag kan controleren en volgen.

## <a name="resource-availability"></a>Resourcebeschikbaarheid

Het is essentieel dat resourcemanagers de beschikbaarheid van resources kunnen bekijken en boekingen kunnen bijwerken. In sommige gevallen is er geen formele vraag (resourceaanvraag), maar moet een resourcemanager reageren op een niet-geplande vraag die binnenkomt via kanalen zoals een e-mail, telefoongesprek of chat. Resourcemanagers gebruiken het planbord om resources en boekingen bij te werken.

Werkuren van een resource worden gebruikt als basis voor het berekenen van de beschikbaarheid van een resource. Resourceboekingen verbruiken de capaciteit van de resources.

Het planbord gebruikt kleuren en arcering om boekingen, beschikbaarheid en overboekingen weer te geven, en ook de status van boekingen. Met een instelling in de instellingen van het planbord kunt u een legenda laten weergeven.

Als er naast een individuele boekbare resource op het planbord een pijl naar rechts wordt weergegeven, kan de resource worden uitgevouwen om details weer te geven van het werk waarvoor de resource is geboekt.

Omdat Dynamics 365 Project Operations de Universal Resource Scheduling-engine gebruikt kunt u, als ook Dynamics 365 Field Service is geïnstalleerd, de details van resourceboekingen weergeven voor projecten, werkorders en andere entiteiten waarnaar u de planning hebt uitgebreid.

Als u meer details voor een individuele resource wilt weergeven, klikt u er met de rechtermuisknop op om de resourcekaart te openen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]