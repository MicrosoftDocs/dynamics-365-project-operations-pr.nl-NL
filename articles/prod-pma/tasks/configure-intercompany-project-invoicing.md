---
title: Intercompany-projectfacturering configureren
description: In dit onderwerp wordt getoond hoe u projectfacturering tussen twee bedrijven in uw organisatie instelt.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074623"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="f20c3-103">Intercompany-projectfacturering configureren</span><span class="sxs-lookup"><span data-stu-id="f20c3-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f20c3-104">In dit onderwerp wordt getoond hoe u projectfacturering tussen twee bedrijven in uw organisatie instelt.</span><span class="sxs-lookup"><span data-stu-id="f20c3-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="f20c3-105">Deze taak maakt gebruik van de USSI-gegevensset.</span><span class="sxs-lookup"><span data-stu-id="f20c3-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f20c3-106">Ga in het navigatievenster naar **Modules > Leveranciers > Leveranciers > Alle leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="f20c3-107">Zoek in de lijst **Alle verkopers** de gewenste record en selecteer deze.</span><span class="sxs-lookup"><span data-stu-id="f20c3-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="f20c3-108">Selecteer **Algemeen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="f20c3-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="f20c3-109">Selecteer **Intercompany**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="f20c3-110">Stel **Actief** in op **Ja** om intercompany-handel mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="f20c3-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="f20c3-111">Typ of selecteer een waarde in het veld **Klantbedrijf**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="f20c3-112">Typ of selecteer een waarde in het veld **Mijn account**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="f20c3-113">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-113">Select **Save**.</span></span>
9. <span data-ttu-id="f20c3-114">Sluit de pagina's om terug te keren naar de startpagina.</span><span class="sxs-lookup"><span data-stu-id="f20c3-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="f20c3-115">Ga in het navigatievenster naar **Modules > Projectmanagement en financiële administratie > Instellingen > Parameters voor Projectmanagement en financiële administratie**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="f20c3-116">Selecteer het tabblad **Intercompany**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="f20c3-117">Verplaats de schuifregelaar naar **Ja** om intercompany-resourceplanning en -urenstaten mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="f20c3-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="f20c3-118">Markeer de geselecteerde rij in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f20c3-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="f20c3-119">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-119">Select **New**.</span></span>
15. <span data-ttu-id="f20c3-120">Typ of selecteer een waarde in het veld **Lenende rechtspersoon**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="f20c3-121">Schakel het selectievakje **Omzet toerekenen** in.</span><span class="sxs-lookup"><span data-stu-id="f20c3-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="f20c3-122">Typ of selecteer een waarde in het veld **Standaardurenstaatcategorie**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="f20c3-123">Typ of selecteer een waarde in het veld **Standaardonkostencategorie**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="f20c3-124">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-124">Select **Save**.</span></span>
20. <span data-ttu-id="f20c3-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f20c3-125">Close the page.</span></span>
21. <span data-ttu-id="f20c3-126">Ga in het navigatievenster naar **Modules > Projectmanagement en financiële administratie > Instellingen > Boeking > Instellingen voor boeking in grootboek**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="f20c3-127">Selecteer een optie in het veld **Typen grootboekrekening**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="f20c3-128">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-128">Select **New**.</span></span>
24. <span data-ttu-id="f20c3-129">Geef in het veld **Hoofdaccount** van de nieuwe rij de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="f20c3-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="f20c3-130">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-130">Select **Save**.</span></span>
26. <span data-ttu-id="f20c3-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f20c3-131">Close the page.</span></span>
27. <span data-ttu-id="f20c3-132">Ga in het navigatievenster naar **Modules > Projectmanagement en financiële administratie > Instellingen > Prijzen > Verrekenprijs**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="f20c3-133">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-133">Select **New**.</span></span>
29. <span data-ttu-id="f20c3-134">Voer in het veld **Ingangsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="f20c3-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="f20c3-135">Typ of selecteer een waarde in het veld **Lenende rechtspersoon**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="f20c3-136">Selecteer een optie in het veld **Verrekenprijsmodel**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="f20c3-137">Voer een getal in het veld **Prijzen** in.</span><span class="sxs-lookup"><span data-stu-id="f20c3-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="f20c3-138">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-138">Select **Save**.</span></span>

