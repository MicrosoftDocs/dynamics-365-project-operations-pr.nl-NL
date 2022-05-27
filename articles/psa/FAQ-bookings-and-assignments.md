---
title: De relatie tussen resourceboekingen en taaktoewijzingen
description: Dit onderwerp bevat informatie over het beheren van benoemde resources, resourceboekingen en taaktoewijzingen, en hoe deze betrekking hebben op elkaar.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 953d7ca1995eae823fd29d0a9e85ff6a2a2eb59b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575473"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>De relatie tussen resourceboekingen en taaktoewijzingen

[!include [banner](../includes/psa-now-project-operations.md)]

Benoemde resources kunnen op twee manieren naar een projectteam worden geboekt en vervolgens aan projecttaken worden toegewezen:

- De resource kan direct naar een project worden geboekt en vervolgens aan projecttaken worden toegewezen.
- De taken kunnen worden toegewezen aan een algemene resource, die vervolgens wordt vervangen door een benoemde resource. 

In beide gevallen wordt met het boeken van de resource de capaciteit van de resource gereserveerd.

De projectmanager die het project plant, is eigenaar van het projectplan en de planning. Door de algemene resource voor de toewijzing te gebruiken en hiervan vervolgens een resourceaanvraag te genereren, kan de projectmanager resources naar het project boeken met opgegeven contouren in het projectplan. Vervolgens kunnen projectmanagers resources naar een project boeken en deze toewijzen aan taken, maar de boekingscontouren kunnen niet worden uitgelijnd met de contouren van de taken. Boekingen hebben geen invloed op de projectplanning.

Stel dat u werkt aan een complex project met meerdere overlappende taken waarbij meerdere resources van hetzelfde type tegelijkertijd moeten werken. Als voor een resource een contour wordt opgegeven die afwijkt van het totaal van de toegewezen taken, is het moeilijk om de taken te wijzigen zodat de contouren van de boekingen passen bij hun discrete taken en oorspronkelijke contouren.

In het onderstaande voorbeeld is de benodigde inzet voor een resource voor vier taken in totaal 62 uur gedurende een periode van twee weken en er is een specifieke contour. Als de resource Bob voor 62 uur wordt geboekt tijdens dezelfde periode van twee weken, maar met een verschillende contour, zijn de vereiste en boekingen uitgelijnd.

| **Taakcontouren**    | **Totale aantal uren** | Ma 4-6 | Di 5-6 | Wo 6-6 | Do 7-6 | Vr 8-6 | Za 9-6 | Zo 10-6 | Ma 11-6 | Di 12-6 | Wo 13-6 | Do 14-6 | Vr 15-6 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Taak 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Taak 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Taak 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Taak 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Totaalbedragen**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>De beschikbaarheid van Bob
| **Resourceboeking** | **Totale aantal uren** | Ma 4-6 | Di 5-6 | Wo 6-6 | Do 7-6 | Vr 8-6 | Za 9-6 | Zo 10-6 | Ma 11-6 | Di 12-6 | Wo 13-6 | Do 14-6 | Vr 15-6 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Er is echter geen systematische manier om de geboekte contour van uren per dag toe te wijzen aan taken. Als de projectmanager bereid is om de projectplanning aan te passen aan de beschikbaarheid van de resource, moet hij of zij de toewijzing verwijderen en alle taken herzien op basis van de boekingscontouren.

Als een organisatie de taak van projectplanning zowel aan een projectmanager als aan een resourcemanager heeft gegeven, bepaalt de projectmanager de planning. Het bepalen van de contouren van het vereiste werk hoort hierbij. De resourcemanager mag de planning niet zonder medeweten van de projectmanager aanpassen door de inspanningscontouren te wijzigen tijdens het boeken van echte resources. Als de resourcemanager iets anders doet dan wat de projectmanager heeft aangevraagd, moeten ze overeenstemming bereiken over de benodigde wijzigingen in de projectplanning.

Omdat boekingen en toewijzingen niet nauw gekoppeld zijn, is het mogelijk om contouren te boeken die afwijken van de taakcontouren of de toewijzingen zo te wijzigen dat boekingen en toewijzingen niet meer zijn afgestemd.

In de weergave **Vereffening** kan de projectmanager de boekingen en toewijzingen voor elk lid van het projectteam weergeven. In de weergave worden kleuren en arceringen gebruikt om aan te geven waar boekingen en toewijzingen van teamleden niet op elkaar zijn afgestemd. Op basis van deze informatie kan de projectmanager corrigerende maatregelen nemen om resourceboekingen uit te breiden wanneer er wel toewijzingen, maar geen boekingen zijn of boekingen te annuleren wanneer er resources zijn geboekt, maar er geen toewijzingen zijn.

> [!NOTE]
> Als u een taak verplaatst waarvoor u zelf de contouren hebt ingesteld, worden de contouren niet behouden. De contouren worden opnieuw gegenereerd op basis van de projectagenda voor wijzigingen in werkuren en sluitingsperioden. Dit is zo ontworpen. Het systeem is namelijk niet op de hoogte van de bedoeling van de oorspronkelijke contour en kan niet bepalen of het zinvol is om die contour te behouden in een nieuwe periode. Omdat boekingen en toewijzingen niet verbonden zijn, behouden de boekingen de oorspronkelijke boekingscontouren. In dit geval moet u annuleren en opnieuw boeken in de nieuwe toewijzingscontour.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
