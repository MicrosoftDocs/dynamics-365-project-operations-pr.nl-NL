---
title: Een pro-formaprojectfactuur bevestigen
description: Dit onderwerp biedt informatie over het bevestigen van pro-formaprojectfacturen in Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004120"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="26fe1-103">Een pro-formaprojectfactuur bevestigen</span><span class="sxs-lookup"><span data-stu-id="26fe1-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="26fe1-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="26fe1-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="26fe1-105">Nadat een pro-formafactuur is bevestigd, wordt de status van de projectfactuur bijgewerkt in **Bevestigd**.</span><span class="sxs-lookup"><span data-stu-id="26fe1-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="26fe1-106">Wanneer een factuur is bevestigd, wordt deze alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="26fe1-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="26fe1-107">Vervolgens kan de factuur alleen worden gecorrigeerd door middel van door de klant geïnitieerde correcties of crediteringen.</span><span class="sxs-lookup"><span data-stu-id="26fe1-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="26fe1-108">In de volgende tabel vindt u de werkelijke waarden die door het systeem zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="26fe1-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="26fe1-109">Deze werkelijke waarden worden gemaakt wanneer bepaalde bewerkingen worden uitgevoerd op de conceptprojectfactuur voordat deze wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="26fe1-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="26fe1-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26fe1-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="26fe1-111">
                    <strong>Werkelijke waarden gemaakt bij bevestiging</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26fe1-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26fe1-112">Een vooruitbetaling of voorschot factureren</span><span class="sxs-lookup"><span data-stu-id="26fe1-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-113">Een gefactureerde werkelijke verkoop van het type <strong>Voorschot</strong> wordt gemaakt voor het bedrag op de vooruitbetaling of het voorschot.</span><span class="sxs-lookup"><span data-stu-id="26fe1-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-114">Een niet-gefactureerde werkelijke verkoop van een negatief bedrag van het voorschot of de vooruitbetaling dat voor afstemming moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="26fe1-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26fe1-115">Na het volledig afstemmen van een voorschot of vooruitbetaling op een factuur.</span><span class="sxs-lookup"><span data-stu-id="26fe1-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-116">Een niet-gefactureerde verkoopterugboeking van het voorschot of de vooruitbetaling die is gemaakt voor afstemming.</span><span class="sxs-lookup"><span data-stu-id="26fe1-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="26fe1-117">Dit bedrag is positief omdat het bedoeld is om het negatieve bedrag op te heffen dat is ontstaan toen het voorschot of de vooruitbetaling werd gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="26fe1-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-118">Een gefactureerde werkelijke verkoopwaarde voor het bedrag op deze factuur.</span><span class="sxs-lookup"><span data-stu-id="26fe1-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="26fe1-119">Na gedeeltelijke afstemming van een voorschot of vooruitbetaling op een factuur.</span><span class="sxs-lookup"><span data-stu-id="26fe1-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-120">Een niet-gefactureerde verkoopterugboeking van het voorschot of de vooruitbetaling die is gemaakt voor afstemming.</span><span class="sxs-lookup"><span data-stu-id="26fe1-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="26fe1-121">Dit bedrag is positief omdat het bedoeld is om het negatieve bedrag op te heffen dat is ontstaan toen het voorschot of de vooruitbetaling werd gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="26fe1-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-122">Een gefactureerde werkelijke verkoopwaarde voor het bedrag op deze factuur.</span><span class="sxs-lookup"><span data-stu-id="26fe1-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-123">Een negatieve niet-gefactureerde werkelijke verkoop van het resterende voorschot of vooruitbetaalde bedrag die voor afstemming moet worden gebruikt op toekomstige facturen.</span><span class="sxs-lookup"><span data-stu-id="26fe1-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26fe1-124">Een tijdtransactie factureren zonder wijzigingen op de conceptfactuur.</span><span class="sxs-lookup"><span data-stu-id="26fe1-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-125">Een niet-gefactureerde verkoopterugboeking voor de uren en het bedrag op de oorspronkelijke tijdgoedkeuring</span><span class="sxs-lookup"><span data-stu-id="26fe1-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-126">Een gefactureerde werkelijke verkoopwaarde voor de uren en het bedrag op de oorspronkelijke tijdgoedkeuring</span><span class="sxs-lookup"><span data-stu-id="26fe1-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="26fe1-127">Facturering van een tijdtransactie die is bewerkt om de hoeveelheid te verminderen.</span><span class="sxs-lookup"><span data-stu-id="26fe1-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-128">Een niet-gefactureerde verkoopterugboeking voor de uren en het bedrag op de oorspronkelijke tijdgoedkeuring</span><span class="sxs-lookup"><span data-stu-id="26fe1-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-129">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de uren en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="26fe1-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-130">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die niet-toerekenbaar is voor de resterende uren en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de bewerkte factuurregeldetails, een terugboeking van de werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="26fe1-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26fe1-131">Facturering van een tijdtransactie die is bewerkt om de hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="26fe1-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-132">Een niet-gefactureerde verkoopterugboeking voor de uren en het bedrag op de oorspronkelijke tijdgoedkeuring</span><span class="sxs-lookup"><span data-stu-id="26fe1-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-133">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de uren en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="26fe1-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26fe1-134">Een onkostentransactie factureren zonder wijzigingen op de conceptfactuur.</span><span class="sxs-lookup"><span data-stu-id="26fe1-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-135">Een niet-gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke onkostengoedkeuring.</span><span class="sxs-lookup"><span data-stu-id="26fe1-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-136">Een gefactureerde werkelijke verkoopwaarde voor de hoeveelheid en het bedrag op de oorspronkelijke onkostengoedkeuring</span><span class="sxs-lookup"><span data-stu-id="26fe1-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="26fe1-137">Facturering van een onkostentransactie die is bewerkt om de hoeveelheid te verminderen.</span><span class="sxs-lookup"><span data-stu-id="26fe1-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-138">Een niet-gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke onkostengoedkeuring.</span><span class="sxs-lookup"><span data-stu-id="26fe1-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-139">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="26fe1-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-140">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die niet-toerekenbaar is voor de resterende hoeveelheid en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="26fe1-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26fe1-141">Facturering van een onkostentransactie die is bewerkt om de hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="26fe1-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-142">Een niet-gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke onkostengoedkeuring.</span><span class="sxs-lookup"><span data-stu-id="26fe1-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-143">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="26fe1-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26fe1-144">Een materiaaltransactie factureren zonder bewerkingen van de conceptfactuur.</span><span class="sxs-lookup"><span data-stu-id="26fe1-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-145">Een niet-gefactureerde terugboeking voor de hoeveelheid en het bedrag in de oorspronkelijke goedkeuring van het materiaalgebruik.</span><span class="sxs-lookup"><span data-stu-id="26fe1-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-146">Een gefactureerde werkelijke verkoopwaarde voor de hoeveelheid en het bedrag in de oorspronkelijke goedkeuring van het materiaalgebruik.</span><span class="sxs-lookup"><span data-stu-id="26fe1-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="26fe1-147">Facturering van een materiaaltransactie die is bewerkt om de hoeveelheid te beperken.</span><span class="sxs-lookup"><span data-stu-id="26fe1-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-148">Een niet-gefactureerde terugboeking voor de hoeveelheid en het bedrag in de oorspronkelijke goedkeuring van tijd.</span><span class="sxs-lookup"><span data-stu-id="26fe1-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-149">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="26fe1-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-150">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die niet-toerekenbaar is voor de resterende hoeveelheid en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="26fe1-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26fe1-151">Facturering van een materiaaltransactie die is bewerkt om de hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="26fe1-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-152">Een niet-gefactureerde terugboeking voor de hoeveelheid en het bedrag in de oorspronkelijke goedkeuring van het materiaalgebruik.</span><span class="sxs-lookup"><span data-stu-id="26fe1-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-153">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="26fe1-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26fe1-154">Facturering van kosten.</span><span class="sxs-lookup"><span data-stu-id="26fe1-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-155">Een niet-gefactureerde verkoopterugboeking voor het kostenbedrag op de oorspronkelijke journaalregel.</span><span class="sxs-lookup"><span data-stu-id="26fe1-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-156">Een gefactureerde werkelijke verkoopwaarde voor de hoeveelheid en het bedrag op de oorspronkelijke kostenjournaalregel.</span><span class="sxs-lookup"><span data-stu-id="26fe1-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="26fe1-157">Facturering van een mijlpaal.</span><span class="sxs-lookup"><span data-stu-id="26fe1-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-158">Een gefactureerde werkelijke verkoop voor het mijlpaalbedrag voor de oorspronkelijke mijlpaal op de projectcontractregel.</span><span class="sxs-lookup"><span data-stu-id="26fe1-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="26fe1-159">Een productgebaseerde contractregel factureren.</span><span class="sxs-lookup"><span data-stu-id="26fe1-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="26fe1-160">Een gefactureerde werkelijke verkoopwaarde voor de productregel met de hoeveelheid en het bedrag afkomstig van de productgebaseerde contractregel.</span><span class="sxs-lookup"><span data-stu-id="26fe1-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
