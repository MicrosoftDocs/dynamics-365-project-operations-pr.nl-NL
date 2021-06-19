---
title: Nieuw in mei 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit onderwerp biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de mei 2021-release van Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07ae18faef6acb9d64b889bbfdba89de0c96a453
ms.sourcegitcommit: d48dce64f6c5b16db3250096715c9d9f92a81971
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083920"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuw in mei 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

- Project Operations in Dynamics 365 Dataverse-omgeving, versie 4.10.0.186
- Projectbeheer en financiële administratie in omgevingen van Finance and Operations-apps, versie 10.0.18

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

In deze versie zijn de volgende functies opgenomen:

- [Planningsmodi](../project-management/scheduling-modes.md): projectmanagers kunnen bepalen of een project moet worden beheerd met de planningsmodus voor vaste duur, vast werk of vaste eenheden.
- [Kilometerstand instellen met kilometertariefniveaus](../expense/set-up-mileage.md): kilometertariefniveaus bijwerken voor onkostendeclaraties van werknemers.

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

De volgende lijst toont de toewijzingen voor twee keer wegschrijven die zijn gewijzigd of toegevoegd in de release van Project Operations van mei 2021.

| Entiteitstoewijzing | Bijgewerkte versie | Opmerkingen  |
| --- | --- | --- |
| Bron voor projectfinanciering (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | De betalingsvoorwaarden van de klant voor projectcontracten synchroniseren. |
| Projectfactuurvoorstel V2 (facturen) | 1.0.0.3 | Betalingsvoorwaarden van pro-formafacturen synchroniseren. |
| Entiteit voor exporteren van leverancierfactuurregels in Project Operations-integratieprojecten (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Kwaliteitsupdates |
| Projecten V2 (msdyn\_projects) | 1.0.0.2 | Kwaliteitsupdates |

Voer altijd de meest recente versie van de toewijzing in uw omgeving uit en schakel alle gerelateerde tabeltoewijzingen in terwijl u uw Project Operations Dataverse-oplossing en uw oplossingsversie van de Finance and Operations-apps bijwerkt. Bepaalde functies en mogelijkheden werken mogelijk niet correct als niet de meest recente versie van de toewijzing is geactiveerd. U kunt de actieve versie van de toewijzing zien in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de toewijzing activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management.md) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in het gedeelte [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) van de handleiding voor probleemoplossing voor Twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Functiegebied** | **Referentienummer** | **Kwaliteitsupdate** |
| --- | --- | --- |
| Facturering en prijzen | 2227635 | De waarden in de velden **Eenheidsgroep** en **Eenheid** worden standaard overgenomen van het product in het raster **Materiaalschattingen**. |
| Facturering en prijzen | 2234127 | Het veld **Taak-ID** wordt nu juist geïntegreerd met werkelijke Dataverse-projectwaarden wanneer een leveranciersfactuur wordt geboekt. |
| Facturering en prijzen | 2235564 | Door de journaalregel op te slaan zorgt u ervoor dat de valuta die wordt weergegeven in de journaalregelpost na het opslaan overeenkomt met de standaardvaluta met de regel. |
| Facturering en prijzen | 2246671 | Als u een transactie tijdens de facturering niet-toerekenbaar maakt, wordt de oorspronkelijke niet-gefactureerde verkooprecord ongedaan gemaakt en wordt een nieuwe niet-gefactureerde verkooprecord als niet-toerekenbaar gemaakt. |
| Facturering en prijzen | 2264042 | Geldige factuurcorrectie mag niet worden geblokkeerd als er een factuurcorrectiedetail is dat niet geldig is in de omgeving. |
| Facturering en prijzen | 2146367 | Toewijzing voor twee keer wegschrijven voor de projectfactuurkoptekst is uitgebreid om betalingsvoorwaarden op te nemen. |
| Verkoopkansenbeheer | 2086888 | Voeg geen rollen en categorieën toe die zijn gedeactiveerd voordat u een offerte kopieert naar toerekenbare rollen en categorieën van een nieuw gekopieerde offerte. |
| Verkoopkansenbeheer | 2234376 | Alleen-lezen velden worden grijs weergegeven in het raster **Materiaalschattingen**. |
| Verkoopkansenbeheer | 2238337 | Een offerte op basis van een contactpersoon kan worden opgeslagen, zelfs als deze niet is gekoppeld aan een projectprijslijst. |
| Verkoopkansenbeheer | 2239810 | Als u een offerte als verloren sluit, wordt ook het bijbehorende project gesloten en worden eventuele boekingen geannuleerd. |
| Projecten plannen en bijhouden | 2099559 | Extra validaties voor systeemstatus toegevoegd voordat het raster **Projecttaken** wordt geopend. |
| Projecten plannen en bijhouden | 2178987 | Een tijdelijke fout opgelost die optreedt bij het selecteren van **Volgende fase** op de pagina **Project**. |
| Resourcebeheer | 2224817 | De functionaliteit om boekingen uit te breiden is standaard ingesteld op de juiste boekingsstatus. |
| Tijdsvermelding | 2202476 | Op de pagina **Tijdsvermelding** wordt nu gebruikgemaakt van het reactierasterbesturingselement en worden problemen opgelost zoals verkeerde uitlijning van het raster. |
| Tijdsvermelding | 2223377 | Tijdsvermeldingen worden verborgen in de sectie **Gerelateerd** de pagina **Boekbare resource** om verwarring met bruikbaarheid te voorkomen. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projectbeheer en boekhouding in Dynamics 365 Finance

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Projectbeheer en boekhouding | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Op resources gebaseerde scenario's in Project Operations: vanwege een integratiefout kunt u een prijsopgave niet converteren. |
| Projectbeheer en boekhouding | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: er verschijnt een foutbericht wanneer u een contractregel aan een project-id probeert te koppelen vanwege de controle op overlappende contractregels en transactietypen. |
| Projectbeheer en boekhouding | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | Met **ProjCDSprojectContractEntity** kan het factuuradres van de financieringsbron van een andere klant worden ingesteld. |
| Reizen en onkosten | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Er kan een boekingsfout met betrekking tot het instellen van kilometerstanden optreden. |
| Reizen en onkosten | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | De functionaliteit **Splitsen naar persoonlijk** werkt niet voor onkostentransacties in vreemde valuta's. |
| Reizen en onkosten | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | De waarden van het vervolgkeuzemenu van de onkostencategorie toont onjuiste categorieën voor gemachtigden, ongeacht of deze een resource zijn. |
| Reizen en onkosten | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | U kunt een intercompany-onkostendeclaratie niet opslaan vanwege een fout met **validatie van resource/categorie**. |
| Reizen en onkosten | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | De verkeerde berekening van het kilometertarief bij het boeken van onkostendeclaraties zorgt voor gesplitste regels. |
| Reizen en onkosten | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | U kunt geen intercompany-onkostendeclaratie boeken als de omzetbelasting is inbegrepen en het tegenrekeningtype van de betalingsmethode **Werknemer** is. |
| Reizen en onkosten | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | De gegevensentiteit **TrvRequisitionLine** voor terugdraaien en de unieke index zijn gekoppeld. |
| Reizen en onkosten | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Onkostendeclaratie ondersteunt het maken en bijwerken van brondocumentregels. |
| Reizen en onkosten | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Er wordt een onjuist subgrootboekjournaal weergegeven in een intercompany-scenario als de omzetbelasting wordt geboekt naar de rechtspersoon van bestemming. |
| Reizen en onkosten | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: de onkostenschatting wordt niet verwijderd uit Finance bij verwijdering uit Dataverse. |
| Reizen en onkosten | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Als de onkostencategorie een niet-projectcategorie is, worden de financiële dimensies die zijn geselecteerd op de pagina **Onkosten** niet naar de onkostennota gekopieerd. |
