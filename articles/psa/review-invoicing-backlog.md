---
title: De factureringsbacklog voor projecten en projectcontracten controleren
description: In dit onderwerp wordt uitgelegd hoe u backlogs voor tijd, onkosten en producten bekijkt en hoe u deze markeert als gereed voor facturering.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: cec09ca39563e3faf0f3b2c10cf9bde3feb020b0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008530"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="e1b43-103">De factureringsbacklog voor projecten en projectcontracten controleren</span><span class="sxs-lookup"><span data-stu-id="e1b43-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e1b43-104">Wanneer een transactie gereed is voor het maken en verwerken van een factuur, moet de transactie actie zijn gemarkeerd als **Gereed voor facturering**.</span><span class="sxs-lookup"><span data-stu-id="e1b43-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="e1b43-105">In dit onderwerp worden de typen transacties beschreven die kunnen worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e1b43-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="e1b43-106">De backlog voor facturering van tijd en materiaal controleren</span><span class="sxs-lookup"><span data-stu-id="e1b43-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="e1b43-107">Wanneer een tijd- of onkostenvermelding wordt ingediend en goedgekeurd voor een project, maakt PSA een werkelijke projectwaarde.</span><span class="sxs-lookup"><span data-stu-id="e1b43-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="e1b43-108">Als de combinatie van het project en de transactieklasse zijn toegewezen aan een contractregel voor een tijd-en-materiaalproject, worden twee werkelijke waarden gemaakt wanneer de vermelding wordt goedgekeurd:</span><span class="sxs-lookup"><span data-stu-id="e1b43-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="e1b43-109">Werkelijke waarde voor kosten</span><span class="sxs-lookup"><span data-stu-id="e1b43-109">Cost actual</span></span> 
- <span data-ttu-id="e1b43-110">Niet-gefactureerde werkelijke waarde voor verkoop</span><span class="sxs-lookup"><span data-stu-id="e1b43-110">Unbilled sales actual</span></span>

<span data-ttu-id="e1b43-111">Niet-gefactureerde werkelijke waarden voor verkoop vertegenwoordigen de factureringsbacklog en hun factureringsstatus moet worden ingesteld op **Gereed voor facturering**.</span><span class="sxs-lookup"><span data-stu-id="e1b43-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="e1b43-112">Wanneer een projectfactuur wordt gemaakt, worden niet-gefactureerde werkelijke waarden voor verkoop die zijn gemarkeerd als **Gereed voor facturering** gekopieerd als factuurregeldetails.</span><span class="sxs-lookup"><span data-stu-id="e1b43-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="e1b43-113">Als u de factureringsbacklog voor tijd en materialen wilt controleren, gaat u naar **Verkoop** \> **Facturering** \> **Backlog voor facturering van tijd en materiaal**.</span><span class="sxs-lookup"><span data-stu-id="e1b43-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="e1b43-114">Selecteer alle niet-gefactureerde werkelijke waarden voor verkoop die gereed zijn om te worden gefactureerd en selecteer vervolgens **Gereed voor facturering**.</span><span class="sxs-lookup"><span data-stu-id="e1b43-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="e1b43-115">De factureringsstatus van deze werkelijke waarden wordt gewijzigd in **Gereed voor facturering**.</span><span class="sxs-lookup"><span data-stu-id="e1b43-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Backlog voor facturering van tijd en materiaal](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="e1b43-117">De backlog voor facturering voor producten controleren</span><span class="sxs-lookup"><span data-stu-id="e1b43-117">Review the product billing backlog</span></span>

<span data-ttu-id="e1b43-118">Wanneer in PSA een projectcontract op product gebaseerde contractregels bevat, worden deze regels meegenomen voor facturering wanneer een factuur voor het projectcontract wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e1b43-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="e1b43-119">Elk product waarvoor contractregels zijn gemarkeerd als **Gereed voor facturering** wordt naar de projectfactuur gekopieerd als projectfactuurregels.</span><span class="sxs-lookup"><span data-stu-id="e1b43-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="e1b43-120">Als u de factureringsbacklog voor producten wilt controleren, gaat u naar **Verkoop** \> **Facturering** \> **Backlog voor facturering voor producten**.</span><span class="sxs-lookup"><span data-stu-id="e1b43-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="e1b43-121">Selecteer alle productgebaseerde contractregels die gereed zijn om te worden gefactureerd en selecteer vervolgens **Gereed voor facturering**.</span><span class="sxs-lookup"><span data-stu-id="e1b43-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="e1b43-122">De factureringsstatus van deze regels wordt gewijzigd in **Gereed voor facturering**.</span><span class="sxs-lookup"><span data-stu-id="e1b43-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Backlog voor facturering voor producten](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="e1b43-124">De factureringsmijlpalen voor contracten met een vaste prijs controleren</span><span class="sxs-lookup"><span data-stu-id="e1b43-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="e1b43-125">Voor elke projectcontractregel met een factureringsmethode met vaste prijs moeten contractmijlpalen zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="e1b43-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="e1b43-126">Deze contractmijlpalen kunnen alleen worden gefactureerd als ze zijn gemarkeerd als **Gereed voor facturering**.</span><span class="sxs-lookup"><span data-stu-id="e1b43-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="e1b43-127">Als u factureringsmijlpalen wilt controleren, gaat u naar **Verkoop** \> **Facturering** \> **Mijlpalen voor vaste prijs**.</span><span class="sxs-lookup"><span data-stu-id="e1b43-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="e1b43-128">Selecteer alle mijlpalen die gereed zijn om te worden gefactureerd en selecteer vervolgens **Gereed voor facturering**.</span><span class="sxs-lookup"><span data-stu-id="e1b43-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="e1b43-129">De factureringsstatus van deze mijlpalen wordt gewijzigd in **Gereed voor facturering**.</span><span class="sxs-lookup"><span data-stu-id="e1b43-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Mijlpalen voor vaste prijs](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]