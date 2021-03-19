---
title: Overzicht van werkelijke waarden
description: In dit onderwerp krijgt u informatie over werkelijke projectwaarden.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285612"
---
# <a name="actuals-overview"></a><span data-ttu-id="cccc3-103">Overzicht van werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cccc3-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cccc3-104">Werkelijke waarden zijn de hoeveelheid werk die is voltooid voor een project.</span><span class="sxs-lookup"><span data-stu-id="cccc3-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="cccc3-105">Werkelijke projectwaarden kunnen worden herleid naar hun brondocumenten.</span><span class="sxs-lookup"><span data-stu-id="cccc3-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="cccc3-106">Deze brondocumenten bevatten tijd-, onkosten- en journaalboekingen, en ook facturen.</span><span class="sxs-lookup"><span data-stu-id="cccc3-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Hoe werkelijke projectwaarden kunnen worden herleid naar brondocumenten](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="cccc3-108">Een tijdsvermelding indienen</span><span class="sxs-lookup"><span data-stu-id="cccc3-108">Submitting a time entry</span></span>

<span data-ttu-id="cccc3-109">Wanneer in PSA een tijdsvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel voor tijd- en materiaalverbruik, worden er twee journaalregels gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cccc3-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="cccc3-110">Eén regel is voor de kosten en de andere regel is voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="cccc3-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="cccc3-111">Wanneer een tijdsvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er alleen een journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cccc3-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="cccc3-112">De logica voor het invoeren van standaardprijzen bevindt zich op de dagboekregel.</span><span class="sxs-lookup"><span data-stu-id="cccc3-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="cccc3-113">Alle veldwaarden uit een tijdsvermelding worden naar de dagboekregel gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="cccc3-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="cccc3-114">Deze velden bevatten de datum van de transactie, de contractregel waaraan het project is toegewezen en het resultaat van de valuta in de juiste prijslijst.</span><span class="sxs-lookup"><span data-stu-id="cccc3-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="cccc3-115">De velden die van invloed zijn op standaardprijzen, zoals **Rol** en **organisatie-eenheid**, zorgen ervoor dat de juiste prijs standaard op de journaalregel wordt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="cccc3-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="cccc3-116">Als u een aangepast veld toevoegt aan de tijdsvermelding en u wilt dat de veldwaarde wordt doorgegeven aan werkelijke waarden, maakt u het veld in de entiteit Werkelijke waarden en gebruikt u veldtoewijzingen om het veld van de tijdsvermelding naar de werkelijke waarde te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="cccc3-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="cccc3-117">Een onkostenvermelding indienen</span><span class="sxs-lookup"><span data-stu-id="cccc3-117">Submitting an expense entry</span></span>

