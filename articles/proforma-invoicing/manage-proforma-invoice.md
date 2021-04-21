---
title: Een projectgebaseerde pro-formafactuur beheren
description: Dit onderwerp biedt informatie over het beheer en gebruik van projectgebaseerde pro-formafacturen.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9fd357648f8166cbcbe91ca1922739585f9fcfa9
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867215"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Een projectgebaseerde pro-formafactuur beheren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

In Dynamics 365 Project Operations worden pro-formafacturen gebruikt als een uitbreiding op de facturen in Dynamics 365 Sales. Er zijn echter veel verschillen in het facturatieproces tussen Sales en Project Operations als het gaat om facturering. Het is bijvoorbeeld niet mogelijk om een nieuwe factuur te maken vanuit de pagina **Facturenlijst** in Project Operations, maar dit is wel mogelijk in Sales. Deze verschillen en uitbreidingen zijn bedoeld om factureringsprocessen te ondersteunen voor projecten die verschillen van een typische factuur voor een verkooporder.

> [!IMPORTANT]
> Vanwege de verschillen mag u facturen in Sales en Project Operations niet door elkaar gebruiken.

## <a name="invoice-header"></a>Factuurkoptekst

De volgende informatie is beschikbaar in de koptekst van een pro-formafactuur in Project Operations.

| Veld | Locatie | Beschrijving |
| --- | --- | --- | 
| **Factuur-id** | Tabblad **Overzicht** | De id die automatisch wordt gegenereerd wanneer een pro-formafactuur wordt gemaakt. Een alleen-lezen veld dat niet kan worden bewerkt. Dit veld wordt gebruikt als referentie voor elke pro-formafactuur. |
| **Name** | Tabblad **Overzicht** | Standaard ingesteld op de naam van het projectcontract. Dit veld kan worden bewerkt. | 
| **Valuta** | Tabblad **Overzicht** | Standaard ingesteld op de valuta van het projectcontract. Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Prijslijst** | Tabblad **Overzicht** | Standaard ingesteld op de prijslijst van het projectcontract. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Verkoopkans** | Tabblad **Overzicht** | De verwijzing naar de gekoppelde verkoopkans. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Contract** | Tabblad **Overzicht** | De verwijzing naar het gekoppelde projectcontract. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Klanten** | Tabblad **Overzicht** | De verwijzing naar het gekoppelde projectcontract. Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Beschrijving** | Tabblad **Overzicht** | Het tekstveld dat de factuur beschrijft. Dit veld kan worden bewerkt. | 
| **Factureren aan** en gerelateerde velden | **Tabblad Overzicht** | De standaardwaarden worden ingesteld vanuit de projectcontractklant. Dit veld kan worden bewerkt.  | 
| **Status** | Tabblad **Overzicht** | Hier stelt u de volgende opties in: **Actief**, **Gesloten**, **Betaald** en **Geannuleerd**. Deze kunnen worden bewerkt. Niet-ondersteunde statussen voor Project Operations omvatten **Gesloten** en **Geannuleerd**. </br> De status is ingesteld op **Actief** wanneer de factuur wordt gemaakt. </br>De status moet pas worden ingesteld op **Betaald** nadat de factuur is bevestigd.  | 
| **Status van projectfactuur** | Tabblad **Overzicht** | Hier stelt u de volgende opties in: **Concept**, **Wordt geëvalueerd** en **Bevestigd**. Deze kunnen worden bewerkt. In de statussen **Concept** en **Wordt geëvalueerd** kan de factuur worden bewerkt. De factuur kan niet worden gewijzigd nadat deze is bevestigd. | 
| **Gedetailleerd bedrag** | Tabblad **Overzicht** | De som van bedragen op alle factuurregels na aftrek van voorschotten en inhoudingen. Een alleen-lezen veld dat niet kan worden bewerkt.  Dit veld wordt gebruikt om het uiteindelijke bedrag te berekenen. | 
| **Korting (%)** | Tabblad **Overzicht** | Dit veld kan worden bewerkt om een kortingspercentage in te voeren. Dit veld wordt niet ondersteund door de functionaliteit van Project Operations. Dit veld wordt niet ondersteund.|  
| **Kortingsbedrag** | Tabblad **Overzicht** | Dit veld kan worden bewerkt om het kortingsbedrag in te voeren. Dit veld wordt niet ondersteund door de functionaliteit van Project Operations. Dit veld wordt niet ondersteund. |  
| **Bedrag vóór vracht** | **Tabblad Overzicht** | Het totale factuurbedrag nadat kortingen zijn toegepast. Een alleen-lezen veld dat niet kan worden bewerkt. Dit veld wordt gebruikt om het uiteindelijke bedrag te berekenen.  | 
| **Vrachtkosten** | Tabblad **Overzicht** | Dit veld kan worden bewerkt om het vrachtbedrag in te voeren. Dit veld wordt niet ondersteund door de functionaliteit van Project Operations. Dit veld wordt niet ondersteund. |
| **Totaal belastingen** | Tabblad **Overzicht** | De totale belasting van alle factuurregels op de factuur. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Totaalbedrag** | Tabblad **Overzicht** | De som van het bedrag na kortingen en belastingen. De som is het bedrag dat de klant moet betalen. | 

