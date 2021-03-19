---
title: Een pro-formafactuur beheren
description: Dit onderwerp bevat informatie over het beheren en werken met pro-formafacturen.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29e301062f8f3ba955a95953bc2e891f3acaf765
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287682"
---
# <a name="manage-a-proforma-invoice"></a>Een pro-formafactuur beheren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

In Dynamics 365 Project Operations worden pro-formafacturen gebruikt als een uitbreiding op de facturen in Dynamics 365 Sales. Er zijn echter veel verschillen in het facturatieproces tussen Sales en Project Operations als het gaat om facturering. Het is bijvoorbeeld niet mogelijk om een nieuwe factuur te maken vanuit de pagina **Facturenlijst** in Project Operations, maar dit is wel mogelijk in Sales. Deze verschillen en uitbreidingen zijn bedoeld om factureringsprocessen te ondersteunen voor projecten die verschillen van een typische factuur voor een verkooporder.

> [!IMPORTANT]
> Vanwege de verschillen mag u facturen in Sales en Project Operations niet door elkaar gebruiken.

## <a name="invoice-header"></a>Factuurkoptekst

De volgende informatie is beschikbaar in de koptekst van een pro-formafactuur in Project Operations.

| Veld | Locatie | Beschrijving | Downstreamimpact |
| --- | --- | --- | --- |
| **Factuur-id** | Tabblad **Overzicht** | De id die automatisch wordt gegenereerd wanneer een pro-formafactuur wordt gemaakt. Een alleen-lezen veld dat niet kan worden bewerkt. | Dit veld wordt gebruikt als referentie voor elke pro-formafactuur. |
| **Name** | Tabblad **Overzicht** | Standaard ingesteld op de naam van het projectcontract. Dit veld kan door de gebruiker worden bewerkt. | &nbsp;  |
| **Valuta** | Tabblad **Overzicht** | Standaard ingesteld op de valuta van het projectcontract. Een alleen-lezen veld dat niet kan worden bewerkt. |&nbsp; |
| **Prijslijst** | Tabblad **Overzicht** | Standaard ingesteld op de prijslijst van het projectcontract. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Verkoopkans** | Tabblad **Overzicht** | De verwijzing naar de gekoppelde verkoopkans. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp;  |
| **Contract** | Tabblad **Overzicht** | De verwijzing naar het gekoppelde projectcontract. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Klanten** | Tabblad **Overzicht** | De verwijzing naar het gekoppelde projectcontract. Een alleen-lezen veld dat niet kan worden bewerkt. |&nbsp;  |
| **Beschrijving** | Tabblad **Overzicht** | Het tekstveld dat de factuur beschrijft. Dit veld kan door de gebruiker worden bewerkt. | &nbsp; |
| **Factureren aan** en gerelateerde velden | **Tabblad Overzicht** | De standaardwaarden worden ingesteld vanuit de projectcontractklant. Dit veld kan door de gebruiker worden bewerkt.  | &nbsp; |
| **Status** | Tabblad **Overzicht** | Hier worden de volgende opties ingesteld: **Actief**, **Gesloten**, **Betaald** en **Geannuleerd** die door de gebruiker kunnen worden bewerkt. | Niet-ondersteunde statussen voor Project Operations omvatten **Gesloten** en **Geannuleerd**. </br> De status is ingesteld op **Actief** wanneer de factuur wordt gemaakt. </br>De status moet pas worden ingesteld op **Betaald** nadat de factuur is bevestigd. |
| **Status van projectfactuur** | Tabblad **Overzicht** | Hier worden de volgende opties ingesteld: **Concept**, **Wordt geëvalueerd** en **Bevestigd** die door de gebruiker kunnen worden bewerkt. | In de statussen **Concept** en **Wordt geëvalueerd** kan de factuur worden bewerkt. De factuur kan niet worden gewijzigd nadat deze is bevestigd. |
| **Gedetailleerd bedrag** | Tabblad **Overzicht** | De som van bedragen op alle factuurregels na aftrek van voorschotten en inhoudingen. Een alleen-lezen veld dat niet kan worden bewerkt. | Dit veld wordt gebruikt om het uiteindelijke bedrag te berekenen. |
| **Korting (%)** | Tabblad **Overzicht** | Dit veld kan worden bewerkt om een kortingspercentage in te voeren. Dit veld wordt niet ondersteund door de functionaliteit van Project Operations. | Dit veld wordt niet ondersteund. |
| **Kortingsbedrag** | Tabblad **Overzicht** | Dit veld kan worden bewerkt om het kortingsbedrag in te voeren. Dit veld wordt niet ondersteund door de functionaliteit van Project Operations. | Dit veld wordt niet ondersteund. |
| **Bedrag vóór vracht** | **Tabblad Overzicht** | Het totale factuurbedrag nadat kortingen zijn toegepast. Een alleen-lezen veld dat niet kan worden bewerkt. | Dit veld wordt gebruikt om het uiteindelijke bedrag te berekenen. |
| **Vrachtkosten** | Tabblad **Overzicht** | Dit veld kan worden bewerkt om het vrachtbedrag in te voeren. Dit veld wordt niet ondersteund door de functionaliteit van Project Operations. | Dit veld wordt niet ondersteund. |
| **Totaal belastingen** | Tabblad **Overzicht** | De totale belasting van alle factuurregels op de factuur. Een alleen-lezen veld dat niet kan worden bewerkt. | Geen. |
| **Totaalbedrag** | Tabblad **Overzicht** | De som van het bedrag na kortingen en belastingen. | De som is het bedrag dat de klant moet betalen. |