<span data-ttu-id="cccc3-118">Wanneer in PSA een onkostenvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel voor tijd- en materiaalverbruik, worden er twee journaalregels gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cccc3-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="cccc3-119">Eén regel is voor de kosten en de andere regel is voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="cccc3-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="cccc3-120">Wanneer een onkostenvermelding wordt ingediend voor een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er alleen een journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cccc3-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="cccc3-121">Logica voor het invoeren van standaardprijzen voor onkosten is gebaseerd op de onkostencategorie die is geselecteerd op de pagina **Onkostenpost**.</span><span class="sxs-lookup"><span data-stu-id="cccc3-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="cccc3-122">De datum van de transactie, de contractregel waaraan het project is toegewezen en de valuta worden allemaal gebruikt om de juiste prijslijst te bepalen.</span><span class="sxs-lookup"><span data-stu-id="cccc3-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="cccc3-123">Voor de prijs zelf wordt het bedrag dat de gebruiker heeft ingevoerd echter standaard rechtstreeks op de gerelateerde onkostenjournaalregels ingesteld voor kosten en verkoop.</span><span class="sxs-lookup"><span data-stu-id="cccc3-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="cccc3-124">In de huidige versie van PSA is de vermelding op categoriebasis van standaardprijzen per eenheid niet beschikbaar voor onkostenposten.</span><span class="sxs-lookup"><span data-stu-id="cccc3-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="cccc3-125">Invoerjournalen gebruiken om kosten vast te leggen</span><span class="sxs-lookup"><span data-stu-id="cccc3-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="cccc3-126">In PSA kunt u in invoerjournalen de kosten of onkosten vastleggen in de klassen voor materiaal, tarief, tijd, onkosten of belastingtransactie.</span><span class="sxs-lookup"><span data-stu-id="cccc3-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="cccc3-127">Een journaal heeft een koptekst, regels en een actie **Bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="cccc3-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="cccc3-128">Hier volgen enkele scenario's waarin u mogelijk een journaal gebruikt:</span><span class="sxs-lookup"><span data-stu-id="cccc3-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="cccc3-129">U moet werkelijke materiaalkosten en -verkopen voor een project vastleggen.</span><span class="sxs-lookup"><span data-stu-id="cccc3-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="cccc3-130">U moet werkelijke transactiewaarden van een ander systeem naar PSA verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="cccc3-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="cccc3-131">U moet kosten vastleggen die zijn opgetreden in een ander systeem, zoals inkoop- of uitbestedingskosten.</span><span class="sxs-lookup"><span data-stu-id="cccc3-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cccc3-132">Invoerjournalen gebruiken om werkelijke waarden te maken mag alleen worden gedaan door een gebruiker die zich volledig bewust is van de boekhoudkundige impact die de werkelijke waarden hebben op het project.</span><span class="sxs-lookup"><span data-stu-id="cccc3-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="cccc3-133">Dit komt doordat de toepassing het journaalregeltype of de gerelateerde prijzen die op de journaalregel zijn ingevoerd, niet valideert.</span><span class="sxs-lookup"><span data-stu-id="cccc3-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="cccc3-134">Door de impact van dit journaaltype moet u goed opletten wie toegang krijgt om invoerjournalen te maken.</span><span class="sxs-lookup"><span data-stu-id="cccc3-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="cccc3-135">Werkelijke waarden vastleggen op basis van projectgebeurtenissen</span><span class="sxs-lookup"><span data-stu-id="cccc3-135">Recording actuals based on project events</span></span>

