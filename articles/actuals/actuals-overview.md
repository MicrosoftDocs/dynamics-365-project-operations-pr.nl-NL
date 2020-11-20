---
title: Werkelijke waarden
description: Dit onderwerp biedt informatie over het werken met werkelijke waarden in Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126297"
---
# <a name="actuals"></a><span data-ttu-id="7b62d-103">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="7b62d-103">Actuals</span></span> 

<span data-ttu-id="7b62d-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="7b62d-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7b62d-105">Werkelijke waarden zijn de hoeveelheid werk die is voltooid voor een project.</span><span class="sxs-lookup"><span data-stu-id="7b62d-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="7b62d-106">Ze worden gemaakt als resultaat van tijdsvermeldingen en onkostenposten, journaalboekingen en facturen.</span><span class="sxs-lookup"><span data-stu-id="7b62d-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="7b62d-107">Journaalregels en tijdsvermelding</span><span class="sxs-lookup"><span data-stu-id="7b62d-107">Journal lines and time submission</span></span>

<span data-ttu-id="7b62d-108">Zie voor meer informatie over tijdinvoer [Overzicht van tijdinvoer](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7b62d-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="7b62d-109">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="7b62d-109">Time and materials</span></span>

<span data-ttu-id="7b62d-110">Wanneer een ingediende tijdsvermelding is gekoppeld aan een project dat is toegewezen aan een contractregel voor tijd en materiaal, maakt het systeem twee journaalregels aan, één voor kosten en één voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="7b62d-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="7b62d-111">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="7b62d-111">Fixed price</span></span>

<span data-ttu-id="7b62d-112">Wanneer een ingediende tijdsvermelding is gekoppeld aan een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er één journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7b62d-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="7b62d-113">Standaardprijs</span><span class="sxs-lookup"><span data-stu-id="7b62d-113">Default pricing</span></span>

<span data-ttu-id="7b62d-114">De logica voor het maken van standaardprijzen bevindt zich op de journaalregel.</span><span class="sxs-lookup"><span data-stu-id="7b62d-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="7b62d-115">De veldwaarden uit de tijdsvermelding worden naar de journaalregel gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="7b62d-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="7b62d-116">Deze waarden bevatten de transactiedatum, de contractregel waaraan het project is toegewezen en het resultaat van de valuta in de juiste prijslijst.</span><span class="sxs-lookup"><span data-stu-id="7b62d-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="7b62d-117">De velden die van invloed zijn op standaardprijzen, zoals **Rol** en **Organisatie-eenheid** zorgen ervoor dat de juiste prijs standaard op de journaalregel wordt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="7b62d-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="7b62d-118">U kunt een aangepast veld toevoegen aan de tijdsvermelding.</span><span class="sxs-lookup"><span data-stu-id="7b62d-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="7b62d-119">Als u wilt dat de veldwaarde wordt doorgegeven aan werkelijke waarden, maakt u het veld in de entiteit Werkelijke waarden en gebruikt u veldtoewijzingen om het veld van de tijdsvermelding naar de werkelijke waarde te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="7b62d-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="7b62d-120">Indiening van journaalregels en basisonkosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="7b62d-121">Zie voor meer informatie over de invoer van onkosten [Onkostenoverzicht](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7b62d-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="7b62d-122">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="7b62d-122">Time and materials</span></span>

<span data-ttu-id="7b62d-123">Wanneer ingediende basisonkosten zijn gekoppeld aan een project dat is toegewezen aan een contractregel voor tijd en materiaal, maakt het systeem twee journaalregels aan, één voor kosten en één voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="7b62d-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="7b62d-124">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="7b62d-124">Fixed price</span></span>

<span data-ttu-id="7b62d-125">Wanneer een ingediende basisonkostenvermelding is gekoppeld aan een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er één journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7b62d-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="7b62d-126">Standaardprijs</span><span class="sxs-lookup"><span data-stu-id="7b62d-126">Default pricing</span></span>

<span data-ttu-id="7b62d-127">De logica voor het invoeren van standaardprijzen voor onkosten is gebaseerd op de onkostencategorie.</span><span class="sxs-lookup"><span data-stu-id="7b62d-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="7b62d-128">De datum van de transactie, de contractregel waaraan het project is toegewezen en de valuta worden allemaal gebruikt om de juiste prijslijst te bepalen.</span><span class="sxs-lookup"><span data-stu-id="7b62d-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="7b62d-129">Het bedrag dat voor de prijs zelf wordt ingevoerd, wordt echter standaard rechtstreeks op de gerelateerde onkostenjournaalregels ingesteld voor kosten en verkoop.</span><span class="sxs-lookup"><span data-stu-id="7b62d-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="7b62d-130">De vermelding op categoriebasis van standaardprijzen per eenheid is niet beschikbaar voor onkostenposten.</span><span class="sxs-lookup"><span data-stu-id="7b62d-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="7b62d-131">Invoerjournalen gebruiken om kosten vast te leggen</span><span class="sxs-lookup"><span data-stu-id="7b62d-131">Use entry journals to record costs</span></span>

<span data-ttu-id="7b62d-132">U kunt invoerjournalen gebruiken om de kosten of onkosten vast te leggen in de klassen voor materiaal, tarief, tijd, onkosten of belastingtransactie.</span><span class="sxs-lookup"><span data-stu-id="7b62d-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="7b62d-133">U kunt de volgende journalen gebruiken voor de volgende doeleinden:</span><span class="sxs-lookup"><span data-stu-id="7b62d-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="7b62d-134">Leg de werkelijke materiaalkosten en verkopen voor een project vast.</span><span class="sxs-lookup"><span data-stu-id="7b62d-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="7b62d-135">Verplaats werkelijke transactiewaarden van een ander systeem naar Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7b62d-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="7b62d-136">Leg kosten vast die zich in een ander systeem hebben voorgedaan.</span><span class="sxs-lookup"><span data-stu-id="7b62d-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="7b62d-137">Deze kosten kunnen inkoop- of uitbestedingskosten omvatten.</span><span class="sxs-lookup"><span data-stu-id="7b62d-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b62d-138">De toepassing valideert het journaalregeltype of de gerelateerde prijzen die op de journaalregel zijn ingevoerd niet.</span><span class="sxs-lookup"><span data-stu-id="7b62d-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="7b62d-139">Daarom mag alleen een gebruiker die zich volledig bewust is van de boekhoudkundige impact van werkelijke waarden op het project invoerjournalen gebruiken om werkelijke waarden te maken.</span><span class="sxs-lookup"><span data-stu-id="7b62d-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="7b62d-140">Vanwege de impact van dit journaaltype, moet u zorgvuldig kiezen wie toegang heeft om boekingsjournalen te maken.</span><span class="sxs-lookup"><span data-stu-id="7b62d-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="7b62d-141">Werkelijke waarden vastleggen op basis van projectgebeurtenissen</span><span class="sxs-lookup"><span data-stu-id="7b62d-141">Record actuals based on project events</span></span>

<span data-ttu-id="7b62d-142">In Project Operations worden de financiële transacties vastgelegd die tijdens een project plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="7b62d-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="7b62d-143">Deze transacties worden geregistreerd als werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="7b62d-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="7b62d-144">In de volgende tabellen ziet u de verschillende typen werkelijke waarden die worden gemaakt, afhankelijk van of het project een project op basis van tijd- en materiaalverbruik of een project met een vaste prijs is en of dit zich in de pre-salesfase bevindt of een intern project is.</span><span class="sxs-lookup"><span data-stu-id="7b62d-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="7b62d-145">De resource behoort tot dezelfde organisatie-eenheid als de contracterende eenheid van het project</span><span class="sxs-lookup"><span data-stu-id="7b62d-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="7b62d-146">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="7b62d-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="7b62d-147">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="7b62d-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="7b62d-148">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="7b62d-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="7b62d-149">Intern project</span><span class="sxs-lookup"><span data-stu-id="7b62d-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="7b62d-150">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="7b62d-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="7b62d-151">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="7b62d-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7b62d-152">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="7b62d-152">Actuals</span></span></th>
<th><span data-ttu-id="7b62d-153">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="7b62d-153">Transaction currency</span></span></th>
<th><span data-ttu-id="7b62d-154">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="7b62d-154">Fixed price</span></span></th>
<th><span data-ttu-id="7b62d-155">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="7b62d-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7b62d-156">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7b62d-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="7b62d-157">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="7b62d-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-158">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="7b62d-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="7b62d-159">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="7b62d-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7b62d-160">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="7b62d-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="7b62d-161">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-161">Cost actual</span></span></td>
<td><span data-ttu-id="7b62d-162">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7b62d-163">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="7b62d-164">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="7b62d-165">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="7b62d-166">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-167">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="7b62d-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="7b62d-168">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7b62d-169">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="7b62d-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="7b62d-170">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-170">Cost actual</span></span></td>
<td><span data-ttu-id="7b62d-171">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="7b62d-172">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="7b62d-173">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="7b62d-174">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="7b62d-175">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-176">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="7b62d-177">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-178">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="7b62d-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="7b62d-179">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7b62d-180">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="7b62d-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="7b62d-181">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="7b62d-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="7b62d-182">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7b62d-183">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="7b62d-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="7b62d-184">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7b62d-185">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="7b62d-186">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-187">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="7b62d-187">Billed sales</span></span></td>
<td><span data-ttu-id="7b62d-188">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7b62d-189">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="7b62d-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="7b62d-190">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="7b62d-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="7b62d-191">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="7b62d-192">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7b62d-193">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7b62d-194">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7b62d-195">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-196">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="7b62d-197">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-198">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="7b62d-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="7b62d-199">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7b62d-200">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="7b62d-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="7b62d-201">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="7b62d-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="7b62d-202">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="7b62d-203">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="7b62d-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="7b62d-204">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="7b62d-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="7b62d-205">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="7b62d-206">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="7b62d-207">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-208">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="7b62d-208">Billed sales</span></span></td>
<td><span data-ttu-id="7b62d-209">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7b62d-210">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="7b62d-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="7b62d-211">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="7b62d-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="7b62d-212">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-213">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="7b62d-214">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-215">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="7b62d-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="7b62d-216">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="7b62d-217">De resource behoort tot een andere organisatie-eenheid dan de contracterende eenheid van het project</span><span class="sxs-lookup"><span data-stu-id="7b62d-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="7b62d-218">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="7b62d-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="7b62d-219">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="7b62d-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="7b62d-220">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="7b62d-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="7b62d-221">Intern project</span><span class="sxs-lookup"><span data-stu-id="7b62d-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="7b62d-222">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="7b62d-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="7b62d-223">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="7b62d-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7b62d-224">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="7b62d-224">Actuals</span></span></th>
<th><span data-ttu-id="7b62d-225">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="7b62d-225">Transaction currency</span></span></th>
<th><span data-ttu-id="7b62d-226">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="7b62d-226">Fixed price</span></span></th>
<th><span data-ttu-id="7b62d-227">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="7b62d-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7b62d-228">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7b62d-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="7b62d-229">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="7b62d-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-230">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="7b62d-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="7b62d-231">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="7b62d-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="7b62d-232">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="7b62d-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="7b62d-233">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-233">Cost actual</span></span></td>
<td><span data-ttu-id="7b62d-234">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="7b62d-235">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="7b62d-236">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="7b62d-237">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="7b62d-238">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-239">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="7b62d-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="7b62d-240">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-241">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="7b62d-242">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-243">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="7b62d-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="7b62d-244">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="7b62d-245">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="7b62d-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="7b62d-246">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-246">Cost actual</span></span></td>
<td><span data-ttu-id="7b62d-247">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="7b62d-248">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="7b62d-249">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="7b62d-250">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="7b62d-251">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="7b62d-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-252">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="7b62d-253">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-254">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="7b62d-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="7b62d-255">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-256">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="7b62d-257">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-258">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="7b62d-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="7b62d-259">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7b62d-260">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="7b62d-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="7b62d-261">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="7b62d-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="7b62d-262">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7b62d-263">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="7b62d-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="7b62d-264">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7b62d-265">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="7b62d-266">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-267">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="7b62d-267">Billed sales</span></span></td>
<td><span data-ttu-id="7b62d-268">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7b62d-269">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="7b62d-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="7b62d-270">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="7b62d-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="7b62d-271">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="7b62d-272">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7b62d-273">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7b62d-274">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7b62d-275">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-276">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="7b62d-277">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-278">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="7b62d-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="7b62d-279">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7b62d-280">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="7b62d-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="7b62d-281">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="7b62d-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="7b62d-282">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="7b62d-283">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="7b62d-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="7b62d-284">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="7b62d-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="7b62d-285">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="7b62d-286">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="7b62d-287">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="7b62d-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-288">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="7b62d-288">Billed sales</span></span></td>
<td><span data-ttu-id="7b62d-289">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7b62d-290">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="7b62d-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="7b62d-291">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="7b62d-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="7b62d-292">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-293">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7b62d-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="7b62d-294">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7b62d-295">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="7b62d-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="7b62d-296">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="7b62d-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
