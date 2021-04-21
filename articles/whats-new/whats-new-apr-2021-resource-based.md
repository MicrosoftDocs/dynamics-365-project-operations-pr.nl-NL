---
title: Nieuw in april 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Deze onderwerp biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de april 2021-release van Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
manager: tfehr
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 359d39898ed60c7253b122cb884465fbd9605e0c
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867987"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuw in april 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

- Project Operations in Dataverse-omgeving, versie 4.9.0.221
- Projectbeheer en financiële administratie in Dynamics 365 Finance-omgeving, versie 10.0.17

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

In deze versie zijn de volgende functies opgenomen:

- Niet-voorradige materialen voor projecten. De belangrijkste mogelijkheden zijn onder meer:
  - Schatten en prijzen van niet-voorradige materialen tijdens de verkoopcyclus voor een project. Zie voor meer informatie [Kosten- en verkooptarieven voor catalogusproducten instellen - lite](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Het gebruik van niet-voorradige materialen volgen tijdens de levering van het project. Zie [Materiaalgebruik voor projecten en projecttaken registreren](../material/material-usage-log.md) voor meer informatie.
  - Facturering van gebruikte niet-voorradige materiaalkosten. Zie [Achterstallige facturen beheren](../proforma-invoicing/manage-billing-backlog.md) voor meer informatie.
- Taakgebaseerde facturering: de mogelijkheid toegevoegd om projecttaken te koppelen aan projectcontractregels, waardoor ze worden onderworpen aan dezelfde factureringsmethode, factuurfrequentie en klanten als die op de contractregel. Deze koppeling zorgt voor nauwkeurige facturering, boekhouding, schattingen van inkomsten en de erkenning om in overeenstemming met deze opzet te werken aan projecttaken.
- Met nieuwe API's in Dynamics 365 Dataverse kunnen bewerkingen voor maken, bijwerken en verwijderen worden uitgevoerd met **planningsentiteiten**. Zie [Plannings-API's gebruiken om bewerkingen uit te voeren met planningsentiteiten](../project-management/schedule-api-preview.md) voor meer informatie.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations in Dynamics 365 Dataverse

| **Functiegebied** | **Referentienummer** | **Kwaliteitsupdate** |
| --- | --- | --- |
| Facturering en prijzen | 2124532 | De knop **Factuur corrigeren** wordt weergegeven in een pro-formafactuur wanneer het voorschotbedrag of het toegepaste voorschotbedrag op de originele factuur staat. De knop wordt alleen weergegeven voor omgevingen met Finance-versie 10.0.19 of hoger. |
| Facturering en prijzen | 2224568 | Logica toegevoegd om aanpassingen mogelijk te maken waarbij de invoegtoepassing voor factuurbevestiging wordt aangeroepen. |
| Facturering en prijzen | 2101098 | Verbeterde logica van standaardvelden naar pro-formafactuur: **Factuuradres**, **Naam voor factuur** en **Betalingsvoorwaarden** worden nu standaard uit het corresponderende klantrecord van het projectcontract gehaald. |
| Facturering en prijzen | 2021413 | De velden **Werkelijke kosten** en **Verkoop** in de entiteit **Taak** zijn bijgewerkt om verkoopwaarden van niet-gefactureerde en gefactureerde uitgaven voor taken op te nemen. |
| Facturering en prijzen | 2182110 | Bij het kopiëren van een projectcontract wordt de contractregel-id opnieuw gegenereerd in het doelprojectcontract om ervoor te zorgen dat het uniek is. |
| Verkoopkansenbeheer | 2186741 | Validaties toegevoegd om ervoor te zorgen dat het veld **Oorsprong** en **Transactietype** niet kunnen worden bijgewerkt voor bestaande prijsopgaveregeldetails. |
| Verkoopkansenbeheer | 2191353 | Mijlpalen mogen niet worden gemaakt op een contractregel voor tijd en materiaal. |
| Verkoopkansenbeheer | 2216956 | Problemen met **Prijzen**​ zijn opgelost. |
| Planning en tracering | 2182979 | De functie Project kopiëren is verbeterd om ervoor te zorgen dat de kostenschattingsregels worden gekopieerd uit het oorspronkelijke project. |
| Planning en tracering | 2184144 | De functie Project kopiëren is verbeterd om ervoor te zorgen dat de naam van de resourcepositie wordt gekopieerd uit het oorspronkelijke project. |
| Planning en tracering | 2184799 | Project kopiëren: verscherpte controle om ervoor te zorgen dat de geschatte begindatum niet kan worden gewijzigd tijdens het kopiëren. |
| Planning en tracering | 2185134 | Project kopiëren: de geschatte begindatum van het doelproject wordt ingesteld op de datum van vandaag. |
| Planning en tracering | 2196373 | Project kopiëren: dat de records van de projectmanager en het teamlid worden niet gedupliceerd in het projectteam. |
| Planning en tracering | 2211833 | Project kopiëren: Resourcetoewijzingen worden gekopieerd van de bronprojecttaak naar het doelproject. |
| Planning en tracering | 2186541 | Problemen in het raster **Schattingen** bij het groeperen op resource zijn opgelost. |
| Planning en tracering | 2166906 | De transactiecategorie van een taak moet worden gekopieerd naar de entiteit **Resourcetoewijzing**. |
| Resourcebeheer | 2125362 | Problemen met het maken van een algemeen teamlid met een op uren gebaseerde toewijzingsmethode zijn opgelost. |
| Tijd en onkosten | 2113603 | Oplossing voor het aanpassingsprobleem met het verwijderen van kenmerken van de pagina **Tijdinvoer**. Er wordt nu gecontroleerd of het kenmerk op de pagina bestaat voordat het met een script wordt geopend. |
| Tijd en onkosten | 2204377 | Gekopieerde urenstaten moeten automatisch worden weergegeven wanneer u **Week kopiëren** selecteert tijdens tijdinvoer. |
| Tijd en onkosten | 2209059 | Het veld **Status** kan worden bewerkt voor Dynamics 365 Field Service-tijdinvoer. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projectbeheer en boekhouding in Dynamics 365 Finance

