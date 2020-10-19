---
title: Een project kopiëren
description: Dit onderwerp biedt informatie over het kopiëren van projecten in Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908033"
---
# <a name="copy-a-project"></a><span data-ttu-id="b0446-103">Een project kopiëren</span><span class="sxs-lookup"><span data-stu-id="b0446-103">Copy a project</span></span>

<span data-ttu-id="b0446-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="b0446-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b0446-105">Met Dynamics 365 Project Operations kunt u snel nieuwe projecten bouwen met behulp van de actie **Project kopiëren** in het formulier **Projecten**.</span><span class="sxs-lookup"><span data-stu-id="b0446-105">With Dynamics 365 Project Operations, you can quickly build new projects by using the **Copy Project** action on the **Projects** from.</span></span> <span data-ttu-id="b0446-106">Als u een project wilt kopiëren, selecteert u een project en vervolgens **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="b0446-106">To copy a project, select a project, and then select **Copy**.</span></span> <span data-ttu-id="b0446-107">Met de actie kopieert u het volgende:</span><span class="sxs-lookup"><span data-stu-id="b0446-107">The action will copy:</span></span>

- <span data-ttu-id="b0446-108">Projecteigenschappen</span><span class="sxs-lookup"><span data-stu-id="b0446-108">Project properties</span></span>
- <span data-ttu-id="b0446-109">De structuur voor werkspecificatie</span><span class="sxs-lookup"><span data-stu-id="b0446-109">The Work breakdown structure</span></span>
- <span data-ttu-id="b0446-110">Projectteamleden</span><span class="sxs-lookup"><span data-stu-id="b0446-110">Project team members</span></span>
- <span data-ttu-id="b0446-111">Projectschattingen</span><span class="sxs-lookup"><span data-stu-id="b0446-111">Project estimates</span></span>
- <span data-ttu-id="b0446-112">Projectonkostenschattingen</span><span class="sxs-lookup"><span data-stu-id="b0446-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="b0446-113">Projecteigenschappen</span><span class="sxs-lookup"><span data-stu-id="b0446-113">Project properties</span></span>

<span data-ttu-id="b0446-114">Wanneer het project wordt gekopieerd, worden de waarden in de volgende velden gekopieerd:</span><span class="sxs-lookup"><span data-stu-id="b0446-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="b0446-115">Meetcriterium</span><span class="sxs-lookup"><span data-stu-id="b0446-115">Name</span></span>
- <span data-ttu-id="b0446-116">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="b0446-116">Description</span></span>
- <span data-ttu-id="b0446-117">Klant</span><span class="sxs-lookup"><span data-stu-id="b0446-117">Customer</span></span>
- <span data-ttu-id="b0446-118">Agendasjabloon</span><span class="sxs-lookup"><span data-stu-id="b0446-118">Calendar Template</span></span>
- <span data-ttu-id="b0446-119">Valuta</span><span class="sxs-lookup"><span data-stu-id="b0446-119">Currency</span></span>
- <span data-ttu-id="b0446-120">Contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="b0446-120">Contracting Unit</span></span>
- <span data-ttu-id="b0446-121">Projectmanager</span><span class="sxs-lookup"><span data-stu-id="b0446-121">Project Manager</span></span>
- <span data-ttu-id="b0446-122">Status</span><span class="sxs-lookup"><span data-stu-id="b0446-122">Status</span></span>
- <span data-ttu-id="b0446-123">Algehele projectstatus</span><span class="sxs-lookup"><span data-stu-id="b0446-123">Overall Project Status</span></span>
- <span data-ttu-id="b0446-124">Opmerkingen </span><span class="sxs-lookup"><span data-stu-id="b0446-124">Comments</span></span>
- <span data-ttu-id="b0446-125">Schattingen</span><span class="sxs-lookup"><span data-stu-id="b0446-125">Estimates</span></span>
- <span data-ttu-id="b0446-126">Geschatte begindatum</span><span class="sxs-lookup"><span data-stu-id="b0446-126">Estimated Start Date</span></span>
- <span data-ttu-id="b0446-127">Einddatum</span><span class="sxs-lookup"><span data-stu-id="b0446-127">Finish Date</span></span>
- <span data-ttu-id="b0446-128">Inspanning (uren)</span><span class="sxs-lookup"><span data-stu-id="b0446-128">Effort (Hours)</span></span>
- <span data-ttu-id="b0446-129">Geschatte arbeidskosten</span><span class="sxs-lookup"><span data-stu-id="b0446-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="b0446-130">Geschatte onkosten</span><span class="sxs-lookup"><span data-stu-id="b0446-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="b0446-131">Structuur voor werkspecificatie</span><span class="sxs-lookup"><span data-stu-id="b0446-131">Work breakdown structure</span></span>

<span data-ttu-id="b0446-132">Wanneer het project wordt gekopieerd, wordt de volledige voor de resource geladen structuur voor werkspecificatie gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="b0446-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="b0446-133">Benoemde resources worden vervangen door algemene resource.</span><span class="sxs-lookup"><span data-stu-id="b0446-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="b0446-134">Als de benoemde resources niet dezelfde werkuren heeft als de algemene resource, wordt de planning opnieuw berekend en kan de duur van de taak veranderen.</span><span class="sxs-lookup"><span data-stu-id="b0446-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="b0446-135">Projectteamleden</span><span class="sxs-lookup"><span data-stu-id="b0446-135">Project team members</span></span>

<span data-ttu-id="b0446-136">Wanneer een projectteam wordt gekopieerd uit het bronproject, worden de algemene resources gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="b0446-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="b0446-137">Algemene resourcetoewijzingen worden ook onderhouden, net zoals in het bronproject.</span><span class="sxs-lookup"><span data-stu-id="b0446-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="b0446-138">Benoemde resources worden omgezet in algemene teamleden.</span><span class="sxs-lookup"><span data-stu-id="b0446-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="b0446-139">Schattingen</span><span class="sxs-lookup"><span data-stu-id="b0446-139">Estimates</span></span>

<span data-ttu-id="b0446-140">Wanneer het project wordt gekopieerd, worden zowel resource- als kostenramingsregels uit het bronproject gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="b0446-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span>