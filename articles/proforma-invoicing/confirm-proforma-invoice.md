---
title: Een pro-formafactuur bevestigen
description: Dit onderwerp biedt informatie over het bevestigen van een pro-formafactuur.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 560bb68cba865a6af60504114126ae6ea73dde2d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074409"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="0cdef-103">Een pro-formafactuur bevestigen</span><span class="sxs-lookup"><span data-stu-id="0cdef-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="0cdef-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="0cdef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0cdef-105">Nadat een pro-formafactuur is bevestigd, wordt de status van de projectfactuur bijgewerkt in **Bevestigd**.</span><span class="sxs-lookup"><span data-stu-id="0cdef-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="0cdef-106">Wanneer een factuur is bevestigd, wordt deze alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="0cdef-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="0cdef-107">Voortaan kan de factuur alleen worden gecorrigeerd als er door de klant geïnitieerde correcties of tegoeden zijn, of als de factuur als betaald is gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="0cdef-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="0cdef-108">In de volgende tabel vindt u de werkelijke waarden die door het systeem zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0cdef-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="0cdef-109">Deze werkelijke waarden worden gemaakt wanneer bepaalde bewerkingen worden uitgevoerd op de conceptprojectfactuur voordat deze wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="0cdef-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="0cdef-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0cdef-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="0cdef-111">
                    <strong>Werkelijke waarden gemaakt bij bevestiging</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0cdef-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0cdef-112">Een tijdtransactie factureren zonder wijzigingen op de conceptfactuur.</span><span class="sxs-lookup"><span data-stu-id="0cdef-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-113">Een niet-gefactureerde verkoopterugboeking voor de uren en het bedrag op de oorspronkelijke tijdgoedkeuring</span><span class="sxs-lookup"><span data-stu-id="0cdef-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-114">Een gefactureerde werkelijke verkoopwaarde voor de uren en het bedrag op de oorspronkelijke tijdgoedkeuring</span><span class="sxs-lookup"><span data-stu-id="0cdef-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0cdef-115">Facturering van een tijdtransactie die is bewerkt om de hoeveelheid te verminderen.</span><span class="sxs-lookup"><span data-stu-id="0cdef-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-116">Een niet-gefactureerde verkoopterugboeking voor de uren en het bedrag op de oorspronkelijke tijdgoedkeuring</span><span class="sxs-lookup"><span data-stu-id="0cdef-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-117">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de uren en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="0cdef-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-118">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die niet-toerekenbaar is voor de resterende uren en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="0cdef-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0cdef-119">Facturering van een tijdtransactie die is bewerkt om de hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="0cdef-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-120">Een niet-gefactureerde verkoopterugboeking voor de uren en het bedrag op de oorspronkelijke tijdgoedkeuring</span><span class="sxs-lookup"><span data-stu-id="0cdef-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-121">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de uren en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="0cdef-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0cdef-122">Facturering van een onkostentransactie zonder wijzigingen op de conceptfactuur.</span><span class="sxs-lookup"><span data-stu-id="0cdef-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-123">Een niet-gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke onkostengoedkeuring.</span><span class="sxs-lookup"><span data-stu-id="0cdef-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-124">Een gefactureerde werkelijke verkoopwaarde voor de hoeveelheid en het bedrag op de oorspronkelijke onkostengoedkeuring.</span><span class="sxs-lookup"><span data-stu-id="0cdef-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0cdef-125">Facturering van een onkostentransactie die is bewerkt om de hoeveelheid te verminderen.</span><span class="sxs-lookup"><span data-stu-id="0cdef-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-126">Een niet-gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke onkostengoedkeuring.</span><span class="sxs-lookup"><span data-stu-id="0cdef-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-127">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="0cdef-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-128">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die niet-toerekenbaar is voor de resterende hoeveelheid en het resterende bedrag na aftrek van de gecorrigeerde cijfers op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="0cdef-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0cdef-129">Facturering van een onkostentransactie die is bewerkt om de hoeveelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="0cdef-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-130">Een niet-gefactureerde verkoopterugboeking voor de hoeveelheid en het bedrag op de oorspronkelijke onkostengoedkeuring.</span><span class="sxs-lookup"><span data-stu-id="0cdef-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-131">Een nieuwe niet-gefactureerde werkelijke verkoopwaarde die toerekenbaar is voor de hoeveelheid en het bedrag op de bewerkte factuurregeldetails, een terugboeking van de niet-gefactureerde werkelijke verkoopwaarde en een equivalente gefactureerde werkelijke verkoopwaarde.</span><span class="sxs-lookup"><span data-stu-id="0cdef-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0cdef-132">Facturering van kosten.</span><span class="sxs-lookup"><span data-stu-id="0cdef-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-133">Een niet-gefactureerde verkoopterugboeking voor het kostenbedrag op de oorspronkelijke journaalregel.</span><span class="sxs-lookup"><span data-stu-id="0cdef-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-134">Een gefactureerde werkelijke verkoopwaarde voor de hoeveelheid en het bedrag op de oorspronkelijke kostenjournaalregel.</span><span class="sxs-lookup"><span data-stu-id="0cdef-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0cdef-135">Facturering van een mijlpaal.</span><span class="sxs-lookup"><span data-stu-id="0cdef-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cdef-136">Een gefactureerde werkelijke verkoop voor het mijlpaalbedrag voor de oorspronkelijke mijlpaal op de projectcontractregel.</span><span class="sxs-lookup"><span data-stu-id="0cdef-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
