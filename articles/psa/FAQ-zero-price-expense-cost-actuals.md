---
title: Waarom wordt de prijs standaard op nul gezet voor de werkelijke kostenwaarden op basis van onkosten?
description: Het probleem oplossen waarbij de prijs standaard op nul wordt gezet voor werkelijke kostenwaarden op basis van onkosten.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074585"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="2e79e-103">Waarom wordt de prijs standaard op nul gezet voor de werkelijke kostenwaarden op basis van onkosten?</span><span class="sxs-lookup"><span data-stu-id="2e79e-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2e79e-104">Dit artikel is van toepassing op werkelijke waarden op basis van onkosten waarvoor de transactieklasse is ingesteld op Onkosten en het transactietype Kosten is.</span><span class="sxs-lookup"><span data-stu-id="2e79e-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="2e79e-105">Problemen met kostentarieven in werkelijke kostenwaarden op basis van onkosten oplossen</span><span class="sxs-lookup"><span data-stu-id="2e79e-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="2e79e-106">Ga naar de gerelateerde onkostenvermelding en controleer of het veld voor de onkostenvermelding een bedrag bevat.</span><span class="sxs-lookup"><span data-stu-id="2e79e-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="2e79e-107">Als voor de oorspronkelijke onkostenvermelding geen bedrag is ingevuld, hebt u het probleem gevonden.</span><span class="sxs-lookup"><span data-stu-id="2e79e-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="2e79e-108">U lost dit probleem op door de onkostenvermelding opnieuw te maken met een geldig bedrag en deze vervolgens goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="2e79e-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
