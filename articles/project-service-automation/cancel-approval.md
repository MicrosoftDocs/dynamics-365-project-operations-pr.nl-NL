---
title: Eerder goedgekeurde tijdsvermeldingen en onkostenposten annuleren
description: Dit onderwerp bevat informatie over het annuleren van een goedgekeurde projecttijd en onkostentransactie.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fc74aba2a837b7cdff55385ffa20d78c2678bb7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750669"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="e0082-103">Eerder goedgekeurde tijdsvermeldingen of onkostenposten annuleren</span><span class="sxs-lookup"><span data-stu-id="e0082-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e0082-104">In de nieuwste versie van Dynamics 365 Project Service Automation kunnen fiatteurs eerder goedgekeurde tijdsvermeldingen of onkostenposten annuleren.</span><span class="sxs-lookup"><span data-stu-id="e0082-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="e0082-105">Een eerder goedgekeurde tijdsvermelding of onkostenpost annuleren</span><span class="sxs-lookup"><span data-stu-id="e0082-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="e0082-106">Volg deze stappen om een eerder goedgekeurde tijdsvermelding of onkostenpost te annuleren.</span><span class="sxs-lookup"><span data-stu-id="e0082-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="e0082-107">Ga naar **Projecten** \> **Mijn werk** \> **Goedkeuringen**.</span><span class="sxs-lookup"><span data-stu-id="e0082-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="e0082-108">Wijzig op de lijstpagina **Goedkeuringen** de weergave in **Mijn eerdere goedkeuringen**.</span><span class="sxs-lookup"><span data-stu-id="e0082-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="e0082-109">Er wordt een lijst weergegeven met de tijdsvermeldingen en onkostenposten die u eerder hebt goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="e0082-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="e0082-110">Selecteer een of meer vermeldingen of posten en selecteer vervolgens **Goedkeuring annuleren**.</span><span class="sxs-lookup"><span data-stu-id="e0082-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="e0082-111">Er wordt een waarschuwingsbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e0082-111">You receive a warning message.</span></span>
4. <span data-ttu-id="e0082-112">Selecteer **OK** als u de goedkeuring wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="e0082-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="e0082-113">De gevolgen van het annuleren van de goedkeuring van een tijdsvermelding of onkostenpost begrijpen</span><span class="sxs-lookup"><span data-stu-id="e0082-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="e0082-114">Wanneer een goedkeuring wordt geannuleerd, heeft dit zowel operationele als financiële gevolgen.</span><span class="sxs-lookup"><span data-stu-id="e0082-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="e0082-115">Operationele gevolgen</span><span class="sxs-lookup"><span data-stu-id="e0082-115">Operational impact</span></span>

<span data-ttu-id="e0082-116">Wanneer een goedkeuring wordt geannuleerd, wordt de status van de record opnieuw ingesteld op **Concept** en wordt de goedkeuring niet meer weergegeven in de weergave **Mijn eerdere goedkeuringen**.</span><span class="sxs-lookup"><span data-stu-id="e0082-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="e0082-117">In plaats daarvan wordt de geannuleerde goedkeuring weergegeven in de weergave **Tijdsvermeldingen voor goedkeuring** of **Onkostenposten voor goedkeuring**, afhankelijk van of het een tijdsvermelding of onkostenpost betreft.</span><span class="sxs-lookup"><span data-stu-id="e0082-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="e0082-118">Bovendien wordt de status van de gerelateerde tijdsvermelding of onkostenpost gewijzigd in **Verzonden**, zodat de gerelateerde vermelding of post consistent is met goedkeuringen met de status **Concept.**</span><span class="sxs-lookup"><span data-stu-id="e0082-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="e0082-119">Als fiatteur kunt u enkele velden van een goedkeuring met de status **Concept** bewerken.</span><span class="sxs-lookup"><span data-stu-id="e0082-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="e0082-120">Deze velden zijn **Factureringstype** en **Factureerbare uren voor tijdsvermeldingen**.</span><span class="sxs-lookup"><span data-stu-id="e0082-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="e0082-121">Nadat u wijzigingen hebt aangebracht, kunt u de record opnieuw goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="e0082-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="e0082-122">U kunt deze ook afwijzen.</span><span class="sxs-lookup"><span data-stu-id="e0082-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="e0082-123">Als u de goedkeuring van een tijdsvermelding afwijst, wordt de status van de vermelding gewijzigd in **Geretourneerd**.</span><span class="sxs-lookup"><span data-stu-id="e0082-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="e0082-124">Als u de goedkeuring van een onkostenpost afwijst, wordt de status gewijzigd in **Afgewezen**.</span><span class="sxs-lookup"><span data-stu-id="e0082-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="e0082-125">Functioneel gedragen geretourneerde en afgewezen posten en vermeldingen zich hetzelfde als een post of vermelding met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="e0082-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="e0082-126">Een lid van het projectteam kan de vereiste wijzigingen in de post/vermelding aanbrengen en deze vervolgens opnieuw indienen ter goedkeuring of de post/vermelding volledig verwijderen.</span><span class="sxs-lookup"><span data-stu-id="e0082-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="e0082-127">Financiële gevolgen</span><span class="sxs-lookup"><span data-stu-id="e0082-127">Financial impact</span></span>

<span data-ttu-id="e0082-128">Een project wordt ook financieel beïnvloed wanneer een goedkeuring wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="e0082-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="e0082-129">Ten eerste worden de corresponderende werkelijke waarden voor kosten en verkopen op de volgende manier bijgewerkt:</span><span class="sxs-lookup"><span data-stu-id="e0082-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="e0082-130">De aanpassingsstatus wordt ingesteld op **Aangepast**.</span><span class="sxs-lookup"><span data-stu-id="e0082-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="e0082-131">De factureringsstatus wordt ingesteld op **Geannuleerd**.</span><span class="sxs-lookup"><span data-stu-id="e0082-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="e0082-132">Vervolgens worden er stornoposten gemaakt in de tabel Werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="e0082-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="e0082-133">Om stornoposten te maken, kopieert het systeem de veldwaarden van de oorspronkelijke werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="e0082-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="e0082-134">De enige waarden die niet worden gekopieerd, zijn de hoeveelheidswaarden.</span><span class="sxs-lookup"><span data-stu-id="e0082-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="e0082-135">In plaats daarvan worden deze waarden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="e0082-135">These values are reversed instead.</span></span> <span data-ttu-id="e0082-136">Omgekeerde werkelijke waarden worden gemaakt voor de werkelijke waarden **Kosten** en **Niet-gefactureerde verkoop**.</span><span class="sxs-lookup"><span data-stu-id="e0082-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="e0082-137">Het veld **Aanpassingsstatus** voor de omgekeerde werkelijke waarden wordt ingesteld op **Niet aanpasbaar** en de factureringsstatus wordt ingesteld op **Geannuleerd**.</span><span class="sxs-lookup"><span data-stu-id="e0082-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="e0082-138">Als deze wijzigingen zijn doorgevoerd, komen de vastgelegde uitgaven voor het project en de omzetbacklog voor het project niet meer overeen met de bedragen die deze werkelijke waarden vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="e0082-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
