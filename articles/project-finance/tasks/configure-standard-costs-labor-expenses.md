---
title: Standaardkosten voor arbeid en onkosten configureren
description: In dit onderwerp wordt uitgelegd hoe u standaardkosten voor arbeid en onkosten voor een project instelt.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750846"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="e7a0c-103">Standaardkosten voor arbeid en onkosten configureren</span><span class="sxs-lookup"><span data-stu-id="e7a0c-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7a0c-104">In dit onderwerp wordt uitgelegd hoe u standaardkosten voor arbeid en onkosten voor een project instelt.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="e7a0c-105">Deze taak maakt gebruik van de USSI-gegevensset.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e7a0c-106">Ga in het navigatievenster naar **Modules > Projectmanagement en financiële administratie > Instellingen > Prijzen > Kostprijs (uur)**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="e7a0c-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-107">Select **New**.</span></span>
3. <span data-ttu-id="e7a0c-108">Voer in het veld **Ingangsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="e7a0c-109">Voer een getal in het veld **Kostprijs** in.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="e7a0c-110">U kunt een standaardkostprijs instellen voor de projectcategorie of u kunt een kostprijs instellen op personeelsnummer, projectnummer, categorie, datum of een combinatie hiervan.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="e7a0c-111">De kostprijs die wordt gehanteerd is de kostprijs met het hoogste detailniveau.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="e7a0c-112">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-112">Select **Save**.</span></span>
6. <span data-ttu-id="e7a0c-113">Ga in het navigatievenster naar **Modules > Projectmanagement en financiële administratie > Instellingen > Prijzen > Verkoopprijs (uur)**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="e7a0c-114">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-114">Select **New**.</span></span>
8. <span data-ttu-id="e7a0c-115">Voer in het veld **Ingangsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="e7a0c-116">Selecteer een optie in het veld **Geldig voor**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="e7a0c-117">Voer een getal in het veld **Prijzen** in.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="e7a0c-118">U kunt een standaardverkoopprijs instellen voor uurtransacties of voor een projectcategorie.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="e7a0c-119">U kunt ook verkoopprijzen instellen op werknemersnummer, projectnummer, categorie, transactiedatum of een combinatie hiervan.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="e7a0c-120">De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer een transactie invoert in het urenjournaal, is de verkoopprijs met het hoogste detailniveau.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="e7a0c-121">Als bijvoorbeeld zowel een algemene verkoopprijs als een werknemerspecifieke verkoopprijs zijn ingesteld, wordt de werknemerspecifieke verkoopprijs gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="e7a0c-122">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-122">Select **Save**.</span></span>
12. <span data-ttu-id="e7a0c-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-123">Close the page.</span></span>
13. <span data-ttu-id="e7a0c-124">Ga in het navigatievenster naar **Modules > Projectmanagement en financiële administratie > Instellingen > Prijzen > Kostprijs (onkosten)**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="e7a0c-125">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-125">Select **New**.</span></span>
15. <span data-ttu-id="e7a0c-126">Voer in het veld **Ingangsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="e7a0c-127">Voer een getal in het veld **Kostprijs** in.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="e7a0c-128">Er kunnen meerdere velden worden ingevuld, maar dit is het minimum dat nodig is om de record op te slaan.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="e7a0c-129">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-129">Select **Save**.</span></span>
18. <span data-ttu-id="e7a0c-130">Ga in het navigatievenster naar **Modules > Projectmanagement en financiële administratie > Instellingen > Prijzen > Verkoopprijs (onkosten)**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="e7a0c-131">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-131">Select **New**.</span></span>
20. <span data-ttu-id="e7a0c-132">Voer in het veld **Ingangsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="e7a0c-133">Selecteer een optie in het veld **Geldig voor**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="e7a0c-134">Voer een getal in het veld **Prijzen** in.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="e7a0c-135">De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer transacties invoert in een onkostenjournaal, is de verkoopprijs met het hoogste detailniveau.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="e7a0c-136">Als bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs zijn ingesteld, wordt de werknemerspecifieke verkoopprijs gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="e7a0c-137">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e7a0c-137">Select **Save**.</span></span>

