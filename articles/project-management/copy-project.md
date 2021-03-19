---
title: Een project kopiëren
description: In dit onderwerp krijgt u informatie over het kopiëren van projecten in Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479513"
---
# <a name="copy-a-project"></a><span data-ttu-id="f6f3c-103">Een project kopiëren</span><span class="sxs-lookup"><span data-stu-id="f6f3c-103">Copy a project</span></span>

<span data-ttu-id="f6f3c-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="f6f3c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f6f3c-105">Met Dynamics 365 Project Operations kunt u snel nieuwe projecten bouwen door **Project kopiëren** te selecteren op het formulier **Projecten**.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="f6f3c-106">Als u een project wilt kopiëren, opent u het project dat u wilt kopiëren en selecteert u vervolgens **Project kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="f6f3c-107">Met de actie kopieert u het volgende:</span><span class="sxs-lookup"><span data-stu-id="f6f3c-107">The action will copy:</span></span>

- <span data-ttu-id="f6f3c-108">Projecteigenschappen (de geschatte begindatum wordt gekopieerd vanuit het bronproject)</span><span class="sxs-lookup"><span data-stu-id="f6f3c-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="f6f3c-109">De structuur voor werkspecificatie</span><span class="sxs-lookup"><span data-stu-id="f6f3c-109">The Work breakdown structure</span></span>
- <span data-ttu-id="f6f3c-110">Projectteamleden</span><span class="sxs-lookup"><span data-stu-id="f6f3c-110">Project team members</span></span>
- <span data-ttu-id="f6f3c-111">Projectschattingen</span><span class="sxs-lookup"><span data-stu-id="f6f3c-111">Project estimates</span></span>
- <span data-ttu-id="f6f3c-112">Projectonkostenschattingen</span><span class="sxs-lookup"><span data-stu-id="f6f3c-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="f6f3c-113">Projecteigenschappen</span><span class="sxs-lookup"><span data-stu-id="f6f3c-113">Project properties</span></span>

<span data-ttu-id="f6f3c-114">Wanneer het project wordt gekopieerd, worden de waarden in de volgende velden gekopieerd:</span><span class="sxs-lookup"><span data-stu-id="f6f3c-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="f6f3c-115">Meetcriterium</span><span class="sxs-lookup"><span data-stu-id="f6f3c-115">Name</span></span>
- <span data-ttu-id="f6f3c-116">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f6f3c-116">Description</span></span>
- <span data-ttu-id="f6f3c-117">Klant</span><span class="sxs-lookup"><span data-stu-id="f6f3c-117">Customer</span></span>
- <span data-ttu-id="f6f3c-118">Agendasjabloon</span><span class="sxs-lookup"><span data-stu-id="f6f3c-118">Calendar Template</span></span>
- <span data-ttu-id="f6f3c-119">Valuta</span><span class="sxs-lookup"><span data-stu-id="f6f3c-119">Currency</span></span>
- <span data-ttu-id="f6f3c-120">Contracterende eenheid</span><span class="sxs-lookup"><span data-stu-id="f6f3c-120">Contracting Unit</span></span>
- <span data-ttu-id="f6f3c-121">Projectmanager</span><span class="sxs-lookup"><span data-stu-id="f6f3c-121">Project Manager</span></span>
- <span data-ttu-id="f6f3c-122">Status</span><span class="sxs-lookup"><span data-stu-id="f6f3c-122">Status</span></span>
- <span data-ttu-id="f6f3c-123">Algehele projectstatus</span><span class="sxs-lookup"><span data-stu-id="f6f3c-123">Overall Project Status</span></span>
- <span data-ttu-id="f6f3c-124">Opmerkingen </span><span class="sxs-lookup"><span data-stu-id="f6f3c-124">Comments</span></span>
- <span data-ttu-id="f6f3c-125">Schattingen</span><span class="sxs-lookup"><span data-stu-id="f6f3c-125">Estimates</span></span>
- <span data-ttu-id="f6f3c-126">Geschatte begindatum</span><span class="sxs-lookup"><span data-stu-id="f6f3c-126">Estimated Start Date</span></span>
- <span data-ttu-id="f6f3c-127">Einddatum</span><span class="sxs-lookup"><span data-stu-id="f6f3c-127">Finish Date</span></span>
- <span data-ttu-id="f6f3c-128">Inspanning (uren)</span><span class="sxs-lookup"><span data-stu-id="f6f3c-128">Effort (Hours)</span></span>
- <span data-ttu-id="f6f3c-129">Geschatte arbeidskosten</span><span class="sxs-lookup"><span data-stu-id="f6f3c-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="f6f3c-130">Geschatte onkosten</span><span class="sxs-lookup"><span data-stu-id="f6f3c-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="f6f3c-131">Structuur voor werkspecificatie</span><span class="sxs-lookup"><span data-stu-id="f6f3c-131">Work breakdown structure</span></span>

<span data-ttu-id="f6f3c-132">Wanneer het project wordt gekopieerd, wordt de volledige voor de resource geladen structuur voor werkspecificatie gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="f6f3c-133">Benoemde resources worden vervangen door algemene resource.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="f6f3c-134">Als de benoemde resources niet dezelfde werkuren heeft als de algemene resource, wordt de planning opnieuw berekend en kan de duur van de taak veranderen.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="f6f3c-135">Projectteamleden</span><span class="sxs-lookup"><span data-stu-id="f6f3c-135">Project team members</span></span>

<span data-ttu-id="f6f3c-136">Wanneer een projectteam wordt gekopieerd uit het bronproject, worden de algemene resources gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="f6f3c-137">Algemene resourcetoewijzingen worden ook onderhouden, net zoals in het bronproject.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="f6f3c-138">Benoemde resources worden omgezet in algemene teamleden.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="f6f3c-139">Schattingen</span><span class="sxs-lookup"><span data-stu-id="f6f3c-139">Estimates</span></span>

<span data-ttu-id="f6f3c-140">Wanneer het project wordt gekopieerd, worden zowel resource- als kostenramingsregels uit het bronproject gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="f6f3c-141">Zie voor informatie over het programmatisch openen van Project kopiëren [Projectsjablonen ontwikkelen met Project kopiëren](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="f6f3c-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
