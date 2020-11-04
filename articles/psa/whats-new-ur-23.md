---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 23, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 23, v3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: eaae9cc62c449695cb2e999be48c57075aadbb21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074511"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation, updaterelease 23, v3

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 23. Deze versie heeft het buildnummer V 3.10.34.30 en is algemeen beschikbaar via een zelf-update vanaf augustus 2020.

## <a name="update-release-23"></a>Updaterelease 23

### <a name="bug-fixes"></a>Opgeloste fouten

**Tijd en onkosten**

De volgende problemen zijn opgelost:
- Afhandeling van randgeval in **Project-teamlid verwijderen** om een zinvolle uitzondering te bieden.
- Import van toewijzingen resulteert in een leeg verwijderscherm.

**Resourcebeheer**

De volgende problemen zijn opgelost:

- De resourcekaart voor het raster **Bestede uren van resource** bevat onjuiste gegevens als de tijdschaal meer dan vijf dagen is.
- Wanneer klanten een boekbare resource maken, kan de invoegtoepassing de resource af en toe niet automatisch toevoegen aan een Microsoft Office 365-groep.
- In de weergave **Vereffening** worden handmatige contouren onjuist weergegeven in de weergave **Week** of **Maand**.

**Projectbeheer**

De volgende problemen zijn opgelost:

- Een te groot aantal entiteiten voor **RetrieveMultiple for usersettings** leidt tot mindere prestaties voor projectgoedkeuringen en andere bewerkingen.
- In de opzoekfunctie voor resources in het raster **Taakplanning** kunnen maximaal vijf teamleden van het projectteam worden weergegeven. 
- In de opzoekfunctie voor resources in het raster **Taakplanning** worden inactieve resources niet gefilterd.
- De handmatige modus werkt niet zoals verwacht in de projectplanningsstructuur voor werkspecificatie.
- In het raster **Taakplanning** wordt **Inactieve transactiecategorieën** weergegeven.
- Het raster **Resourcetoewijzing** rondt onjuist af wanneer een taak meerdere toewijzingen heeft.
- Afrondingswaarden verschillen tussen geplande en werkelijke kosten voor een enkele taak.

**Sales**

De volgende problemen zijn opgelost:

- Wanneer in **Alle transactiecategorieën ophalen** wordt gedubbelklikt, worden er meerdere regels gemaakt.