---
title: Startpagina voor werkelijke waarden
description: Dit onderwerp biedt informatie over het werken met werkelijke waarden in Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907312"
---
# <a name="actuals"></a><span data-ttu-id="cb283-103">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cb283-103">Actuals</span></span>

<span data-ttu-id="cb283-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="cb283-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cb283-105">Werkelijke waarden zijn de hoeveelheid werk die is voltooid voor een project.</span><span class="sxs-lookup"><span data-stu-id="cb283-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="cb283-106">Ze worden gemaakt als resultaat van tijdsvermeldingen en onkostenposten, journaalboekingen en facturen.</span><span class="sxs-lookup"><span data-stu-id="cb283-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="cb283-107">Journaalregels en tijdsvermelding</span><span class="sxs-lookup"><span data-stu-id="cb283-107">Journal lines and time submission</span></span>

<span data-ttu-id="cb283-108">Zie voor meer informatie over tijdinvoer [Overzicht van tijdinvoer](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cb283-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="cb283-109">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="cb283-109">Time and materials</span></span>

<span data-ttu-id="cb283-110">Wanneer een ingediende tijdsvermelding is gekoppeld aan een project dat is toegewezen aan een contractregel voor tijd en materiaal, maakt het systeem twee journaalregels aan, één voor kosten en één voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="cb283-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="cb283-111">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="cb283-111">Fixed price</span></span>

<span data-ttu-id="cb283-112">Wanneer een ingediende tijdsvermelding is gekoppeld aan een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er één journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cb283-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="cb283-113">Standaardprijs</span><span class="sxs-lookup"><span data-stu-id="cb283-113">Default pricing</span></span>

<span data-ttu-id="cb283-114">De logica voor het maken van standaardprijzen bevindt zich op de journaalregel.</span><span class="sxs-lookup"><span data-stu-id="cb283-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="cb283-115">De veldwaarden uit de tijdsvermelding worden naar de journaalregel gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="cb283-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="cb283-116">Deze waarden bevatten de transactiedatum, de contractregel waaraan het project is toegewezen en het resultaat van de valuta in de juiste prijslijst.</span><span class="sxs-lookup"><span data-stu-id="cb283-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="cb283-117">De velden die van invloed zijn op standaardprijzen, zoals **Rol** en **Organisatie-eenheid** zorgen ervoor dat de juiste prijs standaard op de journaalregel wordt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="cb283-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="cb283-118">U kunt een aangepast veld toevoegen aan de tijdsvermelding.</span><span class="sxs-lookup"><span data-stu-id="cb283-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="cb283-119">Als u wilt dat de veldwaarde wordt doorgegeven aan werkelijke waarden, maakt u het veld in de entiteit Werkelijke waarden en gebruikt u veldtoewijzingen om het veld van de tijdsvermelding naar de werkelijke waarde te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="cb283-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="cb283-120">Indiening van journaalregels en basisonkosten</span><span class="sxs-lookup"><span data-stu-id="cb283-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="cb283-121">Zie voor meer informatie over de invoer van onkosten [Onkostenoverzicht](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cb283-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="cb283-122">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="cb283-122">Time and materials</span></span>

<span data-ttu-id="cb283-123">Wanneer ingediende basisonkosten zijn gekoppeld aan een project dat is toegewezen aan een contractregel voor tijd en materiaal, maakt het systeem twee journaalregels aan, één voor kosten en één voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="cb283-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="cb283-124">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="cb283-124">Fixed price</span></span>

<span data-ttu-id="cb283-125">Wanneer een ingediende basisonkostenvermelding is gekoppeld aan een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er één journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cb283-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="cb283-126">Standaardprijs</span><span class="sxs-lookup"><span data-stu-id="cb283-126">Default pricing</span></span>

<span data-ttu-id="cb283-127">De logica voor het invoeren van standaardprijzen voor onkosten is gebaseerd op de onkostencategorie.</span><span class="sxs-lookup"><span data-stu-id="cb283-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="cb283-128">De datum van de transactie, de contractregel waaraan het project is toegewezen en de valuta worden allemaal gebruikt om de juiste prijslijst te bepalen.</span><span class="sxs-lookup"><span data-stu-id="cb283-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="cb283-129">Het bedrag dat voor de prijs zelf wordt ingevoerd, wordt echter standaard rechtstreeks op de gerelateerde onkostenjournaalregels ingesteld voor kosten en verkoop.</span><span class="sxs-lookup"><span data-stu-id="cb283-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="cb283-130">De vermelding op categoriebasis van standaardprijzen per eenheid is niet beschikbaar voor onkostenposten.</span><span class="sxs-lookup"><span data-stu-id="cb283-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="cb283-131">Invoerjournalen gebruiken om kosten vast te leggen</span><span class="sxs-lookup"><span data-stu-id="cb283-131">Use entry journals to record costs</span></span>

<span data-ttu-id="cb283-132">U kunt invoerjournalen gebruiken om de kosten of onkosten vast te leggen in de klassen voor materiaal, tarief, tijd, onkosten of belastingtransactie.</span><span class="sxs-lookup"><span data-stu-id="cb283-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="cb283-133">U kunt de volgende journalen gebruiken voor de volgende doeleinden:</span><span class="sxs-lookup"><span data-stu-id="cb283-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="cb283-134">Leg de werkelijke materiaalkosten en verkopen voor een project vast.</span><span class="sxs-lookup"><span data-stu-id="cb283-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="cb283-135">Verplaats werkelijke transactiewaarden van een ander systeem naar Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="cb283-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="cb283-136">Leg kosten vast die zich in een ander systeem hebben voorgedaan.</span><span class="sxs-lookup"><span data-stu-id="cb283-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="cb283-137">Deze kosten kunnen inkoop- of uitbestedingskosten omvatten.</span><span class="sxs-lookup"><span data-stu-id="cb283-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb283-138">De toepassing valideert het journaalregeltype of de gerelateerde prijzen die op de journaalregel zijn ingevoerd niet.</span><span class="sxs-lookup"><span data-stu-id="cb283-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="cb283-139">Daarom mag alleen een gebruiker die zich volledig bewust is van de boekhoudkundige impact van werkelijke waarden op het project invoerjournalen gebruiken om werkelijke waarden te maken.</span><span class="sxs-lookup"><span data-stu-id="cb283-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="cb283-140">Vanwege de impact van dit journaaltype, moet u zorgvuldig kiezen wie toegang heeft om boekingsjournalen te maken.</span><span class="sxs-lookup"><span data-stu-id="cb283-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="cb283-141">Werkelijke waarden vastleggen op basis van projectgebeurtenissen</span><span class="sxs-lookup"><span data-stu-id="cb283-141">Record actuals based on project events</span></span>

<span data-ttu-id="cb283-142">In Project Operations worden de financiële transacties vastgelegd die tijdens een project plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="cb283-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="cb283-143">Deze transacties worden geregistreerd als werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="cb283-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="cb283-144">In de volgende tabellen ziet u de verschillende typen werkelijke waarden die worden gemaakt, afhankelijk van of het project een project op basis van tijd- en materiaalverbruik of een project met een vaste prijs is en of dit zich in de pre-salesfase bevindt of een intern project is.</span><span class="sxs-lookup"><span data-stu-id="cb283-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="cb283-145">De resource behoort tot dezelfde organisatie-eenheid als de contracterende eenheid van het project</span><span class="sxs-lookup"><span data-stu-id="cb283-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="cb283-146">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="cb283-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="cb283-147">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="cb283-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="cb283-148">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="cb283-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="cb283-149">Intern project</span><span class="sxs-lookup"><span data-stu-id="cb283-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="cb283-150">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="cb283-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="cb283-151">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="cb283-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="cb283-152">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cb283-152">Actuals</span></span></th>
<th><span data-ttu-id="cb283-153">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="cb283-153">Transaction currency</span></span></th>
<th><span data-ttu-id="cb283-154">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="cb283-154">Fixed price</span></span></th>
<th><span data-ttu-id="cb283-155">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="cb283-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cb283-156">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cb283-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="cb283-157">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cb283-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-158">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="cb283-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="cb283-159">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cb283-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cb283-160">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="cb283-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cb283-161">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-161">Cost actual</span></span></td>
<td><span data-ttu-id="cb283-162">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cb283-163">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="cb283-164">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="cb283-165">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="cb283-166">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-167">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="cb283-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="cb283-168">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cb283-169">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="cb283-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cb283-170">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-170">Cost actual</span></span></td>
<td><span data-ttu-id="cb283-171">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cb283-172">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="cb283-173">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cb283-174">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="cb283-175">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-176">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="cb283-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cb283-177">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-178">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="cb283-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cb283-179">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cb283-180">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="cb283-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cb283-181">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="cb283-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cb283-182">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cb283-183">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="cb283-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="cb283-184">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cb283-185">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="cb283-186">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-187">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="cb283-187">Billed sales</span></span></td>
<td><span data-ttu-id="cb283-188">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cb283-189">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="cb283-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cb283-190">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="cb283-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cb283-191">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cb283-192">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cb283-193">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cb283-194">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cb283-195">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-196">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="cb283-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cb283-197">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-198">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="cb283-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cb283-199">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cb283-200">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="cb283-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cb283-201">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="cb283-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cb283-202">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="cb283-203">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="cb283-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="cb283-204">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="cb283-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="cb283-205">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cb283-206">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="cb283-207">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-208">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="cb283-208">Billed sales</span></span></td>
<td><span data-ttu-id="cb283-209">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cb283-210">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="cb283-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cb283-211">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="cb283-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cb283-212">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-213">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="cb283-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="cb283-214">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-215">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="cb283-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="cb283-216">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="cb283-217">De resource behoort tot een andere organisatie-eenheid dan de contracterende eenheid van het project</span><span class="sxs-lookup"><span data-stu-id="cb283-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="cb283-218">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="cb283-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="cb283-219">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="cb283-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="cb283-220">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="cb283-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="cb283-221">Intern project</span><span class="sxs-lookup"><span data-stu-id="cb283-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="cb283-222">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="cb283-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="cb283-223">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="cb283-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="cb283-224">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cb283-224">Actuals</span></span></th>
<th><span data-ttu-id="cb283-225">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="cb283-225">Transaction currency</span></span></th>
<th><span data-ttu-id="cb283-226">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="cb283-226">Fixed price</span></span></th>
<th><span data-ttu-id="cb283-227">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="cb283-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cb283-228">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cb283-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="cb283-229">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cb283-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-230">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="cb283-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="cb283-231">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cb283-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="cb283-232">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="cb283-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cb283-233">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-233">Cost actual</span></span></td>
<td><span data-ttu-id="cb283-234">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="cb283-235">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="cb283-236">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="cb283-237">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="cb283-238">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-239">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="cb283-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="cb283-240">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-241">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="cb283-242">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-243">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="cb283-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="cb283-244">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="cb283-245">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="cb283-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cb283-246">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-246">Cost actual</span></span></td>
<td><span data-ttu-id="cb283-247">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cb283-248">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="cb283-249">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cb283-250">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="cb283-251">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cb283-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-252">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="cb283-253">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-254">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="cb283-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="cb283-255">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cb283-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-256">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="cb283-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cb283-257">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-258">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="cb283-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cb283-259">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cb283-260">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="cb283-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cb283-261">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="cb283-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cb283-262">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cb283-263">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="cb283-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="cb283-264">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cb283-265">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="cb283-266">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-267">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="cb283-267">Billed sales</span></span></td>
<td><span data-ttu-id="cb283-268">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cb283-269">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="cb283-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cb283-270">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="cb283-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cb283-271">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cb283-272">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cb283-273">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cb283-274">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cb283-275">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-276">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="cb283-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cb283-277">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-278">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="cb283-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cb283-279">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cb283-280">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="cb283-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cb283-281">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="cb283-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cb283-282">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="cb283-283">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="cb283-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="cb283-284">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="cb283-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="cb283-285">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cb283-286">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="cb283-287">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cb283-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-288">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="cb283-288">Billed sales</span></span></td>
<td><span data-ttu-id="cb283-289">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cb283-290">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="cb283-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cb283-291">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="cb283-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cb283-292">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-293">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="cb283-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="cb283-294">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb283-295">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="cb283-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="cb283-296">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cb283-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
