---
title: Onkostenpost (Lite)
description: Dit onderwerp biedt informatie over het werken met onkosteninvoer in een Lite-implementatie.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074448"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="fc868-103">Onkostenpost (Lite)</span><span class="sxs-lookup"><span data-stu-id="fc868-103">Expense entry (lite)</span></span>

<span data-ttu-id="fc868-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="fc868-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fc868-105">Eenvoudig, of Lite, onkostenbeheer is de mogelijkheid om eenvoudige onkosten vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="fc868-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="fc868-106">U kunt onkosten voor een project boeken waarna de projectfiatteur deze beoordeelt en goedkeurt.</span><span class="sxs-lookup"><span data-stu-id="fc868-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="fc868-107">Zie [Onkostenoverzicht](expense-overview.md) voor meer informatie over mogelijkheden voor onkosten in Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fc868-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="fc868-108">Eenvoudige onkosten vastleggen</span><span class="sxs-lookup"><span data-stu-id="fc868-108">Capture a basic expense</span></span>

<span data-ttu-id="fc868-109">U kunt uw onkosten vastleggen, zodat u ze kunt indienen bij de fiatteur.</span><span class="sxs-lookup"><span data-stu-id="fc868-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="fc868-110">Ga naar **Onkosten** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="fc868-110">Go to **Expenses** , and select **New**.</span></span>
2. <span data-ttu-id="fc868-111">Voer op de pagina **Nieuwe onkosten** de vereiste onkostengegevens in en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="fc868-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="fc868-112">Eenvoudige onkosten indienen</span><span class="sxs-lookup"><span data-stu-id="fc868-112">Submit a basic expense</span></span>

<span data-ttu-id="fc868-113">Nadat u al uw onkosten hebt vastgelegd en klaar bent om deze te laten goedkeuren, moet u ze indienen.</span><span class="sxs-lookup"><span data-stu-id="fc868-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="fc868-114">Ga naar **Onkosten** en selecteer een item.</span><span class="sxs-lookup"><span data-stu-id="fc868-114">Go to **Expenses** , and select an expense.</span></span> <span data-ttu-id="fc868-115">Of selecteer alle onkosten met behulp van het selectievakje in de koptekst.</span><span class="sxs-lookup"><span data-stu-id="fc868-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="fc868-116">Selecteer **Indienen**.</span><span class="sxs-lookup"><span data-stu-id="fc868-116">Select **Submit**.</span></span> <span data-ttu-id="fc868-117">De geselecteerde items worden verwerkt en vervolgens worden er aanvragen voor onkostengoedkeuring gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fc868-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="fc868-118">Eenvoudige onkosten intrekken</span><span class="sxs-lookup"><span data-stu-id="fc868-118">Recall a basic expense</span></span>

<span data-ttu-id="fc868-119">Als u onkosten per ongeluk indient, kunt u deze intrekken.</span><span class="sxs-lookup"><span data-stu-id="fc868-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="fc868-120">Binnen hoeveel tijd u onkosten moet intrekken, is afhankelijk van de goedkeuringsfase.</span><span class="sxs-lookup"><span data-stu-id="fc868-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="fc868-121">Als de fiatteur de onkosten nog niet heeft goedgekeurd, kan de intrekking onmiddellijk plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="fc868-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="fc868-122">Is de boeking echter al goedgekeurd, dan wordt de fiatteur gevraagd om de intrekking goed te keuren en de transacties terug te draaien.</span><span class="sxs-lookup"><span data-stu-id="fc868-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="fc868-123">Ga naar **Onkosten** en selecteer vervolgens in de lijst met onkosten de onkosten die u wilt intrekken.</span><span class="sxs-lookup"><span data-stu-id="fc868-123">Go to **Expenses** , and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="fc868-124">Selecteer **Intrekken**.</span><span class="sxs-lookup"><span data-stu-id="fc868-124">Select **Recall**.</span></span> <span data-ttu-id="fc868-125">Als de onkostenvermelding nog niet is goedgekeurd, wordt deze direct ingetrokken.</span><span class="sxs-lookup"><span data-stu-id="fc868-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="fc868-126">Als de onkostenvermelding al is goedgekeurd, wordt een intrekkingsverzoek gemaakt om de fiatteur te laten weten dat u de onkosten wilt storneren.</span><span class="sxs-lookup"><span data-stu-id="fc868-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="fc868-127">De fiatteur bevestigt dan dat de terugboeking kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="fc868-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="fc868-128">Eenvoudige onkosten verwijderen</span><span class="sxs-lookup"><span data-stu-id="fc868-128">Delete a basic expense</span></span>

<span data-ttu-id="fc868-129">Onkosten die nog niet zijn ingediend, kunnen worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="fc868-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="fc868-130">Om onkosten te verwijderen die al zijn ingediend, moet u deze eerst intrekken.</span><span class="sxs-lookup"><span data-stu-id="fc868-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="fc868-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fc868-131">See also</span></span>

- [<span data-ttu-id="fc868-132">Overzicht van goedkeuringen</span><span class="sxs-lookup"><span data-stu-id="fc868-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