## <a name="project-based-invoice-lines"></a>Projectgebaseerde factuurregels

In Project Operations is er altijd één factuurregel voor elke projectcontractregel. De factuurregel wordt gemaakt, zelfs als er geen werkelijke waarden zijn. De volgende informatie is beschikbaar in een pro-formafactuurregel.

| Veld | Locatie | Beschrijving | Downstreamimpact |
| --- | --- | --- | --- |
| **Factuur-id** | Tabblad **Algemeen** | De verwijzing naar de factuur-id. Een alleen-lezen veld dat niet kan worden bewerkt. | De koppeling naar de factuur-id kan worden gebruikt om terug te navigeren naar de factuurkoptekst. |
| **Name** | Tabblad **Algemeen** | De naam van de factuurregel die standaard wordt ingesteld op basis van de contractregelnaam. Dit veld kan door de gebruiker worden bewerkt. | &nbsp; |
| **Project** | Tabblad **Algemeen** | Het project op de gerelateerde projectcontractregel. Een alleen-lezen veld dat niet kan worden bewerkt. | De projectkoppeling kan worden gebruikt om naar het project te navigeren. |
| **Factureringsmethode** | Tabblad **Algemeen** | De factureringsmethode op de gerelateerde projectcontractregel. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Bedrag contractregel** | Tabblad **Algemeen** | Het contractbedrag op de gerelateerde projectcontractregel. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Tot op heden gefactureerd** | Tabblad **Algemeen** | De som van de bedragen op alle factuurregeldetails van deze factuur. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Bedrag** | Tabblad **Algemeen** | De som van de bedragen op alle toerekenbare factuurregeldetails van deze factuur. Een alleen-lezen veld dat niet kan worden bewerkt. | Dit veld wordt gebruikt om het uiteindelijke bedrag op de factuurkoptekst te berekenen. |
| **Belastingen** | Tabblad **Algemeen** | De som van de belastingbedragen op alle factuurregeldetails van deze factuurregel. Een alleen-lezen veld dat niet kan worden bewerkt. | Dit veld wordt gebruikt om het uiteindelijke belastingbedrag op de factuurkoptekst te berekenen. |
| **Berekend bedrag** | Tabblad **Algemeen** | De som van de totale bedragen (**Belasting + bedragen**) op alle toerekenbare factuurregeldetails van deze factuurregel. Een alleen-lezen veld dat niet kan worden bewerkt. | Dit veld wordt gebruikt om het uiteindelijke bedrag op de factuurkoptekst te berekenen. |

## <a name="invoice-line-details"></a>Factuurregeldetails

Elke factuurregel in een projectfactuur bevat factuurregeldetails. Deze regeldetails zijn gerelateerd aan de niet-gefactureerde werkelijke verkoopcijfers en mijlpalen die betrekking hebben op de contractregel waarnaar wordt verwezen door de factuurregel. Al deze transacties zijn gemarkeerd **Gereed voor facturering**.

Voor de regel **Tijd- en materiaalfactuur** worden factuurregeldetails gegroepeerd in **Toerekenbaar**, **Niet-toerekenbaar** en **Gratis** op de pagina **Factuurregel**. **Toerekenbare factuurregel** details worden toegevoegd aan het totaal van de factuurregel. **Gratis** en **Niet-toerekenbare werkelijke waarden** worden niet toegevoegd aan het totaal van de factuurregel.

