---
title: Overzicht van inkomstenverantwoording
description: Dit onderwerp bevat informatie over inkomstenverantwoording in Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531398"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="64af7-103">Overzicht van inkomstenverantwoording</span><span class="sxs-lookup"><span data-stu-id="64af7-103">Revenue recognition overview</span></span>

<span data-ttu-id="64af7-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="64af7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="64af7-105">In Dynamics 365 Project Operations verschillen de principes van inkomstenverantwoording op basis van de geselecteerde factureringsmethode voor een project of een deel van het project.</span><span class="sxs-lookup"><span data-stu-id="64af7-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="64af7-106">Dit onderwerp bevat informatie over inkomstenverantwoording in Project Operations.</span><span class="sxs-lookup"><span data-stu-id="64af7-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="64af7-107">Transacties die worden geboekt met de factureringsmethode voor tijd en materiaal</span><span class="sxs-lookup"><span data-stu-id="64af7-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="64af7-108">Kosten en inkomstenverantwoording hangen samen.</span><span class="sxs-lookup"><span data-stu-id="64af7-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="64af7-109">Transactiekosten en niet-gefactureerde verkopen worden geboekt met het [Project Operations-integratiejournaal](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="64af7-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="64af7-110">Het profiel voor projectkosten en omzet bepaalt of niet-gefactureerde verkooptransacties naar het grootboek worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="64af7-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="64af7-111">Als **Inkomsten toerekenen** is geselecteerd, gebruikt het systeem de rekeningen **OHW-verkoopwaarde** en de **Waarde van de toegerekende inkomsten** tijdens het boeken.</span><span class="sxs-lookup"><span data-stu-id="64af7-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="64af7-112">Hieronder ziet u een voorbeeld van deze methode.</span><span class="sxs-lookup"><span data-stu-id="64af7-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="64af7-113">Transactietype</span><span class="sxs-lookup"><span data-stu-id="64af7-113">Transaction type</span></span> | <span data-ttu-id="64af7-114">Debet/Credit</span><span class="sxs-lookup"><span data-stu-id="64af7-114">Debit/Credit</span></span> | <span data-ttu-id="64af7-115">Bedrag</span><span class="sxs-lookup"><span data-stu-id="64af7-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="64af7-116">OHW-verkoopwaarde</span><span class="sxs-lookup"><span data-stu-id="64af7-116">WIP Sales value</span></span> | <span data-ttu-id="64af7-117">Debet</span><span class="sxs-lookup"><span data-stu-id="64af7-117">Debit</span></span> | <span data-ttu-id="64af7-118">100</span><span class="sxs-lookup"><span data-stu-id="64af7-118">100</span></span> |
  | <span data-ttu-id="64af7-119">Verkoopwaarde toegerekende inkomsten</span><span class="sxs-lookup"><span data-stu-id="64af7-119">Accrued revenue sales value</span></span> | <span data-ttu-id="64af7-120">Credit</span><span class="sxs-lookup"><span data-stu-id="64af7-120">Credit</span></span> | <span data-ttu-id="64af7-121">100</span><span class="sxs-lookup"><span data-stu-id="64af7-121">100</span></span> |

- <span data-ttu-id="64af7-122">Omzet wordt toegerekend bij facturering.</span><span class="sxs-lookup"><span data-stu-id="64af7-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="64af7-123">Het systeem gebruikt de rekening **Gefactureerde omzet** tijdens het boeken.</span><span class="sxs-lookup"><span data-stu-id="64af7-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="64af7-124">Hieronder ziet u een voorbeeld van deze methode.</span><span class="sxs-lookup"><span data-stu-id="64af7-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="64af7-125">Transactietype</span><span class="sxs-lookup"><span data-stu-id="64af7-125">Transaction type</span></span> | <span data-ttu-id="64af7-126">Debet/Credit</span><span class="sxs-lookup"><span data-stu-id="64af7-126">Debit/Credit</span></span> | <span data-ttu-id="64af7-127">Bedrag</span><span class="sxs-lookup"><span data-stu-id="64af7-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="64af7-128">Klantensaldo</span><span class="sxs-lookup"><span data-stu-id="64af7-128">Customer balance</span></span> | <span data-ttu-id="64af7-129">Debet</span><span class="sxs-lookup"><span data-stu-id="64af7-129">Debit</span></span> | <span data-ttu-id="64af7-130">120</span><span class="sxs-lookup"><span data-stu-id="64af7-130">120</span></span> |
  | <span data-ttu-id="64af7-131">Te betalen omzetbelasting</span><span class="sxs-lookup"><span data-stu-id="64af7-131">Sales tax payable</span></span> | <span data-ttu-id="64af7-132">Credit</span><span class="sxs-lookup"><span data-stu-id="64af7-132">Credit</span></span> | <span data-ttu-id="64af7-133">20</span><span class="sxs-lookup"><span data-stu-id="64af7-133">20</span></span> |
  | <span data-ttu-id="64af7-134">Gefactureerde omzet</span><span class="sxs-lookup"><span data-stu-id="64af7-134">Invoiced Revenue</span></span> | <span data-ttu-id="64af7-135">Credit</span><span class="sxs-lookup"><span data-stu-id="64af7-135">Credit</span></span> | <span data-ttu-id="64af7-136">100</span><span class="sxs-lookup"><span data-stu-id="64af7-136">100</span></span> |

- <span data-ttu-id="64af7-137">Als er inkomsten zijn toegerekend toen de niet-gefactureerde verkopen werden geboekt, zal het systeem de toegerekende inkomsten bij facturering terugboeken.</span><span class="sxs-lookup"><span data-stu-id="64af7-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="64af7-138">Transactietype</span><span class="sxs-lookup"><span data-stu-id="64af7-138">Transaction type</span></span> | <span data-ttu-id="64af7-139">Debet/Credit</span><span class="sxs-lookup"><span data-stu-id="64af7-139">Debit/Credit</span></span> | <span data-ttu-id="64af7-140">Bedrag</span><span class="sxs-lookup"><span data-stu-id="64af7-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="64af7-141">OHW-verkoopwaarde</span><span class="sxs-lookup"><span data-stu-id="64af7-141">WIP Sales value</span></span> | <span data-ttu-id="64af7-142">Credit</span><span class="sxs-lookup"><span data-stu-id="64af7-142">Credit</span></span> | <span data-ttu-id="64af7-143">100</span><span class="sxs-lookup"><span data-stu-id="64af7-143">100</span></span> |
  | <span data-ttu-id="64af7-144">Verkoopwaarde toegerekende inkomsten</span><span class="sxs-lookup"><span data-stu-id="64af7-144">Accrued revenue sales value</span></span> | <span data-ttu-id="64af7-145">Debet</span><span class="sxs-lookup"><span data-stu-id="64af7-145">Debit</span></span> | <span data-ttu-id="64af7-146">100</span><span class="sxs-lookup"><span data-stu-id="64af7-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="64af7-147">Transacties die worden geboekt met de factureringsmethode voor vaste prijs</span><span class="sxs-lookup"><span data-stu-id="64af7-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="64af7-148">Kosten en inkomstenverantwoording hangen niet samen.</span><span class="sxs-lookup"><span data-stu-id="64af7-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="64af7-149">Transactiekosten worden geboekt met het [Project Operations-integratiejournaal](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="64af7-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="64af7-150">Niet-gefactureerde verkooptransacties worden niet gemaakt.</span><span class="sxs-lookup"><span data-stu-id="64af7-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="64af7-151">Opbrengsten kunnen tijdens de facturering worden verantwoord als voor het projectkosten- en opbrengstenprofiel **Principe gebruikt voor berekeningen van de voltooiing van projecten** is ingesteld op **Geen OHW**.</span><span class="sxs-lookup"><span data-stu-id="64af7-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="64af7-152">Gebruik deze methode alleen voor korte, eenvoudige projecten.</span><span class="sxs-lookup"><span data-stu-id="64af7-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="64af7-153">Opbrengsten kunnen worden verantwoord op basis van omzetschattingen met vaste prijs, met de methode **Voltooid contract** of **Inkomstenverantwoording voor voltooiingspercentage**.</span><span class="sxs-lookup"><span data-stu-id="64af7-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64af7-154">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="64af7-154">Additional resources</span></span>
[<span data-ttu-id="64af7-155">Artikel Boekhouding configureren voor factureerbare projecten</span><span class="sxs-lookup"><span data-stu-id="64af7-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="64af7-156">Projecten met omzetschattingen met een vaste prijs</span><span class="sxs-lookup"><span data-stu-id="64af7-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="64af7-157">Omzetschattingen beheren</span><span class="sxs-lookup"><span data-stu-id="64af7-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="64af7-158">Kosten om methoden te voltooien</span><span class="sxs-lookup"><span data-stu-id="64af7-158">Cost to complete methods</span></span>](cost-complete-methods.md)
