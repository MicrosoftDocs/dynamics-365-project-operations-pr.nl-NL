---
title: Projectresources voorstellen
description: Dit onderwerp bevat informatie over het voorstellen van projectresources.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 18d7dcd95806841c952ea621ec65b513ef614958
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074783"
---
# <a name="propose-project-resources"></a>Projectresources voorstellen

Resourcemanagers kunnen een resource voorstellen aan de projectmanager door middel van een resourceaanvraag.

1. Selecteer in het aanvraagraster of in de aanvraag zelf **Resources zoeken**.
2. Selecteer op de pagina **Planningsassistent** de resource en selecteer vervolgens in het deelvenster **Resourceboeking maken** in het veld **Boekingsstatus** de optie **Boeken**.

    ![Voorgestelde resource geselecteerd](media/Resource-Management-image62.png)

De volgende statusupdates worden uitgevoerd:

- Op de pagina **Planningsassistent** worden de statusindicatoren bijgewerkt om aan te geven dat de boeking wordt voorgesteld en niet hard geboekt is.

    ![Statusindicatoren voor voorgestelde boeking op de pagina Planningsassistent](media/Resource-Management-image63.png)

- Op de resourceaanvraag wordt de status gewijzigd in **Moet worden geëvalueerd**.

    ![Status van resourceaanvraag wordt gewijzigd in Moet worden geëvalueerd](media/Resource-Management-image64.png)

- Op het tabblad **Team** van het project wordt de **Aanvraagstatus** van het algemene teamlid gewijzigd in **Moet worden geëvalueerd**.

    ![Aanvraagstatus van algemeen teamlid op het tabblad Team gewijzigd in Moet worden geëvalueerd](media/Resource-Management-image48.png)

De projectmanager kan het voorstel accepteren of afwijzen.

Wanneer resourcemanagers resourceaanvragen verwerken, kunnen ze een van de volgende benaderingen gebruiken:

- Stel meerdere resources voor om aan de vraag te voldoen, als er niet een enkele resource beschikbaar is om de vereiste uren te vervullen. Voorgestelde uren worden vervolgens verdeeld over meerdere resources, die kunnen voldoen aan de vereiste uren. In dit scenario kunnen de uren niet overlappen.
- Stel minder resources voor dan nodig is. In dit scenario is de voorgestelde resourcecapaciteit minder dan de vereiste uren die de aanvrager heeft opgegeven. Wanneer de aanvrager de voorgestelde resources accepteert, wordt er daarom een niet-vervulde resourcevereiste gemaakt om de overblijvende vraag vast te leggen.
- Boek meerdere resources om aan de vraag te voldoen, als er niet één enkele resource beschikbaar is om het werk te voltooien.
- Boek minder resources dan vereist. In dit scenario zijn de geboekte uren minder dan de vereiste uren. Het systeem begeleidt u bij het voorstellen van resources in plaats van boekingen, zodat de aanvrager de resterende vraag kan controleren en volgen.

## <a name="billable-utilization"></a>Factureerbare uren

Resources kunnen een doelwaarde voor factureerbare bestede uren hebben. Dit doel voor bestede uren is gedefinieerd als een kenmerk voor de standaardrol van een resource, of is ingesteld in de record van de individuele boekbare resource. Berekeningen van bestede uren zijn gebaseerd op de werkelijke uren die resources hebben gerapporteerd door middel van goedgekeurde tijdsvermeldingen.

De volgende formules worden gebruikt om het gebruik te berekenen:

- Factureerbare uren = Factureerbare werkelijke uren ÷ Resourcecapaciteit
- Niet-factureerbare uren = Werkelijke tijd met factureringstype-ID = Niet-factureerbaar, Complementair of Niet beschikbaar ÷ Resourcecapaciteit
- Intern = Werkelijke tijd zonder verkoopcontract ÷ Resourcecapaciteit
- Resourcecapaciteit = Werkuren van resource – Afwezig – Niet-werkdagen

De weergave **Bestede uren van resource** vindt u in het deelvenster **Resources**.

![Weergave Bestede uren van resource](media/Resource-Management-image65.png)

Elke cel in het raster vertegenwoordigt het het percentage factureerbare uren van de resource in een periode, zoals een dag, week of maand. De volgende formules worden gebruikt voor de kleur van de cellen:

- **Groen:** Factureerbare bestede uren \>= doel voor Bestede uren van resource
- **Geel:** Doel voor bestede uren - 20 \<= Factureerbare bestede uren \< doel voor Bestede uren
- **Rood:** Factureerbare bestede uren \< doel voor bestede uren – 20

Omdat de weergave **Bestede uren van resource** is gebaseerd op het planbord, kunt u met de filtermogelijkheden van het planbord uw resultaten filteren.

Het raster vereist dat u een doelwaarde voor bestede uren instelt voor de rol of voor de individuele resource. Dit kunt u doen in **Resources** \> **Resourcerollen**.

Daarnaast moet een standaardrol worden toegewezen aan elke boekbare resource. Ga naar **Resources** \> **Resources**. Controleer op het tabblad **Project Service** of een resourerol is gedefinieerd en of het veld **Is standaard** is ingesteld op **Ja**. U kunt extra rollen toevoegen waar **Is standaard = Nee**. De rol waar **Is standaard = Ja** , wordt gebruikt voor het evalueren van de bestede uren van de resource ten opzichte van het doel voor die rol.

![Standaardrol ingesteld](media/Resource-Management-image67.png)

Op het tabblad **Project Service** kunt u ook een afzonderlijk doel voor bestede uren voor de resource instellen. De berekening van de bestede uren gebruikt vervolgens die doelwaarde om te het doel van de resource te evalueren, in plaats van het doel van de standaardrol van de resource.

De bestede uren worden alleen voor een resource weergegeven als die resource goedgekeurde, factureerbare tijd heeft in de periode die wordt weergegeven in het raster.

## <a name="resource-availability"></a>Resourcebeschikbaarheid

Het is essentieel dat resourcemanagers de beschikbaarheid van resources kunnen bekijken en boekingen kunnen bijwerken. In sommige gevallen is er geen formele vraag (resourceaanvraag), maar moet een resourcemanager reageren op een niet-geplande vraag die binnenkomt via kanalen zoals een e-mail, telefoongesprek of chat. Resourcemanagers gebruiken het planbord om resources en boekingen bij te werken.

Werkuren van een resource worden gebruikt als basis voor het berekenen van de beschikbaarheid van een resource. Resourceboekingen verbruiken de capaciteit van de resources.

![Planbord](media/Resource-Management-image68.png)

Het planbord gebruikt kleuren en arcering om boekingen, beschikbaarheid en overboekingen weer te geven, en ook de status van boekingen. Met een instelling in de instellingen van het planbord kunt u een legenda laten weergeven.

Als er naast een individuele boekbare resource op het planbord een pijl naar rechts wordt weergegeven, kan de resource worden uitgevouwen om details weer te geven van het werk waarvoor de resource is geboekt.

![Boekbare resource uitgevouwen op het planbord](media/Resource-Management-image69.png)

Omdat Dynamics 365 Project Service Automation de Universal Resource Scheduling-engine gebruikt kunt u, als ook Dynamics 365 Field Service is geïnstalleerd, de details van resourceboekingen weergeven voor projecten, werkorders en andere entiteiten waarnaar u de planning hebt uitgebreid.

![Details van resourceboekingen voor projecten en werkorders](media/Resource-Management-image70.png)

Als u meer details voor een individuele resource wilt weergeven, klikt u er met de rechtermuisknop op om de resourcekaart te openen.

![Resourcekaart](media/Resource-Management-image71.png)