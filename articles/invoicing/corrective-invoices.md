---
title: Projectgebaseerde correctiefacturen maken
description: Dit onderwerp biedt informatie over correctiefacturen in Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788846"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="ced0d-103">Projectgebaseerde correctiefacturen maken</span><span class="sxs-lookup"><span data-stu-id="ced0d-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="ced0d-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="ced0d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ced0d-105">Een bevestigde projectfactuur kan worden gecorrigeerd om wijzigingen of tegoeden te verwerken, zoals overeengekomen met de klant en de projectmanager.</span><span class="sxs-lookup"><span data-stu-id="ced0d-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="ced0d-106">Als u wijzigingen wilt aanbrengen in een bevestigde factuur, opent u de bevestigde factuur en selecteert u **Deze factuur corrigeren**.</span><span class="sxs-lookup"><span data-stu-id="ced0d-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="ced0d-107">Deze selectie is alleen beschikbaar als een projectfactuur is bevestigd.</span><span class="sxs-lookup"><span data-stu-id="ced0d-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="ced0d-108">Er wordt een nieuwe conceptfactuur gemaakt op basis van de bevestigde factuur.</span><span class="sxs-lookup"><span data-stu-id="ced0d-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="ced0d-109">Alle factuurregeldetails van de eerder bevestigde factuur worden naar het nieuwe concept gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="ced0d-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="ced0d-110">Hieronder volgen enkele belangrijke punten om u meer inzicht te geven in de regeldetails op de nieuwe gecorrigeerde factuur:</span><span class="sxs-lookup"><span data-stu-id="ced0d-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="ced0d-111">Alle hoeveelheden worden bijgewerkt naar nul.</span><span class="sxs-lookup"><span data-stu-id="ced0d-111">All quantities are updated to zero.</span></span> <span data-ttu-id="ced0d-112">Hierbij wordt ervan uitgegaan dat alle gefactureerde artikelen volledig zijn gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="ced0d-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="ced0d-113">Indien nodig kunt u deze hoeveelheden handmatig bijwerken om de hoeveelheid weer te geven die wordt gefactureerd, en niet de hoeveelheid die wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="ced0d-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="ced0d-114">Op basis van de hoeveelheid die u invoert, wordt de gecrediteerde hoeveelheid berekend.</span><span class="sxs-lookup"><span data-stu-id="ced0d-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="ced0d-115">Dit bedrag wordt weergegeven in de werkelijke waarden die worden gemaakt wanneer de gecorrigeerde factuur wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="ced0d-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="ced0d-116">Als u wijzigingen aanbrengt in het belastingbedrag, moet u het juiste belastingbedrag invoeren en niet het belastingbedrag dat wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="ced0d-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="ced0d-117">Mijlpaalcorrecties worden altijd verwerkt als volledige tegoeden.</span><span class="sxs-lookup"><span data-stu-id="ced0d-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="ced0d-118">Voorschot- of vooruitbetalingsbedragen kunnen worden gecorrigeerd als de klant voor een onjuist bedrag is gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="ced0d-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="ced0d-119">Afstemmingen van voorschotten en vooruitbetalingen kunnen worden gecorrigeerd als een onjuist bedrag is gebruikt om af te stemmen met de kosten op een eerder bevestigde factuur.</span><span class="sxs-lookup"><span data-stu-id="ced0d-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ced0d-120">Voor factuurregeldetails die correcties zijn voor andere reeds gefactureerde kosten is het veld **Correctie** ingesteld op **Ja**​.</span><span class="sxs-lookup"><span data-stu-id="ced0d-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="ced0d-121">Facturen met gecorrigeerde factuurregeldetails hebben een veld met de naam **Heeft correcties** dat ook is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ced0d-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="ced0d-122">Werkelijke waarden die bij bevestiging van een correctiefactuur worden gemaakt</span><span class="sxs-lookup"><span data-stu-id="ced0d-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="ced0d-123">De volgende tabel biedt een overzicht van de werkelijke waarden die worden gemaakt wanneer een correctiefactuur wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="ced0d-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="ced0d-124">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ced0d-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="ced0d-125">
                    <strong>Werkelijke waarden gemaakt bij bevestiging</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ced0d-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="ced0d-126">Bevestig de correctie van een gefactureerd voorschot of gefactureerde vooruitbetaling.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ced0d-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-127">Een niet-gefactureerde verkoopterugboeking van het voorschot of de vooruitbetaling die is gemaakt voor afstemming.</span><span class="sxs-lookup"><span data-stu-id="ced0d-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="ced0d-128">Dit bedrag is positief omdat het bedoeld is om het negatieve bedrag op te heffen dat is ontstaan toen het voorschot of de vooruitbetaling werd gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="ced0d-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-129">Er wordt een werkelijke waarde voor gefactureerde verkoopterugboeking gemaakt voor het bedrag op het voorschot of de vooruitbetaling om de oorspronkelijke gefactureerde verkoop terug te boeken.</span><span class="sxs-lookup"><span data-stu-id="ced0d-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-130">Er wordt een nieuwe werkelijke waarde voor gefactureerde verkoop gemaakt voor het gecorrigeerde bedrag op de gecorrigeerde factuurregel van het voorschot of de vooruitbetaling.</span><span class="sxs-lookup"><span data-stu-id="ced0d-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-131">Een werkelijke waarde voor niet-gefactureerde verkoop van een negatief bedrag op de factuurregel van het voorschot of de vooruitbetaling, die voor afstemming wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ced0d-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="ced0d-132">Een bevestiging van de correctie van een eerder afgestemd voorschot of afgestemde vooruitbetaling.</span><span class="sxs-lookup"><span data-stu-id="ced0d-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-133">Een niet-gefactureerde verkoopterugboeking van het voorschot of de vooruitbetaling die is gemaakt voor afstemming.</span><span class="sxs-lookup"><span data-stu-id="ced0d-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="ced0d-134">Dit bedrag is positief en is bedoeld om het negatieve bedrag op te heffen dat is ontstaan toen de vorige afstemming plaatsvond.</span><span class="sxs-lookup"><span data-stu-id="ced0d-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-135">Een werkelijke waarde voor gefactureerde verkoopterugboeking voor het bedrag op de vorige factuur.</span><span class="sxs-lookup"><span data-stu-id="ced0d-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-136">Een nieuwe werkelijke waarde voor gefactureerde verkoop gemaakt voor het gecorrigeerde bedrag van het voorschot, die op de gecorrigeerde factuur wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="ced0d-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-137">Een werkelijke waarde voor niet-gefactureerde verkoop met een negatief bedrag van het gecorrigeerde resterende voorschot of de gecorrigeerde resterende vooruitbetaling, die voor afstemming op latere facturen wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ced0d-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ced0d-138">Facturering van het volledige tegoed van een eerder gefactureerde tijdtransactie.</span><span class="sxs-lookup"><span data-stu-id="ced0d-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-139">Een gefactureerde verkoopterugboeking voor de uren en het bedrag op de oorspronkelijke factuurregeldetails voor tijd.</span><span class="sxs-lookup"><span data-stu-id="ced0d-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-140">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop voor de uren en het bedrag op de oorspronkelijke factuurregeldetails voor tijd.</span><span class="sxs-lookup"><span data-stu-id="ced0d-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ced0d-141">Facturering van het gedeeltelijke tegoed voor een tijdtransactie.</span><span class="sxs-lookup"><span data-stu-id="ced0d-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-142">Een gefactureerde verkoopterugboeking voor de uren en het gefactureerde bedrag op de oorspronkelijke factuurregeldetails voor tijd.</span><span class="sxs-lookup"><span data-stu-id="ced0d-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-143">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de uren en het bedrag op de bewerkte factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="ced0d-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-144">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de resterende uren en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de factuurregeldetails.</span><span class="sxs-lookup"><span data-stu-id="ced0d-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ced0d-145">Facturering van het volledige tegoed van een eerder gefactureerde onkostentransactie.</span><span class="sxs-lookup"><span data-stu-id="ced0d-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-146">Een gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de onkosten.</span><span class="sxs-lookup"><span data-stu-id="ced0d-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-147">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de onkosten.</span><span class="sxs-lookup"><span data-stu-id="ced0d-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ced0d-148">Facturering van het gedeeltelijke tegoed van een eerder gefactureerde onkostentransactie.</span><span class="sxs-lookup"><span data-stu-id="ced0d-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-149">Een gefactureerde verkoopterugboeking voor de hoeveelheid en het gefactureerde bedrag op de oorspronkelijke factuurregeldetails voor onkosten.</span><span class="sxs-lookup"><span data-stu-id="ced0d-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-150">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de hoeveelheid en het bedrag op de gecorrigeerde factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="ced0d-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-151">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de resterende hoeveelheid en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de factuurregeldetails.</span><span class="sxs-lookup"><span data-stu-id="ced0d-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ced0d-152">Facturering van het volledige tegoed van een eerder gefactureerde kostentransactie.</span><span class="sxs-lookup"><span data-stu-id="ced0d-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-153">Een gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de kosten.</span><span class="sxs-lookup"><span data-stu-id="ced0d-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-154">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de kosten.</span><span class="sxs-lookup"><span data-stu-id="ced0d-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ced0d-155">Facturering van het gedeeltelijke tegoed van een eerder gefactureerde kostentransactie.</span><span class="sxs-lookup"><span data-stu-id="ced0d-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-156">Een gefactureerde verkoopterugboeking voor de hoeveelheid en het gefactureerde bedrag op de oorspronkelijke factuurregeldetails voor kosten.</span><span class="sxs-lookup"><span data-stu-id="ced0d-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-157">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte gecorrigeerde factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="ced0d-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ced0d-158">Facturering van het volledige tegoed van een eerder gefactureerde mijlpaal.</span><span class="sxs-lookup"><span data-stu-id="ced0d-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-159">Een gefactureerde verkoopterugboeking voor het bedrag op de oorspronkelijke factuurregeldetails voor de mijlpaal.</span><span class="sxs-lookup"><span data-stu-id="ced0d-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="ced0d-160">De factuurstatus van de mijlpaal wordt bijgewerkt van <b>Klantfactuur geboekt</b> naar <b>Gereed voor facturering</b>​.</span><span class="sxs-lookup"><span data-stu-id="ced0d-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ced0d-161">Facturering van het gedeeltelijke tegoed van een eerder gefactureerde mijlpaal.</span><span class="sxs-lookup"><span data-stu-id="ced0d-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ced0d-162">Niet ondersteund</span><span class="sxs-lookup"><span data-stu-id="ced0d-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
