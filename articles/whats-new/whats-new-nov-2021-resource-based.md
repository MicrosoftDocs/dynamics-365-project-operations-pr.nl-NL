---
title: Nieuwe functies van november 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit onderwerp biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Project Operations van november 2021 voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827320"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies van november 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

*Van toepassing op: Project Operations voor scenario's op basis van resources/niet-voorradige artikelen*

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.26.0.145, 4.26.0.148 en 4.26.0.150
- Projectbeheer en financiële administratie in een Dynamics 365 Finance-omgeving versie 10.0.22

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

In deze versie zijn de volgende functies opgenomen:

- API's (Application Programming Interfaces) voor projectplanning ondersteunen nu de mogelijkheid om Project-buckets te maken en te verwijderen.

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

Er zijn geen updates voor toewijzingen van twee keer wegschrijven in Project Operations in deze release. Zie [Toewijzingsversies van twee keer wegschrijven voor Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps) voor een actuele lijst en versies van toewijzingen van twee keer wegschrijven voor Project Operations.

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Sommige functies en mogelijkheden werken mogelijk niet correct als de nieuwste versie van de toewijzing niet wordt geactiveerd. U kunt de actieve versie van de kaart weergeven in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de toewijzing activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in de sectie [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) van de probleemoplossingsgids voor Twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-in-dataverse"></a>Project Operations in Dataverse

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Facturering en prijzen | 2240080 | Het veld **Betalingsvoorwaarden** mag niet worden gedupliceerd op de pro-formafactuur. |
| Facturering en prijzen | 2358236 | Factuurcorrectie moet correcties met nulprijsregels toestaan. |
| Resourcebeheer | 2410072 | Mogelijkheid om een resource die is toegewezen aan de taak als projectmanager in te stellen. |
| Facturering en prijzen | 2430234 | Oplossen van een probleem met de berekening van kostenprestaties. |
| Tijd en onkosten | 2436978 | Toestaan dat tijd wordt ingevoerd in de indeling uu:mm. |
| Facturering en prijzen | 2448623 | Toestaan dat prijslijsten worden bijgewerkt nadat deze aan een organisatie-eenheid zijn gekoppeld. |
| Tijd en onkosten | 2460396 | Toestaan dat een tijdsinvoer wordt verwijderd door de cel te wissen. |
| Facturering en prijzen | 2467386 | Toestaan dat een project met een taak wordt verwijderd, zelfs als de taak is gekoppeld aan een gewonnen offerte. |
| Tijd en onkosten | 2461744 | De weergave **Mijn mislukte goedkeuring** bevat alleen projectgoedkeuringen in de fase **Ingediend**. |
| Tijd en onkosten | 2464082 | Verwijderen van de koppeling van projectgoedkeuringen naar de goedkeuringsset wanneer aan een doelstatus wordt voldaan. |
| Tijd en onkosten | 2468108 | De taak Plannen mag niet een status **Verwerken** instellen voor de goedkeuringsset. |
| Tijd en onkosten | 2471503 | Verwijderen van goedkeuringssets die zeven dagen oud zijn. |
| Facturering en prijzen | 2480687 | De verwijzing naar de prijsopgaveregel mag niet worden verwijderd wanneer een mijlpaal voor de prijsopgaveregel wordt gemaakt. |

### <a name="project-management-and-accounting-in-finance"></a>Projectbeheer en financiële administratie in Finance

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Projectbeheer en boekhouding | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Ingehouden leveranciersbedragen in projectonkostentransacties worden niet weergegeven in de transactielijst. |
| Projectbeheer en boekhouding | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | De intercompany-leveranciersfactuur wordt verbroken wanneer integratie van leveranciersfacturen is ingeschakeld. |
| Projectbeheer en boekhouding | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | De betalingsvoorwaarden op projectfacturen werken niet zoals verwacht. |
| Projectbeheer en boekhouding | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Wanneer de leveranciersinhouding wordt vrijgegeven, bevat de boekstukboeking aanvullende regels die onjuist zijn. |
| Projectbeheer en boekhouding | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Wanneer het integratiejournaal van Project Operations wordt geboekt, mislukt dit vanwege ontbrekende dimensies voor een account waar niet naar geboekt wordt. |
| Projectbeheer en boekhouding | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Het tabblad **Project** kan niet worden bewerkt op een openstaande leveranciersfactuur wanneer de inkoopcategorie aan het artikel wordt toegewezen. |
| Projectbeheer en boekhouding | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Het navigatiedeelvenster ontbreekt als u niet bent aangemeld bij project Operations Dataverse. |
| Projectbeheer en boekhouding | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Wanneer u opbrengsten boekt vanaf een projectfactuur bij een toegepast voorschot treedt er een fout op, omdat transacties op het boekstuk niet in evenwicht zijn. |
| Projectbeheer en boekhouding | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Het maken van een raming nadat u een factuurvoorstel hebt geboekt, voorkomt dat correctieregels kunnen worden geïmporteerd. |
| Projectbeheer en boekhouding | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Wijziging van een volledig gefactureerde mijlpaalrecord zou niet mogelijk moeten zijn. |
| Reizen en onkosten | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Alle onkostennota's zijn te zien wanneer u zoekt naar een categorie in de mobiele app voor onkosten. |
| Reizen en onkosten | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Er worden onjuiste bedragen voor leveranciers- en btw-transacties geboekt op basis van een onkostenpost die wordt gemaakt op basis van een creditcardtransactie. |
| Reizen en onkosten | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Er treedt een irrelevant waarschuwingsbericht op wanneer u de pagina **Onkostennota** vernieuwt. |
| Reizen en onkosten | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | De verkeerde tussentijdse fiatteur wordt gebruikt wanneer u een tussentijdse fiatteur verwijdert en vervolgens een onkostennota opnieuw indient via de werkstroom. |
| Reizen en onkosten | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Er treedt een boekingsfout op die verband houdt met de kilometerstand. |
