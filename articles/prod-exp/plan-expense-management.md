---
title: Onkostenbeheer configureren
description: In dit artikel worden de overwegingen en beslissingen beschreven die u tijdens het planningsproces moet maken voordat u Onkostenbeheer in Microsoft Dynamics 365 Finance configureert.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2291515cc154fb5b34ca5802135791958bea1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074712"
---
# <a name="configure-expense-management"></a><span data-ttu-id="be3dc-103">Onkostenbeheer configureren</span><span class="sxs-lookup"><span data-stu-id="be3dc-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be3dc-104">In dit onderwerp worden de overwegingen en beslissingen beschreven die u tijdens het planningsproces moet maken voordat u Onkostenbeheer configureert.</span><span class="sxs-lookup"><span data-stu-id="be3dc-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="be3dc-105">In Onkostenbeheer kunt u informatie opslaan over betalingswijzen, reisaanvragen, onkostendeclaraties, beleid, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="be3dc-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="be3dc-106">Omdat veel van de beslissingen die u neemt wanneer u uw configuratie voor Onkostenbeheer plant, is gebaseerd op de hiërarchie en financiële structuur van uw organisatie, moet u de planningsdocumenten voor deze gebieden raadplegen.</span><span class="sxs-lookup"><span data-stu-id="be3dc-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="be3dc-107">Intercompany-onkosten</span><span class="sxs-lookup"><span data-stu-id="be3dc-107">Intercompany expenses</span></span>

<span data-ttu-id="be3dc-108">Wanneer u intercompany-onkosten inschakelt, staat u rechtspersonen en werknemers toe om kosten te maken namens een andere rechtspersoon, en ontvangt u betalingen van de rechtspersoon waarvoor werk wordt uitgevoerd binnen uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="be3dc-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="be3dc-109">Een werknemer in rechtspersoon A voltooit bijvoorbeeld een project voor rechtspersoon B, en voor het project worden reisgerelateerde kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="be3dc-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="be3dc-110">Als intercompany-onkosten worden ingeschakeld, kan de werknemer een onkostendeclaratie indienen waarmee de onkosten naar rechtspersoon B worden geboekt, en de onkosten moeten vervolgens worden betaald door rechtspersoon A. Als uw organisatie geen meerdere rechtspersonen heeft, hoeft u geen intercompany-onkosten in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="be3dc-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="be3dc-111">**Beslissing:** wilt u intercompany-onkosten inschakelen?</span><span class="sxs-lookup"><span data-stu-id="be3dc-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="be3dc-112">Financieel beheer</span><span class="sxs-lookup"><span data-stu-id="be3dc-112">Financial management</span></span>

<span data-ttu-id="be3dc-113">Onkostenbeheer is nauw geïntegreerd met het financiële beheer van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="be3dc-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="be3dc-114">Een groot deel van uw configuratie voor Onkostenbeheer wordt gebaseerd op de beslissingen die u hebt genomen over de financiën van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="be3dc-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="be3dc-115">In de volgende secties worden de verschillende gebieden beschreven waarvoor planning en beslissingen nodig zijn, op basis van de financiële beslissingen van uw organisatie en de begeleiding van uw leidinggevende team.</span><span class="sxs-lookup"><span data-stu-id="be3dc-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="be3dc-116">Dagvergoedingen</span><span class="sxs-lookup"><span data-stu-id="be3dc-116">Per diems</span></span>

<span data-ttu-id="be3dc-117">U moet de dagvergoedingen voor werknemers definiëren die uw organisatie biedt.</span><span class="sxs-lookup"><span data-stu-id="be3dc-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="be3dc-118">Omdat dagvergoedingen doorgaans worden gebruikt om onkosten te dekken, zoals maaltijden, huisvesting en andere incidentele uitgaven, kunt u regels opstellen voor de dagvergoedingen die uw organisatie aanbiedt.</span><span class="sxs-lookup"><span data-stu-id="be3dc-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="be3dc-119">Dagvergoedingstarieven kunnen worden gebaseerd op de tijd van het jaar, de reislocatie of beide.</span><span class="sxs-lookup"><span data-stu-id="be3dc-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="be3dc-120">Wanneer u een dagvergoedingsregel definieert, kunt u opgeven dat een percentage van het dagvergoedingstarief wordt ingehouden als een werknemer gratis maaltijden of diensten ontvangt.</span><span class="sxs-lookup"><span data-stu-id="be3dc-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="be3dc-121">U kunt ook niveaus voor dagvergoedingstarieven definiëren om het minimum en maximum aantal uren in te stellen dat het dagvergoedingstarief op de reis van een werknemer kan worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="be3dc-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="be3dc-122">**Beslissingen:**</span><span class="sxs-lookup"><span data-stu-id="be3dc-122">**Decisions:**</span></span>

