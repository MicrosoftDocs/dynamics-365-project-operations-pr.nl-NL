---
title: Werkelijke waarden
description: Dit onderwerp biedt informatie over het werken met werkelijke waarden in Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074554"
---
# <a name="actuals"></a><span data-ttu-id="0d10b-103">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="0d10b-103">Actuals</span></span> 

<span data-ttu-id="0d10b-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="0d10b-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0d10b-105">Werkelijke waarden zijn de hoeveelheid werk die is voltooid voor een project.</span><span class="sxs-lookup"><span data-stu-id="0d10b-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="0d10b-106">Ze worden gemaakt als resultaat van tijdsvermeldingen en onkostenposten, journaalboekingen en facturen.</span><span class="sxs-lookup"><span data-stu-id="0d10b-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="0d10b-107">Journaalregels en tijdsvermelding</span><span class="sxs-lookup"><span data-stu-id="0d10b-107">Journal lines and time submission</span></span>

<span data-ttu-id="0d10b-108">Zie voor meer informatie over tijdinvoer [Overzicht van tijdinvoer](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0d10b-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="0d10b-109">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="0d10b-109">Time and materials</span></span>

<span data-ttu-id="0d10b-110">Wanneer een ingediende tijdsvermelding is gekoppeld aan een project dat is toegewezen aan een contractregel voor tijd en materiaal, maakt het systeem twee journaalregels aan, één voor kosten en één voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="0d10b-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="0d10b-111">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="0d10b-111">Fixed price</span></span>

<span data-ttu-id="0d10b-112">Wanneer een ingediende tijdsvermelding is gekoppeld aan een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er één journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0d10b-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="0d10b-113">Standaardprijs</span><span class="sxs-lookup"><span data-stu-id="0d10b-113">Default pricing</span></span>

<span data-ttu-id="0d10b-114">De logica voor het maken van standaardprijzen bevindt zich op de journaalregel.</span><span class="sxs-lookup"><span data-stu-id="0d10b-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="0d10b-115">De veldwaarden uit de tijdsvermelding worden naar de journaalregel gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="0d10b-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="0d10b-116">Deze waarden bevatten de transactiedatum, de contractregel waaraan het project is toegewezen en het resultaat van de valuta in de juiste prijslijst.</span><span class="sxs-lookup"><span data-stu-id="0d10b-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="0d10b-117">De velden die van invloed zijn op standaardprijzen, zoals **Rol** en **Organisatie-eenheid** zorgen ervoor dat de juiste prijs standaard op de journaalregel wordt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="0d10b-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="0d10b-118">U kunt een aangepast veld toevoegen aan de tijdsvermelding.</span><span class="sxs-lookup"><span data-stu-id="0d10b-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="0d10b-119">Als u wilt dat de veldwaarde wordt doorgegeven aan werkelijke waarden, maakt u het veld in de entiteit Werkelijke waarden en gebruikt u veldtoewijzingen om het veld van de tijdsvermelding naar de werkelijke waarde te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="0d10b-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="0d10b-120">Indiening van journaalregels en basisonkosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="0d10b-121">Zie voor meer informatie over de invoer van onkosten [Onkostenoverzicht](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0d10b-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="0d10b-122">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="0d10b-122">Time and materials</span></span>

<span data-ttu-id="0d10b-123">Wanneer ingediende basisonkosten zijn gekoppeld aan een project dat is toegewezen aan een contractregel voor tijd en materiaal, maakt het systeem twee journaalregels aan, één voor kosten en één voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="0d10b-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="0d10b-124">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="0d10b-124">Fixed price</span></span>

<span data-ttu-id="0d10b-125">Wanneer een ingediende basisonkostenvermelding is gekoppeld aan een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er één journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0d10b-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="0d10b-126">Standaardprijs</span><span class="sxs-lookup"><span data-stu-id="0d10b-126">Default pricing</span></span>

<span data-ttu-id="0d10b-127">De logica voor het invoeren van standaardprijzen voor onkosten is gebaseerd op de onkostencategorie.</span><span class="sxs-lookup"><span data-stu-id="0d10b-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="0d10b-128">De datum van de transactie, de contractregel waaraan het project is toegewezen en de valuta worden allemaal gebruikt om de juiste prijslijst te bepalen.</span><span class="sxs-lookup"><span data-stu-id="0d10b-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="0d10b-129">Het bedrag dat voor de prijs zelf wordt ingevoerd, wordt echter standaard rechtstreeks op de gerelateerde onkostenjournaalregels ingesteld voor kosten en verkoop.</span><span class="sxs-lookup"><span data-stu-id="0d10b-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="0d10b-130">De vermelding op categoriebasis van standaardprijzen per eenheid is niet beschikbaar voor onkostenposten.</span><span class="sxs-lookup"><span data-stu-id="0d10b-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="0d10b-131">Invoerjournalen gebruiken om kosten vast te leggen</span><span class="sxs-lookup"><span data-stu-id="0d10b-131">Use entry journals to record costs</span></span>

<span data-ttu-id="0d10b-132">U kunt invoerjournalen gebruiken om de kosten of onkosten vast te leggen in de klassen voor materiaal, tarief, tijd, onkosten of belastingtransactie.</span><span class="sxs-lookup"><span data-stu-id="0d10b-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="0d10b-133">U kunt de volgende journalen gebruiken voor de volgende doeleinden:</span><span class="sxs-lookup"><span data-stu-id="0d10b-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="0d10b-134">Leg de werkelijke materiaalkosten en verkopen voor een project vast.</span><span class="sxs-lookup"><span data-stu-id="0d10b-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="0d10b-135">Verplaats werkelijke transactiewaarden van een ander systeem naar Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0d10b-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="0d10b-136">Leg kosten vast die zich in een ander systeem hebben voorgedaan.</span><span class="sxs-lookup"><span data-stu-id="0d10b-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="0d10b-137">Deze kosten kunnen inkoop- of uitbestedingskosten omvatten.</span><span class="sxs-lookup"><span data-stu-id="0d10b-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d10b-138">De toepassing valideert het journaalregeltype of de gerelateerde prijzen die op de journaalregel zijn ingevoerd niet.</span><span class="sxs-lookup"><span data-stu-id="0d10b-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="0d10b-139">Daarom mag alleen een gebruiker die zich volledig bewust is van de boekhoudkundige impact van werkelijke waarden op het project invoerjournalen gebruiken om werkelijke waarden te maken.</span><span class="sxs-lookup"><span data-stu-id="0d10b-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="0d10b-140">Vanwege de impact van dit journaaltype, moet u zorgvuldig kiezen wie toegang heeft om boekingsjournalen te maken.</span><span class="sxs-lookup"><span data-stu-id="0d10b-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="0d10b-141">Werkelijke waarden vastleggen op basis van projectgebeurtenissen</span><span class="sxs-lookup"><span data-stu-id="0d10b-141">Record actuals based on project events</span></span>

<span data-ttu-id="0d10b-142">In Project Operations worden de financiële transacties vastgelegd die tijdens een project plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="0d10b-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="0d10b-143">Deze transacties worden geregistreerd als werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="0d10b-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="0d10b-144">In de volgende tabellen ziet u de verschillende typen werkelijke waarden die worden gemaakt, afhankelijk van of het project een project op basis van tijd- en materiaalverbruik of een project met een vaste prijs is en of dit zich in de pre-salesfase bevindt of een intern project is.</span><span class="sxs-lookup"><span data-stu-id="0d10b-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="0d10b-145">De resource behoort tot dezelfde organisatie-eenheid als de contracterende eenheid van het project</span><span class="sxs-lookup"><span data-stu-id="0d10b-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0d10b-146">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="0d10b-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0d10b-147">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="0d10b-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0d10b-148">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="0d10b-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0d10b-149">Intern project</span><span class="sxs-lookup"><span data-stu-id="0d10b-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0d10b-150">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="0d10b-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0d10b-151">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="0d10b-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0d10b-152">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="0d10b-152">Actuals</span></span></th>
<th><span data-ttu-id="0d10b-153">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="0d10b-153">Transaction currency</span></span></th>
<th><span data-ttu-id="0d10b-154">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="0d10b-154">Fixed price</span></span></th>
<th><span data-ttu-id="0d10b-155">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="0d10b-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0d10b-156">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0d10b-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0d10b-157">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="0d10b-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-158">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="0d10b-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0d10b-159">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="0d10b-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0d10b-160">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="0d10b-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0d10b-161">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-161">Cost actual</span></span></td>
<td><span data-ttu-id="0d10b-162">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0d10b-163">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0d10b-164">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="0d10b-165">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0d10b-166">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-167">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="0d10b-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0d10b-168">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0d10b-169">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="0d10b-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0d10b-170">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-170">Cost actual</span></span></td>
<td><span data-ttu-id="0d10b-171">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0d10b-172">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0d10b-173">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0d10b-174">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0d10b-175">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-176">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0d10b-177">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-178">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="0d10b-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0d10b-179">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0d10b-180">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="0d10b-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0d10b-181">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="0d10b-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0d10b-182">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0d10b-183">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="0d10b-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0d10b-184">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0d10b-185">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0d10b-186">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-187">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="0d10b-187">Billed sales</span></span></td>
<td><span data-ttu-id="0d10b-188">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0d10b-189">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="0d10b-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0d10b-190">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="0d10b-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0d10b-191">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0d10b-192">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0d10b-193">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0d10b-194">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0d10b-195">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-196">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0d10b-197">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-198">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="0d10b-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0d10b-199">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0d10b-200">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="0d10b-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0d10b-201">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="0d10b-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0d10b-202">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0d10b-203">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="0d10b-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0d10b-204">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="0d10b-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0d10b-205">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0d10b-206">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0d10b-207">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-208">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="0d10b-208">Billed sales</span></span></td>
<td><span data-ttu-id="0d10b-209">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0d10b-210">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="0d10b-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0d10b-211">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="0d10b-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0d10b-212">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-213">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0d10b-214">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-215">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="0d10b-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0d10b-216">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="0d10b-217">De resource behoort tot een andere organisatie-eenheid dan de contracterende eenheid van het project</span><span class="sxs-lookup"><span data-stu-id="0d10b-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0d10b-218">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="0d10b-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0d10b-219">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="0d10b-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0d10b-220">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="0d10b-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0d10b-221">Intern project</span><span class="sxs-lookup"><span data-stu-id="0d10b-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0d10b-222">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="0d10b-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0d10b-223">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="0d10b-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0d10b-224">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="0d10b-224">Actuals</span></span></th>
<th><span data-ttu-id="0d10b-225">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="0d10b-225">Transaction currency</span></span></th>
<th><span data-ttu-id="0d10b-226">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="0d10b-226">Fixed price</span></span></th>
<th><span data-ttu-id="0d10b-227">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="0d10b-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0d10b-228">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0d10b-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0d10b-229">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="0d10b-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-230">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="0d10b-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0d10b-231">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="0d10b-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="0d10b-232">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="0d10b-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0d10b-233">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-233">Cost actual</span></span></td>
<td><span data-ttu-id="0d10b-234">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0d10b-235">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0d10b-236">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0d10b-237">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0d10b-238">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-239">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="0d10b-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0d10b-240">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-241">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0d10b-242">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-243">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="0d10b-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0d10b-244">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="0d10b-245">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="0d10b-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0d10b-246">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-246">Cost actual</span></span></td>
<td><span data-ttu-id="0d10b-247">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0d10b-248">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0d10b-249">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0d10b-250">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0d10b-251">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="0d10b-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-252">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0d10b-253">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-254">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="0d10b-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0d10b-255">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-256">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0d10b-257">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-258">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="0d10b-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0d10b-259">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0d10b-260">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="0d10b-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0d10b-261">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="0d10b-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0d10b-262">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0d10b-263">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="0d10b-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0d10b-264">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0d10b-265">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0d10b-266">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-267">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="0d10b-267">Billed sales</span></span></td>
<td><span data-ttu-id="0d10b-268">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0d10b-269">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="0d10b-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0d10b-270">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="0d10b-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0d10b-271">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0d10b-272">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0d10b-273">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0d10b-274">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0d10b-275">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-276">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0d10b-277">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-278">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="0d10b-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0d10b-279">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0d10b-280">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="0d10b-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0d10b-281">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="0d10b-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0d10b-282">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0d10b-283">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="0d10b-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0d10b-284">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="0d10b-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0d10b-285">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0d10b-286">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0d10b-287">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="0d10b-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-288">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="0d10b-288">Billed sales</span></span></td>
<td><span data-ttu-id="0d10b-289">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0d10b-290">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="0d10b-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0d10b-291">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="0d10b-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0d10b-292">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-293">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="0d10b-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0d10b-294">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0d10b-295">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="0d10b-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0d10b-296">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="0d10b-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
