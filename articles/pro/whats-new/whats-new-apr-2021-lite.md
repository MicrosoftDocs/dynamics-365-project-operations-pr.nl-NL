---
title: Nieuw in april 2021 - lite-implementatie van Project Operations
description: Deze onderwerp biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de april 2021-release van de lite-implementatie van Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 10d9498636d8c5f72b7544be4ec30f399d5e0311
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598114"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Nieuw in april 2021 - lite-implementatie van Project Operations

_Van toepassing op: Lite-implementatie - van deal tot pro-formafacturering_

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

  - Project Operations in Dataverse-omgeving, versie 4.9.0.221 

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

In deze versie zijn de volgende functies opgenomen:

- Niet-voorradige materialen voor projecten. De belangrijkste mogelijkheden zijn onder meer:
  - Schatten en prijzen van niet-voorradige materialen tijdens de verkoopcyclus voor een project. Zie voor meer informatie [Kosten- en verkooptarieven voor catalogusproducten instellen - lite](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Het gebruik van niet-voorradige materialen volgen tijdens de levering van het project. Zie [Materiaalgebruik voor projecten en projecttaken registreren](../../material/material-usage-log.md) voor meer informatie.
  - Facturering van gebruikte niet-voorradige materiaalkosten. Zie [Achterstallige facturen beheren - lite](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog) voor meer informatie.
  - Met nieuwe API's in Dynamics 365 Dataverse kunnen bewerkingen voor maken, bijwerken en verwijderen worden uitgevoerd met **planningsentiteiten**. Zie [Plannings-API's gebruiken om bewerkingen uit te voeren met planningsentiteiten](../../project-management/schedule-api-preview.md) voor meer informatie.

## <a name="quality-updates"></a>Kwaliteitsupdates

| **Functiegebied** | **Referentienummer** | **Kwaliteitsupdate** |
| --- | --- | --- |
| Facturering en prijzen | 2224568 | Logica toegevoegd om aanpassingen mogelijk te maken waarbij de invoegtoepassing voor factuurbevestiging wordt aangeroepen. |
| Facturering en prijzen | 2101098 | Verbeterde logica van standaardvelden naar pro-formafactuur: **Factuuradres**, **Naam voor factuur** en **Betalingsvoorwaarden** worden nu standaard uit het corresponderende klantrecord van het projectcontract gehaald. |
| Facturering en prijzen | 2021413 | De velden **Werkelijke kosten** en **Verkoop** in de entiteit **Taak** zijn bijgewerkt om verkoopwaarden van niet-gefactureerde en gefactureerde uitgaven voor taken op te nemen. |
| Facturering en prijzen | 2182110 | Bij het kopiëren van een projectcontract wordt de contractregel-id opnieuw gegenereerd in het doelprojectcontract om ervoor te zorgen dat het uniek is. |
| Verkoopkansenbeheer | 2186741 | Validaties toegevoegd om ervoor te zorgen dat het veld **Oorsprong** en **Transactietype** niet kunnen worden bijgewerkt voor bestaande prijsopgaveregeldetails. |
| Verkoopkansenbeheer | 2191353 | Mijlpalen mogen niet worden gemaakt op een contractregel voor tijd en materiaal. |
| Verkoopkansenbeheer | 2216956 | Problemen met **Prijzen bijwerken** zijn opgelost. |
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