- <span data-ttu-id="be3dc-123">Standaardregels voor dagvergoedingen voor de eerste en laatste dag:</span><span class="sxs-lookup"><span data-stu-id="be3dc-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="be3dc-124">Wat is het minimum aantal uren dat een werknemer per dag kan claimen en toch een dagvergoeding kan ontvangen?</span><span class="sxs-lookup"><span data-stu-id="be3dc-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="be3dc-125">Is er een verlaging van het bedrag dat wordt aangeboden voor maaltijden voor de eerste dag en de laatste dag?</span><span class="sxs-lookup"><span data-stu-id="be3dc-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="be3dc-126">Als er een verlaging is, wat is dan het percentage van de verlaging?</span><span class="sxs-lookup"><span data-stu-id="be3dc-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="be3dc-127">Is er een verlaging van het bedrag dat wordt aangeboden voor een hotel voor de eerste en laatste dag?</span><span class="sxs-lookup"><span data-stu-id="be3dc-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="be3dc-128">Als er een verlaging is, wat is dan het percentage van de verlaging?</span><span class="sxs-lookup"><span data-stu-id="be3dc-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="be3dc-129">Is er een verlaging van het bedrag dat wordt aangeboden voor andere onkosten die worden gemaakt op de eerste en laatste dag?</span><span class="sxs-lookup"><span data-stu-id="be3dc-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="be3dc-130">Als er een verlaging is, wat is dan het percentage van de verlaging?</span><span class="sxs-lookup"><span data-stu-id="be3dc-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="be3dc-131">Standaardregels voor dagvergoedingen:</span><span class="sxs-lookup"><span data-stu-id="be3dc-131">Default per diem rules:</span></span>

    - <span data-ttu-id="be3dc-132">Is er een procentuele verlaging in de dagvergoeding voor elke maaltijd als de maaltijd bijvoorbeeld gratis is?</span><span class="sxs-lookup"><span data-stu-id="be3dc-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="be3dc-133">Als er een verlaging is, wat is dan het percentage van de verlaging voor elke maaltijd?</span><span class="sxs-lookup"><span data-stu-id="be3dc-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="be3dc-134">Wordt de maaltijdreductie berekend per dag, per reis of op basis van het aantal maaltijden per dag?</span><span class="sxs-lookup"><span data-stu-id="be3dc-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="be3dc-135">Moeten bedragen van dagvergoedingen op de reguliere manier worden afgerond of moeten ze naar boven worden afgerond?</span><span class="sxs-lookup"><span data-stu-id="be3dc-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="be3dc-136">Worden dagvergoedingen berekend over een periode van 24 uur of op een kalenderdag?</span><span class="sxs-lookup"><span data-stu-id="be3dc-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="be3dc-137">Dagvergoedingsregels die op locatie worden gebaseerd:</span><span class="sxs-lookup"><span data-stu-id="be3dc-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="be3dc-138">Variëren de dagvergoedingstarieven afhankelijk van de locatie?</span><span class="sxs-lookup"><span data-stu-id="be3dc-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="be3dc-139">Welke locaties zijn opgenomen?</span><span class="sxs-lookup"><span data-stu-id="be3dc-139">What locations are included?</span></span>
    - <span data-ttu-id="be3dc-140">Als dagvergoedingstarieven per locatie verschillen, welk percentagebedrag wordt dan voor elke locatie verstrekt voor de volgende soorten onkosten:</span><span class="sxs-lookup"><span data-stu-id="be3dc-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="be3dc-141">Maaltijden</span><span class="sxs-lookup"><span data-stu-id="be3dc-141">Meals</span></span>
        - <span data-ttu-id="be3dc-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="be3dc-142">Hotel</span></span>
        - <span data-ttu-id="be3dc-143">Overige onkosten</span><span class="sxs-lookup"><span data-stu-id="be3dc-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="be3dc-144">Journalen en rekeningen voor onkostendeclaraties</span><span class="sxs-lookup"><span data-stu-id="be3dc-144">Expense management journals and accounts</span></span>

