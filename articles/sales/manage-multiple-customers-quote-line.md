---
title: Meerdere klanten in projectgebaseerde prijsopgaveregels beheren
description: Dit onderwerp biedt informatie over hoe u meerdere klanten op projectgebaseerde prijsopgaveregels kunt beheren.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4fa0adc877797d782173f29690b33d38ba7f8dcd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277917"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Meerdere klanten in projectgebaseerde prijsopgaveregels beheren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Projectgebaseerde prijsopgaveregels ondersteunen scenario's waarin elke prijsopgaveregel een lijst heeft met klanten die ervoor betalen. Deze lijst met klanten op de projectgebaseerde prijsopgaveregel kan hetzelfde zijn als de lijst met klanten in de prijsopgave. U kunt de lijst met klanten ook wijzigen. Wanneer het uiteindelijke projectcontract wordt gecreëerd nadat een projectprijsopgave wordt geaccepteerd, wordt de klantenlijst op de projectgebaseerde prijsopgaveregel gekopieerd naar de corresponderende projectgebaseerde contractregel. Klanten in de projectgebaseerde prijsopgave worden gekopieerd naar het projectcontract.

Wanneer u het uiteindelijke projectcontract factureert, krijgt de klantenlijst op de projectgebaseerde contractregel voorrang op de lijst op het projectcontract. De klantenlijst op het projectcontract wordt alleen gebruikt voor standaardwaarden op nieuwe projectcontractregels.

Alle klanten voor prijsopgave op het tabblad **Klanten** van de projectprijsopgave zijn standaard de klanten van de nieuwe projectgebaseerde prijsopgaveregels die zijn gemaakt voor de projectprijsopgave. Eventuele bestaande projectgebaseerde prijsopgaveregels nemen geen nieuwe klantrecords voor prijsopgaven over die daarna zijn gemaakt.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Een klantrecord voor een prijsopgaveregel maken, bijwerken of verwijderen

U kunt een klant voor een prijsopgaveregel maken, bijwerken of verwijderen op het tabblad **Prijsopgaveregelklanten** op de pagina **Projectgebaseerde prijsopgaveregel**. Wanneer u een nieuwe klant toevoegt op de projectgebaseerde prijsopgaveregel, wordt de klant ook toegevoegd aan de totale prijsopgave als prijsopgaveklant, met een standaard factureringsverdelingspercentage op de totale prijsopgave van 0%. Het splitsingspercentage voor de facturering op de totale prijsopgave wordt gekopieerd naar nieuwe prijsopgaveregels en naar het uiteindelijke projectcontract. Wanneer u echter vanuit het contract factureert, wordt het splitsingspercentage voor de facturering op het prijsopgaveregelniveau gebruikt, niet het splitsingspercentage op het algemene contractniveau. 

De volgende tabel geeft de velden weer uit de klantrecord van een projectgebaseerde prijsopgaveregel.

| Veld | Locatie | Beschrijving en richtlijn | Downstreamimpact |
| --- | --- | --- | --- |
| **Account** | Een bewerkbaar raster op het tabblad **Prijsopgaveregelklanten** en de formulieren Hoofd en Snelle invoer voor een prijsopgaveregelklant. | Geeft een overzicht van alle actieve accounts. Dit veld is vergrendeld nadat de record is gemaakt. Als u het veld moet bijwerken, verwijdert u de record en maakt u deze opnieuw. Als u werkelijke waarden hebt opgenomen, kunt u de record niet verwijderen. | Wanneer u een account kiest uit de hoofdlijst met accounts om toe te voegen, wordt de klant van de prijsopgaveregel ook toegevoegd als klant van een prijsopgave. Prijsopgaveregelklanten worden gekopieerd naar de klanten op de projectcontractregel wanneer een prijsopgave wordt geaccepteerd. |
| **Gesplitst percentage facturering** | Een bewerkbaar raster op het tabblad **Prijsopgaveregelklanten** en de formulieren Hoofd en Snelle invoer voor een prijsopgaveregelklant. | Geeft het percentage aan van elke niet-gefactureerde verkooptransactie die aan deze prijsopgaveregelklant wordt toegewezen. | Wordt gekopieerd naar projectcontractregelklanten. |
| **Niet-overschrijdingslimiet** | Een bewerkbaar raster op het tabblad **Prijsopgaveregelklanten** en de formulieren Hoofd en Snelle invoer voor een prijsopgaveregelklant. | Geeft aan of er een onderhandelde limiet of maximum is voor het totale bedrag dat voor deze prijsopgaveregel aan deze klant wordt gefactureerd. | Wordt gekopieerd naar de klanten op de projectcontractregel wanneer een prijsopgave wordt geaccepteerd. |
| **Bedrijf dat eigenaar is** | Een bewerkbaar raster op het tabblad **Prijsopgaveregelklanten** en de formulieren Hoofd en Snelle invoer voor een prijsopgaveregelklant. | De rechtspersoon waarvoor deze klant is ingesteld in de module **Projectmanagement en financiële administratie**. Dit veld is alleen-lezen en is ingesteld op het bedrijf dat eigenaar is van de prijsopgave zelf. De lijst met klanten die moeten worden toegevoegd in het veld **Account** is al gefilterd op de lijst van het bedrijf dat eigenaar is in de module **Projectmanagement en financiële administratie** van Project Operations. | Het bedrijf dat de eigenaar is, komt overeen met het concept van rechtspersoon. Alle kosten en opbrengsten die voortvloeien uit dit project worden verantwoord in het grootboek van het bedrijf dat de eigenaar is. |
| **Is afronding** | Een bewerkbaar raster op het tabblad **Prijsopgaveregelklanten** en de formulieren Hoofd en Snelle invoer voor een prijsopgaveregelklant. | Geeft aan of deze klant een standaard afrondingsklant is voor deze projectgebaseerde prijsopgaveregel. | Wordt gekopieerd naar de klanten op het projectcontract wanneer een prijsopgave wordt geaccepteerd. |

## <a name="edit-billing-split-percentages"></a>Percentages voor gesplitste factuur bewerken

U kunt de percentages voor factureringssplitsing op de regel bewerken. Als de percentages voor factuursplitsing niet in totaal 100% bedragen, treedt er een fout op. Nadat u de percentages voor factuursplitsing hebt bewerkt, vernieuwt u de pagina met de prijsopgaveregel om de fout te verwijderen.

Gebruik de actie voor gelijkmatig verdelen op het subraster met prijsopgaveregelklanten om factureringssplitsingen toe te wijzen aan alle klanten van de prijsopgaveregel. Als er een afrondingsfactor is, wordt die toegevoegd voor de afrondingsklant. Een van de klanten van de prijsopgaveregel wordt altijd getagd als de afrondingsklant, wat betekent dat de afrondingsvlag in de record van de prijsopgaveregelklant is ingesteld op **Ja**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]