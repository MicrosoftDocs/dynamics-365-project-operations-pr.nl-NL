---
title: Nieuw in mei 2021 - lite-implementatie van Project Operations
description: Dit onderwerp biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de mei 2021-release van de lite-implementatie van Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6fb1955e2adb8562ac00a90880bf8e147bf5ed6a
ms.sourcegitcommit: 18bb56676999dbde1cf880239847ee9c2b216fe4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6060427"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Nieuw in mei 2021 - lite-implementatie van Project Operations

_Van toepassing op: Lite-implementatie - van deal tot pro-formafacturering_

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

   - Project Operations in Dataverse-omgeving, versie 4.10.0.186.

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

In deze versie zijn de volgende functies opgenomen:

- [Planningsmodi](../../project-management/scheduling-modes.md): projectmanagers kunnen nu bepalen of een project moet worden beheerd met de planningsmodus voor vaste duur, vast werk of vaste eenheden.

## <a name="quality-updates"></a>Kwaliteitsupdates

| **Functiegebied** | **Referentienummer** | **Kwaliteitsupdate** |
| --- | --- | --- |
| Facturering en prijzen | 2224568 | Logica toegevoegd om aanpassingen mogelijk te maken waarbij de invoegtoepassing voor factuurbevestiging wordt aangeroepen. |
| Facturering en prijzen | 2101098 | Verbeterde logica van standaardvelden voor pro-formafactuur. Deze velden bevatten **Factuuradres**, **Naam voor factuur** en **Betalingsvoorwaarden**. De velden komen nu standaard uit de corresponderende klantrecord van het projectcontract. |
| Facturering en prijzen | 2021413 | De velden **Werkelijke kosten** en **Verkoop** in de entiteit **Taak** zijn bijgewerkt om verkoopwaarden van niet-gefactureerde en gefactureerde uitgaven voor taken op te nemen. |
| Facturering en prijzen | 2182110 | Bij het kopiëren van een projectcontract wordt de contractregel-id opnieuw gegenereerd in het doelprojectcontract om ervoor te zorgen dat het uniek is. |
| Verkoopkansenbeheer | 2186741 | Validaties toegevoegd om ervoor te zorgen dat het veld **Oorsprong** en het transactietype niet kunnen worden bijgewerkt voor bestaande prijsopgaveregeldetails. |
| Verkoopkansenbeheer | 2191353 | Mijlpalen mogen niet worden gemaakt op een contractregel voor tijd en materiaal. |
| Verkoopkansenbeheer | 2216956 | Problemen met **Prijzen**​ zijn opgelost. |
| Planning en tracering | 2182979 | De functie Project kopiëren is verbeterd om ervoor te zorgen dat de kostenschattingsregels worden gekopieerd uit het oorspronkelijke project. |
| Planning en tracering | 2184144 | De functie Project kopiëren is verbeterd om ervoor te zorgen dat de naam van de resourcepositie wordt gekopieerd uit het oorspronkelijke project. |
| Planning en tracering | 2184799 | De controle bij het kopiëren van een project is verscherpt om ervoor te zorgen dat de geschatte begindatum niet kan worden gewijzigd tijdens het kopiëren. |
| Planning en tracering | 2185134 | Tijdens het kopiëren van een project wordt de geschatte begindatum van het doelproject ingesteld op de datum van vandaag. |
| Planning en tracering | 2196373 | Bij het kopiëren van een project moet u ervoor zorgen dat de records van de projectmanager en het teamlid niet worden gedupliceerd in het projectteam. |
| Planning en tracering | 2211833 | Resourcetoewijzingen worden gekopieerd van de bronprojecttaak naar het doelproject. |
| Planning en tracering | 2186541 | Problemen in het raster **Schattingen** bij het groeperen op **Resource** zijn opgelost. |
| Planning en tracering | 2166906 | De transactiecategorie van een taak moet worden gekopieerd naar de entiteit **Resourcetoewijzing**. |
| Resourcebeheer | 2125362 | Problemen met het maken van een algemeen teamlid met de op uren gebaseerde toewijzingsmethode zijn opgelost. |
| Tijd en onkosten | 2113603 | Oplossing voor het aanpassingsprobleem met het verwijderen van kenmerken van de pagina **Tijdsvermelding**. Er wordt nu gecontroleerd of het kenmerk op de pagina bestaat voordat het met een script wordt geopend. |
| Tijd en onkosten | 2204377 | Gekopieerde urenstaten moeten automatisch worden weergegeven wanneer u **Week kopiëren** selecteert. |
| Tijd en onkosten | 2209059 | Het veld **Status** kan worden bewerkt voor Dynamics 365 Field Service-tijdsvermeldingen. |
