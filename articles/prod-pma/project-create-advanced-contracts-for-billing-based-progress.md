---
title: Geavanceerde contracten maken voor facturering op basis van voortgang
description: In dit onderwerp wordt uitgelegd hoe u projectcontracten maakt, zodat u facturen voor klanten kunt genereren op basis van een percentage voltooid werk.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b1de330df8cf85ed30c0ee4e4f2f2fe74d05dbff
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289498"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="e557a-103">Geavanceerde contracten maken voor facturering op basis van voortgang</span><span class="sxs-lookup"><span data-stu-id="e557a-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="e557a-104">In dit onderwerp wordt uitgelegd hoe u projectcontracten maakt, zodat u facturen voor klanten kunt maken op basis van een percentage voltooid werk.</span><span class="sxs-lookup"><span data-stu-id="e557a-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="e557a-105">Factuurbedragen worden automatisch berekend voor de budgetcategorieën van werk dat u voor een project instelt.</span><span class="sxs-lookup"><span data-stu-id="e557a-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="e557a-106">De timing van de factuur wordt bepaald wanneer u over het projectcontract met de klant onderhandelt.</span><span class="sxs-lookup"><span data-stu-id="e557a-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="e557a-107">Gebruik de procedures in dit onderwerp om een contract, een bijbehorend project en de factureringsregels op te stellen waarmee de factuurbedragen worden berekend voor de budgetcategorieën met werk die u voor het project instelt.</span><span class="sxs-lookup"><span data-stu-id="e557a-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="e557a-108">Nadat u het contract en het project hebt aangemaakt, kunt u de details van het project instellen.</span><span class="sxs-lookup"><span data-stu-id="e557a-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="e557a-109">U kunt bijvoorbeeld activiteiten definiëren en werknemers aan het project toewijzen.</span><span class="sxs-lookup"><span data-stu-id="e557a-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="e557a-110">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="e557a-110">Example</span></span>

<span data-ttu-id="e557a-111">Uw organisatie is een softwareontwikkelingsbedrijf.</span><span class="sxs-lookup"><span data-stu-id="e557a-111">Your organization is a software development firm.</span></span> <span data-ttu-id="e557a-112">U stemt ermee in om een salarisadministratiepakket voor een klant te ontwikkelen voor een totaalbedrag van 20.000 USD.</span><span class="sxs-lookup"><span data-stu-id="e557a-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="e557a-113">Uw organisatie stemt ermee in om de klant te factureren wanneer u bepaalde percentages van het project voltooit.</span><span class="sxs-lookup"><span data-stu-id="e557a-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="e557a-114">U stelt de volgende projectcategorieën in voor het werk, zodat u deze kunt gebruiken in het facturatieproces:</span><span class="sxs-lookup"><span data-stu-id="e557a-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="e557a-115">Consultancy</span><span class="sxs-lookup"><span data-stu-id="e557a-115">Consulting</span></span>
- <span data-ttu-id="e557a-116">Ontwerp</span><span class="sxs-lookup"><span data-stu-id="e557a-116">Design</span></span>
- <span data-ttu-id="e557a-117">Installatie</span><span class="sxs-lookup"><span data-stu-id="e557a-117">Installation</span></span>

<span data-ttu-id="e557a-118">U stelt ook factureringsregels in waarmee automatisch de factuurbedragen worden berekend voor het percentage projectwerk dat in elke categorie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="e557a-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="e557a-119">De budgetmanager maakt een budget voor de projectcategorieën.</span><span class="sxs-lookup"><span data-stu-id="e557a-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="e557a-120">De hoeveelheid voltooid werk wordt automatisch berekend als een percentage van het werkelijke werk in vergelijking met de gebudgetteerde bedragen.</span><span class="sxs-lookup"><span data-stu-id="e557a-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e557a-121">Vereisten</span><span class="sxs-lookup"><span data-stu-id="e557a-121">Prerequisites</span></span>