Voor de regel **Factuur met vaste prijs** worden factuurregeldetails gemaakt op basis van mijlpalen die zijn gemarkeerd als **Gereed voor facturering** op de gerelateerde contractregel. Nadat de factuurregeldetails zijn gemaakt op basis van een mijlpaal, wordt de factureringsstatus van de mijlpaal bijgewerkt naar **Klantfactuur gemaakt**.

### <a name="edit-invoice-line-details"></a>Factuurregeldetails bewerken

De volgende velden zijn beschikbaar in factuurregeldetails die worden ondersteund door een niet-gefactureerde werkelijke verkoopwaarde.

| Veld | Beschrijving | Downstreamimpact |
| --- | --- | --- |
| **Factuurregel** | Een verwijzing naar de **Factuurregel-id**. Alleen-lezenveld dat niet kan worden bewerkt. | Deze koppeling naar de factuur-id kan worden gebruikt om terug te navigeren naar de factuurkoptekst. |
| **Beschrijving** | Een beschrijving van de factuurregeldetails. Standaard ingesteld op basis van het veld **Interne opmerkingen** in **Tijdsvermelding** en het veld **Omschrijving** in **Onkostenpost**. Het veld kan door de gebruiker worden bewerkt.| &nbsp; |
| **Externe beschrijving** | Een beschrijving van de factuurregeldetails. Standaard ingesteld op basis van het veld **Externe opmerkingen** in **Tijdsvermelding** en het veld **Omschrijving** in **Onkostenpost**. Het veld kan door de gebruiker worden bewerkt. | Deze beschrijving kan worden gebruikt om te bepalen wat er op de afgedrukte factuur moet staan die naar de klant wordt gestuurd. In Project Operations heeft een pro-formafactuur niet alle vereiste functionaliteit om afdrukinstellingen voor een factuur te configureren. |
| **Begindatum** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Dit veld kan worden bewerkt in een nieuw factuurregeldetail dat niet wordt ondersteund door werkelijke bronwaarden. |
| **Project** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Standaard ingesteld op het project op de gerelateerde contractregel. |
| **Taak** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Het veld kan worden bewerkt in een nieuw factuurregeldetail dat niet wordt ondersteund door werkelijke bronwaarden. Een vervolgkeuzelijst toont alle taken die zijn gekoppeld aan de gerelateerde projectcontractregel.  |
| **Transactiecategorie** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Het veld kan worden bewerkt in een nieuw factuurregeldetail dat niet wordt ondersteund door werkelijke bronwaarden. |
| **- Rol** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Het veld kan worden bewerkt in een nieuw factuurregeldetail dat niet wordt ondersteund door werkelijke bronwaarden. |
| **Boekbare resource** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Het veld kan worden bewerkt in een nieuw factuurregeldetail dat niet wordt ondersteund door werkelijke bronwaarden. |
| **Bedrijf voor resources** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Het veld kan worden bewerkt in een nieuw factuurregeldetail dat niet wordt ondersteund door werkelijke bronwaarden. |
| **Resource-eenheid** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Het veld kan worden bewerkt in een nieuw factuurregeldetail dat niet wordt ondersteund door werkelijke bronwaarden. |
| **Hoeveelheid** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Het veld kan worden bewerkt in een nieuw factuurregeldetail dat niet wordt ondersteund door werkelijke bronwaarden. |
| **Eenheidsplanning** | Voor factuurregeldetails voor tijd is dit altijd ingesteld op tijd en kan dit niet worden bewerkt. Voor onkosten wordt dit standaard ingesteld op basis van de werkelijke brononkosten. Een alleen-lezen veld dat niet kan worden bewerkt. | Standaard ingesteld op **Tijd** in een nieuw factuurregeldetail dat niet wordt ondersteund door een werkelijke waarde. |
| **Eenheid** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Het veld kan worden bewerkt in een nieuw factuurregeldetail dat niet wordt ondersteund door werkelijke bronwaarden |
| **Prijs** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Het veld kan worden bewerkt in een nieuw factuurregeldetail dat niet wordt ondersteund door werkelijke bronwaarden. Als er geen waarde wordt ingevoerd, wordt dit standaard ingesteld na **Opslaan**. |
| **Valuta** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Standaard ingesteld op basis van de factuurkoptekst bij het maken van een nieuw factuurdetail zonder ondersteunende werkelijke waarden.  Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Bedrag** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Berekend als **Hoeveelheid \* Prijs** bij het maken van een nieuw factuurdetail zonder ondersteunende werkelijke waarden. Het wordt berekend na **Opslaan**. Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Belastingen** | Standaard ingesteld op basis van de werkelijke bronwaarden. Het veld kan door de gebruiker worden bewerkt | Het veld kan door de gebruiker worden bewerkt bij het maken van een nieuw factuurregeldetail zonder ondersteunende werkelijke waarden. |
| **Berekend bedrag** | Een berekend veld, berekend als **Bedrag + belasting**. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Factureringstype** | Standaard ingesteld op basis van de werkelijke bronwaarden. Het veld kan door de gebruiker worden bewerkt. | Als u **Toerekenbaar** selecteert, wordt de regel toegevoegd aan het totaal van de factuurregel. Met de opties **Gratis** en **Niet-toerekenbaar** wordt deze uitgesloten van het totaal van de factuurregel. |
| **Transactietype** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Wordt standaard ingesteld op **Gefactureerde verkoop** en vergrendeld bij het maken van een nieuw **Factuurregeldetail** zonder ondersteunende werkelijke waarden.  |
| **Transactieklasse** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Wordt standaard ingesteld als de gebruiker kiest om een factuurregeldetail voor **Tijd**, **Onkosten** of **Vergoeding** te maken waarbij ook een nieuw **Factuurregeldetail** wordt gemaakt zonder ondersteunende werkelijke waarden. Vergrendeld voor bewerking. |

