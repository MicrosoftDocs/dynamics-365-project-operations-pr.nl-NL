---
title: Belangrijke concepten
description: Dit onderwerp bevat informatie over de belangrijke concepten voor resourcebeheer in Project Service Automation.
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
ms.openlocfilehash: 1e5e78bbeb1086fada799cf7ac66173e5a563e2d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074788"
---
# <a name="key-concepts"></a>Belangrijke concepten

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In de volgende tabel zijn de belangrijkste concepten gedefinieerd die in de app Dynamics 365 Project Service Automation worden gebruikt.

| Concept                    | Definitie |
|----------------------------|------------|
| Projectteamlid        | Als onderdeel van het projectteam kan een projectteamlid een benoemde resource met boekingen, een benoemde resource zonder boekingen of een algemene resource zijn. Algemene resources hebben geen boekingen, zijn lokaal voor het project en hebben geen capaciteitsbeperkingen in projecten. |
| Algemene projectresource   | Een tijdelijke aanduiding voor resources waarmee u een team kunt vormen en resources aan een projectplan kunt toewijzen zonder dat u de benoemde resource hoeft te kennen. De projectagenda wordt gebruikt als de agenda van de algemene resource. Algemene resources kunnen aan een projectteam worden toegevoegd en aan taken worden toegewezen. |
| Geboekte uren               | Resource-uren worden hard geboekt voor een project om ervoor te zorgen dat het projectwerk wordt voltooid. Geboekte uren worden verbruikt vanuit de totale capaciteit van de resource. Boekingen worden alleen gemaakt voor benoemde resources, niet voor algemene resources. |
| Toegewezen uren             | Resource-uren worden toegewezen aan taken in de projectplanning. Toewijzingen kunnen worden uitgevoerd op basis van benoemde resources of algemene resources. Toewijzingen kunnen onafhankelijk van boekingen zijn. |
| Vereiste uren             | De capaciteit die is vereist, maar die nog niet is vervuld door een benoemde resource. Vereiste uren zijn alleen relevant voor algemene teamleden die resourcevereisten hebben gegenereerd. |
| Vraag                     | De huidige en binnenkomende workload. In Project Service Automation wordt de vraag weergegeven in de vorm van resourcevereisten of resourceaanvragen. |
| Resourcevereiste       | Een entiteit die wordt gebruikt voor het vastleggen van vereiste uren, begin- en einddatums, vaardigheden, geografie en andere prijsdimensies voor de vereiste resources. Resourcevereisten worden gegenereerd op basis van projectteamleden of worden afzonderlijk gemaakt. |
| Resourceaanvraag           | Een entiteit die wordt gebruikt als een 'envelop' die de resourcevereiste bevat waaraan moet worden voldaan door een resourcebeheerder. |
| Standaardresourcerol      | De rol waarbij een resource is ingedeeld voor de berekening van bestede uren. Er wordt aangenomen dat de resource over de vereiste vaardigheden voor de rol beschikt en aan het doel voor bestede uren voor die rol voldoet |
| Organisatie-eenheid van resource | De organisatie-eenheid waaraan een resource is toegewezen. |
| Contour                    | Taak, vereiste of toewijzingsuren, zoals die zijn opgesplitst in een dagelijkse distributie. Een taak van vijf dagen en 40 uur kan bijvoorbeeld worden uitgevoerd in acht uur per dag gedurende vijf dagen. |
| De weergave Afstemming        | Een weergave waarin de boekingen en toewijzingen voor elk projectteamlid worden weergegeven. In deze weergave kan de projectbeheerder zoeken naar eventuele discrepanties tussen boekingen en toewijzingen en corrigerende maatregelen nemen als er een discrepantie optreedt. |
| werkuren                 | Een entiteit die wordt gebruikt om resourcecapaciteit en werk- en niet-werkuren te identificeren. Deze entiteit wordt ook wel de resourceagenda genoemd. |