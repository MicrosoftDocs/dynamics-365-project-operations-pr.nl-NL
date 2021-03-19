---
title: Projectfasen
description: Dit onderwerp bevat informatie over de projectfasen die beschikbaar zijn in Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286782"
---
# <a name="project-stages"></a><span data-ttu-id="78fae-103">Projectfasen</span><span class="sxs-lookup"><span data-stu-id="78fae-103">Project stages</span></span>

<span data-ttu-id="78fae-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="78fae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="78fae-105">Projectfasen zijn ontworpen om tijdens de voortgang van het project de status aan te geven.</span><span class="sxs-lookup"><span data-stu-id="78fae-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="78fae-106">Aanpassingen kunnen worden gebruikt om de fasen automatisch bij te werken met bedrijfsprocesstromen, Power Automate, of plug-in extensies.</span><span class="sxs-lookup"><span data-stu-id="78fae-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="78fae-107">De volgende fasen worden gedefinieerd in de standaardbedrijfsprocesstroom:</span><span class="sxs-lookup"><span data-stu-id="78fae-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="78fae-108">Nieuw:</span><span class="sxs-lookup"><span data-stu-id="78fae-108">New</span></span>
- <span data-ttu-id="78fae-109">Prijsopgave</span><span class="sxs-lookup"><span data-stu-id="78fae-109">Quote</span></span>
- <span data-ttu-id="78fae-110">Plan</span><span class="sxs-lookup"><span data-stu-id="78fae-110">Plan</span></span>
- <span data-ttu-id="78fae-111">Bezorgen</span><span class="sxs-lookup"><span data-stu-id="78fae-111">Deliver</span></span>
- <span data-ttu-id="78fae-112">Voltooien</span><span class="sxs-lookup"><span data-stu-id="78fae-112">Complete</span></span>
- <span data-ttu-id="78fae-113">Afsluiten</span><span class="sxs-lookup"><span data-stu-id="78fae-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="78fae-114">Nieuw:</span><span class="sxs-lookup"><span data-stu-id="78fae-114">New</span></span>

<span data-ttu-id="78fae-115">Wanneer u een project maakt, wordt de projectfase ingesteld op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="78fae-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="78fae-116">Als het project is gemaakt op basis van een sjabloon, kan het project plannings-, schattings- en teamgegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="78fae-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="78fae-117">Als dit niet het geval is, is het een schets van het project en moeten de resterende onderdelen worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="78fae-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="78fae-118">Prijsopgave</span><span class="sxs-lookup"><span data-stu-id="78fae-118">Quote</span></span>

<span data-ttu-id="78fae-119">Wanneer u een project aan een prijsopgave koppelt of wanneer u een project maakt op basis van een prijsopgave, wordt de projectfase ingesteld op **Prijsopgave** en worden de geschatte begin- en einddatum bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="78fae-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="78fae-120">Als het project zich in de fase **Prijsopgave** bevindt, worden op het tabblad **Verkoop** van de pagina **Projectentiteit** details van de prijsopgave weergegeven.</span><span class="sxs-lookup"><span data-stu-id="78fae-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="78fae-121">Plannen</span><span class="sxs-lookup"><span data-stu-id="78fae-121">Plan</span></span>

<span data-ttu-id="78fae-122">Wanneer u een order binnenhaalt op basis van een prijsopgave die aan een project is gekoppeld en het project overgaat naar de fase **Contract**, wordt de projectfase bijgewerkt naar **Plannen**.</span><span class="sxs-lookup"><span data-stu-id="78fae-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="78fae-123">Als het project zich in de fase **Plannen** bevindt, worden op de pagina **Projectentiteit** de details van het contract weergegeven.</span><span class="sxs-lookup"><span data-stu-id="78fae-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="78fae-124">Leveren</span><span class="sxs-lookup"><span data-stu-id="78fae-124">Deliver</span></span>

<span data-ttu-id="78fae-125">Wanneer het projectplan is voltooid en u aan het project kunt beginnen, moet de projectmanager de projectfase bijwerken naar **Leveren** om aan te geven dat het project is gestart.</span><span class="sxs-lookup"><span data-stu-id="78fae-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="78fae-126">Voltooid</span><span class="sxs-lookup"><span data-stu-id="78fae-126">Complete</span></span> 

<span data-ttu-id="78fae-127">Wanneer het werk voor het project is voltooid, kan de projectmanager de fase bijwerken naar **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="78fae-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="78fae-128">Als u de projectfase bijwerkt naar **Voltooid**, geeft de projectmanager aan dat het werk voor 100 procent is voltooid, maar dat het project nog open wordt gehouden om eventuele openstaande tijdsvermeldingen of onkostenposten te kunnen vastleggen.</span><span class="sxs-lookup"><span data-stu-id="78fae-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="78fae-129">Sluiten</span><span class="sxs-lookup"><span data-stu-id="78fae-129">Close</span></span>

<span data-ttu-id="78fae-130">Wanneer alle transacties voor het project zijn vastgelegd, kan de projectmanager de fase bijwerken naar **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="78fae-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="78fae-131">Op dat moment kunnen er geen transacties meer worden vastgelegd en wordt het project ingesteld op alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="78fae-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]