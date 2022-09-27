---
title: Verificatie van leveranciersfacturen met goedgekeurde werkelijke waarden
description: In dit artikel wordt uitgelegd hoe Microsoft Dynamics 365 Project Operations projectmanagers in staat stelt leveranciersfacturen te verifiëren met de werkelijke waarden die zijn goedgekeurd terwijl aannemers werk hebben uitgevoerd en tijd hebben geregistreerd, evenals de onkosten en materialen die zijn gebruikt door projectteamleden.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522882"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verificatie van leveranciersfacturen met goedgekeurde werkelijke waarden

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Microsoft Dynamics 365 Project Operations stelt projectmanagers in staat leveranciersfactuurregels op de volgende manieren te verifiëren:

- Gebruik het veld **Verificatiestatus** op de leveranciersfactuurregels.
- Als de leveranciersfactuurregels verwijzen naar een subcontractregel, koppelt u werkelijke kosten van activiteiten van onderaannemers aan die leveranciersfactuurregels. De koppeling wordt gemaakt door werkelijke kosten af te stemmen op de leveranciersfactuurregels.

    > [!NOTE]
    > Hoewel de verificatiestatus kan worden gevolgd voor leveranciersfactuurregels die niet naar een subcontract verwijzen, kunnen werkelijke kosten niet aan die leveranciersfactuurregels worden gekoppeld.

## <a name="verification-status"></a>Verificatiestatus

Het veld **Verificatiestatus** op een leveranciersfactuurregel geeft die status van de verificatie aan. De volgende statussen worden ondersteund:

1. Niet gestart
2. In uitvoering
3. Voltooien

Leveranciersfactuurregels met een verificatiestatus **Niet gestart** kunnen worden bewerkt.

Leveranciersfactuurregels met een verificatiestatus **In uitvoering** kunnen niet langer worden bewerkt. Voor een leveranciersfactuurregel die verwijst naar een subcontract, wordt de verificatiestatus automatisch ingesteld op **In uitvoering** zodra de eerste werkelijke kostprijs is afgestemd op de leveranciersfactuurregel.

Leveranciersfactuurregels met een verificatiestatus **Voltooid** kunnen niet langer worden bewerkt. Als alle regels op een leveranciersfactuur deze verificatiestatus hebben, kan de leveranciersfactuur worden bevestigd.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Werkelijke kosten afstemmen op leveranciersfactuurregels

Het afstemmen van werkelijke kosten helpt bij het verificatieproces voor een leveranciersfactuurregel. Volg deze stappen om werkelijke kosten af te stemmen op een leveranciersfactuurregel.

1. Open de leveranciersfactuurregel en selecteer het tabblad **Niet-afgestemde werkelijke kosten**. Een raster toont een lijst met werkelijke kosten die verwijzen naar dezelfde subcontractregel als de leveranciersfactuurregel.
2. Selecteer een of meer van de werkelijke kosten en selecteer vervolgens **Afstemmen** op de werkbalk boven het raster. Het systeem valideert of de geselecteerde werkelijke kosten kunnen worden afgestemd. Nadat de validatie is uitgevoerd, worden de werkelijke kosten aan de leveranciersfactuurregel gekoppeld.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Validatiecriteria die worden gebruikt om werkelijke kosten aan leveranciersfactuurregels te koppelen

Tijdens het afstemmingsproces kan alleen een koppeling tussen een werkelijke kostprijs en een leveranciersfactuurregel tot stand worden gebracht als aan beide volgende voorwaarden wordt voldaan:

- Het veld **Aanpassingsstatus** voor elke geselecteerde werkelijke kostenpost moet leeg zijn. Met andere woorden, de werkelijke kosten mogen niet zijn vervangen door andere werkelijke kosten tijdens een intrekkings-, goedkeuringsannulerings- of correctiejournaalproces.
- De waarden van de volgende velden worden afgestemd tussen de leveranciersfactuurregel en de geselecteerde werkelijke kosten. Als er geen veld is ingesteld op de leveranciersfactuurregel, wordt dit niet meegenomen bij de afstemming.

    - Projectcontract
    - Projectcontractregel
    - Transactieklasse
    - Project
    - Opdracht
    - Resourcecategorie
    - Transactiecategorie
    - Product
    - Subcontractregel
    - Boekbare resource

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Afstemming van werkelijke kosten op een leveranciersfactuurregel ongedaan maken

Het ongedaan maken van de afstemming van werkelijke kosten kan ook helpen bij het verificatieproces op een leveranciersfactuur door ervoor te zorgen dat eerder gemaakte koppelingen kunnen worden verwijderd. De afstemming van werkelijke kosten kan alleen ongedaan worden gemaakt vanaf leveranciersfactuurregels met een verificatiestatus **In uitvoering**. Volg deze stappen om de afstemming van werkelijke kosten op een leveranciersfactuurregel ongedaan te maken.

1. Open de leveranciersfactuurregel en selecteer het tabblad **Afgestemde werkelijke kosten**. Een raster toont een lijst met werkelijke kosten die verwijzen naar de leveranciersfactuurregel.
2. Selecteer een of meer van de werkelijke kosten en selecteer vervolgens **Afstemming ongedaan maken** op de werkbalk boven het raster.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
