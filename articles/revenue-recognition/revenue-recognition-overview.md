---
title: Overzicht van inkomstenverantwoording
description: Dit onderwerp bevat informatie over inkomstenverantwoording in Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368020"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="64eb2-103">Overzicht van inkomstenverantwoording</span><span class="sxs-lookup"><span data-stu-id="64eb2-103">Revenue recognition overview</span></span>

<span data-ttu-id="64eb2-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="64eb2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="64eb2-105">In Dynamics 365 Project Operations verschillen de principes van inkomstenverantwoording op basis van de geselecteerde factureringsmethode voor een project of een deel van het project.</span><span class="sxs-lookup"><span data-stu-id="64eb2-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="64eb2-106">Dit onderwerp bevat informatie over inkomstenverantwoording in Project Operations.</span><span class="sxs-lookup"><span data-stu-id="64eb2-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="64eb2-107">Transacties die worden geboekt met de factureringsmethode voor tijd en materiaal</span><span class="sxs-lookup"><span data-stu-id="64eb2-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="64eb2-108">Kosten en inkomstenverantwoording hangen samen.</span><span class="sxs-lookup"><span data-stu-id="64eb2-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="64eb2-109">Transactiekosten en niet-gefactureerde verkopen worden geboekt met het [Project Operations-integratiejournaal](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="64eb2-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="64eb2-110">Het profiel voor projectkosten en omzet bepaalt of niet-gefactureerde verkooptransacties naar het grootboek worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="64eb2-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="64eb2-111">Als **Inkomsten toerekenen** is geselecteerd, gebruikt het systeem de rekeningen **OHW-verkoopwaarde** en de **Waarde van de toegerekende inkomsten** tijdens het boeken.</span><span class="sxs-lookup"><span data-stu-id="64eb2-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="64eb2-112">Hieronder ziet u een voorbeeld van deze methode.</span><span class="sxs-lookup"><span data-stu-id="64eb2-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="64eb2-113">Transactietype</span><span class="sxs-lookup"><span data-stu-id="64eb2-113">Transaction type</span></span> | <span data-ttu-id="64eb2-114">Debet/Credit</span><span class="sxs-lookup"><span data-stu-id="64eb2-114">Debit/Credit</span></span> | <span data-ttu-id="64eb2-115">Bedrag</span><span class="sxs-lookup"><span data-stu-id="64eb2-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="64eb2-116">OHW-verkoopwaarde</span><span class="sxs-lookup"><span data-stu-id="64eb2-116">WIP Sales value</span></span> | <span data-ttu-id="64eb2-117">Debet</span><span class="sxs-lookup"><span data-stu-id="64eb2-117">Debit</span></span> | <span data-ttu-id="64eb2-118">100</span><span class="sxs-lookup"><span data-stu-id="64eb2-118">100</span></span> |
  | <span data-ttu-id="64eb2-119">Verkoopwaarde toegerekende inkomsten</span><span class="sxs-lookup"><span data-stu-id="64eb2-119">Accrued revenue sales value</span></span> | <span data-ttu-id="64eb2-120">Credit</span><span class="sxs-lookup"><span data-stu-id="64eb2-120">Credit</span></span> | <span data-ttu-id="64eb2-121">100</span><span class="sxs-lookup"><span data-stu-id="64eb2-121">100</span></span> |

- <span data-ttu-id="64eb2-122">Omzet wordt toegerekend bij facturering.</span><span class="sxs-lookup"><span data-stu-id="64eb2-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="64eb2-123">Het systeem gebruikt de rekening **Gefactureerde omzet** tijdens het boeken.</span><span class="sxs-lookup"><span data-stu-id="64eb2-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="64eb2-124">Hieronder ziet u een voorbeeld van deze methode.</span><span class="sxs-lookup"><span data-stu-id="64eb2-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="64eb2-125">Transactietype</span><span class="sxs-lookup"><span data-stu-id="64eb2-125">Transaction type</span></span> | <span data-ttu-id="64eb2-126">Debet/Credit</span><span class="sxs-lookup"><span data-stu-id="64eb2-126">Debit/Credit</span></span> | <span data-ttu-id="64eb2-127">Bedrag</span><span class="sxs-lookup"><span data-stu-id="64eb2-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="64eb2-128">Klantensaldo</span><span class="sxs-lookup"><span data-stu-id="64eb2-128">Customer balance</span></span> | <span data-ttu-id="64eb2-129">Debet</span><span class="sxs-lookup"><span data-stu-id="64eb2-129">Debit</span></span> | <span data-ttu-id="64eb2-130">120</span><span class="sxs-lookup"><span data-stu-id="64eb2-130">120</span></span> |
  | <span data-ttu-id="64eb2-131">Te betalen omzetbelasting</span><span class="sxs-lookup"><span data-stu-id="64eb2-131">Sales tax payable</span></span> | <span data-ttu-id="64eb2-132">Credit</span><span class="sxs-lookup"><span data-stu-id="64eb2-132">Credit</span></span> | <span data-ttu-id="64eb2-133">20</span><span class="sxs-lookup"><span data-stu-id="64eb2-133">20</span></span> |
  | <span data-ttu-id="64eb2-134">Gefactureerde omzet</span><span class="sxs-lookup"><span data-stu-id="64eb2-134">Invoiced Revenue</span></span> | <span data-ttu-id="64eb2-135">Credit</span><span class="sxs-lookup"><span data-stu-id="64eb2-135">Credit</span></span> | <span data-ttu-id="64eb2-136">100</span><span class="sxs-lookup"><span data-stu-id="64eb2-136">100</span></span> |

- <span data-ttu-id="64eb2-137">Als er inkomsten zijn toegerekend toen de niet-gefactureerde verkopen werden geboekt, zal het systeem de toegerekende inkomsten bij facturering terugboeken.</span><span class="sxs-lookup"><span data-stu-id="64eb2-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="64eb2-138">Transactietype</span><span class="sxs-lookup"><span data-stu-id="64eb2-138">Transaction type</span></span> | <span data-ttu-id="64eb2-139">Debet/Credit</span><span class="sxs-lookup"><span data-stu-id="64eb2-139">Debit/Credit</span></span> | <span data-ttu-id="64eb2-140">Bedrag</span><span class="sxs-lookup"><span data-stu-id="64eb2-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="64eb2-141">OHW-verkoopwaarde</span><span class="sxs-lookup"><span data-stu-id="64eb2-141">WIP Sales value</span></span> | <span data-ttu-id="64eb2-142">Credit</span><span class="sxs-lookup"><span data-stu-id="64eb2-142">Credit</span></span> | <span data-ttu-id="64eb2-143">100</span><span class="sxs-lookup"><span data-stu-id="64eb2-143">100</span></span> |
  | <span data-ttu-id="64eb2-144">Verkoopwaarde toegerekende inkomsten</span><span class="sxs-lookup"><span data-stu-id="64eb2-144">Accrued revenue sales value</span></span> | <span data-ttu-id="64eb2-145">Debet</span><span class="sxs-lookup"><span data-stu-id="64eb2-145">Debit</span></span> | <span data-ttu-id="64eb2-146">100</span><span class="sxs-lookup"><span data-stu-id="64eb2-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="64eb2-147">Transacties die worden geboekt met de factureringsmethode voor vaste prijs</span><span class="sxs-lookup"><span data-stu-id="64eb2-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="64eb2-148">Kosten en inkomstenverantwoording hangen niet samen.</span><span class="sxs-lookup"><span data-stu-id="64eb2-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="64eb2-149">Transactiekosten worden geboekt met het [Project Operations-integratiejournaal](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="64eb2-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="64eb2-150">Niet-gefactureerde verkooptransacties worden niet gemaakt.</span><span class="sxs-lookup"><span data-stu-id="64eb2-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="64eb2-151">Opbrengsten kunnen tijdens de facturering worden verantwoord als voor het projectkosten- en opbrengstenprofiel **Principe gebruikt voor berekeningen van de voltooiing van projecten** is ingesteld op **Geen OHW**.</span><span class="sxs-lookup"><span data-stu-id="64eb2-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="64eb2-152">Gebruik deze methode alleen voor korte, eenvoudige projecten.</span><span class="sxs-lookup"><span data-stu-id="64eb2-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="64eb2-153">Opbrengsten kunnen worden verantwoord op basis van omzetschattingen met vaste prijs, met de methode **Voltooid contract** of **Inkomstenverantwoording voor voltooiingspercentage**.</span><span class="sxs-lookup"><span data-stu-id="64eb2-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64eb2-154">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="64eb2-154">Additional resources</span></span>
[<span data-ttu-id="64eb2-155">Artikel Boekhouding configureren voor factureerbare projecten</span><span class="sxs-lookup"><span data-stu-id="64eb2-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="64eb2-156">Projecten met omzetschattingen met een vaste prijs</span><span class="sxs-lookup"><span data-stu-id="64eb2-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="64eb2-157">Omzetschattingen beheren</span><span class="sxs-lookup"><span data-stu-id="64eb2-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="64eb2-158">Kosten om methoden te voltooien</span><span class="sxs-lookup"><span data-stu-id="64eb2-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]