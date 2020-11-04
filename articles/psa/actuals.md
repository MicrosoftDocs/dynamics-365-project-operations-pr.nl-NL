---
title: Overzicht van werkelijke waarden
description: In dit onderwerp krijgt u informatie over werkelijke projectwaarden.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
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
ms.openlocfilehash: 9559cb2dcc38cb8058c5a9a3b97a35019fea486f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074762"
---
# <a name="actuals-overview"></a><span data-ttu-id="760fd-103">Overzicht van werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="760fd-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="760fd-104">Werkelijke waarden zijn de hoeveelheid werk die is voltooid voor een project.</span><span class="sxs-lookup"><span data-stu-id="760fd-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="760fd-105">Werkelijke projectwaarden kunnen worden herleid naar hun brondocumenten.</span><span class="sxs-lookup"><span data-stu-id="760fd-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="760fd-106">Deze brondocumenten bevatten tijd-, onkosten- en journaalboekingen, en ook facturen.</span><span class="sxs-lookup"><span data-stu-id="760fd-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Hoe werkelijke projectwaarden kunnen worden herleid naar brondocumenten](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="760fd-108">Een tijdsvermelding indienen</span><span class="sxs-lookup"><span data-stu-id="760fd-108">Submitting a time entry</span></span>

<span data-ttu-id="760fd-109">Wanneer in PSA een tijdsvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel voor tijd- en materiaalverbruik, worden er twee journaalregels gemaakt.</span><span class="sxs-lookup"><span data-stu-id="760fd-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="760fd-110">Eén regel is voor de kosten en de andere regel is voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="760fd-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="760fd-111">Wanneer een tijdsvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er alleen een journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="760fd-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="760fd-112">De logica voor het invoeren van standaardprijzen bevindt zich op de dagboekregel.</span><span class="sxs-lookup"><span data-stu-id="760fd-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="760fd-113">Alle veldwaarden uit een tijdsvermelding worden naar de dagboekregel gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="760fd-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="760fd-114">Deze velden bevatten de datum van de transactie, de contractregel waaraan het project is toegewezen en het resultaat van de valuta in de juiste prijslijst.</span><span class="sxs-lookup"><span data-stu-id="760fd-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="760fd-115">De velden die van invloed zijn op standaardprijzen, zoals **Rol** en **organisatie-eenheid** , zorgen ervoor dat de juiste prijs standaard op de journaalregel wordt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="760fd-115">The fields that affect default prices, such as **Role** and **Org Unit** , cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="760fd-116">Als u een aangepast veld toevoegt aan de tijdsvermelding en u wilt dat de veldwaarde wordt doorgegeven aan werkelijke waarden, maakt u het veld in de entiteit Werkelijke waarden en gebruikt u veldtoewijzingen om het veld van de tijdsvermelding naar de werkelijke waarde te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="760fd-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="760fd-117">Een onkostenvermelding indienen</span><span class="sxs-lookup"><span data-stu-id="760fd-117">Submitting an expense entry</span></span>

