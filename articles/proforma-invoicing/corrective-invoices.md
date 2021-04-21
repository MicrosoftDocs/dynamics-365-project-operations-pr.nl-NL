---
title: Projectgebaseerde correctiefacturen
description: Dit onderwerp biedt informatie over het maken en bevestigen van projectgebaseerde correctiefacturen in Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867035"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="e2fc5-103">Projectgebaseerde correctiefacturen</span><span class="sxs-lookup"><span data-stu-id="e2fc5-103">Corrective project-based invoices</span></span>

<span data-ttu-id="e2fc5-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="e2fc5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e2fc5-105">Een bevestigde projectfactuur kan worden gecorrigeerd om wijzigingen of tegoeden te verwerken, zoals overeengekomen met de klant en de projectmanager.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="e2fc5-106">Als u wijzigingen wilt aanbrengen in een bevestigde factuur, opent u de bevestigde factuur en selecteert u **Deze factuur corrigeren**.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="e2fc5-107">Deze selectie is niet beschikbaar tenzij een projectfactuur wordt bevestigd of de projectgebaseerde factuur voorschotten of vooruitbetalingen of afstemmingen van voorschotten of vooruitbetalingen bevat.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="e2fc5-108">Er wordt een nieuwe conceptfactuur gemaakt op basis van de bevestigde factuur.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="e2fc5-109">Alle factuurregeldetails van de eerder bevestigde factuur worden naar het nieuwe concept gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="e2fc5-110">Hieronder volgen enkele van de belangrijkste punten die u moet weten over de regeldetails van de nieuwe gecorrigeerde factuur:</span><span class="sxs-lookup"><span data-stu-id="e2fc5-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="e2fc5-111">Alle hoeveelheden worden bijgewerkt naar nul.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-111">All quantities are updated to zero.</span></span> <span data-ttu-id="e2fc5-112">In Dynamics 365 Project Operations wordt ervan uitgegaan dat alle gefactureerde artikelen volledig zijn gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="e2fc5-113">Indien nodig kunt u deze hoeveelheden handmatig bijwerken om de hoeveelheid weer te geven die wordt gefactureerd, en niet de hoeveelheid die wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="e2fc5-114">Op basis van de hoeveelheid die u invoert, wordt de gecrediteerde hoeveelheid berekend.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="e2fc5-115">Dit bedrag wordt weergegeven in de werkelijke waarden die worden gemaakt wanneer de gecorrigeerde factuur wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="e2fc5-116">Als u wijzigingen aanbrengt in het belastingbedrag, moet u het juiste belastingbedrag invoeren en niet het belastingbedrag dat wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="e2fc5-117">Mijlpaalcorrecties worden altijd verwerkt als volledige tegoeden.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="e2fc5-118">Voor factuurregeldetails die correcties zijn voor andere reeds gefactureerde kosten is het veld **Correctie** ingesteld op **Ja**​.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="e2fc5-119">Voor facturen met gecorrigeerde factuurregeldetails is het veld **Bevat correcties** ingesteld op **Ja**​.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="e2fc5-120">Werkelijke waarden die worden gemaakt wanneer een correctiefactuur wordt bevestigd</span><span class="sxs-lookup"><span data-stu-id="e2fc5-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="e2fc5-121">De volgende tabel biedt een overzicht van de werkelijke waarden die worden gemaakt wanneer een correctiefactuur wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="e2fc5-122">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2fc5-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="e2fc5-123">
                    <strong>Werkelijke waarden gemaakt bij bevestiging</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2fc5-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2fc5-124">Facturering van het volledige tegoed van een eerder gefactureerde tijdtransactie.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-125">Een gefactureerde verkoopterugboeking voor de uren en het bedrag op de oorspronkelijke factuurregeldetails voor tijd.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-126">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop voor de uren en het bedrag op de oorspronkelijke factuurregeldetails voor tijd.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e2fc5-127">Facturering van het gedeeltelijke tegoed voor een tijdtransactie.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-128">Een gefactureerde verkoopterugboeking voor de uren en het gefactureerde bedrag op de oorspronkelijke factuurregeldetails voor tijd.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-129">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de uren en het bedrag op de bewerkte factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-130">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de resterende uren en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de factuurregeldetails.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2fc5-131">Facturering van het volledige tegoed van een eerder gefactureerde onkostentransactie.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-132">Een gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de onkosten.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-133">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de onkosten.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e2fc5-134">Facturering van het gedeeltelijke tegoed van een eerder gefactureerde onkostentransactie.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-135">Een gefactureerde verkoopterugboeking voor de hoeveelheid en het gefactureerde bedrag op de oorspronkelijke factuurregeldetails voor onkosten.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-136">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de hoeveelheid en het bedrag op de gecorrigeerde factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-137">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de resterende hoeveelheid en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de factuurregeldetails.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2fc5-138">Het volledige krediet van een eerder gefactureerde materiaaltransactie factureren.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-139">Een gefactureerde terugboeking voor de hoeveelheid en het bedrag in de oorspronkelijke factuurregeldetails voor materiaal.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-140">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde voor de hoeveelheid en het bedrag in de oorspronkelijke factuurregeldetails voor materiaal.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e2fc5-141">Het gedeeltelijke krediet voor een materiaaltransactie factureren.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-142">Een gefactureerde terugboeking voor de hoeveelheid en het gefactureerde bedrag in de oorspronkelijke factuurregeldetails voor materiaal.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-143">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de hoeveelheid en het bedrag in de bewerkte factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-144">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de resterende hoeveelheid en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de factuurregeldetails.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2fc5-145">Facturering van het volledige tegoed van een eerder gefactureerde kostentransactie.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-146">Een gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de kosten.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-147">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop voor de hoeveelheid en het bedrag op de oorspronkelijke factuurregeldetails voor de kosten.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2fc5-148">Facturering van het gedeeltelijke tegoed van een eerder gefactureerde kostentransactie.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-149">Een gefactureerde verkoopterugboeking voor de hoeveelheid en het gefactureerde bedrag op de oorspronkelijke factuurregeldetails voor kosten.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-150">Een nieuwe werkelijke waarde voor niet-gefactureerde verkoop die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte gecorrigeerde factuurregeldetails, een terugboeking hiervan en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="e2fc5-151">Facturering van het volledige tegoed van een eerder gefactureerde mijlpaal.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-152">Een gefactureerde verkoopterugboeking voor het bedrag op de oorspronkelijke factuurregeldetails voor de mijlpaal.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="e2fc5-153">De factuurstatus van de mijlpaal wordt bijgewerkt van <b>Klantfactuur geboekt</b> naar <b>Gereed voor facturering</b>​.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="e2fc5-154">Facturering van het gedeeltelijke tegoed van een eerder gefactureerde mijlpaal.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2fc5-155">Dit scenario wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="e2fc5-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
