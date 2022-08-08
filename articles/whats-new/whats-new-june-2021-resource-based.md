---
title: Nieuwe functies van juni 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit artikel biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Project Operations van juni 2021 voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd745107fa6d50882ebea302d3d2ae0de21b79ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028169"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies van juni 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit artikel is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

- Project Operations in Dynamics 365 Dataverse-omgeving versie 4.11.0.156 of 4.11.0.164.
- Projectbeheer en financiële administratie in omgevingen van apps voor financiën en bedrijfsactiviteiten versie 10.0.19.

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

In deze versie zijn de volgende functies opgenomen:

- Mogelijkheid om [Factuurvoorstelregels van projecten voor aanpassingsscenario's](../invoicing/correct-project-invoice-proposals.md) te verwijderen.
- Gespecificeerde onkostenregels geven namen weer van subcategorieën in de onkostennota [Onkostennota´s opnieuw ontworpen - nieuwe functies](../expense/expense-reports-reimagined.md#new-features).
- De betalingswijze is beschikbaar in het nieuwe onkostenvenster wanneer u nieuwe onkosten maakt.
- Algemene beschikbaarheid van API's voor projectplanning. Met deze nieuwe functionaliteit kunnen klanten programmatisch bewerkingen voor maken, bijwerken en verwijderen uitvoeren voor projecttaken, resourcetoewijzingen, taakafhankelijkheden en records van projectteamleden. Zie voor meer informatie [API's voor projectplanning gebruiken om bewerkingen met planningsentiteiten uit te voeren](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

Er zijn geen updates voor toewijzingen van twee keer wegschrijven in Project Operations in deze release. 

Zie [Toewijzingsversies van twee keer wegschrijven voor Project Operations](../environment/resource-dual-write-maps.md) voor een actuele lijst en versies van toewijzingen van twee keer wegschrijven voor Project Operations.

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en oplossing voor apps voor financiën en bedrijfsactiviteiten bijwerkt. Bepaalde functies en mogelijkheden werken mogelijk niet correct als niet de meest recente versie van de toewijzing is geactiveerd. U kunt de actieve versie van de toewijzing zien op de pagina **Twee keer wegschrijven** in de kolom **Versie**. Activeer een nieuwe versie van de toewijzing door **Versies van tabeltoewijzing** te selecteren, de nieuwste versie te selecteren en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in het gedeelte [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) in de handleiding voor het oplossen van problemen met twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Functiegebied** | **Referentienummer** | **Kwaliteitsupdate** |
| --- | --- | --- |
| Facturering en prijzen | 2281417 | Het probleem is opgelost met betrekking tot de fout met de actie voor het automatisch maken van facturen via de factuurplanning. |
| Facturering en prijzen | 2287835 | Verbeterde prestatie van factuurbevestiging. |
| Verkoopkansenbeheer | 2222555 | De toerekenbaarheid van materiaalschattingen moet correct worden gekopieerd naar details van prijsopgaveregels wanneer **Importeren uit projectraming** wordt gebruikt. |
| Verkoopkansenbeheer | 2223427 | Aanpassingen zijn nu toegestaan voor de actie **GenerateRetainersFromRetainerScheduleOptions**. |
| Verkoopkansenbeheer | 2277528 | Berekening van vaste mijlpaalwaarde voor facturering voor projectcontractregels met meerdere klanten. |
| Projecten plannen en bijhouden | 2226110 | Het terugkerende probleem met de functie **Vereiste genereren** in het raster **Projectteam** is opgelost. |
| Projecten plannen en bijhouden | 2208109 | Gebruikers kunnen geen project in de ene valuta maken met gerelateerde taken in een andere valuta. |
| Projecten plannen en bijhouden | 2258228 | De lijst met velden die mogen worden gewijzigd met **Planningsentiteiten** die de API voor planning gebruiken, is bijgewerkt. |
| Projecten plannen en bijhouden | 2293989 | De juiste taal- en landinstellingen moeten worden doorgegeven aan het raster **Projecttaken**. |
| Resourcebeheer | 2220493 | Het probleem met de gebruikerservaring in het raster **Taak** bij het snel markeren van een resourceaanvraag als voltooid is opgelost. |
| Resourcebeheer | 2330496 | Het probleem met het laden van het **Planbord** is opgelost. (Kwaliteitsupdate is beschikbaar in versie 4.11.0.164) |
| Tijd en onkosten | 2194431 | Het raster **Tijdsvermelding** moet rekening houden met het begin van de week zoals is ingesteld in de **Systeeminstellingen**. |
| Tijd en onkosten | 2277311 | Nadat u de waarde in een cel in het raster **Tijdsvermelding** hebt verwijderd, blijft de cursor in het raster. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projectbeheer en financiële administratie in Dynamics 365 Finance

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Projectbeheer en financiële administratie | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Formuliernotities** en **Formulierinstellingen** zijn niet zichtbaar onder **Projectbeheerinstellingen** in Finance-rechtspersonen die zijn geïntegreerd met Project Operations. |
| Projectbeheer en financiële administratie | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | De standaardbeschrijving voor btw is leeg, wanneer het **Boekingstype** = **Btw** voor projectfactuurboekstukken. |
| Projectbeheer en financiële administratie | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Er worden dubbele transacties geboekt wanneer op taken gebaseerde facturering wordt gebruikt in Dataverse met Project Operations-integratie. |
| Projectbeheer en financiële administratie | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Het percentage voltooid voor opbrengstverantwoording is onjuist wanneer Project Operations-integratie wordt gebruikt. |
| Projectbeheer en financiële administratie | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | De opbrengstenopbouw wordt verdubbeld in een in behandeling zijnde leveranciersfactuur gebruikt in een geïntegreerd scenario van Project Operations. |
| Projectbeheer en financiële administratie | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Kan het integratiejournaal niet boeken als de regel voor het opbrengstprofiel is ingesteld op **Groepsconfiguratie**. |
| Projectbeheer en financiële administratie | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Een inkoopfactuur kan niet worden geboekt voor projectinkooporders die regels bevatten met meerdere maateenheden. |
| Projectbeheer en financiële administratie | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | De standaard financiële dimensie voor een project kan niet worden bijgewerkt met de gegevensentiteit **V2** van projecten. |
| Projectbeheer en financiële administratie | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Het batchproces voor het maken van projectramingen duurt te lang om te voltooien. |
| Projectbeheer en financiële administratie | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Wanneer u een contract verwijdert, wordt ook het aan de klant gekoppelde adres verwijderd. |
| Reizen en onkosten | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | De werkstroomvoorwaarde voor goedkeuring van onkostennota´s wordt niet correct geëvalueerd. |
| Reizen en onkosten | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Het beleid voor onkostennota´s evalueert de project-ID niet correct. |
| Reizen en onkosten | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | De actie **Splitsen naar persoonlijk voor intercompany-onkostentransacties** werkt niet correct. |
| Reizen en onkosten | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Rechtvaardigingen van een onkostennotaregel worden per ongeluk verwijderd wanneer bepaalde reisaanvragen worden verwijderd. Dit gebeurt wanneer de record-ID van de onkostennota en de reisaanvraag hetzelfde zijn. |
| Reizen en onkosten | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Er is een probleem met de mobiele app voor onkosten wanneer het veld **Project-ID** wordt vereist voor het beleid voor onkostennota´s. |
| Reizen en onkosten | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Intercompany-onkosten die aan een project zijn gekoppeld, kunnen niet worden bewerkt. In plaats daarvan wordt het volgende foutbericht weergegeven: 'Objectverwijzing niet ingesteld op een exemplaar van een object'. |
| Reizen en onkosten | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Nadat een onkostennota is geboekt, wordt de verkeerde valuta en het verkeerde bedrag vermeld in het subgrootboek van de bank. |
| Reizen en onkosten | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Er zijn verbeteringen aangebracht in de functie *Creditcardtransacties verwijderen*.  |
| Reizen en onkosten | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Btw die in een onkostennota is opgenomen, wordt niet consistent berekend wanneer een andere aangiftevaluta is opgegeven in een rechtspersoon. |
| Reizen en onkosten | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | De prestaties worden beïnvloed wanneer nieuwe contante reisonkosten worden toegevoegd. |
| Reizen en onkosten | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Onkostenbeleidsregels worden niet geactiveerd voor een onkostennota. |
| Reizen en onkosten | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Als u een nieuwe gedeelde categorie uploadt met behulp van het Data Management Framework, worden alle subcategorieën voor alle gedeelde categorieën verwijderd. |
| Reizen en onkosten | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Wanneer u een onkostenregel maakt en vervolgens een categorie selecteert, wordt het volgende foutbericht weergegeven: "De combinatie van btw-groep DOM en btw-groep STD is niet geldig." |
| Reizen en onkosten | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Er zijn synchronisatieproblemen in de mobiele toepassing voor onkosten. |