## <a name="project-based-invoice-lines"></a>Projectgebaseerde factuurregels

In Project Operations is er altijd één factuurregel voor elke projectcontractregel. De factuurregel wordt gemaakt, zelfs als er geen werkelijke waarden zijn. De volgende informatie is beschikbaar in een pro-formafactuurregel.

| Veld | Locatie | Beschrijving | 
| --- | --- | --- |
| **Factuur-id** | Tabblad **Algemeen** | De verwijzing naar de factuur-id. Een alleen-lezen veld dat niet kan worden bewerkt. De koppeling naar de factuur-id kan worden gebruikt om terug te navigeren naar de factuurkoptekst. | 
| **Name** | Tabblad **Algemeen** | De naam van de factuurregel die standaard wordt ingesteld op basis van de contractregelnaam. Dit veld kan worden bewerkt. |
| **Project** | Tabblad **Algemeen** | Het project op de gerelateerde projectcontractregel. Een alleen-lezen veld dat niet kan worden bewerkt. De projectkoppeling kan worden gebruikt om naar het project te navigeren. | 
| **Factureringsmethode** | Tabblad **Algemeen** | De factureringsmethode op de gerelateerde projectcontractregel. Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Bedrag contractregel** | Tabblad **Algemeen** | Het contractbedrag op de gerelateerde projectcontractregel. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Tot op heden gefactureerd** | Tabblad **Algemeen** | De som van de bedragen op alle factuurregeldetails van deze factuur. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Bedrag** | Tabblad **Algemeen** | De som van de bedragen op alle toerekenbare factuurregeldetails van deze factuur. Een alleen-lezen veld dat niet kan worden bewerkt. Dit veld wordt gebruikt om het uiteindelijke bedrag op de factuurkoptekst te berekenen. | 
| **Belastingen** | Tabblad **Algemeen** | De som van de belastingbedragen op alle factuurregeldetails van deze factuurregel. Een alleen-lezen veld dat niet kan worden bewerkt. Dit veld wordt gebruikt om het uiteindelijke belastingbedrag op de factuurkoptekst te berekenen. | 
| **Berekend bedrag** | Tabblad **Algemeen** | De som van de totale bedragen (**Belasting + bedragen**) op alle toerekenbare factuurregeldetails van deze factuurregel. Een alleen-lezen veld dat niet kan worden bewerkt. Dit veld wordt gebruikt om het uiteindelijke bedrag op de factuurkoptekst te berekenen. |

## <a name="invoice-line-details"></a>Factuurregeldetails

Elke factuurregel in een projectfactuur bevat factuurregeldetails. Deze regeldetails zijn gerelateerd aan de niet-gefactureerde werkelijke verkoopcijfers en mijlpalen die betrekking hebben op de contractregel waarnaar wordt verwezen door de factuurregel. Al deze transacties zijn gemarkeerd **Gereed voor facturering**.

Voor een regel **Tijd- en materiaalfactuur** worden factuurregeldetails gegroepeerd in **Toerekenbaar**, **Niet-toerekenbaar** en **Gratis** op de pagina **Factuurregel**. **Toerekenbare factuurregel** details worden toegevoegd aan het totaal van de factuurregel. **Gratis** en **Niet-toerekenbare werkelijke waarden** worden niet toegevoegd aan het totaal van de factuurregel.

Voor een regel **Factuur met vaste prijs** worden factuurregeldetails gemaakt op basis van mijlpalen die zijn gemarkeerd als **Gereed voor facturering** op de gerelateerde contractregel. Nadat de factuurregeldetails zijn gemaakt op basis van een mijlpaal, wordt de factureringsstatus van de mijlpaal bijgewerkt naar **Klantfactuur gemaakt**.

### <a name="edit-invoice-line-details"></a>Factuurregeldetails bewerken

De volgende velden zijn beschikbaar in factuurregeldetails die worden ondersteund door een niet-gefactureerde werkelijke verkoopwaarde.

