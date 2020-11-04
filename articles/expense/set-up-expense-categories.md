---
title: Onkostencategorieën instellen
description: Dit onderwerp biedt informatie over het instellen van onkostencategorieën en gedeelde categorieën voor onkostendeclaraties.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074454"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="bc94a-103">Onkostencategorieën instellen</span><span class="sxs-lookup"><span data-stu-id="bc94a-103">Set up expense categories</span></span>

<span data-ttu-id="bc94a-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="bc94a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bc94a-105">Wanneer werknemers onkostendeclaraties maken, moet elke uitgave die ze registreren, worden gekoppeld aan een onkostencategorie.</span><span class="sxs-lookup"><span data-stu-id="bc94a-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="bc94a-106">Onkostencategorieën zijn afgeleid van gedeelde categorieën die kunnen worden gedeeld door de rechtspersonen in uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="bc94a-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="bc94a-107">Afhankelijk van hoe uw organisatie is gedefinieerd, kunnen deze onkostencategorieën ook op andere gebieden worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="bc94a-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="bc94a-108">Op basis van de definitie van uw organisatie en richtlijnen van het implementatieteam, moet u bepalen of de categorieën die worden gebruikt in Onkostenbeheer alleen worden gebruikt in Onkostenbeheer of moeten worden gedeeld op andere gebieden.</span><span class="sxs-lookup"><span data-stu-id="bc94a-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="bc94a-109">Deze categorieën kunnen worden gedeeld tussen Projectbeheer en boekhouding en Onkostenbeheer, of tussen Projectbeheer en boekhouding en Productie.</span><span class="sxs-lookup"><span data-stu-id="bc94a-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="bc94a-110">Ze kunnen echter niet worden gedeeld tussen Onkostenbeheer en Productie.</span><span class="sxs-lookup"><span data-stu-id="bc94a-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="bc94a-111">Voordat u met het instellen begint, moeten de volgende beslissingen worden genomen voor elke onkostencategorie:</span><span class="sxs-lookup"><span data-stu-id="bc94a-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="bc94a-112">Wat is de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="bc94a-112">What is the expense category?</span></span> <span data-ttu-id="bc94a-113">Voorbeelden zijn categorieën voor vluchten, hotel of kilometerstand.</span><span class="sxs-lookup"><span data-stu-id="bc94a-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="bc94a-114">Kan de onkostencategorie ook worden gebruikt in Projectmanagement en financiële administratie?</span><span class="sxs-lookup"><span data-stu-id="bc94a-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="bc94a-115">Als dat zo is, moet u bovendien de volgende beslissingen nemen:</span><span class="sxs-lookup"><span data-stu-id="bc94a-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="bc94a-116">Welke kostenrekeningen worden gebruikt voor de volgende uitgaven?</span><span class="sxs-lookup"><span data-stu-id="bc94a-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="bc94a-117">Kosten</span><span class="sxs-lookup"><span data-stu-id="bc94a-117">Cost</span></span>
        - <span data-ttu-id="bc94a-118">Salaristoewijzing</span><span class="sxs-lookup"><span data-stu-id="bc94a-118">Payroll allocation</span></span>
        - <span data-ttu-id="bc94a-119">OHW - waarde van kostprijs</span><span class="sxs-lookup"><span data-stu-id="bc94a-119">WIP-cost value</span></span>
        - <span data-ttu-id="bc94a-120">Kosten - artikel</span><span class="sxs-lookup"><span data-stu-id="bc94a-120">Cost-item</span></span>
        - <span data-ttu-id="bc94a-121">OHW - waarde van kostprijs - artikel</span><span class="sxs-lookup"><span data-stu-id="bc94a-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="bc94a-122">Opgelopen verlies</span><span class="sxs-lookup"><span data-stu-id="bc94a-122">Accrued loss</span></span>
        - <span data-ttu-id="bc94a-123">Opgelopen verlies OHW</span><span class="sxs-lookup"><span data-stu-id="bc94a-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="bc94a-124">Welke inkomstenrekeningen worden gebruikt voor de volgende inkomstenbronnen?</span><span class="sxs-lookup"><span data-stu-id="bc94a-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="bc94a-125">Gefactureerde omzet</span><span class="sxs-lookup"><span data-stu-id="bc94a-125">Invoiced revenue</span></span>
        - <span data-ttu-id="bc94a-126">Toegerekende omzet - verkoopwaarde</span><span class="sxs-lookup"><span data-stu-id="bc94a-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="bc94a-127">OHW - verkoopwaarde</span><span class="sxs-lookup"><span data-stu-id="bc94a-127">WIP-sales value</span></span>
        - <span data-ttu-id="bc94a-128">Opgebouwde opbrengst - productie</span><span class="sxs-lookup"><span data-stu-id="bc94a-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="bc94a-129">OHW - productie</span><span class="sxs-lookup"><span data-stu-id="bc94a-129">WIP-production</span></span>
        - <span data-ttu-id="bc94a-130">Opgebouwde opbrengst - winst</span><span class="sxs-lookup"><span data-stu-id="bc94a-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="bc94a-131">OHW - winst</span><span class="sxs-lookup"><span data-stu-id="bc94a-131">WIP-profit</span></span>
        - <span data-ttu-id="bc94a-132">Opgebouwde opbrengst - abonnement</span><span class="sxs-lookup"><span data-stu-id="bc94a-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="bc94a-133">OHW - abonnement</span><span class="sxs-lookup"><span data-stu-id="bc94a-133">WIP-subscription</span></span>

- <span data-ttu-id="bc94a-134">Wat is het onkostentype?</span><span class="sxs-lookup"><span data-stu-id="bc94a-134">What is the expense type?</span></span>
- <span data-ttu-id="bc94a-135">Wat is de standaard betalingsmethode voor de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="bc94a-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="bc94a-136">Moeten onkosten in de onkostencategorie gespecificeerd worden?</span><span class="sxs-lookup"><span data-stu-id="bc94a-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="bc94a-137">Wat is de standaard hoofdrekening voor de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="bc94a-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="bc94a-138">Wat is de standaard btw-groep van artikelen voor de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="bc94a-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="bc94a-139">Zijn aanvullende betalingsmethoden toegestaan voor de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="bc94a-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="bc94a-140">Indien ja, wat zijn dit?</span><span class="sxs-lookup"><span data-stu-id="bc94a-140">If so, what are they?</span></span>
- <span data-ttu-id="bc94a-141">Zijn er subcategorieën in deze onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="bc94a-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="bc94a-142">Als er subcategorieën zijn, moet u bovendien de volgende beslissingen nemen:</span><span class="sxs-lookup"><span data-stu-id="bc94a-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="bc94a-143">Zijn subcategorieën uitgesloten van belastingteruggave?</span><span class="sxs-lookup"><span data-stu-id="bc94a-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="bc94a-144">Wat is de btw-groep van de subcategorieën?</span><span class="sxs-lookup"><span data-stu-id="bc94a-144">What is the item sales tax group of the subcategories?</span></span>