<span data-ttu-id="be3dc-145">Voor Onkostenbeheer moet u meerdere journalen en rekeningen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="be3dc-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="be3dc-146">U moet bijvoorbeeld beslissen of dezelfde rekening wordt gebruikt voor kasvoorschotten en creditcardgeschillen.</span><span class="sxs-lookup"><span data-stu-id="be3dc-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="be3dc-147">**Beslissingen:**</span><span class="sxs-lookup"><span data-stu-id="be3dc-147">**Decisions:**</span></span>

- <span data-ttu-id="be3dc-148">Naar welke grootboekjournalen mogen onkostendeclaraties worden geboekt?</span><span class="sxs-lookup"><span data-stu-id="be3dc-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="be3dc-149">Welke rekening wordt gebruikt voor kasvoorschotten?</span><span class="sxs-lookup"><span data-stu-id="be3dc-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="be3dc-150">Moeten kasvoorschotten onmiddellijk worden geboekt?</span><span class="sxs-lookup"><span data-stu-id="be3dc-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="be3dc-151">Betalingswijzen</span><span class="sxs-lookup"><span data-stu-id="be3dc-151">Payment methods</span></span>

<span data-ttu-id="be3dc-152">Wanneer u werknemers toestaat om onkosten te maken namens uw bedrijf, moet u de betalingswijzen definiëren die werknemers mogen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="be3dc-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="be3dc-153">U kunt bijvoorbeeld werknemers toestaan om contant geld of een bedrijfscreditcard te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="be3dc-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="be3dc-154">U kunt werknemers ook toestaan persoonlijke creditcards te gebruiken en de werknemers vervolgens vergoeden.</span><span class="sxs-lookup"><span data-stu-id="be3dc-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="be3dc-155">U moet de volgende beslissingen nemen voor elke betalingswijze die u toestaat.</span><span class="sxs-lookup"><span data-stu-id="be3dc-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="be3dc-156">**Beslissingen:**</span><span class="sxs-lookup"><span data-stu-id="be3dc-156">**Decisions:**</span></span>

- <span data-ttu-id="be3dc-157">Welke betalingswijzen zijn toegestaan?</span><span class="sxs-lookup"><span data-stu-id="be3dc-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="be3dc-158">Wie is de eigenaar van de onkosten van de betalingswijze?</span><span class="sxs-lookup"><span data-stu-id="be3dc-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="be3dc-159">Is er een tegenrekeningtype?</span><span class="sxs-lookup"><span data-stu-id="be3dc-159">Is there an offset account type?</span></span> <span data-ttu-id="be3dc-160">Als er een tegenrekeningtype is, welke is dat dan?</span><span class="sxs-lookup"><span data-stu-id="be3dc-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="be3dc-161">Als er een tegenrekening is, wat is de rekening dan?</span><span class="sxs-lookup"><span data-stu-id="be3dc-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="be3dc-162">Als de betalingswijze een creditcard is, mag de betalingswijze dan alleen worden gebruikt bij geïmporteerde transacties?</span><span class="sxs-lookup"><span data-stu-id="be3dc-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="be3dc-163">Onkostencategorieën en gedeelde categorieën</span><span class="sxs-lookup"><span data-stu-id="be3dc-163">Expense categories and shared categories</span></span>

<span data-ttu-id="be3dc-164">Wanneer werknemers een onkostendeclaratie maken, moeten alle onkosten die ze registreren, aan een onkostencategorie worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="be3dc-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="be3dc-165">Onkostencategorieën zijn afgeleid van gedeelde categorieën die kunnen worden gedeeld door de rechtspersonen in uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="be3dc-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="be3dc-166">Deze categorieën kunnen ook worden gedeeld in Projectbeheer en financiële administratie, afhankelijk van de manier waarop uw organisatie is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="be3dc-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="be3dc-167">Op basis van de definitie van uw organisatie en de richtlijnen van het implementatieteam moet u bepalen of de categorieën die worden gebruikt in Onkostenbeheer alleen worden gebruikt in Onkostenbeheer of dat ze moeten worden gedeeld tussen Projectbeheer en financiële administratie en Onkostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="be3dc-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="be3dc-168">Deze categorieën kunnen worden gedeeld tussen Project en Onkosten of Project en Productie, maar niet tussen Onkosten en Productie.</span><span class="sxs-lookup"><span data-stu-id="be3dc-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="be3dc-169">Voor elke onkostencategorie moet u de volgende beslissingen nemen.</span><span class="sxs-lookup"><span data-stu-id="be3dc-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="be3dc-170">**Beslissingen:**</span><span class="sxs-lookup"><span data-stu-id="be3dc-170">**Decisions:**</span></span>

