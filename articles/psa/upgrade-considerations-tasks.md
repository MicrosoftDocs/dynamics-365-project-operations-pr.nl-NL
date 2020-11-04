---
title: Upgradeoverwegingen voor de structuur voor werkspecificatie
description: Dit onderwerp bevat informatie over het upgraden van de structuur voor werkspecificatie van Project Service Automation 2.x naar 3.x.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 169dc24f0d1ae151ea5927123fb738221de88250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074646"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Upgradeoverwegingen voor de structuur voor werkspecificatie
Dit onderwerp bevat informatie over het upgraden van de structuur voor werkspecificatie van Project Service Automation 2.x naar 3.x. In dit onderwerp wordt de status van een project in Project Service Automation (PSA) bepaald die is vereist voor een geslaagde upgrade. Ook vindt u informatie over de algemene blokkerende voorwaarden die ervoor zorgen dat de upgrade mislukt. Zie [Projectplanningen](project-creating.md) voor meer informatie over het definiëren van projecttaken en hun functies binnen een projectplanning.

## <a name="key-entities"></a>Belangrijke entiteiten
Voor een correcte structuur voor werkspecificatie die al is geladen met resources, zijn de volgende entiteiten vereist:

- [Project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Projecttaak](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Resourcetoewijzingen](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Projecttaakafhankelijkheid](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Boekbare resources](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Als u een structuur voor werkspecificatie wilt definiëren die is geladen voor een resource, moet u de volgende stappen uitvoeren:

1. Maak een nieuw project. Zie [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project) voor meer informatie over het maken van een nieuw project.
2. Maak een of meer taken. Zie [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask) voor meer informatie over het maken van een nieuwe taak.
3. Definieer de taakafhankelijkheden. Meer informatie vindt u in [Afhankelijkheid van projecttaken](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Wijs projectteamleden toe aan het project. Zie [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam) voor meer informatie.
5. Wijs projectteamleden toe aan de taken. Zie [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment) voor meer informatie.

## <a name="project-team-relationships"></a>Relaties van projectteams

Voor een geslaagde upgrade moeten de volgende relaties correct worden onderhouden:
- Alle projectteamleden moeten aan een boekbare resource zijn gekoppeld.
- Alle projectteamleden moeten aan hetzelfde project zijn gekoppeld. 

## <a name="project-task-relationships"></a>Relaties van projecttaken
Voor een geslaagde upgrade moeten de volgende relaties correct worden onderhouden:

- Alle gerelateerde taken moeten aan hetzelfde project zijn gekoppeld.
- Elke regeltaak moet een bovenliggende taak hebben.
- Elke taak moet een bovenliggend project hebben.

### <a name="valid-conditions"></a>Geldige voorwaarden

- De duur van elke taak moet groter zijn dan of gelijk zijn aan (>=) één uur en minder dan 1.800.000 minuten (1.250 dagen).*
- Alle taken moeten een begindatum hebben die niet eerder is dan 01/01/2000.*
- Alle taken moeten een begindatum van uiterlijk 17 jaar na de huidige dag hebben.*
- Alle taken moeten een begindatum hebben die eerder dan of gelijk is aan de einddatum.
- Alle transactietypen op classificaties (onkosten, materiaal, btw en tijd) moeten waarden hebben voor **standaardeenheid** en **eenhedengroep**.
- Datumnotaties met letters moeten worden vermeden.

### <a name="potential-mitigation-steps"></a>Mogelijke correctiestappen
- Gebruik Geavanceerd zoeken om projecttaken te vinden die geen project-id bevatten.
- Gebruik Geavanceerd zoeken om projecttaken te vinden waarvan de geplande duur meer is dan 1.800.000.
- Voordat u gegevens wijzigt, moet u alle aanpassingen onderzoeken die zijn gekoppeld aan de entiteit die ertoe kunnen hebben geleid dat de gegevens in slechte staat zijn geraakt. Deze aanpassingen moeten worden gecorrigeerd voordat u doorgaat met gegevensgerelateerde updates.
- Overweeg voor de geïdentificeerde taken die zwevend zijn geworden om deze te verwijderen als ze niet nodig zijn, of ze aan het juiste ouderproject te koppelen.
- Overweeg voor alle taken waarvan de duur langer is dan 1250 dagen om meerdere taken toe te voegen om de totale duur weer te geven, indien mogelijk.

> [!NOTE]
> Voor items die zijn gemarkeerd met een sterretje (\*) gelden limieten, omdat Customer Relationship Management (CRM) maximaal 7.320 terugkeerpatroonuitbreidingen ondersteunt. U moet onder deze limiet blijven.

## <a name="resource-assignment-relationships"></a>Relaties van resourcetoewijzingen
Voor een geslaagde upgrade moeten de volgende relaties correct worden onderhouden:

- Alle resourcetoewijzingen in een structuur voor werkspecificatie moeten betrekking hebben op hetzelfde project.
- Alle resourcetoewijzingen in een structuur voor werkspecificatie moeten zijn gekoppeld aan projectteamleden in hetzelfde project.

### <a name="potential-mitigation-steps"></a>Mogelijke correctiestappen
- Identificeer alle taken die buiten de hierboven beschreven voorwaarden vallen.  
- Resourcetoewijzingen die niet langer geldig zijn, moeten worden verwijderd.

## <a name="project-task-dependency-relationships"></a>Relaties van afhankelijkheid van projecttaken
Voor een geslaagde upgrade moeten de volgende relaties correct worden onderhouden:

- Alle projecttaakafhankelijkheden moeten zijn gerelateerd aan hetzelfde project.
- Er kan niet meerdere keren worden verwezen naar dezelfde afhankelijkheid in een taak.