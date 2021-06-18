---
title: Werkelijke waarden
description: Dit onderwerp biedt informatie over hoe u met werkelijke waarden kunt werken in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996605"
---
# <a name="actuals"></a><span data-ttu-id="fc2c0-103">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="fc2c0-103">Actuals</span></span> 

<span data-ttu-id="fc2c0-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="fc2c0-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fc2c0-105">Werkelijke waarden vertegenwoordigen de beoordeelde en goedgekeurde financiële en geplande voortgang van een project.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="fc2c0-106">Ze worden gemaakt als resultaat van goedkeuring van tijd, onkosten, boekingen voor materiaalgebruik en journaalboekingen en facturen.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="fc2c0-107">Journaalregels en tijdsvermelding</span><span class="sxs-lookup"><span data-stu-id="fc2c0-107">Journal lines and time submission</span></span>

<span data-ttu-id="fc2c0-108">Zie voor meer informatie over tijdinvoer [Overzicht van tijdinvoer](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fc2c0-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="fc2c0-109">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="fc2c0-109">Time and materials</span></span>

<span data-ttu-id="fc2c0-110">Wanneer een ingediende tijdsvermelding is gekoppeld aan een project dat is toegewezen aan een contractregel voor tijd en materiaal, maakt het systeem twee journaalregels aan, één voor kosten en één voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="fc2c0-111">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="fc2c0-111">Fixed price</span></span>

<span data-ttu-id="fc2c0-112">Wanneer een ingediende tijdsvermelding is gekoppeld aan een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er één journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="fc2c0-113">Standaardprijs</span><span class="sxs-lookup"><span data-stu-id="fc2c0-113">Default pricing</span></span>

<span data-ttu-id="fc2c0-114">De logica voor het maken van standaardprijzen bevindt zich op de journaalregel.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="fc2c0-115">De veldwaarden uit de tijdsvermelding worden naar de journaalregel gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="fc2c0-116">Deze waarden bevatten de transactiedatum, de contractregel waaraan het project is toegewezen en het resultaat van de valuta in de juiste prijslijst.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="fc2c0-117">De velden die van invloed zijn op standaardprijzen, zoals **Rol** en **Resource-eenheid**, worden gebruikt om de juiste prijs op de journaalregel te bepalen.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="fc2c0-118">U kunt een aangepast veld toevoegen aan de tijdsvermelding.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="fc2c0-119">Als u wilt dat de veldwaarde wordt gepropageerd naar werkelijke waarden, maakt u het veld in de tabellen **Werkelijke waarden** en **Journaalregel**.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="fc2c0-120">Gebruik aangepaste code om de geselecteerde veldwaarde via de journaalregel met behulp van transactieherkomsten door te geven van Tijdsvermelding naar Werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="fc2c0-121">Zie voor meer informatie over de oorsprong van transacties en verbindingen het onderwerp [Werkelijke waarden koppelen aan oorspronkelijke records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)​.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="fc2c0-122">Indiening van journaalregels en basisonkosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="fc2c0-123">Zie voor meer informatie over de invoer van onkosten [Onkostenoverzicht](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fc2c0-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="fc2c0-124">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="fc2c0-124">Time and materials</span></span>

<span data-ttu-id="fc2c0-125">Wanneer ingediende basisonkosten zijn gekoppeld aan een project dat is toegewezen aan een contractregel voor tijd en materiaal, maakt het systeem twee journaalregels aan, één voor kosten en één voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="fc2c0-126">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="fc2c0-126">Fixed price</span></span>

<span data-ttu-id="fc2c0-127">Wanneer een ingediende basisonkostenpost wordt gekoppeld aan een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er één journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="fc2c0-128">Standaardprijs</span><span class="sxs-lookup"><span data-stu-id="fc2c0-128">Default pricing</span></span>

<span data-ttu-id="fc2c0-129">De logica voor het invoeren van standaardprijzen voor onkosten is gebaseerd op de onkostencategorie.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="fc2c0-130">De datum van de transactie, de contractregel waaraan het project is toegewezen en de valuta worden allemaal gebruikt om de juiste prijslijst te bepalen.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="fc2c0-131">De velden die van invloed zijn op standaardprijzen, zoals **Transactiecategorie** en **Eenheid**, worden gebruikt om de juiste prijs op de journaalregel te bepalen.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="fc2c0-132">Dit werkt echter alleen als de prijsmethode in de prijslijst **Prijs per eenheid**​ is.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="fc2c0-133">Als de prijsmethode **Tegen kosten** of **Toeslag op kosten** is, wordt de prijs die is ingevoerd bij het aanmaken van de onkostenpost gebruikt voor kosten en wordt de prijs op de verkoopjournaalregel berekend op basis van de prijsmethode.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="fc2c0-134">U kunt een aangepast veld toevoegen aan de onkostenpost.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="fc2c0-135">Als u wilt dat de veldwaarde wordt gepropageerd naar werkelijke waarden, maakt u het veld in de tabellen **Werkelijke waarden** en **Journaalregel**.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="fc2c0-136">Gebruik aangepaste code om de geselecteerde veldwaarde via de journaalregel met behulp van transactieherkomsten door te geven van Tijdsvermelding naar Werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="fc2c0-137">Zie voor meer informatie over de oorsprong van transacties en verbindingen het onderwerp [Werkelijke waarden koppelen aan oorspronkelijke records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)​.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="fc2c0-138">Journaalregels en de indiening van logboeken voor materiaalgebruik</span><span class="sxs-lookup"><span data-stu-id="fc2c0-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="fc2c0-139">Zie [Logboek voor materiaalgebruik](../material/material-usage-log.md) voor meer informatie over het boeken van onkosten.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="fc2c0-140">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="fc2c0-140">Time and materials</span></span>

<span data-ttu-id="fc2c0-141">Wanneer een verzonden logboekitem voor materiaalgebruik is gekoppeld aan een project dat is toegewezen aan een contractregel voor tijd en materiaal, worden er twee journaalregels gemaakt, één voor kosten en één voor niet-gefactureerde verkopen.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="fc2c0-142">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="fc2c0-142">Fixed price</span></span>

<span data-ttu-id="fc2c0-143">Wanneer een ingediende logboekvermelding voor materiaalgebruik wordt gekoppeld aan een project dat is toegewezen aan een contractregel met een vaste prijs, wordt er één journaalregel voor kosten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="fc2c0-144">Standaardprijs</span><span class="sxs-lookup"><span data-stu-id="fc2c0-144">Default pricing</span></span>

<span data-ttu-id="fc2c0-145">De logica voor het invoeren van standaardprijzen voor materiaal is gebaseerd op de combinatie van product en eenheid.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="fc2c0-146">De datum van de transactie, de contractregel waaraan het project is toegewezen en de valuta worden allemaal gebruikt om de juiste prijslijst te bepalen.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="fc2c0-147">De velden die van invloed zijn op standaardprijzen, zoals **Product-id** en **Resource-eenheid**, worden gebruikt om de juiste prijs op de journaalregel te bepalen.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="fc2c0-148">Dit werkt echter alleen voor catalogusproducten.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-148">However, this only works for catalog products.</span></span> <span data-ttu-id="fc2c0-149">Voor toe te voegen producten wordt de ingevoerde prijs bij het maken van de logboekvermelding voor materiaalgebruik gebruikt voor de kostprijs en verkoopprijs op de journaalregels.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="fc2c0-150">U kunt een aangepast veld toevoegen aan de vermelding **Logboek voor materiaalgebruik**.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="fc2c0-151">Als u wilt dat de veldwaarde wordt gepropageerd naar werkelijke waarden, maakt u het veld in de tabellen **Werkelijke waarden** en **Journaalregel**.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="fc2c0-152">Gebruik aangepaste code om de geselecteerde veldwaarde via de journaalregel met behulp van transactieherkomsten door te geven van Tijdsvermelding naar Werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="fc2c0-153">Zie voor meer informatie over de oorsprong van transacties en verbindingen het onderwerp [Werkelijke waarden koppelen aan oorspronkelijke records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)​.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="fc2c0-154">Invoerjournalen gebruiken om kosten vast te leggen</span><span class="sxs-lookup"><span data-stu-id="fc2c0-154">Use entry journals to record costs</span></span>

<span data-ttu-id="fc2c0-155">U kunt invoerjournalen gebruiken om de kosten of onkosten vast te leggen in de klassen voor materiaal, tarief, tijd, onkosten of belastingtransactie.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="fc2c0-156">U kunt de volgende journalen gebruiken voor de volgende doeleinden:</span><span class="sxs-lookup"><span data-stu-id="fc2c0-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="fc2c0-157">Verplaats werkelijke transactiewaarden van een ander systeem naar Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="fc2c0-158">Leg kosten vast die zich in een ander systeem hebben voorgedaan.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="fc2c0-159">Deze kosten kunnen inkoop- of uitbestedingskosten omvatten.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc2c0-160">De toepassing valideert het journaalregeltype of de gerelateerde prijzen die op de journaalregel zijn ingevoerd niet.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="fc2c0-161">Daarom mag alleen een gebruiker die zich volledig bewust is van de boekhoudkundige impact van werkelijke waarden op het project invoerjournalen gebruiken om werkelijke waarden te maken.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="fc2c0-162">Vanwege de impact van dit journaaltype, moet u zorgvuldig kiezen wie toegang heeft om boekingsjournalen te maken.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="fc2c0-163">Werkelijke waarden vastleggen op basis van projectgebeurtenissen</span><span class="sxs-lookup"><span data-stu-id="fc2c0-163">Record actuals based on project events</span></span>

<span data-ttu-id="fc2c0-164">In Project Operations worden de financiële transacties vastgelegd die tijdens een project plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="fc2c0-165">Deze transacties worden geregistreerd als werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="fc2c0-166">In de volgende tabellen ziet u de verschillende typen werkelijke waarden die worden gemaakt, afhankelijk van of het project een project op basis van tijd- en materiaalverbruik of een project met een vaste prijs is en of dit zich in de pre-salesfase bevindt of een intern project is.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="fc2c0-167">De resource behoort tot dezelfde organisatie-eenheid als de contracterende eenheid van het project</span><span class="sxs-lookup"><span data-stu-id="fc2c0-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="fc2c0-168">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="fc2c0-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="fc2c0-169">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="fc2c0-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="fc2c0-170">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="fc2c0-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="fc2c0-171">Intern project</span><span class="sxs-lookup"><span data-stu-id="fc2c0-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="fc2c0-172">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="fc2c0-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="fc2c0-173">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="fc2c0-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="fc2c0-174">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="fc2c0-174">Actuals</span></span></th>
<th><span data-ttu-id="fc2c0-175">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="fc2c0-175">Transaction currency</span></span></th>
<th><span data-ttu-id="fc2c0-176">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="fc2c0-176">Fixed price</span></span></th>
<th><span data-ttu-id="fc2c0-177">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="fc2c0-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fc2c0-178">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="fc2c0-179">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="fc2c0-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-180">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="fc2c0-181">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="fc2c0-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="fc2c0-182">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="fc2c0-183">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-183">Cost actual</span></span></td>
<td><span data-ttu-id="fc2c0-184">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="fc2c0-185">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="fc2c0-186">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="fc2c0-187">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="fc2c0-188">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-189">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="fc2c0-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="fc2c0-190">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fc2c0-191">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="fc2c0-192">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-192">Cost actual</span></span></td>
<td><span data-ttu-id="fc2c0-193">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="fc2c0-194">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="fc2c0-195">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="fc2c0-196">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="fc2c0-197">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-198">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="fc2c0-199">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-200">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="fc2c0-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="fc2c0-201">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="fc2c0-202">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="fc2c0-203">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="fc2c0-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="fc2c0-204">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="fc2c0-205">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="fc2c0-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="fc2c0-206">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="fc2c0-207">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="fc2c0-208">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-209">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="fc2c0-209">Billed sales</span></span></td>
<td><span data-ttu-id="fc2c0-210">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fc2c0-211">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="fc2c0-212">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="fc2c0-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="fc2c0-213">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="fc2c0-214">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="fc2c0-215">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="fc2c0-216">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="fc2c0-217">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-218">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="fc2c0-219">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-220">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="fc2c0-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="fc2c0-221">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="fc2c0-222">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="fc2c0-223">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="fc2c0-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="fc2c0-224">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="fc2c0-225">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="fc2c0-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="fc2c0-226">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="fc2c0-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="fc2c0-227">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="fc2c0-228">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="fc2c0-229">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-230">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="fc2c0-230">Billed sales</span></span></td>
<td><span data-ttu-id="fc2c0-231">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fc2c0-232">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="fc2c0-233">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="fc2c0-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="fc2c0-234">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-235">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="fc2c0-236">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-237">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="fc2c0-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="fc2c0-238">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="fc2c0-239">De resource behoort tot een andere organisatie-eenheid dan de contracterende eenheid van het project</span><span class="sxs-lookup"><span data-stu-id="fc2c0-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="fc2c0-240">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="fc2c0-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="fc2c0-241">Factureerbaar of verkocht project</span><span class="sxs-lookup"><span data-stu-id="fc2c0-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="fc2c0-242">Project in de pre-salesfase</span><span class="sxs-lookup"><span data-stu-id="fc2c0-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="fc2c0-243">Intern project</span><span class="sxs-lookup"><span data-stu-id="fc2c0-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="fc2c0-244">Tijd- en materiaalverbruik</span><span class="sxs-lookup"><span data-stu-id="fc2c0-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="fc2c0-245">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="fc2c0-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="fc2c0-246">Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="fc2c0-246">Actuals</span></span></th>
<th><span data-ttu-id="fc2c0-247">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="fc2c0-247">Transaction currency</span></span></th>
<th><span data-ttu-id="fc2c0-248">Vaste prijs</span><span class="sxs-lookup"><span data-stu-id="fc2c0-248">Fixed price</span></span></th>
<th><span data-ttu-id="fc2c0-249">Transactievaluta</span><span class="sxs-lookup"><span data-stu-id="fc2c0-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fc2c0-250">Er wordt een tijdsvermelding gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="fc2c0-251">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="fc2c0-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-252">Er wordt een tijdsvermelding ingediend.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="fc2c0-253">Geen activiteit in de entiteit Werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="fc2c0-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="fc2c0-254">De tijd wordt goedgekeurd en er treedt geen wijziging of toename in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="fc2c0-255">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-255">Cost actual</span></span></td>
<td><span data-ttu-id="fc2c0-256">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="fc2c0-257">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="fc2c0-258">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="fc2c0-259">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="fc2c0-260">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-261">Niet-gefactureerde werkelijke waarde voor verkoop - Toerekenbaar</span><span class="sxs-lookup"><span data-stu-id="fc2c0-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="fc2c0-262">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-263">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="fc2c0-264">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-265">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="fc2c0-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="fc2c0-266">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="fc2c0-267">De tijd wordt goedgekeurd en er treedt een afname in de factureerbare uren op tijdens de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="fc2c0-268">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-268">Cost actual</span></span></td>
<td><span data-ttu-id="fc2c0-269">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="fc2c0-270">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="fc2c0-271">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="fc2c0-272">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="fc2c0-273">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="fc2c0-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-274">Kosten van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="fc2c0-275">Valuta van resource-eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-276">Interorganisatorische verkopen</span><span class="sxs-lookup"><span data-stu-id="fc2c0-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="fc2c0-277">Valuta van contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-278">Niet-gefactureerde werkelijke waarde voor verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="fc2c0-279">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-280">Niet-gefactureerde werkelijke waarde voor verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="fc2c0-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="fc2c0-281">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="fc2c0-282">Een factuur wordt bevestigd en er treedt geen wijziging of toename in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="fc2c0-283">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="fc2c0-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="fc2c0-284">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="fc2c0-285">Gefactureerde verkoop voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="fc2c0-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="fc2c0-286">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="fc2c0-287">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="fc2c0-288">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-289">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="fc2c0-289">Billed sales</span></span></td>
<td><span data-ttu-id="fc2c0-290">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fc2c0-291">Een factuur wordt bevestigd en er treedt een afname in de factureerbare uren op.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="fc2c0-292">Niet-gefactureerde terugboeking</span><span class="sxs-lookup"><span data-stu-id="fc2c0-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="fc2c0-293">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="fc2c0-294">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="fc2c0-295">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="fc2c0-296">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="fc2c0-297">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-298">Gefactureerde verkoop – Toerekenbaar voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="fc2c0-299">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-300">Gefactureerde verkoop – Niet-toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="fc2c0-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="fc2c0-301">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="fc2c0-302">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="fc2c0-303">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="fc2c0-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="fc2c0-304">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="fc2c0-305">Gefactureerde terugboeking voor mijlpaal</span><span class="sxs-lookup"><span data-stu-id="fc2c0-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="fc2c0-306">Wijziging in mijlpaalstatus van <strong>Gefactureerd</strong> in <strong>Gereed voor facturering</strong></span><span class="sxs-lookup"><span data-stu-id="fc2c0-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="fc2c0-307">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="fc2c0-308">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="fc2c0-309">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="fc2c0-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-310">Gefactureerde verkoop</span><span class="sxs-lookup"><span data-stu-id="fc2c0-310">Billed sales</span></span></td>
<td><span data-ttu-id="fc2c0-311">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fc2c0-312">Een factuur wordt gecorrigeerd om de toerekenbare hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="fc2c0-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="fc2c0-313">Gefactureerde verkoop - Terugboeking</span><span class="sxs-lookup"><span data-stu-id="fc2c0-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="fc2c0-314">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-315">Gefactureerde verkoop voor de nieuwe hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="fc2c0-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="fc2c0-316">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc2c0-317">Niet-gefactureerde verkoop – Toerekenbaar voor het verschil</span><span class="sxs-lookup"><span data-stu-id="fc2c0-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="fc2c0-318">Valuta voor projectcontract</span><span class="sxs-lookup"><span data-stu-id="fc2c0-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