- <span data-ttu-id="be3dc-171">Wat is de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="be3dc-171">What is the expense category?</span></span> <span data-ttu-id="be3dc-172">Voorbeelden zijn categorieën voor vluchten, hotel of kilometerstand.</span><span class="sxs-lookup"><span data-stu-id="be3dc-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="be3dc-173">Kan de onkostencategorie ook worden gebruikt in Projectmanagement en financiële administratie?</span><span class="sxs-lookup"><span data-stu-id="be3dc-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="be3dc-174">Wat is het onkostentype?</span><span class="sxs-lookup"><span data-stu-id="be3dc-174">What is the expense type?</span></span>
- <span data-ttu-id="be3dc-175">Wat is de standaard betalingsmethode voor de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="be3dc-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="be3dc-176">Moeten onkosten in de onkostencategorie gespecificeerd worden?</span><span class="sxs-lookup"><span data-stu-id="be3dc-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="be3dc-177">Wat is de standaard hoofdrekening voor de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="be3dc-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="be3dc-178">Wat is de standaard btw-groep van artikelen voor de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="be3dc-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="be3dc-179">Zijn aanvullende betalingsmethoden toegestaan voor de onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="be3dc-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="be3dc-180">Als aanvullende betalingswijzen zijn toegestaan, welke zijn dat dan?</span><span class="sxs-lookup"><span data-stu-id="be3dc-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="be3dc-181">Zijn er subcategorieën in deze onkostencategorie?</span><span class="sxs-lookup"><span data-stu-id="be3dc-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="be3dc-182">Als er subcategorieën zijn, moet u bovendien de volgende beslissingen nemen:</span><span class="sxs-lookup"><span data-stu-id="be3dc-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="be3dc-183">Zijn subcategorieën uitgesloten van belastingteruggave?</span><span class="sxs-lookup"><span data-stu-id="be3dc-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="be3dc-184">Wat is de btw-groep van de subcategorieën?</span><span class="sxs-lookup"><span data-stu-id="be3dc-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="be3dc-185">Als de onkostencategorie ook wordt gebruikt in Projectbeheer en financiële administratie, beantwoord dan de overige vragen.</span><span class="sxs-lookup"><span data-stu-id="be3dc-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="be3dc-186">Ga anders naar de volgende sectie.</span><span class="sxs-lookup"><span data-stu-id="be3dc-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="be3dc-187">Welke kostenrekeningen worden gebruikt voor de volgende uitgaven?</span><span class="sxs-lookup"><span data-stu-id="be3dc-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="be3dc-188">Kosten</span><span class="sxs-lookup"><span data-stu-id="be3dc-188">Cost</span></span>
    - <span data-ttu-id="be3dc-189">Salaristoewijzing</span><span class="sxs-lookup"><span data-stu-id="be3dc-189">Payroll allocation</span></span>
    - <span data-ttu-id="be3dc-190">OHW - waarde van kostprijs</span><span class="sxs-lookup"><span data-stu-id="be3dc-190">WIP-cost value</span></span>
    - <span data-ttu-id="be3dc-191">Kosten - artikel</span><span class="sxs-lookup"><span data-stu-id="be3dc-191">Cost-item</span></span>
    - <span data-ttu-id="be3dc-192">OHW - waarde van kostprijs - artikel</span><span class="sxs-lookup"><span data-stu-id="be3dc-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="be3dc-193">Opgelopen verlies</span><span class="sxs-lookup"><span data-stu-id="be3dc-193">Accrued loss</span></span>
    - <span data-ttu-id="be3dc-194">Opgelopen verlies OHW</span><span class="sxs-lookup"><span data-stu-id="be3dc-194">WIP-accrued loss</span></span>

- <span data-ttu-id="be3dc-195">Welke inkomstenrekeningen worden gebruikt voor het volgende?</span><span class="sxs-lookup"><span data-stu-id="be3dc-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="be3dc-196">Gefactureerde omzet</span><span class="sxs-lookup"><span data-stu-id="be3dc-196">Invoiced revenue</span></span>
    - <span data-ttu-id="be3dc-197">Toegerekende omzet - verkoopwaarde</span><span class="sxs-lookup"><span data-stu-id="be3dc-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="be3dc-198">OHW - verkoopwaarde</span><span class="sxs-lookup"><span data-stu-id="be3dc-198">WIP-sales value</span></span>
    - <span data-ttu-id="be3dc-199">Opgebouwde opbrengst - productie</span><span class="sxs-lookup"><span data-stu-id="be3dc-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="be3dc-200">OHW - productie</span><span class="sxs-lookup"><span data-stu-id="be3dc-200">WIP-production</span></span>
    - <span data-ttu-id="be3dc-201">Opgebouwde opbrengst - winst</span><span class="sxs-lookup"><span data-stu-id="be3dc-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="be3dc-202">OHW - winst</span><span class="sxs-lookup"><span data-stu-id="be3dc-202">WIP-profit</span></span>
    - <span data-ttu-id="be3dc-203">Opgebouwde opbrengst - abonnement</span><span class="sxs-lookup"><span data-stu-id="be3dc-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="be3dc-204">OHW - abonnement</span><span class="sxs-lookup"><span data-stu-id="be3dc-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="be3dc-205">Belastingen</span><span class="sxs-lookup"><span data-stu-id="be3dc-205">Taxes</span></span>