| Veld | Beschrijving |
| --- | --- | 
| **Factuurregel** | Een verwijzing naar de **Factuurregel-id**. Dit veld is alleen-lezen en vergrendeld voor bewerking. Deze koppeling naar de factuur-id kan worden gebruikt om terug te navigeren naar de factuurkoptekst. | 
| **Beschrijving** | Een beschrijving van de factuurregeldetails. Standaard ingesteld op basis van het veld **Interne opmerkingen** in **Tijdsvermelding** en het veld **Omschrijving** in **Onkostenpost**. Het veld kan worden bewerkt.| 
| **Externe beschrijving** | Een beschrijving van de factuurregeldetails. Standaard ingesteld op basis van het veld **Externe opmerkingen** in **Tijdsvermelding** en het veld **Omschrijving** in **Onkostenpost**. Het veld kan worden bewerkt. Deze beschrijving kan worden gebruikt om te bepalen wat er op de afgedrukte factuur moet staan die naar de klant wordt gestuurd. In Project Operations heeft een pro-formafactuur niet alle vereiste functionaliteit om afdrukinstellingen voor een factuur te configureren. | 
| **Begindatum** | Dit is een alleen-lezen veld dat standaard wordt ingesteld op basis van de bron voor de werkelijke waarde. |
| **Project** | Dit is een alleen-lezen veld dat standaard wordt ingesteld op basis van de bron van de werkelijke waarde voor het project op de gerelateerde contractregel. |  
| **Opdracht** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Transactiecategorie** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **- Rol** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. |  
| **Boekbare resource** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Bedrijf voor resources** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Resource-eenheid** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Aantal** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. |  
| **Eenheidsplanning** | Voor factuurregeldetails voor tijd is dit altijd ingesteld op tijd en kan dit niet worden bewerkt. Voor onkosten wordt dit standaard ingesteld op basis van de werkelijke brononkosten. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Eenheid** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. |  
| **Prijs** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Valuta** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Bedrag:** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Belastingen** | Standaard ingesteld op basis van de werkelijke bronwaarden. Het veld kan worden bewerkt.| 
| **Berekend bedrag** | Een berekend veld, berekend als **Bedrag + belasting**. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Factureringstype** | Standaard ingesteld op basis van de werkelijke bronwaarden. Het veld kan worden bewerkt. Als u **Toerekenbaar** selecteert, wordt de regel toegevoegd aan het totaal van de factuurregel. Met de opties **Gratis** en **Niet-toerekenbaar** wordt deze uitgesloten van het totaal van de factuurregel.| 
| **Product selecteren** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Product** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Productnaam** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. |  
| **Beschrijving van toe te voegen product** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Transactietype** | Dit is een alleen-lezen veld dat standaard wordt ingesteld op basis van de bron voor de werkelijke waarde voor **Gefactureerde verkoop**. |  
| **Transactieklasse** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | 

De volgende velden zijn beschikbaar in factuurregeldetails die worden ondersteund door een mijlpaal.

| Veld | Beschrijving |
| --- | --- | 
| **Factuurregel** | Verwijzing naar de **Factuurregel-id**. Een alleen-lezen veld dat niet kan worden bewerkt. De koppeling naar de factuur-id kan worden gebruikt om terug te navigeren naar de factuurkoptekst.  | 
| **Beschrijving** | Beschrijving van de factuurregeldetails. Standaard ingesteld op basis van de beschrijving van de bronmijlpaal. | 
|**Externe beschrijving** | Beschrijving van de factuurregeldetails die standaard worden ingesteld op basis van de beschrijving van de bronmijlpaal. Dit veld kan worden gebruikt om te bepalen wat er op de afgedrukte factuur moet staan die naar de klant wordt gestuurd. In Project Operations heeft een pro-formafactuur niet alle vereiste functionaliteit om afdrukinstellingen voor een factuur te configureren. | 
| **Begindatum** | Standaard ingesteld op basis van de datum van de **bronmijlpaal**. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Project** | Standaard ingesteld op basis van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Taak** | Standaard ingesteld op basis van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Transactiecategorie** | Een alleen-lezen veld dat niet kan worden bewerkt. |
| **- Rol** | Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Boekbare resource** | Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Resource-eenheid** | Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Eenheidsplanning** | Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Eenheid** | Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Prijs** | Standaard ingesteld op basis van het bedrag van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Valuta** | Standaard ingesteld op basis van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Bedrag** | Standaard ingesteld op basis van het bedrag van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Belastingen** | Standaard ingesteld op basis van het belastingbedrag van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Berekend bedrag** | Standaard ingesteld op basis van het berekende bedrag van de bronmijlpaal. Het veld kan worden bewerkt. | 
| **Factureringstype** | Standaard altijd ingesteld op **Toerekenbaar**. Een alleen-lezen veld dat niet kan worden bewerkt. |
| **Transactietype** | Standaard ingesteld op basis van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. | 
| **Transactieklasse** | Standaard ingesteld op basis van de bronmijlpaal. Een alleen-lezen veld dat niet kan worden bewerkt. | 

## <a name="refresh-invoice-transactions"></a>Factuurtransacties vernieuwen

Als u werkelijke waarden hebt die zijn binnengekomen nadat de factuur is gemaakt, kunt u deze werkelijke waarden in de factuur opnemen.

1. In de weergave **Achterstallige facturen** markeert u de gegevens als **Gereed voor facturering**.   
2. Open het concept van de pro-formafactuur en selecteer op het lint **Acties** de optie **Factuurregeltransacties vernieuwen**​.

  Er worden factuurregeldetails gemaakt voor elke werkelijke waarde met een datum in het verleden en de markering **Gereed voor facturering**, maar die niet is opgenomen op de factuur.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
