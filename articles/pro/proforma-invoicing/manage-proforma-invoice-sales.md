---
title: Een pro-formaprojectfactuur beheren
description: Dit onderwerp biedt informatie over het gebruik van pro-formaprojectfacturen.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 359f17fb5510b13de97d2349dcbc91d11b48e0f9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582612"
---
# <a name="manage-a-proforma-project-invoice"></a>Een pro-formaprojectfactuur beheren 

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

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

Voor een regel **Tijd- en materiaalfactuur** worden factuurregeldetails gegroepeerd in **Toerekenbaar**, **Niet-toerekenbaar** en **Gratis** op de pagina **Factuurregel**. **Toerekenbare factuurregel** details worden toegevoegd aan het totaal van de factuurregel. **Gratis** en **Niet-toerekenbare werkelijke waarden** worden niet opgeteld bij het totaal van de factuurregel.

Voor een regel **Factuur met vaste prijs** worden factuurregeldetails gemaakt op basis van mijlpalen die zijn gemarkeerd als **Gereed voor facturering** op de gerelateerde contractregel. Nadat de factuurregeldetails zijn gemaakt op basis van een mijlpaal, wordt de factureringsstatus van de mijlpaal bijgewerkt naar **Klantfactuur gemaakt**.

### <a name="edit-invoice-line-details"></a>Factuurregeldetails bewerken

De volgende velden zijn beschikbaar in factuurregeldetails die worden ondersteund door een niet-gefactureerde werkelijke verkoopwaarde:

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
| **Product selecteren** | Dit veld wordt standaard ingesteld op basis van de bron voor de werkelijke waarde en is alleen-lezen. | Wanneer u een nieuw factuurregeldetail maakt zonder een ondersteunende werkelijke waarde, kan dit veld worden bewerkt. |
| **Product** | Dit veld wordt standaard ingesteld op basis van de bron voor de werkelijke waarde en is alleen-lezen. | Wanneer u een nieuw factuurregeldetail maakt zonder een ondersteunende werkelijke waarde, kan dit veld worden bewerkt als het veld **Product selecteren** is ingesteld op **Bestaand product**​. |
| **Productnaam** | Dit veld wordt standaard ingesteld op basis van de bron voor de werkelijke waarde en is alleen-lezen. | Voor een nieuw factuurregeldetail, waar de product-id is geselecteerd uit de catalogus, wordt dit veld ingesteld op de productnaam. Voor een toe te voegen product wordt het veld ingesteld op de toe te voegen naam. |
| **Beschrijving van toe te voegen product** | Dit veld wordt standaard ingesteld op basis van de bron voor de werkelijke waarde en is alleen-lezen. | Wanneer u een nieuw factuurregeldetail maakt zonder een ondersteunende werkelijke waarde, kunt u een beschrijving voor het toe te voegen product toevoegen. |
| **Transactietype** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Wordt standaard ingesteld op **Gefactureerde verkoop** en vergrendeld bij het maken van een nieuw **Factuurregeldetail** zonder ondersteunende werkelijke waarden.  |
| **Transactieklasse** | Standaard ingesteld op basis van de werkelijke bronwaarden. Een alleen-lezen veld dat niet kan worden bewerkt. | Dit veld wordt standaard ingesteld op basis van of de gebruiker ervoor kiest om een factuurregeldetail van het type **Tijd**, **Onkosten**, **Materiaal** of **Vergoeding** te maken terwijl er ook een nieuw **factuurregeldetail** zonder een ondersteunende werkelijke waarde wordt gemaakt. Vergrendeld voor bewerking. |

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

### <a name="create-new-invoice-line-details"></a>Nieuwe factuurregeldetails maken

Op tijd- en materiaalfactuurregels kunt u nieuwe factuurregeldetails maken. Deze factuurregeldetails worden niet ondersteund door een werkelijke waarde. Op een tijd- en materiaalfactuurregel kunt u **Nieuw** selecteren om een nieuw factuurregeldetail te creëren voor de transactieklassen die op de contractregel zijn opgenomen.

## <a name="refresh-invoice-transactions"></a>Factuurtransacties vernieuwen

Als u werkelijke waarden hebt die zijn binnengekomen nadat de factuur is gemaakt, kunt u deze werkelijke waarden in de factuur opnemen.

1. In de weergave **Achterstallige facturen** markeert u de gegevens als **Gereed voor facturering**.   
2. Open het concept van de pro-formafactuur en klik op het lint **Acties** op **Factuurregeltransacties vernieuwen**.

  Hiermee worden factuurregeldetails gemaakt voor elke werkelijke waarde met een datum in het verleden en die is gemarkeerd als **Gereed voor facturering**, maar niet in de factuur is opgenomen.

## <a name="product-based-invoice-lines"></a>Productgebaseerde factuurregels

In Project Operations kunt u factuurregels maken voor producten die niet van toepassing zijn op een project of voor alle projecten, samen met projectgebaseerde factuurregels. Deze factuurregels worden gemaakt als productgebaseerde contractregels en nadat ze zijn gemarkeerd als gereed voor facturering, worden ze toegevoegd als productgebaseerde factuurregels.

Nadat u productgebaseerde factuurregels hebt toegevoegd, kunnen deze niet meer worden gewijzigd. Ze kunnen echter worden verwijderd uit het concept van de pro-formafactuur.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