<span data-ttu-id="760fd-118">Wanneer in PSA een onkostenvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel voor tijd- en materiaalverbruik, worden er twee journaalregels gemaakt.</span><span class="sxs-lookup"><span data-stu-id="760fd-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="760fd-119">Eén regel is voor de kosten en de andere regel is voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="760fd-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="760fd-120">Wanneer een onkostenvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er alleen een journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="760fd-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="760fd-121">Logica voor het invoeren van standaardprijzen voor onkosten is gebaseerd op de onkostencategorie die is geselecteerd op de pagina **Onkostenpost**.</span><span class="sxs-lookup"><span data-stu-id="760fd-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="760fd-122">De datum van de transactie, de contractregel waaraan het project is toegewezen en de valuta worden allemaal gebruikt om de juiste prijslijst te bepalen.</span><span class="sxs-lookup"><span data-stu-id="760fd-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="760fd-123">Voor de prijs zelf wordt het bedrag dat de gebruiker heeft ingevoerd echter standaard rechtstreeks op de gerelateerde onkostenjournaalregels ingesteld voor kosten en verkoop.</span><span class="sxs-lookup"><span data-stu-id="760fd-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="760fd-124">In de huidige versie van PSA is de vermelding op categoriebasis van standaardprijzen per eenheid niet beschikbaar voor onkostenposten.</span><span class="sxs-lookup"><span data-stu-id="760fd-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="760fd-125">Invoerjournalen gebruiken om kosten vast te leggen</span><span class="sxs-lookup"><span data-stu-id="760fd-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="760fd-126">In PSA kunt u in invoerjournalen de kosten of onkosten vastleggen in de klassen voor materiaal, tarief, tijd, onkosten of belastingtransactie.</span><span class="sxs-lookup"><span data-stu-id="760fd-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="760fd-127">Een journaal heeft een koptekst, regels en een actie **Bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="760fd-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="760fd-128">Hier volgen enkele scenario's waarin u mogelijk een journaal gebruikt:</span><span class="sxs-lookup"><span data-stu-id="760fd-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="760fd-129">U moet werkelijke materiaalkosten en -verkopen voor een project vastleggen.</span><span class="sxs-lookup"><span data-stu-id="760fd-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="760fd-130">U moet werkelijke transactiewaarden van een ander systeem naar PSA verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="760fd-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="760fd-131">U moet kosten vastleggen die zijn opgetreden in een ander systeem, zoals inkoop- of uitbestedingskosten.</span><span class="sxs-lookup"><span data-stu-id="760fd-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="760fd-132">Invoerjournalen gebruiken om werkelijke waarden te maken mag alleen worden gedaan door een gebruiker die zich volledig bewust is van de boekhoudkundige impact die de werkelijke waarden hebben op het project.</span><span class="sxs-lookup"><span data-stu-id="760fd-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="760fd-133">Dit komt doordat de toepassing het journaalregeltype of de gerelateerde prijzen die op de journaalregel zijn ingevoerd, niet valideert.</span><span class="sxs-lookup"><span data-stu-id="760fd-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="760fd-134">Door de impact van dit journaaltype moet u goed opletten wie toegang krijgt om invoerjournalen te maken.</span><span class="sxs-lookup"><span data-stu-id="760fd-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="760fd-135">Werkelijke waarden vastleggen op basis van projectgebeurtenissen</span><span class="sxs-lookup"><span data-stu-id="760fd-135">Recording actuals based on project events</span></span>

