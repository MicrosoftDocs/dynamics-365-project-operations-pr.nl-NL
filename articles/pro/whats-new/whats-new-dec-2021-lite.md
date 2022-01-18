---
title: Nieuw in december 2021 - Project Operations Lite-implementatie
description: Dit onderwerp biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Project Operations Lite-implementatie van december 2021.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942971"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Nieuw in december 2021 - Project Operations Lite-implementatie

_Van toepassing op: Lite-implementatie - van deal tot pro-formafacturering_

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

### <a name="subcontract-management"></a>Toeleveringscontractbeheer 

- [Onder contract nemen van projectteamleden](../subcontracting/subcontracting-project-team-members.md): een projectmanager kan benoemde of algemene teamleden maken met toeleveringscontract en toeleveringscontractregels om de personeelsbezetting en schatting te beïnvloeden.
- [Toeleveringscontractopties voor projectteamleden](../subcontracting/subcon-options.md): bij het maken van personeelskeuzes voor benoemde of algemene projectteamleden kan de projectmanager bestaande toeleveringscontracten beoordelen of nieuwe toeleveringscontracten maken voor een of meer projectteamleden. 
- [Kostenraming van toewijzingen van resources op contractbasis](../subcontracting/costing-subcon-ra.md): bij de schatting van de projectkosten wordt rekening gehouden met toewijzingen van resources op contractbasis en worden de kosten ervan berekend met behulp van de inkoopprijslijsten die aan toeleveringscontracten zijn gekoppeld. 
- [Planbord configureren om contractwerknemers en toeleveringscapaciteit weer te geven](../subcontracting/configure-sb-subcon.md): planbord in Project Operations kan nu worden geconfigureerd om te zoeken naar en voorstellen te doen voor het contractwerknemertype van boekbare resources en toeleveringscapaciteit, evenals medewerkers. Deze configuratie kan worden toegepast bij het zoeken naar resources binnen de context van personeelsbezetting voor een specifieke projectvereiste of bij het zoeken buiten de context van een projectvereiste.
- [Een project bemannen met contractwerknemers en toeleveringscapaciteit](../subcontracting/staffing-cw.md) : contractwerknemers kunnen nu worden geboekt voor projecten waarbij gebruik wordt gemaakt van de ervaringen met het planbord.
- [Registratie van tijd, kosten en materiaalgebruik op projecten voor toeleveringscomponenten](../subcontracting/recording-subcon-actuals.md) : contractwerknemers kunnen tijd en onkosten registreren en projectteamleden kunnen ook het gebruik van materialen registreren die met een toeleveringscontract voor een project zijn ingekocht. Dit zal resulteren in het nauwkeurig vastleggen van kosten op projecten die ingekochte capaciteit of materialen gebruiken.
- [Statusovergangen op een toeleveringscontract](../subcontracting/subcon-states.md): toeleveringscontracten kunnen worden bevestigd om de onderhandelingen met de leverancier te voltooien, worden gesloten om de voltooiing van de levering aan te geven of worden geannuleerd om de beëindiging van het contract met de leverancier aan te geven voordat de levering is voltooid.

### <a name="task-planning"></a>Taakplanning
- Verbeterde probleemoplossing voor systeembeheerders. Wanneer een gebruiker een project niet kan openen, kan de beheerder niet-licentiegerelateerde fouten bekijken die zijn gegenereerd vanuit Project for the Web in [Logboeken voor projectplanning](../../project-management/schedule-api-logs.md).
- [Taakcontrolelijsten gebruiken in Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). In Microsoft Project for the Web kunt u een controlelijst aan een taak toevoegen om specifieke items bij te houden.

## <a name="quality-updates"></a>Kwaliteitsupdates

| **Functiegebied** | **Referentienummer** | **Kwaliteitsupdate** |
| --- | --- | --- |
| Planning en tracering | 2392596 | Plannings-API's staan nu bijwerken toe van de velden **Resterende inspanning**, **Inspanning voltooid** en **% voltooid**. |
| Planning en tracering | 2478497 | De velden **Activiteitsnummer** en **Taak-id** van Plannings-API's kunnen bij invoer leeg zijn omdat het systeem ze zal vullen met behulp van geautomatiseerde nummering.|
| Tijd en onkosten | 2468135 | Het aantal nieuwe goedkeuringspogingen is teruggebracht van vijf naar drie. |
| Tijd en onkosten | 2468188 | Probleem opgelost met logtekst die de maximale lengte overschreed in het kenmerk **notetext** van de entiteit **annotation**. |
