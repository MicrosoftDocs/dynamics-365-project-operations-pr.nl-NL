---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 36, v3
description: Dit onderwerp biedt een overzicht van de functies en oplossingen die beschikbaar zijn in Update-versie 36, V3 van Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606743"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 36, v3

[!include [banner](../includes/psa-now-project-operations.md)]

We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze app is compatibel met Dynamics 365 9.x. Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 36, V3. Deze versie heeft het buildnummer V3.10.57.152 en is algemeen beschikbaar via een zelf-update vanaf oktober 2021.

## <a name="update-release-36"></a>Updaterelease 36

### <a name="bug-fixes"></a>Bugfixes

De volgende problemen zijn opgelost.

**Algemeen**
- De naam van het veld **Standaard werkurensjabloon** is onjuist vertaald op de pagina **Projectparameters**.
- Asynchrone invoegtoepassingen verwerken uitzonderingen met betrekking tot de **SharedVariableService** niet op correcte wijze.

**Tijd en onkosten**
- Wanneer journaalregels ontbreken of de gebruiker niet de juiste bevoegdheden heeft om journaalregels te lezen, treedt er een fout op wanneer projectgoedkeuringen worden geannuleerd.
- Gebruikers kunnen een goedkeuring niet annuleren wanneer een onkosten- of tijdsvermelding meer dan één gekoppelde projectgoedkeuring heeft.
- **Afwezigheid** en **Vakantie** zijn onjuist vertaald voor de Chinese taal in een zoekopdracht op de pagina voor snelle invoer **Tijdsvermelding**.

**Resourcebeheer**
- Gebruiker kan niet zoeken naar resources in de **Planningsassistent** wanneer de weergavemodus is ingesteld op **Dag**, **Week** of **Maand**.
- Generieke resources mogen ten onrechte lege positienamen hebben. 
- Als u een contract als verloren sluit, worden toekomstige boekingen niet geannuleerd.

**Verkoop**
- Wanneer een omgeving een groot volume aan producten heeft, nemen de prestaties af in het raster **Materiaalschatting**.
- Bij het maken van een project op basis van een sjabloon, wordt de projectvaluta niet standaard ingesteld op de contracterende eenheid van de desbetreffende projectmanager.
- Werkelijke bedragen komen niet altijd overeen met wat wordt weergegeven voor het verschuldigde project, of de bedragen worden negatief in specifieke terugroepscenario's.
- Er treedt een fout op wanneer u een project dat is gemaakt op basis van een projectsjabloon koppelt aan een contractregel.
- Gebruikers kunnen een contractregel met de mijlpalen **Gereed voor facturering** en **Factuur gemaakt** verwijderen. Dit zou niet mogen.
- Wanneer schattingen uit een project worden geïmporteerd, is de facturering van het prijsopgaveregeldetail onjuist ingesteld wanneer facturering op basis van taken is ingeschakeld voor de prijsopgaveregel.
- Wanneer u een mijlpaal voor facturering met een vaste prijs toevoegt, wordt de mijlpaal pas weerspiegeld in het subraster voor mijlpalen als de pagina wordt vernieuwd.
- Er wordt een null-referentie-uitzondering gegenereerd wanneer u een projectcontract maakt met een offertenaam met de waarde null.
- Taken in de handmatige modus waarbij de projectvaluta afwijkt van de valuta van de resource resulteren in onjuiste prijsschattingen.
- Gebruikers kunnen een transactie die met een correctiefactuur is gecorrigeerd, niet terugroepen.
- Gedeactiveerde transactiecategorieën verschijnen in het raster **Onkostenschattingen**.


