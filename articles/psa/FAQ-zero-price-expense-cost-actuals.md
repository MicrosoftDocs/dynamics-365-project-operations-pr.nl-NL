---
title: Waarom wordt de prijs standaard op nul gezet voor de werkelijke kostenwaarden op basis van onkosten?
description: Het probleem oplossen waarbij de prijs standaard op nul wordt gezet voor werkelijke kostenwaarden op basis van onkosten.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 03c958635dec66b0f243872dfb929eba6a20119b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992780"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="bc425-103">Waarom wordt de prijs standaard op nul gezet voor de werkelijke kostenwaarden op basis van onkosten</span><span class="sxs-lookup"><span data-stu-id="bc425-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="bc425-104">Dit artikel is van toepassing op werkelijke waarden op basis van onkosten waarvoor de transactieklasse is ingesteld op Onkosten en het transactietype Kosten is.</span><span class="sxs-lookup"><span data-stu-id="bc425-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="bc425-105">Problemen met kostentarieven in werkelijke kostenwaarden op basis van onkosten oplossen</span><span class="sxs-lookup"><span data-stu-id="bc425-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="bc425-106">Ga naar de gerelateerde onkostenvermelding en controleer of het veld voor de onkostenvermelding een bedrag bevat.</span><span class="sxs-lookup"><span data-stu-id="bc425-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="bc425-107">Als voor de oorspronkelijke onkostenvermelding geen bedrag is ingevuld, hebt u het probleem gevonden.</span><span class="sxs-lookup"><span data-stu-id="bc425-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="bc425-108">U lost dit probleem op door de onkostenvermelding opnieuw te maken met een geldig bedrag en deze vervolgens goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="bc425-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]