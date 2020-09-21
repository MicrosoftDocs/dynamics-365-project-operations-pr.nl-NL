---
title: Werkelijke waarden
description: In dit onderwerp krijgt u informatie over werkelijke projectwaarden.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750817"
---
# <a name="actuals"></a><span data-ttu-id="623d7-103">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="623d7-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="623d7-104">Werkelijke waarden zijn de hoeveelheid werk die is voltooid voor een project.</span><span class="sxs-lookup"><span data-stu-id="623d7-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="623d7-105">Werkelijke projectwaarden kunnen worden herleid naar hun brondocumenten.</span><span class="sxs-lookup"><span data-stu-id="623d7-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="623d7-106">Deze brondocumenten bevatten tijd-, onkosten- en journaalboekingen, en ook facturen.</span><span class="sxs-lookup"><span data-stu-id="623d7-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Hoe werkelijke projectwaarden kunnen worden herleid naar brondocumenten](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="623d7-108">Een tijdsvermelding indienen</span><span class="sxs-lookup"><span data-stu-id="623d7-108">Submitting a time entry</span></span>

<span data-ttu-id="623d7-109">Wanneer in PSA een tijdsvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel voor tijd- en materiaalverbruik, worden er twee journaalregels gemaakt.</span><span class="sxs-lookup"><span data-stu-id="623d7-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="623d7-110">Eén regel is voor de kosten en de andere regel is voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="623d7-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="623d7-111">Wanneer een tijdsvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er alleen een journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="623d7-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="623d7-112">De logica voor het invoeren van standaardprijzen bevindt zich op de dagboekregel.</span><span class="sxs-lookup"><span data-stu-id="623d7-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="623d7-113">Alle veldwaarden uit een tijdsvermelding worden naar de dagboekregel gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="623d7-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="623d7-114">Deze velden bevatten de datum van de transactie, de contractregel waaraan het project is toegewezen en het resultaat van de valuta in de juiste prijslijst.</span><span class="sxs-lookup"><span data-stu-id="623d7-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="623d7-115">De velden die van invloed zijn op standaardprijzen, zoals **Rol** en **organisatie-eenheid**, zorgen ervoor dat de juiste prijs standaard op de journaalregel wordt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="623d7-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="623d7-116">Als u een aangepast veld toevoegt aan de tijdsvermelding en u wilt dat de veldwaarde wordt doorgegeven aan werkelijke waarden, maakt u het veld in de entiteit Werkelijke waarden en gebruikt u veldtoewijzingen om het veld van de tijdsvermelding naar de werkelijke waarde te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="623d7-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="623d7-117">Een onkostenvermelding indienen</span><span class="sxs-lookup"><span data-stu-id="623d7-117">Submitting an expense entry</span></span>

<span data-ttu-id="623d7-118">Wanneer in PSA een onkostenvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel voor tijd- en materiaalverbruik, worden er twee journaalregels gemaakt.</span><span class="sxs-lookup"><span data-stu-id="623d7-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="623d7-119">Eén regel is voor de kosten en de andere regel is voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="623d7-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="623d7-120">Wanneer een onkostenvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er alleen een journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="623d7-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="623d7-121">Logica voor het invoeren van standaardprijzen voor onkosten is gebaseerd op de onkostencategorie die is geselecteerd op de pagina **Onkostenpost**.</span><span class="sxs-lookup"><span data-stu-id="623d7-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="623d7-122">De datum van de transactie, de contractregel waaraan het project is toegewezen en de valuta worden allemaal gebruikt om de juiste prijslijst te bepalen.</span><span class="sxs-lookup"><span data-stu-id="623d7-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="623d7-123">Voor de prijs zelf wordt het bedrag dat de gebruiker heeft ingevoerd echter standaard rechtstreeks op de gerelateerde onkostenjournaalregels ingesteld voor kosten en verkoop.</span><span class="sxs-lookup"><span data-stu-id="623d7-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="623d7-124">In de huidige versie van PSA is de vermelding op categoriebasis van standaardprijzen per eenheid niet beschikbaar voor onkostenposten.</span><span class="sxs-lookup"><span data-stu-id="623d7-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="623d7-125">Journalen gebruiken om kosten vast te leggen</span><span class="sxs-lookup"><span data-stu-id="623d7-125">Using journals to record costs</span></span>

<span data-ttu-id="623d7-126">In PSA kunt u in journalen kosten of onkosten vastleggen in de klassen voor materiaal, tarief, tijd, onkosten of belastingtransactie.</span><span class="sxs-lookup"><span data-stu-id="623d7-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="623d7-127">Een journaal heeft een koptekst, regels en een actie **Bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="623d7-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="623d7-128">Hier volgen enkele scenario's waarin u mogelijk een journaal gebruikt:</span><span class="sxs-lookup"><span data-stu-id="623d7-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="623d7-129">U moet werkelijke materiaalkosten en -verkopen voor een project vastleggen.</span><span class="sxs-lookup"><span data-stu-id="623d7-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="623d7-130">U moet werkelijke transactiewaarden van een ander systeem naar PSA verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="623d7-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="623d7-131">U moet kosten vastleggen die zijn opgetreden in een ander systeem, zoals inkoop- of uitbestedingskosten.</span><span class="sxs-lookup"><span data-stu-id="623d7-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="623d7-132">Werkelijke waarden vastleggen op basis van projectgebeurtenissen</span><span class="sxs-lookup"><span data-stu-id="623d7-132">Recording actuals based on project events</span></span>

