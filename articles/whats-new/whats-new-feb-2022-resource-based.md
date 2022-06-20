---
title: Nieuwe functies van februari 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit artikel biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Project Operations van februari 2022 voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932980"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies van februari 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

*Van toepassing op: Project Operations voor scenario's op basis van resources/niet-voorradige artikelen*

Dit artikel is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.28.0.120
- Projectbeheer en financiële administratie in een Dynamics 365 Finance-omgeving versie 10.0.24

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

- Vanaf deze release kunt u maximaal 300 teamleden toevoegen aan een enkel project. Voorheen bedroeg de limiet op het aantal teamleden 150. Zie [Projectlimieten](../project-management/create-wbs.md#project-limitations) voor meer informatie.

## <a name="project-operations-dual-write-map-updates"></a>Updates in toewijzing voor twee keer wegschrijven voor Project Operations

De volgende lijst toont de toewijzingen voor twee keer wegschrijven die zijn gewijzigd of toegevoegd in de release van Project Operations van februari 2022.

| Entiteitstoewijzing | Bijgewerkte versie | Opmerkingen  |
| --- | --- | --- |
| Entiteit voor exporteren van projectkosten voor Project Operations-integratie (msdyn\_expenses) | 1.0.0.3 | Uitgebreid voor synchronisatie van projectactiviteiten naar Dataverse. |

Zie [Toewijzingsversies van dubbel wegschrijven voor Project Operations](../environment/resource-dual-write-maps.md) voor de huidige lijst en versies van toewijzingen voor twee keer wegschrijven voor Project Operations.

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Sommige functies en mogelijkheden werken mogelijk niet correct als de nieuwste versie van de toewijzing niet wordt geactiveerd. U kunt de actieve versie van de kaart weergeven in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de toewijzing activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in de sectie [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) van de probleemoplossingsgids voor Twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Facturering en prijzen | 2415109 | De standaardwaarde in het veld **Betalingsvoorwaarden voor bewerkingen** moet de klantrecord van het projectcontract en het pro-formafactuurrecord zijn. |
| Facturering en prijzen | 2497369 | Materiaalcorrectie moet de datumwaarde in de parameters voor **Correctie** volgen. |
| Facturering en prijzen | 2498697 | De beveiligingsconfiguratie voor **Tijdsvermelding intrekken** is verbeterd. |
| Facturering en prijzen | 2513824 | Voor op bronnen gebaseerde scenario's mag de transactiecategorie-id niet langer dan 28 tekens zijn in Project Operations. |
| Facturering en prijzen | 2517455 | De actie **Factuurregeltransacties vernieuwen** mag niet meerdere keren tegelijk worden geactiveerd voor dezelfde factuur. |
| Facturering en prijzen | 2517465 | De actie **Factuurregeldetails deactiveren** is geblokkeerd omdat deze niet wordt ondersteund. |
| Facturering en prijzen | 2556660 | De datumeffectiviteitscontrole die wordt uitgevoerd op de prijslijst die is gekoppeld aan een record met projectparameters is hersteld. |
| Verkoopkansenbeheer | 2369202 | De bedrijfslogica is gecorrigeerd die verifieert dat prijslijsten met overlappende ingangsdatums aan hetzelfde projectcontract kunnen worden gekoppeld. |
| Verkoopkansenbeheer | 2385965 | Het gedrag op het tabblad **Klanten** van de pagina **Projectcontract** bij selectie van **Opslaan en sluiten** is gecorrigeerd. |
| Tijd en onkosten | 2538503 | Er moet een projecttaak beschikbaar zijn in de entiteit **Werkelijke projectwaarden** entiteit nadat een onkostennota is geboekt. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projectbeheer en financiële administratie in Dynamics 365 Finance

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Projectbeheer en financiële administratie | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Tijdens het importeren van creditnota's van leveranciers treedt een fout op. In de foutmelding staat: "Het ingehouden bedrag kan niet hoger zijn dan het resterende nettobedrag." |
| Projectbeheer en financiële administratie | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Als een factuurvoorstel transacties met een nulbedrag bevat die niet-gefactureerde werkelijke verkopen zijn, kan er geen facturering plaatsvinden. |
| Projectbeheer en financiële administratie | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | De geboekte kosten zijn niet correct nadat de aankoopprijs is bijgewerkt en **Wijzigingsbeheer activeren** is ingeschakeld.|
| Projectbeheer en financiële administratie | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | De boekingsraming voor een project met een vaste prijs gebruikt de onjuiste valuta en het onjuiste bedrag in het ramingsboekstuk, zelfs wanneer de functie **Valuta van projectcontract inschakelen voor ramingsberekening** is ingeschakeld. |
| Projectbeheer en financiële administratie | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** mag geen aanroep doen om het bijhouden van wijzigingen in te schakelen zonder uitzonderingen op te vangen voor entiteiten met configuratiesleutels die niet zijn ingeschakeld. |
| Projectbeheer en financiële administratie | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | De batchtaak wordt hersteld wanneer meerdere geavanceerde dagboeken worden geboekt en er een fout optreedt. |
| Reizen en onkosten | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Vanwege een afstemmingsprobleem dat verband houdt met voorschotten op onkostennota's, wordt het belastingbedrag niet gedekt als onderdeel van het voorschot. |
| Reizen en onkosten | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Btw-informatie is niet opgenomen in het rapport **Onkosten - Geboekte transacties**. |
| Reizen en onkosten | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | De schending van het onkostenbeleid **Ontvangstbewijzen vereist** toont ten onrechte een waarschuwing op onkostendeclaraties. |
| Reizen en onkosten | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Een projecttransactie omvat geen niet-terugvorderbare btw in het totale verkoopbedrag wanneer de transactie het resultaat is van kilometerkosten. |
| Reizen en onkosten | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Wanneer een gespecificeerde regel btw bevat, kunt u de datum van de gespecificeerde regel niet wijzigen en treedt er een statusfout in het brondocument op. |

## <a name="removed-and-deprecated-features"></a>Verwijderde en afgeschafte functies

In het artikel [Verwijderde of afgeschafte functies in Project Operations](removed-depreciated-features-project.md) onderwerp beschrijft functies die zijn verwijderd of afgeschaft voor Dynamics 365 Project Operations.

- Een verwijderde functie is niet langer beschikbaar in het product.
- Een afgeschafte functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Er wordt 12 maanden voordat een functie wordt verwijderd uit het product een aankondiging van afschaffing weergegeven in het artikel [Verwijderde of afgeschafte functies in Project Operations](removed-depreciated-features-project.md).

Voor wijzigingen die fouten veroorzaken en alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden. Meestal gaat het bij deze wijzigingen om functionele updates die moeten worden doorgevoerd in de compiler.