De volgende velden zijn beschikbaar in factuurregeldetails die worden ondersteund door een mijlpaal:

| Veld | Beschrijving | Downstreamimpact |
| --- | --- | --- |
| **Factuurregel** | Verwijzing naar de **Factuurregel-id**. Een alleen-lezen veld dat niet kan worden bewerkt. | De koppeling naar de factuur-id kan worden gebruikt om terug te navigeren naar de factuurkoptekst. |
| **Beschrijving** | Beschrijving van de factuurregeldetails. Standaard ingesteld op basis van de beschrijving van de bronmijlpaal. | &nbsp; |
|**Externe beschrijving** | Beschrijving van de factuurregeldetails die standaard worden ingesteld op basis van de beschrijving van de bronmijlpaal. | Dit veld kan worden gebruikt om te bepalen wat er op de afgedrukte factuur moet staan die naar de klant wordt gestuurd. In Project Operations heeft een pro-formafactuur niet alle vereiste functionaliteit om afdrukinstellingen voor een factuur te configureren. |
| **Begindatum** | Standaard ingesteld op basis van de datum van de **bronmijlpaal**. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Project** | Standaard ingesteld op basis van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Taak** | Standaard ingesteld op basis van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Transactiecategorie** | Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **- Rol** | Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Boekbare resource** | Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Resource-eenheid** | Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Eenheidsplanning** | Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Eenheid** | Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Prijs** | Standaard ingesteld op basis van het bedrag van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Valuta** | Standaard ingesteld op basis van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. |&nbsp; |
| **Bedrag** | Standaard ingesteld op basis van het bedrag van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Belastingen** | Standaard ingesteld op basis van het belastingbedrag van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Berekend bedrag** | Standaard ingesteld op basis van het berekende bedrag van de bronmijlpaal. Het veld kan door de gebruiker worden bewerkt | &nbsp; |
| **Factureringstype** | Standaard altijd ingesteld op **Toerekenbaar**. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Transactietype** | Standaard ingesteld op basis van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |
| **Transactieklasse** | Standaard ingesteld op basis van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. | &nbsp; |

## <a name="refresh-invoice-transactions"></a>Factuurtransacties vernieuwen

Als u werkelijke waarden hebt die zijn binnengekomen nadat de factuur is gemaakt, kunt u deze werkelijke waarden in de factuur opnemen.

1. In de weergave **Achterstallige facturen** markeert u de gegevens als **Gereed voor facturering**.   
2. Open het concept van de pro-formafactuur en klik op het lint **Acties** op **Factuurregeltransacties vernieuwen**.

  Hiermee worden factuurregeldetails gemaakt voor elke werkelijke waarde met een datum in het verleden en die is gemarkeerd als **Gereed voor facturering**, maar niet in de factuur is opgenomen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]