<span data-ttu-id="623d7-133">In PSA worden de financiële transacties vastgelegd die tijdens een project plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="623d7-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="623d7-134">Deze transacties worden geregistreerd als **werkelijke waarden**.</span><span class="sxs-lookup"><span data-stu-id="623d7-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="623d7-135">In de volgende tabellen ziet u de verschillende typen werkelijke waarden die worden gemaakt, afhankelijk van of het project een project op basis van tijd- en materiaalverbruik of een project met een vaste prijs is en of dit zich in de pre-salesfase bevindt of een intern project is.</span><span class="sxs-lookup"><span data-stu-id="623d7-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="623d7-136">**De resource behoort tot dezelfde organisatie-eenheid als de contracterende eenheid van het project**</span><span class="sxs-lookup"><span data-stu-id="623d7-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="623d7-137">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="623d7-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="623d7-138">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="623d7-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="623d7-139">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="623d7-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="623d7-140">Intern project</span><span class="sxs-lookup"><span data-stu-id="623d7-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="623d7-141">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="623d7-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="623d7-142">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="623d7-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="623d7-143">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="623d7-143">Actuals</span></span></th>
<th><span data-ttu-id="623d7-144">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="623d7-144">Transaction currency</span></span></th>
<th><span data-ttu-id="623d7-145">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="623d7-145">Fixed price</span></span></th>
<th><span data-ttu-id="623d7-146">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="623d7-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="623d7-147">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="623d7-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="623d7-148">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="623d7-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-149">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="623d7-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="623d7-150">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="623d7-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="623d7-151">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="623d7-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="623d7-152">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-152">Cost actual</span></span></td>
<td><span data-ttu-id="623d7-153">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="623d7-154">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="623d7-155">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="623d7-156">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="623d7-157">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-158">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="623d7-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="623d7-159">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="623d7-160">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="623d7-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="623d7-161">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-161">Cost actual</span></span></td>
<td><span data-ttu-id="623d7-162">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="623d7-163">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="623d7-164">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="623d7-165">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="623d7-166">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-167">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="623d7-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="623d7-168">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-169">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="623d7-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="623d7-170">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="623d7-171">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="623d7-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="623d7-172">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="623d7-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="623d7-173">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="623d7-174">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="623d7-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="623d7-175">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="623d7-176">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="623d7-177">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-178">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="623d7-178">Billed sales</span></span></td>
<td><span data-ttu-id="623d7-179">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="623d7-180">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="623d7-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="623d7-181">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="623d7-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="623d7-182">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="623d7-183">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="623d7-184">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="623d7-185">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="623d7-186">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-187">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="623d7-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="623d7-188">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-189">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="623d7-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="623d7-190">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="623d7-191">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="623d7-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="623d7-192">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="623d7-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="623d7-193">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="623d7-194">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="623d7-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="623d7-195">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="623d7-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="623d7-196">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="623d7-197">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="623d7-198">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-199">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="623d7-199">Billed sales</span></span></td>
<td><span data-ttu-id="623d7-200">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="623d7-201">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="623d7-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="623d7-202">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="623d7-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="623d7-203">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-204">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="623d7-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="623d7-205">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-206">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="623d7-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="623d7-207">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="623d7-208">**De resource behoort tot een andere organisatie-eenheid dan de contracterende eenheid van het project**</span><span class="sxs-lookup"><span data-stu-id="623d7-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="623d7-209">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="623d7-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="623d7-210">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="623d7-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="623d7-211">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="623d7-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="623d7-212">Intern project</span><span class="sxs-lookup"><span data-stu-id="623d7-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="623d7-213">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="623d7-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="623d7-214">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="623d7-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="623d7-215">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="623d7-215">Actuals</span></span></th>
<th><span data-ttu-id="623d7-216">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="623d7-216">Transaction currency</span></span></th>
<th><span data-ttu-id="623d7-217">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="623d7-217">Fixed price</span></span></th>
<th><span data-ttu-id="623d7-218">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="623d7-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="623d7-219">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="623d7-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="623d7-220">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="623d7-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-221">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="623d7-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="623d7-222">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="623d7-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="623d7-223">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="623d7-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="623d7-224">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-224">Cost actual</span></span></td>
<td><span data-ttu-id="623d7-225">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="623d7-226">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="623d7-227">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="623d7-228">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="623d7-229">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-230">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="623d7-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="623d7-231">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-232">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="623d7-233">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-234">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="623d7-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="623d7-235">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="623d7-236">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="623d7-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="623d7-237">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-237">Cost actual</span></span></td>
<td><span data-ttu-id="623d7-238">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="623d7-239">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="623d7-240">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="623d7-241">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="623d7-242">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="623d7-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-243">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="623d7-244">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-245">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="623d7-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="623d7-246">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="623d7-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-247">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="623d7-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="623d7-248">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-249">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="623d7-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="623d7-250">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="623d7-251">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="623d7-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="623d7-252">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="623d7-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="623d7-253">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="623d7-254">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="623d7-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="623d7-255">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="623d7-256">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="623d7-257">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-258">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="623d7-258">Billed sales</span></span></td>
<td><span data-ttu-id="623d7-259">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="623d7-260">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="623d7-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="623d7-261">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="623d7-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="623d7-262">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="623d7-263">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="623d7-264">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="623d7-265">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="623d7-266">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-267">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="623d7-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="623d7-268">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-269">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="623d7-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="623d7-270">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="623d7-271">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="623d7-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="623d7-272">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="623d7-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="623d7-273">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="623d7-274">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="623d7-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="623d7-275">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="623d7-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="623d7-276">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="623d7-277">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="623d7-278">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="623d7-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-279">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="623d7-279">Billed sales</span></span></td>
<td><span data-ttu-id="623d7-280">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="623d7-281">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="623d7-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="623d7-282">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="623d7-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="623d7-283">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-284">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="623d7-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="623d7-285">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="623d7-286">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="623d7-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="623d7-287">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="623d7-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