<span data-ttu-id="e557a-122">Voordat u een project maakt dat factureringsregels gebruikt, moet u de nummerreeksen voor factureringsregels en een kostenjournaal instellen dat wordt gebruikt om voortgangsfacturen te boeken.</span><span class="sxs-lookup"><span data-stu-id="e557a-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="e557a-123">Ga naar **Projectmanagement en financiële administratie** \> **Instellen** \> **Parameters voor Projectmanagement en financiële administratie**.</span><span class="sxs-lookup"><span data-stu-id="e557a-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="e557a-124">Op de pagina **Parameters voor Projectmanagement en financiële administratie** stelt u op het tabblad **Nummerreeksen** de nummerreeks in die u wilt gebruiken wanneer factureringsregels worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e557a-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="e557a-125">Ga naar **Projectmanagement en financiële administratie** \> **Journalen** \> **Vergoeding**.</span><span class="sxs-lookup"><span data-stu-id="e557a-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="e557a-126">Selecteer op de pagina **Kostenjournaal** de optie **Nieuw** en voer de journaalnaam in.</span><span class="sxs-lookup"><span data-stu-id="e557a-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="e557a-127">Een contract maken voor voortgangsfacturen</span><span class="sxs-lookup"><span data-stu-id="e557a-127">Create a contract for progress billings</span></span>

<span data-ttu-id="e557a-128">Gebruik deze procedure om een projectcontract te creëren voor een project met een vaste prijs.</span><span class="sxs-lookup"><span data-stu-id="e557a-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="e557a-129">U maakt een projectfactuur aan wanneer het werk dat aan het project is voltooid een bepaald percentage bereikt.</span><span class="sxs-lookup"><span data-stu-id="e557a-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="e557a-130">Ga naar **Projectmanagement en financiële administratie** \> **Projecten** \> **Projectcontracten**.</span><span class="sxs-lookup"><span data-stu-id="e557a-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="e557a-131">Selecteer op de pagina **Projectcontracten** de optie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e557a-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="e557a-132">Stel in het dialoogvenster **Nieuw projectcontract** de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="e557a-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="e557a-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="e557a-133">**Name**</span></span>
    - <span data-ttu-id="e557a-134">**Type financiering**</span><span class="sxs-lookup"><span data-stu-id="e557a-134">**Funding type**</span></span>
    - <span data-ttu-id="e557a-135">**Financieringsbron**</span><span class="sxs-lookup"><span data-stu-id="e557a-135">**Funding source**</span></span>
    - <span data-ttu-id="e557a-136">**Verkoopvaluta**: standaard wordt deze valuta gebruikt voor klantfacturen die aan het projectcontract zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="e557a-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="e557a-137">U kunt de verkoopvaluta echter op een specifieke klantfactuur wijzigen.</span><span class="sxs-lookup"><span data-stu-id="e557a-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="e557a-138">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e557a-138">Select **OK**.</span></span> <span data-ttu-id="e557a-139">De informatie wordt gekopieerd naar de koptekst van de pagina **Projectcontracten**.</span><span class="sxs-lookup"><span data-stu-id="e557a-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="e557a-140">Vul op de pagina **Projectcontracten** vul de rest van de vereiste informatie voor het project in.</span><span class="sxs-lookup"><span data-stu-id="e557a-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="e557a-141">Een project maken voor voortgangsfacturen</span><span class="sxs-lookup"><span data-stu-id="e557a-141">Create a project for progress billings</span></span>

<span data-ttu-id="e557a-142">Volg deze stappen om een project en eventuele subprojecten te maken die aan een projectcontract zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="e557a-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="e557a-143">Ga naar **Projectmanagement en financiële administratie** \> **Projecten** \> **Alle projecten**.</span><span class="sxs-lookup"><span data-stu-id="e557a-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="e557a-144">Selecteer op de pagina **Alle projecten** de optie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e557a-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="e557a-145">Selecteer in het dialoogvenster **Nieuw project** in het veld **Projecttype** de optie **Tijd en materiaal**.</span><span class="sxs-lookup"><span data-stu-id="e557a-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="e557a-146">Selecteer een projectgroep.</span><span class="sxs-lookup"><span data-stu-id="e557a-146">Select a project group.</span></span> <span data-ttu-id="e557a-147">Een projectgroep definieert de boekingsinformatie voor de projecten die aan de groep zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e557a-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="e557a-148">Selecteer **Project maken**.</span><span class="sxs-lookup"><span data-stu-id="e557a-148">Select **Create project**.</span></span>
6. <span data-ttu-id="e557a-149">Nadat het project is gemaakt, stelt u de projectfase in op **In proces**.</span><span class="sxs-lookup"><span data-stu-id="e557a-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="e557a-150">Een budget maken voor een project</span><span class="sxs-lookup"><span data-stu-id="e557a-150">Create a budget for a project</span></span>

