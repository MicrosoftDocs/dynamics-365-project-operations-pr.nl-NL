---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 18, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 18, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 3a6d3ee21ecf742b2253132f3d3cc1cb2b57af75
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119862"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation, updaterelease 18, v3

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 18. Deze versie heeft een buildnummer van V3.10.8.12 en is algemeen beschikbaar via een zelfupdate in april 2020.

## <a name="update-release-18"></a>Updaterelease 18

### <a name="bug-fixes"></a>Opgeloste fouten

**Tijd en onkosten**

- Opgelost: stromen **Intrekken**, **Aanvragen** en **Goedkeuring annuleren** leiden tot uitzonderingen met onduidelijke foutmeldingen.
- Opgelost: wanneer **Goedkeuring annuleren** mislukt voor een onkostenpost, wordt geen relevante uitzonderingsfout gegenereerd.
- Opgelost: het rooster voor tijdinvoer verwerkt niet-werkdagen in Australië op onjuiste wijze na omschakeing van de zomertijd in oktober.
- Opgelost: onjuiste standaardlogica voorkomt het indienen van onkostenposten.
- Opgelost: als goedkeuring voor tijdinvoer mislukt, blijft de goedkeuring de status **In behandeling** houden.
- Opgelost: SQL-fouten bij bulkgoedkeuringen (impasse/time-out).
- Opgelost: significante prestatieproblemen in de gebruikerservaring veroorzaakt door het bijwerken van teamleden tijdens het goedkeuren van tijdsvermeldingen.

**Projectbeheer**

- Opgelost: tijdzonemelding verplaatst van de weergave **Afstemming** naar het hoofdformulier **Project**.
- Opgelost: agendasjabloon gebruikt geen correcte standaardwaarden bij het openen van een nieuw projectformulier.
- Opgelost: voor op Chromium gebaseerde browsers kunnen gebruikers niet gemakkelijk voorafgaande taken selecteren om ze te verwijderen.
- Opgelost: bij het maken of kopiëren van **Project vanuit lege sjabloon** worden niet-gerelateerde opdrachten opgehaald.
- Opgelost: in specifieke randgevallen resulteert het maken van een nieuwe toewijzing vanuit het taakraster in dubbele records.
- Opgelost: in de handmatige modus kunnen gebruikers de startdatums van taken niet bijwerken tot na de huidige opgeslagen datum.

**Resourcebeheer**

- Opgelost: rij voor subtotaal in weergave **Afstemming** berekent op onjuiste wijze de boekingsvariantie na verlenging van boekingen.
- Opgelost: in de weergave **Afstemming** worden resourcetoewijzingen onjuist weergegeven als de boekbare resource een agenda heeft die niet overeenkomt met de projectagenda.

**Sales**

- Opgelost: wanneer tijdsvermeldingen opnieuw worden goedgekeurd (**Goedkeuren > Annuleren >** opnieuw goedkeuren), wordt een dubbele niet-toerekenbare werkelijke waarde gemaakt.