<span data-ttu-id="be3dc-206">Voor onkostengerelateerde belastingen moet u bepalen wat is opgenomen of ingeschakeld in onkostendeclaraties.</span><span class="sxs-lookup"><span data-stu-id="be3dc-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="be3dc-207">**Beslissingen:**</span><span class="sxs-lookup"><span data-stu-id="be3dc-207">**Decisions:**</span></span>

- <span data-ttu-id="be3dc-208">Is verkoopbelasting inbegrepen in de onkostenbedragen?</span><span class="sxs-lookup"><span data-stu-id="be3dc-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="be3dc-209">Moet belastingteruggave voor onkosten worden ingeschakeld?</span><span class="sxs-lookup"><span data-stu-id="be3dc-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="be3dc-210">Als u bij het plannen van het grootboek besloot om Amerikaanse verkoopbelasting toe te passen en belastingregels te gebruiken, kunt u geen belastingteruggave voor onkosten inschakelen.</span><span class="sxs-lookup"><span data-stu-id="be3dc-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="be3dc-211">(Als u Amerikaanse verkoopbelasting wilt toepassen en belastingregels wilt gebruiken, stelt u de optie **Belastingregels voor verkoopbelasting toepassen** in op **Ja**.)</span><span class="sxs-lookup"><span data-stu-id="be3dc-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="be3dc-212">Beleidsregels</span><span class="sxs-lookup"><span data-stu-id="be3dc-212">Policies</span></span>

<span data-ttu-id="be3dc-213">Door beleid voor onkostendeclaraties op te stellen, kunt u uw organisatie helpen tijd en geld te besparen wanneer werknemers namens de organisatie onkosten maken.</span><span class="sxs-lookup"><span data-stu-id="be3dc-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="be3dc-214">Beleid helpt ervoor te zorgen dat werknemers binnen budget blijven, alle vereiste informatie verstrekken en alleen geld uitgeven wanneer ze het nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="be3dc-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="be3dc-215">U moet de volgende beslissingen nemen voor elk onkostendeclaratiebeleid en elk goedkeuringsbeleid voor onkostendeclaraties dat u opstelt.</span><span class="sxs-lookup"><span data-stu-id="be3dc-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="be3dc-216">**Beslissingen:**</span><span class="sxs-lookup"><span data-stu-id="be3dc-216">**Decisions:**</span></span>

- <span data-ttu-id="be3dc-217">Wat is de naam van het beleid?</span><span class="sxs-lookup"><span data-stu-id="be3dc-217">What is the name of the policy?</span></span>
- <span data-ttu-id="be3dc-218">Waar dient het onkostenbeleid voor?</span><span class="sxs-lookup"><span data-stu-id="be3dc-218">What is the expense policy for?</span></span>
- <span data-ttu-id="be3dc-219">Als u eerder hebt besloten intercompany-onkosten in te schakelen, op welke bedrijven in uw organisatie is dit beleid dan van toepassing?</span><span class="sxs-lookup"><span data-stu-id="be3dc-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="be3dc-220">Wanneer is het beleid van kracht?</span><span class="sxs-lookup"><span data-stu-id="be3dc-220">When does the policy become effective?</span></span>
- <span data-ttu-id="be3dc-221">Wanneer verloopt het beleid?</span><span class="sxs-lookup"><span data-stu-id="be3dc-221">When does the policy expire?</span></span>
- <span data-ttu-id="be3dc-222">Wat is de beleidsregel?</span><span class="sxs-lookup"><span data-stu-id="be3dc-222">What is the policy rule?</span></span>
- <span data-ttu-id="be3dc-223">Wat is het resultaat van de beleidsregel?</span><span class="sxs-lookup"><span data-stu-id="be3dc-223">What is the outcome of the policy rule?</span></span>
