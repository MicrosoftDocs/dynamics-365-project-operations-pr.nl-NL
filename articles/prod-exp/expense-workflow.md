---
title: Werkstroom voor onkostenbeheer
description: In dit onderwerp wordt uitgelegd hoe u het werkstroomsysteem in Microsoft Dynamics 365 Finance kunt gebruiken voor het instellen van een beoordelingsproces voor onkostendeclaraties in Onkostenbeheer.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271662"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="6bee3-103">Werkstroom voor onkostenbeheer</span><span class="sxs-lookup"><span data-stu-id="6bee3-103">Expense management workflow</span></span>

<span data-ttu-id="6bee3-104">U kunt het werkstroomsysteem gebruiken om een beoordelingsproces voor onkostendeclaraties in Onkostenbeheer in te stellen.</span><span class="sxs-lookup"><span data-stu-id="6bee3-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="6bee3-105">U kunt een werkstroom instellen waarin de volgende criteria worden gebruikt om te bepalen wie onkostendeclaraties goedkeurt:</span><span class="sxs-lookup"><span data-stu-id="6bee3-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="6bee3-106">De hiërarchie van werknemersrapportage en vooraf gedefinieerde goedkeuringslimieten</span><span class="sxs-lookup"><span data-stu-id="6bee3-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="6bee3-107">Goedkeuring op meerdere niveaus die tussentijdse fiatteurs en een definitieve goedkeurder ondersteunt</span><span class="sxs-lookup"><span data-stu-id="6bee3-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="6bee3-108">Financiële dimensies en projectverantwoordelijkheid</span><span class="sxs-lookup"><span data-stu-id="6bee3-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="6bee3-109">Toewijzing aan specifieke gebruikers of gebruikersgroepen</span><span class="sxs-lookup"><span data-stu-id="6bee3-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="6bee3-110">Werkstroomgoedkeuringen kunnen worden gemaakt voor onkostendeclaraties, reisaanvragen, contante voorschotten en terugvordering van belasting over de toegevoegde waarde (btw).</span><span class="sxs-lookup"><span data-stu-id="6bee3-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="6bee3-111">**Voorbeeld**</span><span class="sxs-lookup"><span data-stu-id="6bee3-111">**Example**</span></span>

<span data-ttu-id="6bee3-112">Het volgende proces is een voorbeeld van de werkstroom voor onkostenbeheer voor een onkostendeclaratie.</span><span class="sxs-lookup"><span data-stu-id="6bee3-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="6bee3-113">Een werknemer maakt een onkostendeclaratie en slaat deze op.</span><span class="sxs-lookup"><span data-stu-id="6bee3-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="6bee3-114">De werknemer dient de onkostendeclaratie ter goedkeuring in.</span><span class="sxs-lookup"><span data-stu-id="6bee3-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="6bee3-115">De fiatteur wordt geïdentificeerd op basis van de regels die zijn gedefinieerd toen de werkstroom werd ingesteld.</span><span class="sxs-lookup"><span data-stu-id="6bee3-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="6bee3-116">De fiatteur krijgt een melding dat er een onkostendeclaratie klaar ligt voor goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="6bee3-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="6bee3-117">De fiatteur beoordeelt de onkostendeclaratie en controleert of aan de volgende voorwaarden is voldaan:</span><span class="sxs-lookup"><span data-stu-id="6bee3-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="6bee3-118">De onkosten zijn niet in strijd met het onkostenbeleid.</span><span class="sxs-lookup"><span data-stu-id="6bee3-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="6bee3-119">Als onkosten in strijd zijn met een beleid, controleert de fiatteur of de onkostendeclaratie een geldige zakelijke rechtvaardiging bevat.</span><span class="sxs-lookup"><span data-stu-id="6bee3-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="6bee3-120">Elektronische ontvangstbewijzen worden bij de onkostendeclaratie gevoegd.</span><span class="sxs-lookup"><span data-stu-id="6bee3-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="6bee3-121">De fiatteur keurt de onkostendeclaratie goed.</span><span class="sxs-lookup"><span data-stu-id="6bee3-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="6bee3-122">De onkostendeclaratie wordt voor boeking toegewezen aan de crediteurenadministratie.</span><span class="sxs-lookup"><span data-stu-id="6bee3-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="6bee3-123">Een van de volgende stappen vindt plaats, afhankelijk van de vraag of automatisch boeken is geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="6bee3-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="6bee3-124">Als automatisch boeken is geconfigureerd, wordt de onkostendeclaratie verwerkt voor betaling en wordt de status van de onkostendeclaratie bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="6bee3-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="6bee3-125">Als automatisch boeken niet is geconfigureerd, controleert de coördinator van de crediteurenadministratie of alle originele ontvangstbewijzen zijn ingediend en of de ontvangstbewijzen overeenstemmen met de onkosten op de onkostendeclaratie.</span><span class="sxs-lookup"><span data-stu-id="6bee3-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="6bee3-126">Alle belastingcodes die op de onkostendeclaratie worden ingevoerd, moeten ook als correct worden geverifieerd.</span><span class="sxs-lookup"><span data-stu-id="6bee3-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="6bee3-127">Nadat deze vereisten zijn geverifieerd, wordt de onkostendeclaratie geboekt.</span><span class="sxs-lookup"><span data-stu-id="6bee3-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="6bee3-128">Nadat de onkostendeclaratie is geboekt, wordt betaling geautoriseerd voor de onkostendeclaratie en wordt de werknemer vergoed.</span><span class="sxs-lookup"><span data-stu-id="6bee3-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]