<span data-ttu-id="cccc3-136">In PSA worden de financiële transacties vastgelegd die tijdens een project plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="cccc3-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="cccc3-137">Deze transacties worden geregistreerd als **werkelijke waarden**.</span><span class="sxs-lookup"><span data-stu-id="cccc3-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="cccc3-138">In de volgende tabellen ziet u de verschillende typen werkelijke waarden die worden gemaakt, afhankelijk van of het project een project op basis van tijd- en materiaalverbruik of een project met een vaste prijs is en of dit zich in de pre-salesfase bevindt of een intern project is.</span><span class="sxs-lookup"><span data-stu-id="cccc3-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="cccc3-139">**De resource behoort tot dezelfde organisatie-eenheid als de contracterende eenheid van het project**</span><span class="sxs-lookup"><span data-stu-id="cccc3-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="cccc3-140">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="cccc3-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="cccc3-141">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="cccc3-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="cccc3-142">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="cccc3-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="cccc3-143">Intern project</span><span class="sxs-lookup"><span data-stu-id="cccc3-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="cccc3-144">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="cccc3-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="cccc3-145">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="cccc3-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="cccc3-146">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cccc3-146">Actuals</span></span></th>
<th><span data-ttu-id="cccc3-147">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="cccc3-147">Transaction currency</span></span></th>
<th><span data-ttu-id="cccc3-148">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="cccc3-148">Fixed price</span></span></th>
<th><span data-ttu-id="cccc3-149">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="cccc3-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cccc3-150">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cccc3-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="cccc3-151">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cccc3-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-152">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="cccc3-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="cccc3-153">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cccc3-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cccc3-154">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="cccc3-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cccc3-155">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-155">Cost actual</span></span></td>
<td><span data-ttu-id="cccc3-156">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cccc3-157">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="cccc3-158">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="cccc3-159">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="cccc3-160">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-161">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="cccc3-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="cccc3-162">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cccc3-163">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="cccc3-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cccc3-164">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-164">Cost actual</span></span></td>
<td><span data-ttu-id="cccc3-165">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cccc3-166">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="cccc3-167">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cccc3-168">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="cccc3-169">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-170">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cccc3-171">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-172">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="cccc3-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cccc3-173">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cccc3-174">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="cccc3-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cccc3-175">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="cccc3-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cccc3-176">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cccc3-177">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="cccc3-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="cccc3-178">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cccc3-179">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="cccc3-180">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-181">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="cccc3-181">Billed sales</span></span></td>
<td><span data-ttu-id="cccc3-182">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cccc3-183">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="cccc3-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cccc3-184">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="cccc3-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cccc3-185">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cccc3-186">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cccc3-187">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cccc3-188">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cccc3-189">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-190">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cccc3-191">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-192">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="cccc3-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cccc3-193">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cccc3-194">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="cccc3-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cccc3-195">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="cccc3-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cccc3-196">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="cccc3-197">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="cccc3-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="cccc3-198">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="cccc3-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="cccc3-199">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cccc3-200">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="cccc3-201">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-202">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="cccc3-202">Billed sales</span></span></td>
<td><span data-ttu-id="cccc3-203">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cccc3-204">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="cccc3-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cccc3-205">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="cccc3-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cccc3-206">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-207">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="cccc3-208">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-209">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="cccc3-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="cccc3-210">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cccc3-211">**De resource behoort tot een andere organisatie-eenheid dan de contracterende eenheid van het project**</span><span class="sxs-lookup"><span data-stu-id="cccc3-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="cccc3-212">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="cccc3-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="cccc3-213">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="cccc3-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="cccc3-214">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="cccc3-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="cccc3-215">Intern project</span><span class="sxs-lookup"><span data-stu-id="cccc3-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="cccc3-216">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="cccc3-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="cccc3-217">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="cccc3-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="cccc3-218">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cccc3-218">Actuals</span></span></th>
<th><span data-ttu-id="cccc3-219">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="cccc3-219">Transaction currency</span></span></th>
<th><span data-ttu-id="cccc3-220">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="cccc3-220">Fixed price</span></span></th>
<th><span data-ttu-id="cccc3-221">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="cccc3-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cccc3-222">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cccc3-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="cccc3-223">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cccc3-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-224">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="cccc3-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="cccc3-225">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="cccc3-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="cccc3-226">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="cccc3-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cccc3-227">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-227">Cost actual</span></span></td>
<td><span data-ttu-id="cccc3-228">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="cccc3-229">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="cccc3-230">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="cccc3-231">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="cccc3-232">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-233">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="cccc3-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="cccc3-234">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-235">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="cccc3-236">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-237">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="cccc3-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="cccc3-238">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="cccc3-239">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="cccc3-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cccc3-240">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-240">Cost actual</span></span></td>
<td><span data-ttu-id="cccc3-241">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cccc3-242">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="cccc3-243">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cccc3-244">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="cccc3-245">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="cccc3-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-246">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="cccc3-247">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-248">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="cccc3-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="cccc3-249">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-250">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cccc3-251">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-252">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="cccc3-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cccc3-253">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cccc3-254">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="cccc3-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cccc3-255">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="cccc3-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cccc3-256">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cccc3-257">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="cccc3-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="cccc3-258">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cccc3-259">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="cccc3-260">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-261">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="cccc3-261">Billed sales</span></span></td>
<td><span data-ttu-id="cccc3-262">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cccc3-263">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="cccc3-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cccc3-264">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="cccc3-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cccc3-265">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cccc3-266">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cccc3-267">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cccc3-268">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cccc3-269">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-270">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cccc3-271">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-272">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="cccc3-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cccc3-273">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cccc3-274">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="cccc3-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cccc3-275">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="cccc3-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cccc3-276">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="cccc3-277">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="cccc3-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="cccc3-278">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="cccc3-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="cccc3-279">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cccc3-280">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="cccc3-281">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="cccc3-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-282">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="cccc3-282">Billed sales</span></span></td>
<td><span data-ttu-id="cccc3-283">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cccc3-284">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="cccc3-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cccc3-285">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="cccc3-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cccc3-286">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-287">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="cccc3-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="cccc3-288">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cccc3-289">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="cccc3-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="cccc3-290">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="cccc3-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]