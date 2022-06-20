---
title: Wat is er nieuw of gewijzigd in Project Service Automation updateversie 35, v3
description: Dit artikel biedt een overzicht van de functies en oplossingen die beschikbaar zijn in Microsoft Dynamics 365 Project Service Automation-updateversie 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 28b4a5ccbfff83c9b1a18cb0b4062af9cdaf8f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912832"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updateversie 35, v3

[!include [banner](../includes/psa-now-project-operations.md)]

We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze app is compatibel met Dynamics 365 9.x. Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit artikel worden de functies en oplossingen vermeld die nieuw of gewijzigd zijn voor Project Service Automation-updateversie 35, V3. Deze versie heeft een buildnummer van V3.10.56.110 en is algemeen beschikbaar via een zelfupdate in september 2021.

## <a name="update-release-35"></a>Updateversie 35

### <a name="bug-fixes"></a>Opgeloste fouten

De volgende problemen zijn opgelost.

**Tijd en onkosten**

- De projectfiatteur ontvangt een fout over leesbevoegdheden wanneer deze onkostenposten goedkeurt met de rol **Projectfiatteur**.
- De fiatteur van het project ontvangt een fout over schrijfbevoegdheden op **msdyn_projectapproval** wanneer hij/zij een goedgekeurde tijdsinvoer annuleert met de rol **Projectfiatteur**.
- Wanneer u **Week kopiëren** selecteert in een tijdsvermelding in de app-module Dynamics 365 voor telefoons - Hub voor projectresource, treedt de volgende fout op: "...\OfficeProductivity_RibbonRules.js.map: HTTP-fout: statuscode 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- Het beleid **Opnieuw proberen** keurt automatisch inzendingen goed die eerder werden afgewezen.
- Het subraster **Goedkeuringssets** toont niet-toepasselijke lintacties.
- Pictogrammen ontbreken voor **Projecttaak** en **Resourcerol** van de entiteit **Tijdsvermelding**.
- Wanneer u resourcetoewijzingen importeert, hebben geïmporteerde tijdsvermeldingen niet de juiste duur voor toewijzingen die zijn gemaakt via taken in de handmatige modus.
- **Verwijderen** ontbreekt op de pagina **Geavanceerd zoeken voor tijdsvermeldingsrecords**.
- **Opslaan** ontbreekt op de pagina **Informatie over tijdsvermelding**. Dit probleem voorkomt dat wijzigingen worden opgeslagen wanneer de pagina wordt gesloten.

**Projectplanning**

- De rasters **Resourcetoewijzing** en **Afstemming van resources** sorteren gegroepeerde attributen niet alfabetisch.
- Taken kunnen niet worden gemaakt als het datumgedrag is aangepast aan **Alleen datum**.

**Resourcebeheer**

- Als zowel Dynamics 365 Field Service als project Service Automation is geïnstalleerd, treden er problemen met lagen wanneer **Gekoppelde weergave van resourcevereisten** is gekoppeld aan een hoofdpagina.
- Dubbelklik op **Opslaan** in het dialoogvenster **Snelle invoer voor teamleden** om te voorkomen dat de resourcevereiste wordt gemaakt.

**Verkoop**

- Er wordt een uitzondering gegenereerd als u een taak verwijdert die is gekoppeld aan een offerte met de status **Gewonnen**.
