---
title: De factureringsbacklog voor projecten en projectcontracten controleren
description: In dit onderwerp wordt uitgelegd hoe u backlogs voor tijd, onkosten en producten bekijkt en hoe u deze markeert als gereed voor facturering.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 51a7ecfefcc20544f5be378a347e3568285cafb3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600552"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>De factureringsbacklog voor projecten en projectcontracten controleren

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Wanneer een transactie gereed is voor het maken en verwerken van een factuur, moet de transactie actie zijn gemarkeerd als **Gereed voor facturering**. In dit onderwerp worden de typen transacties beschreven die kunnen worden gemaakt.

## <a name="review-the-time-and-material-billing-backlog"></a>De backlog voor facturering van tijd en materiaal controleren

Wanneer een tijd- of onkostenvermelding wordt ingediend en goedgekeurd voor een project, maakt PSA een werkelijke projectwaarde. Als de combinatie van het project en de transactieklasse zijn toegewezen aan een contractregel voor een tijd-en-materiaalproject, worden twee werkelijke waarden gemaakt wanneer de vermelding wordt goedgekeurd:

- Werkelijke waarde voor kosten 
- Niet-gefactureerde werkelijke verkoopwaarde

Niet-gefactureerde werkelijke waarden voor verkoop vertegenwoordigen de factureringsbacklog en hun factureringsstatus moet worden ingesteld op **Gereed voor facturering**. Wanneer een projectfactuur wordt gemaakt, worden niet-gefactureerde werkelijke waarden voor verkoop die zijn gemarkeerd als **Gereed voor facturering** gekopieerd als factuurregeldetails.

Als u de factureringsbacklog voor tijd en materialen wilt controleren, gaat u naar **Verkoop** \> **Facturering** \> **Backlog voor facturering van tijd en materiaal**. Selecteer alle niet-gefactureerde werkelijke waarden voor verkoop die gereed zijn om te worden gefactureerd en selecteer vervolgens **Gereed voor facturering**. De factureringsstatus van deze werkelijke waarden wordt gewijzigd in **Gereed voor facturering**.

![Backlog voor facturering van tijd en materiaal.](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>De backlog voor facturering voor producten controleren

Wanneer in PSA een projectcontract op product gebaseerde contractregels bevat, worden deze regels meegenomen voor facturering wanneer een factuur voor het projectcontract wordt gemaakt. Elk product waarvoor contractregels zijn gemarkeerd als **Gereed voor facturering** wordt naar de projectfactuur gekopieerd als projectfactuurregels.

Als u de factureringsbacklog voor producten wilt controleren, gaat u naar **Verkoop** \> **Facturering** \> **Backlog voor facturering voor producten**. Selecteer alle productgebaseerde contractregels die gereed zijn om te worden gefactureerd en selecteer vervolgens **Gereed voor facturering**. De factureringsstatus van deze regels wordt gewijzigd in **Gereed voor facturering**.

![Backlog voor facturering voor producten.](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>De factureringsmijlpalen voor contracten met een vaste prijs controleren

Voor elke projectcontractregel met een factureringsmethode met vaste prijs moeten contractmijlpalen zijn gedefinieerd. Deze contractmijlpalen kunnen alleen worden gefactureerd als ze zijn gemarkeerd als **Gereed voor facturering**. 

Als u factureringsmijlpalen wilt controleren, gaat u naar **Verkoop** \> **Facturering** \> **Mijlpalen voor vaste prijs**. Selecteer alle mijlpalen die gereed zijn om te worden gefactureerd en selecteer vervolgens **Gereed voor facturering**. De factureringsstatus van deze mijlpalen wordt gewijzigd in **Gereed voor facturering**.

![Mijlpalen voor vaste prijs.](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
