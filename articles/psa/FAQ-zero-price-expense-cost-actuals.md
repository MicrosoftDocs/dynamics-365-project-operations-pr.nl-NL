---
title: Waarom wordt de prijs standaard op nul gezet voor de werkelijke kostenwaarden op basis van onkosten?
description: Het probleem oplossen waarbij de prijs standaard op nul wordt gezet voor werkelijke kostenwaarden op basis van onkosten.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122112"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="39fc8-103">Waarom wordt de prijs standaard op nul gezet voor de werkelijke kostenwaarden op basis van onkosten?</span><span class="sxs-lookup"><span data-stu-id="39fc8-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="39fc8-104">Dit artikel is van toepassing op werkelijke waarden op basis van onkosten waarvoor de transactieklasse is ingesteld op Onkosten en het transactietype Kosten is.</span><span class="sxs-lookup"><span data-stu-id="39fc8-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="39fc8-105">Problemen met kostentarieven in werkelijke kostenwaarden op basis van onkosten oplossen</span><span class="sxs-lookup"><span data-stu-id="39fc8-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="39fc8-106">Ga naar de gerelateerde onkostenvermelding en controleer of het veld voor de onkostenvermelding een bedrag bevat.</span><span class="sxs-lookup"><span data-stu-id="39fc8-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="39fc8-107">Als voor de oorspronkelijke onkostenvermelding geen bedrag is ingevuld, hebt u het probleem gevonden.</span><span class="sxs-lookup"><span data-stu-id="39fc8-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="39fc8-108">U lost dit probleem op door de onkostenvermelding opnieuw te maken met een geldig bedrag en deze vervolgens goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="39fc8-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
