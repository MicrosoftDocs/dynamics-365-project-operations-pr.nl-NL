---
title: Meerdere klanten in projectgebaseerde contractregels beheren
description: Dit onderwerp bevat informatie over het werken met contractregels en contracten die meerdere klanten bevatten.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 71081775ab45167bc1bff1979f7856a2a2a91385
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181896"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Meerdere klanten in projectgebaseerde contractregels beheren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Projectgebaseerde contractregels kunnen een lijst met klanten bevatten die verantwoordelijk zijn voor betaling. Deze lijst met klanten op de projectgebaseerde contractregel kan dezelfde zijn als de lijst met klanten in het contract, maar dat is niet verplicht. Wanneer een projectprijsopgave wordt gewonnen en er een projectcontract wordt gemaakt, wordt de klantenlijst op de prijsopgaveregel gekopieerd naar de corresponderende contractregel. Klanten in de offerte worden naar het contract gekopieerd.

Wanneer het projectcontract wordt gefactureerd, heeft de klantenlijst op de projectgebaseerde contractregel voorrang op de klantenlijst op het contract. De klantenlijst in het projectcontract wordt alleen gebruikt om nieuwe contractregels standaard te maken.

Alle contractklanten op het tabblad **Klanten** van het projectcontract zijn standaard contractregelklanten op nieuwe contractregels die voor het projectcontract worden gemaakt. Eventuele bestaande contractregels nemen de nieuwe contractklantrecords die daarna zijn gemaakt, niet over.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Een klantrecord voor een contractregel maken, bijwerken of verwijderen

U kunt een contractregelklant maken, bijwerken of verwijderen via het tabblad **Contractregelklanten** op de pagina **Projectgebaseerde contractregel**. Wanneer een nieuwe klant wordt toegevoegd aan de projectgebaseerde contractregel, wordt deze ook aan het totale contract toegevoegd als een contractklant met een standaard percentage voor factureringssplitsing van nul procent. Het percentage voor factureringssplitsing op het totale contract wordt gekopieerd naar nieuwe contractregels en naar het uiteindelijke projectcontract. Wanneer u echter vanuit het contract factureert, wordt het percentage voor factureringssplitsing op contractregelniveau gebruikt en niet het percentage op het algemene contractniveau. 

Hieronder staan de velden van het klantrecord op de Contractregel van een projectgebaseerde contractregel die belangrijk zijn:

| Veld | Locatie | Beschrijving | Downstreamimpact |
| --- | --- | --- | --- |
| Account | Bewerkbaar raster op het tabblad **Contractregelklanten** en de formulieren Hoofd en Snelle invoer voor een contractregelklant. | Alle actieve accounts. Dit veld is vergrendeld nadat de record is gemaakt. Als u het veld wilt bijwerken, verwijdert u de record en maakt u een nieuwe record. Als u werkelijke waarden hebt opgenomen, kunt u de record niet verwijderen. U kunt het percentage voor factureringssplitsing echter markeren als nul voor dat account. Als de record is gemarkeerd als nul, heeft dit gevolgen voor alle toekomstige werkelijke kosten en inkomsten die aan deze klant worden toegekend of gesplitst. | Wanneer u een rekening kiest uit de hoofdlijst met accounts om deze toe te voegen en op te slaan, wordt de contractregelklant ook toegevoegd als contractklant. Contractregelklanten worden gebruikt wanneer facturen worden gegenereerd. |
| Gesplitst percentage facturering | Bewerkbaar raster op het tabblad **Contractregelklanten** en de formulieren Hoofd en Snelle invoer voor een contractregelklant. | Dit veld geeft het percentage weer van elke niet-gefactureerde verkooptransactie dat aan deze contractregelklant wordt toegeschreven. | Contractregelklanten en percentages voor facturatiesplitsing worden gebruikt wanneer werkelijke waarden worden aangemaakt na goedkeuring en wanneer de factuur wordt gegenereerd. |
| Niet-overschrijdingslimiet | Bewerkbaar raster op het tabblad **Contractregelklanten** en de formulieren Hoofd en Snelle invoer voor een contractregelklant. | Geeft aan of er een onderhandelde limiet of maximum is voor het totale bedrag dat voor de contractregel aan deze klant wordt gefactureerd. | De niet-overschrijdingslimiet voor de contractregelklant wordt gebruikt wanneer werkelijke waarden worden gemaakt en de facturen worden gegenereerd. |
| Bedrijf dat eigenaar is | Bewerkbaar raster op het tabblad **Prijsopgaveregelklanten** en de formulieren Hoofd en Snelle invoer voor een prijsopgaveregelklant. | De rechtspersoon waarin deze klant is opgericht. Dit veld is alleen-lezen en is ingesteld op het bedrijf dat eigenaar is van de prijsopgave. De lijst met klanten die moeten worden toegevoegd in het veld **Account**, is al gefilterd naar de lijst van dit bedrijf dat eigenaar is. | Het concept van een bedrijf dat eigenaar is, is gelijk aan het concept van een rechtspersoon. Alle kosten en opbrengsten van dit project worden verantwoord in het grootboek van het bedrijf dat de eigenaar is. |
| Is afronding | Bewerkbaar raster op het tabblad **Contractregelklanten** en de formulieren Hoofd en Snelle invoer voor een contractregelklant. | Dit veld geeft aan of deze klant een standaardafrondingsklant is voor deze projectgebaseerde contractregel. | Wanneer u een werkelijke waarde genereert op basis van het percentage voor factureringssplitsing, kunnen er enkele afrondingsverschillen zijn. Aan deze klant worden in dit geval de afrondingsverschillen toegerekend. |

## <a name="edit-billing-split-percentages"></a>Percentages voor gesplitste factuur bewerken

Percentages voor factureringssplitsing kunnen worden bewerkt in het raster. Als de percentages voor factureringssplitsing niet in totaal 100 procent bedragen, krijgt u een foutmelding. Nadat u de percentages voor factureringssplitsing hebt bewerkt, vernieuwt u de pagina om de fout te sluiten.

U kunt ook **Evenredig verdelen** selecteren in het subraster van de contractregelklant. Met deze actie worden factureringssplitsingen gelijkmatig toegewezen aan alle contractregelklanten. Als er een afrondingsfactor is, wordt deze bij de afrondingsklant opgeteld. Eén klant met een contractregel wordt altijd aangeduid als de **Afrondingsklant** met de vlag **Afronding** ingesteld op **Ja**.