| **Functiegebied** | **Referentienummer** | **Kwaliteitsupdate** |
| --- | --- | --- |
| Projectbeheer en boekhouding | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminatie met omgekeerde schatting werkt niet in **Periodiek**​.  |
| Projectbeheer en boekhouding | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Met de functie **Boekhoudkundige aanpassing** ontstaat een probleem met grootboekrekeningen waarvoor **Handmatige invoer niet toestaan** is geselecteerd. |
| Projectbeheer en boekhouding | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Er is bedrijfslogica toegevoegd om correctiefacturen te verwerken, inclusief voorschotbedrag of toegepast voorschotbedrag. |
| Projectbeheer en boekhouding | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Bij het boeken van OHW-verkoopwaarde bij intercompany-projectfacturering wordt een onverwachte rekening gekozen. |
| Projectbeheer en boekhouding | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Wanneer u in Project Operations met voorschotten werkt, veroorzaakt een wijziging van het standaardproject in een contract na facturering van de vooruitbetalingen problemen met inkomende inhoudingen. |
| Projectbeheer en boekhouding | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | In Project Operations moet na verwijdering van een project uit een contract zo nodig het standaardproject van het contract opnieuw worden ingesteld. |
| Projectbeheer en boekhouding | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | In Project Operations worden de verkeerde onkostenregels weergegeven in de lijst **Regel toevoegen** op de intercompany-factuur. |
| Projectbeheer en boekhouding | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | In Project Operations is de pagina **Inkoopovereenkomst** niet zichtbaar in Finance-rechtspersonen die zijn geïntegreerd met Project Operations. |
| Projectbeheer en boekhouding | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Vanwege een Dataverse-integratiefout kunt u een offerte niet converteren naar gewonnen in Project Operations. |
| Projectbeheer en boekhouding | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSprojectContractEntity** kan het factuuradres van de financieringsbron van een andere klant instellen.  |
| Projectbeheer en boekhouding | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | In Project Operations worden geen dimensies geselecteerd wanneer u een boekingsfactuur voor een transactie maakt. |
| Reistijd en onkosten | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Het voorschotsaldo wordt niet bijgewerkt voor een onkostennota als het is goedgekeurd en regel voor regel is geboekt. |
| Reizen en onkosten | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Belastingen voor gespecificeerde intercompany-onkostennota's worden niet correct berekend. |
| Reizen en onkosten | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Extra velden met betrekking tot projecten worden weergegeven op de opnieuw ontworpen pagina **Intercompany-onkostennota's**. |
| Reizen en onkosten | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Er verschijnt een onjuiste foutmelding op de kopteksten van onkostennota's. |
| Reizen en onkosten | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Een onkostennota wordt onjuist geboekt in een intercompany-scenario als de btw wordt geboekt naar de rechtspersoon van bestemming. |
| Reizen en onkosten | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Indieningsdatums van nota's worden niet afgedrukt op goedgekeurde onkostennota's. |
| Reizen en onkosten | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | De velden **Datum goedgekeurd** en **Datum afgewezen** worden niet ingevuld nadat een uitgave is goedgekeurd. |
| Reizen en onkosten | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Een reisaanvraag die voor de ene werknemer is gemaakt, kan worden gebruikt voor de onkostennota van een andere werknemer. |
| Reizen en onkosten | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Onkostencategorieën zijn vergrendeld bij het toevoegen van een nieuwe onkostenregel. |
| Reizen en onkosten | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Het specificeren van al opgesplitste onkostennotaregels resulteert in een onvolledige boeking van het boekstuk Leveranciers\Grootboek en verstoort de werking van Accounting Source Explorer omdat **TRVEXPTRANS.SOURCEDOCUMENTLINE** wordt gedupliceerd. |
| Reizen en onkosten | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Het beleid voor reisaanvragen werkt niet zoals verwacht. |
| Reizen en onkosten | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | De naam van de leveranciersrekening wordt niet weergegeven op geboekte projecttransacties voor onkostennota's. |
| Reizen en onkosten | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | In Project Operations kunt u geen tijd goedkeuren met een taak voor een intercompany-project. |
| Reizen en onkosten | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | De categorie voor het retourneren van contante voorschotten werkt de saldi van contante voorschotten niet bij wanneer deze worden geboekt. |
| Reizen en onkosten | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | De verkoopprijs wordt onjuist berekend op onkostennota's die zijn gemaakt in een vreemde valuta met geïmporteerde creditcardtransacties en die aan een project zijn gekoppeld. |
| Reizen en onkosten | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | De gegevensentiteit **TrvRequisitionLine** en de bijbehorende unieke index zijn teruggedraaid. |
| Reizen en onkosten | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Er is instrumentatie toegevoegd aan de generatie van **SOURCEDOCUMENTLINE**. |
| Reizen en onkosten | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Het onjuiste subgrootboekjournaal wordt weergegeven in een intercompany-scenario als btw wordt geboekt naar de rechtspersoon van bestemming. |
| Reizen en onkosten | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | In Project Operations worden onkostenschattingen niet verwijderd uit Finance wanneer ze worden verwijderd uit Dataverse​. |
| Reizen en onkosten | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Als een onkostencategorie een niet-projectcategorie is, worden de financiële dimensies die zijn geselecteerd op de pagina **Onkosten** niet naar de onkostennota gekopieerd. |
