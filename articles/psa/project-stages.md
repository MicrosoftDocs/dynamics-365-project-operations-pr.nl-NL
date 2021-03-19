---
title: Typen projectfasen
description: In dit onderwerp krijgt u informatie over projectfasen.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3503b17e54fc0b321582c30ce534e4cb3f497a5f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283677"
---
# <a name="project-stage-types"></a><span data-ttu-id="6a1f4-103">Typen projectfasen</span><span class="sxs-lookup"><span data-stu-id="6a1f4-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6a1f4-104">Projectfasen zijn ontworpen om tijdens de voortgang van het project de status aan te geven.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="6a1f4-105">Aanpassingen kunnen worden gebruikt om de fasen automatisch bij te werken met bedrijfsprocesstromen, Power Automate, of plug-in extensies.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="6a1f4-106">De volgende fasen worden gedefinieerd in de standaardbedrijfsprocesstroom:</span><span class="sxs-lookup"><span data-stu-id="6a1f4-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="6a1f4-107">Nieuw:</span><span class="sxs-lookup"><span data-stu-id="6a1f4-107">New</span></span>
- <span data-ttu-id="6a1f4-108">Prijsopgave</span><span class="sxs-lookup"><span data-stu-id="6a1f4-108">Quote</span></span>
- <span data-ttu-id="6a1f4-109">Plannen</span><span class="sxs-lookup"><span data-stu-id="6a1f4-109">Plan</span></span>
- <span data-ttu-id="6a1f4-110">Leveren</span><span class="sxs-lookup"><span data-stu-id="6a1f4-110">Deliver</span></span>
- <span data-ttu-id="6a1f4-111">Voltooid</span><span class="sxs-lookup"><span data-stu-id="6a1f4-111">Complete</span></span>
- <span data-ttu-id="6a1f4-112">Sluiten</span><span class="sxs-lookup"><span data-stu-id="6a1f4-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="6a1f4-113">Nieuw</span><span class="sxs-lookup"><span data-stu-id="6a1f4-113">New</span></span>

<span data-ttu-id="6a1f4-114">Wanneer u een project maakt, wordt de projectfase ingesteld op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="6a1f4-115">Als het project is gemaakt op basis van een sjabloon, kan het project plannings-, schattings- en teamgegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="6a1f4-116">Als dit niet het geval is, is het slechts een schets van het project en moeten de resterende onderdelen worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="6a1f4-117">Prijsopgave</span><span class="sxs-lookup"><span data-stu-id="6a1f4-117">Quote</span></span>

<span data-ttu-id="6a1f4-118">Wanneer u een project aan een prijsopgave koppelt of wanneer u een project maakt op basis van een prijsopgave, wordt de projectfase ingesteld op **Prijsopgave** en worden de geschatte begin- en einddatum bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="6a1f4-119">Als het project zich in de fase **Prijsopgave** bevindt, worden op het tabblad **Verkoop** van de pagina **Projectentiteit** details van de prijsopgave weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="6a1f4-120">Plannen</span><span class="sxs-lookup"><span data-stu-id="6a1f4-120">Plan</span></span>

<span data-ttu-id="6a1f4-121">Wanneer u een order binnenhaalt op basis van een prijsopgave die aan een project is gekoppeld en het project overgaat naar de fase **Contract**, wordt de projectfase bijgewerkt naar **Plannen**.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="6a1f4-122">Als het project zich in de fase **Plannen** bevindt, worden op de pagina **Projectentiteit** de details van het contract weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="6a1f4-123">Leveren</span><span class="sxs-lookup"><span data-stu-id="6a1f4-123">Deliver</span></span>

<span data-ttu-id="6a1f4-124">Wanneer het projectplan is voltooid en u aan het project kunt beginnen, moet de projectmanager de projectfase bijwerken naar **Leveren** om aan te geven dat het project is gestart.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="6a1f4-125">Voltooid</span><span class="sxs-lookup"><span data-stu-id="6a1f4-125">Complete</span></span> 

<span data-ttu-id="6a1f4-126">Wanneer het werk voor het project is voltooid, kan de projectmanager de fase bijwerken naar **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="6a1f4-127">Als u de projectfase bijwerkt naar **Voltooid**, geeft de projectmanager aan dat het werk voor 100 procent is voltooid, maar dat het project nog open wordt gehouden om eventuele openstaande tijdsvermeldingen of onkostenposten te kunnen vastleggen.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="6a1f4-128">Sluiten</span><span class="sxs-lookup"><span data-stu-id="6a1f4-128">Close</span></span>

<span data-ttu-id="6a1f4-129">Wanneer alle transacties voor het project zijn vastgelegd, kan de projectmanager de fase bijwerken naar **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="6a1f4-130">Op dat moment kunnen er geen transacties meer worden vastgelegd en wordt het project ingesteld op alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="6a1f4-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]