<span data-ttu-id="e557a-151">Budgetcategorieën worden gebruikt om automatisch de factuurbedragen te berekenen voor het percentage voltooid werk voor elke categorie.</span><span class="sxs-lookup"><span data-stu-id="e557a-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="e557a-152">Volg deze stappen om budgetcategorieën te maken voor de geschatte kosten.</span><span class="sxs-lookup"><span data-stu-id="e557a-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="e557a-153">Ga naar **Projectmanagement en financiële administratie** \> **Projecten** \> **Alle projecten**.</span><span class="sxs-lookup"><span data-stu-id="e557a-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="e557a-154">Selecteer en open op de pagina **Alle projecten** het gewenste project.</span><span class="sxs-lookup"><span data-stu-id="e557a-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="e557a-155">Op de pagina **Projecten**, in het actievenster, op het tabblad **Plan**, in de groep **Begroting** selecteert u **Projectbudget**.</span><span class="sxs-lookup"><span data-stu-id="e557a-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="e557a-156">Voer op de pagina **Projectbudget** de geschatte kosten in voor elke categorie in het project.</span><span class="sxs-lookup"><span data-stu-id="e557a-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="e557a-157">Factureringsregels maken voor voortgangsfacturen</span><span class="sxs-lookup"><span data-stu-id="e557a-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="e557a-158">Ga naar **Projectmanagement en financiële administratie** \> **Projecten** \> **Projectcontracten**.</span><span class="sxs-lookup"><span data-stu-id="e557a-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="e557a-159">Selecteer op de pagina **Projectcontracten** een projectcontract en open het.</span><span class="sxs-lookup"><span data-stu-id="e557a-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="e557a-160">Selecteer **Toevoegen** op de projectcontractpagina in het sneltabblad **Factureringsregels**.</span><span class="sxs-lookup"><span data-stu-id="e557a-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="e557a-161">Selecteer **Voortgang** op de pagina **Factureringsregel** in het veld **Lijntype**.</span><span class="sxs-lookup"><span data-stu-id="e557a-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="e557a-162">Voer op het sneltabblad **Details van factureringsregels** in het veld **Contractwaarde** de totale waarde van het contract in.</span><span class="sxs-lookup"><span data-stu-id="e557a-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="e557a-163">Selecteer in het veld **Categorie** de categorie waarnaar u de kostentransactie wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="e557a-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="e557a-164">Selecteer in het veld **Project** het project dat deze factureringsregel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e557a-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="e557a-165">Optioneel: wijs de factureringsregel toe aan extra projecten.</span><span class="sxs-lookup"><span data-stu-id="e557a-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="e557a-166">Selecteer op het sneltabblad **Project** in de sectie **Beschikbare projecten** een project en selecteer vervolgens de pijl naar rechts om het project toe te voegen aan de sectie **Geselecteerde projecten**.</span><span class="sxs-lookup"><span data-stu-id="e557a-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="e557a-167">Optioneel: bereken het percentagebedrag dat de klant inhoudt op betalingen op een factuur.</span><span class="sxs-lookup"><span data-stu-id="e557a-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="e557a-168">Selecteer op het sneltabblad **Inhoudingstermijnen voor betalingen** de financieringsbron en vul vervolgens het veld **Inhoudingspercentage** in.</span><span class="sxs-lookup"><span data-stu-id="e557a-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="e557a-169">Herhaal deze stappen om aanvullende factureringsregels voor het projectcontract te maken.</span><span class="sxs-lookup"><span data-stu-id="e557a-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]