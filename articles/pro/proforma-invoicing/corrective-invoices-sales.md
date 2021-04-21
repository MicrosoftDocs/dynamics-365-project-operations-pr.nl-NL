---
title: Correctiefacturen voor project
description: Dit onderwerp biedt informatie over het maken en bevestigen van correctiefacturen in Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae6d881e4e68b9f467478afe9735fc3186e6b0a8
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866585"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="1f5fa-103">Correctiefacturen voor project</span><span class="sxs-lookup"><span data-stu-id="1f5fa-103">Corrective project invoices</span></span>

<span data-ttu-id="1f5fa-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="1f5fa-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1f5fa-105">Een bevestigde projectfactuur kan worden gecorrigeerd om wijzigingen of tegoeden te verwerken, zoals overeengekomen met de klant en de projectmanager.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="1f5fa-106">Als u wijzigingen wilt aanbrengen in een bevestigde factuur, opent u de bevestigde factuur en selecteert u **Deze factuur corrigeren**.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="1f5fa-107">Deze selectie is alleen beschikbaar als een projectfactuur is bevestigd.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="1f5fa-108">Er wordt een nieuwe conceptfactuur gemaakt op basis van de bevestigde factuur.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="1f5fa-109">Alle factuurregeldetails van de eerder bevestigde factuur worden naar het nieuwe concept gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="1f5fa-110">Hieronder volgen enkele van de belangrijkste punten die u moet weten over de regeldetails van de nieuwe gecorrigeerde factuur:</span><span class="sxs-lookup"><span data-stu-id="1f5fa-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="1f5fa-111">Alle hoeveelheden worden bijgewerkt naar nul.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-111">All quantities are updated to zero.</span></span> <span data-ttu-id="1f5fa-112">Er wordt vanuit gegaan dat alle gefactureerde artikelen volledig worden gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="1f5fa-113">Indien nodig kunt u deze hoeveelheden handmatig bijwerken om de hoeveelheid weer te geven die wordt gefactureerd, en niet de hoeveelheid die wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="1f5fa-114">Op basis van de hoeveelheid die u invoert, wordt de gecrediteerde hoeveelheid berekend.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="1f5fa-115">Dit bedrag wordt weergegeven in de werkelijke waarden die worden gemaakt wanneer de gecorrigeerde factuur wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="1f5fa-116">Als u wijzigingen aanbrengt in het belastingbedrag, moet u het juiste belastingbedrag invoeren en niet het belastingbedrag dat wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="1f5fa-117">Eerder bevestigde productgebaseerde contractregels worden niet gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="1f5fa-118">Het verwerken van correcties in een productgebaseerde projectfactuur wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="1f5fa-119">Mijlpaalcorrecties worden altijd verwerkt als volledige tegoeden.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="1f5fa-120">Voorschot- of vooruitbetalingsbedragen kunnen worden gecorrigeerd als de klant voor een onjuist bedrag is gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="1f5fa-121">Afstemmingen van voorschotten en vooruitbetalingen kunnen worden gecorrigeerd als een onjuist bedrag is gebruikt om af te stemmen met de kosten op een eerder bevestigde factuur.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f5fa-122">Voor factuurregeldetails die correcties zijn voor andere reeds gefactureerde kosten, is het veld **Correctie** ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="1f5fa-123">Facturen met gecorrigeerde factuurregeldetails hebben een veld met de naam **Heeft correcties** dat ook is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="1f5fa-124">Werkelijke waarden die worden gemaakt wanneer een correctiefactuur wordt bevestigd</span><span class="sxs-lookup"><span data-stu-id="1f5fa-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="1f5fa-125">De volgende tabel biedt een overzicht van de werkelijke waarden die worden gemaakt wanneer een correctiefactuur wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="1f5fa-126">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1f5fa-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="1f5fa-127">
                    <strong>Werkelijke waarden gemaakt bij bevestiging</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1f5fa-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="1f5fa-128">Bevestig de correctie van een gefactureerd voorschot of gefactureerde vooruitbetaling.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1f5fa-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-129">Een niet-gefactureerde verkoopterugboeking van het voorschot of de vooruitbetaling die is gemaakt voor afstemming.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="1f5fa-130">Dit bedrag is positief omdat het bedoeld is om het negatieve bedrag op te heffen dat is ontstaan toen het voorschot of de vooruitbetaling werd gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-131">Er wordt een werkelijke waarde voor gefactureerde verkoopterugboeking gemaakt voor het bedrag op het voorschot of de vooruitbetaling om de oorspronkelijke gefactureerde verkoop terug te boeken.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-132">Er wordt een nieuwe werkelijke waarde voor gefactureerde verkoop gemaakt voor het gecorrigeerde bedrag op de gecorrigeerde factuurregel van het voorschot of de vooruitbetaling.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-133">Een werkelijke waarde voor niet-gefactureerde verkoop van een negatief bedrag op de factuurregel van het voorschot of de vooruitbetaling, die voor afstemming wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="1f5fa-134">Een bevestiging van de correctie van een eerder afgestemd voorschot of afgestemde vooruitbetaling.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-135">Een niet-gefactureerde verkoopterugboeking van het voorschot of de vooruitbetaling die is gemaakt voor afstemming.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="1f5fa-136">Dit bedrag is positief en is bedoeld om het negatieve bedrag op te heffen dat is ontstaan toen de vorige afstemming plaatsvond.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-137">Een werkelijke waarde voor gefactureerde verkoopterugboeking voor het bedrag op de vorige factuur.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-138">Een nieuwe werkelijke waarde voor gefactureerde verkoop gemaakt voor het gecorrigeerde bedrag van het voorschot, die op de gecorrigeerde factuur wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-139">Een werkelijke waarde voor niet-gefactureerde verkoop met een negatief bedrag van het gecorrigeerde resterende voorschot of de gecorrigeerde resterende vooruitbetaling, die voor afstemming op latere facturen wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1f5fa-140">Facturering van het volledige tegoed van een eerder gefactureerde tijdtransactie.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-141">Een gefactureerde verkoopterugboeking voor de uren en het bedrag op de oorspronkelijke factuurregeldetails voor tijd.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-142">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop voor de uren en het bedrag op de oorspronkelijke factuurregeldetails voor tijd.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1f5fa-143">Facturering van het gedeeltelijke tegoed voor een tijdtransactie.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-144">Een gefactureerde verkoopterugboeking voor de uren en het gefactureerde bedrag op de oorspronkelijke factuurregeldetails voor tijd.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-145">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de uren en het bedrag op de bewerkte factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-146">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de resterende uren en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de factuurregeldetails.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1f5fa-147">Facturering van het volledige tegoed van een eerder gefactureerde onkostentransactie.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-148">Een gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de onkosten.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-149">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de onkosten.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1f5fa-150">Facturering van het gedeeltelijke tegoed van een eerder gefactureerde onkostentransactie.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-151">Een gefactureerde verkoopterugboeking voor de hoeveelheid en het gefactureerde bedrag op de oorspronkelijke factuurregeldetails voor onkosten.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-152">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de hoeveelheid en het bedrag op de gecorrigeerde factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-153">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de resterende hoeveelheid en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de factuurregeldetails.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1f5fa-154">Het volledige krediet van een eerder gefactureerde materiaaltransactie factureren.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-155">Een gefactureerde terugboeking voor de hoeveelheid en het bedrag in de oorspronkelijke factuurregeldetails voor materiaal.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-156">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde voor de hoeveelheid en het bedrag in de oorspronkelijke factuurregeldetails voor materiaal.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1f5fa-157">Het gedeeltelijke krediet voor een materiaaltransactie factureren.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-158">Een gefactureerde terugboeking voor de hoeveelheid en het gefactureerde bedrag in de oorspronkelijke factuurregeldetails voor materiaal.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-159">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de hoeveelheid en het bedrag in de bewerkte factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-160">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de resterende hoeveelheid en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de factuurregeldetails.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1f5fa-161">Facturering van het volledige tegoed van een eerder gefactureerde kostentransactie.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-162">Een gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de kosten.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-163">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de kosten.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1f5fa-164">Facturering van het gedeeltelijke tegoed van een eerder gefactureerde kostentransactie.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-165">Een gefactureerde verkoopterugboeking voor de hoeveelheid en het gefactureerde bedrag op de oorspronkelijke factuurregeldetails voor kosten.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-166">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte gecorrigeerde factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="1f5fa-167">Facturering van het volledige tegoed van een eerder gefactureerde mijlpaal.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-168">Een gefactureerde verkoopterugboeking voor het bedrag op de oorspronkelijke factuurregeldetails voor de mijlpaal.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="1f5fa-169">De factuurstatus van de mijlpaal wordt bijgewerkt van <b>Klantfactuur geboekt</b> naar <b>Gereed voor facturering</b>​.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="1f5fa-170">Facturering van het gedeeltelijke tegoed van een eerder gefactureerde mijlpaal.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-171">Niet ondersteund</span><span class="sxs-lookup"><span data-stu-id="1f5fa-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="1f5fa-172">Tegoeden en correcties van een eerder gefactureerde productgebaseerde contractregel.</span><span class="sxs-lookup"><span data-stu-id="1f5fa-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1f5fa-173">Niet ondersteund</span><span class="sxs-lookup"><span data-stu-id="1f5fa-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