<span data-ttu-id="760fd-136">In PSA worden de financiële transacties vastgelegd die tijdens een project plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="760fd-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="760fd-137">Deze transacties worden geregistreerd als **werkelijke waarden**.</span><span class="sxs-lookup"><span data-stu-id="760fd-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="760fd-138">In de volgende tabellen ziet u de verschillende typen werkelijke waarden die worden gemaakt, afhankelijk van of het project een project op basis van tijd- en materiaalverbruik of een project met een vaste prijs is en of dit zich in de pre-salesfase bevindt of een intern project is.</span><span class="sxs-lookup"><span data-stu-id="760fd-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="760fd-139">**De resource behoort tot dezelfde organisatie-eenheid als de contracterende eenheid van het project**</span><span class="sxs-lookup"><span data-stu-id="760fd-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="760fd-140">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="760fd-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="760fd-141">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="760fd-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="760fd-142">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="760fd-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="760fd-143">Intern project</span><span class="sxs-lookup"><span data-stu-id="760fd-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="760fd-144">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="760fd-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="760fd-145">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="760fd-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="760fd-146">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="760fd-146">Actuals</span></span></th>
<th><span data-ttu-id="760fd-147">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="760fd-147">Transaction currency</span></span></th>
<th><span data-ttu-id="760fd-148">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="760fd-148">Fixed price</span></span></th>
<th><span data-ttu-id="760fd-149">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="760fd-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="760fd-150">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="760fd-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="760fd-151">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="760fd-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-152">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="760fd-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="760fd-153">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="760fd-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="760fd-154">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="760fd-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="760fd-155">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-155">Cost actual</span></span></td>
<td><span data-ttu-id="760fd-156">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="760fd-157">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="760fd-158">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="760fd-159">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="760fd-160">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-161">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="760fd-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="760fd-162">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="760fd-163">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="760fd-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="760fd-164">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-164">Cost actual</span></span></td>
<td><span data-ttu-id="760fd-165">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="760fd-166">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="760fd-167">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="760fd-168">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="760fd-169">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-170">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="760fd-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="760fd-171">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-172">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="760fd-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="760fd-173">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="760fd-174">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="760fd-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="760fd-175">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="760fd-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="760fd-176">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="760fd-177">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="760fd-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="760fd-178">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="760fd-179">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="760fd-180">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-181">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="760fd-181">Billed sales</span></span></td>
<td><span data-ttu-id="760fd-182">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="760fd-183">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="760fd-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="760fd-184">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="760fd-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="760fd-185">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="760fd-186">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="760fd-187">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="760fd-188">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="760fd-189">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-190">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="760fd-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="760fd-191">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-192">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="760fd-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="760fd-193">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="760fd-194">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="760fd-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="760fd-195">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="760fd-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="760fd-196">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="760fd-197">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="760fd-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="760fd-198">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="760fd-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="760fd-199">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="760fd-200">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="760fd-201">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-202">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="760fd-202">Billed sales</span></span></td>
<td><span data-ttu-id="760fd-203">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="760fd-204">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="760fd-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="760fd-205">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="760fd-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="760fd-206">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-207">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="760fd-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="760fd-208">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-209">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="760fd-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="760fd-210">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="760fd-211">**De resource behoort tot een andere organisatie-eenheid dan de contracterende eenheid van het project**</span><span class="sxs-lookup"><span data-stu-id="760fd-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="760fd-212">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="760fd-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="760fd-213">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="760fd-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="760fd-214">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="760fd-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="760fd-215">Intern project</span><span class="sxs-lookup"><span data-stu-id="760fd-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="760fd-216">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="760fd-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="760fd-217">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="760fd-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="760fd-218">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="760fd-218">Actuals</span></span></th>
<th><span data-ttu-id="760fd-219">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="760fd-219">Transaction currency</span></span></th>
<th><span data-ttu-id="760fd-220">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="760fd-220">Fixed price</span></span></th>
<th><span data-ttu-id="760fd-221">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="760fd-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="760fd-222">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="760fd-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="760fd-223">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="760fd-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-224">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="760fd-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="760fd-225">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="760fd-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="760fd-226">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="760fd-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="760fd-227">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-227">Cost actual</span></span></td>
<td><span data-ttu-id="760fd-228">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="760fd-229">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="760fd-230">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="760fd-231">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="760fd-232">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-233">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="760fd-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="760fd-234">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-235">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="760fd-236">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-237">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="760fd-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="760fd-238">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="760fd-239">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="760fd-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="760fd-240">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-240">Cost actual</span></span></td>
<td><span data-ttu-id="760fd-241">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="760fd-242">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="760fd-243">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="760fd-244">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="760fd-245">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="760fd-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-246">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="760fd-247">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-248">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="760fd-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="760fd-249">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="760fd-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-250">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="760fd-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="760fd-251">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-252">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="760fd-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="760fd-253">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="760fd-254">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="760fd-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="760fd-255">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="760fd-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="760fd-256">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="760fd-257">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="760fd-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="760fd-258">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="760fd-259">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="760fd-260">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-261">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="760fd-261">Billed sales</span></span></td>
<td><span data-ttu-id="760fd-262">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="760fd-263">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="760fd-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="760fd-264">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="760fd-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="760fd-265">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="760fd-266">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="760fd-267">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="760fd-268">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="760fd-269">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-270">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="760fd-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="760fd-271">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-272">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="760fd-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="760fd-273">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="760fd-274">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="760fd-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="760fd-275">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="760fd-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="760fd-276">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="760fd-277">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="760fd-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="760fd-278">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="760fd-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="760fd-279">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="760fd-280">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="760fd-281">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="760fd-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-282">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="760fd-282">Billed sales</span></span></td>
<td><span data-ttu-id="760fd-283">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="760fd-284">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="760fd-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="760fd-285">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="760fd-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="760fd-286">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-287">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="760fd-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="760fd-288">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="760fd-289">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="760fd-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="760fd-290">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="760fd-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
