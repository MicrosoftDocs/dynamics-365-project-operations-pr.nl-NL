---
title: Projectfasen
description: In dit onderwerp krijgt u informatie over projectfasen.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750729"
---
# <a name="project-stages"></a><span data-ttu-id="742a7-103">Projectfasen</span><span class="sxs-lookup"><span data-stu-id="742a7-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="742a7-104">Projectfasen worden bijgewerkt om tijdens de voortgang van het project de status aan te geven.</span><span class="sxs-lookup"><span data-stu-id="742a7-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="742a7-105">Met de standaardbedrijfsprocesstroom worden bepaalde fasen van het project automatisch bijgewerkt, terwijl andere fasen handmatig door de projectmanager worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="742a7-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="742a7-106">De volgende fasen worden gedefinieerd in de standaardbedrijfsprocesstroom:</span><span class="sxs-lookup"><span data-stu-id="742a7-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="742a7-107">Nieuw</span><span class="sxs-lookup"><span data-stu-id="742a7-107">New</span></span>
- <span data-ttu-id="742a7-108">Prijsopgave</span><span class="sxs-lookup"><span data-stu-id="742a7-108">Quote</span></span>
- <span data-ttu-id="742a7-109">Plannen</span><span class="sxs-lookup"><span data-stu-id="742a7-109">Plan</span></span>
- <span data-ttu-id="742a7-110">Leveren</span><span class="sxs-lookup"><span data-stu-id="742a7-110">Deliver</span></span>
- <span data-ttu-id="742a7-111">Voltooid</span><span class="sxs-lookup"><span data-stu-id="742a7-111">Complete</span></span>
- <span data-ttu-id="742a7-112">Sluiten</span><span class="sxs-lookup"><span data-stu-id="742a7-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="742a7-113">Nieuw</span><span class="sxs-lookup"><span data-stu-id="742a7-113">New</span></span>

<span data-ttu-id="742a7-114">Wanneer u een project maakt, wordt de projectfase ingesteld op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="742a7-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="742a7-115">Als het project is gemaakt op basis van een sjabloon, kan het project plannings-, schattings- en teamgegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="742a7-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="742a7-116">Als dit niet het geval is, is het slechts een schets van het project en moeten de resterende onderdelen worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="742a7-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="742a7-117">Prijsopgave</span><span class="sxs-lookup"><span data-stu-id="742a7-117">Quote</span></span>

<span data-ttu-id="742a7-118">Wanneer u een project aan een prijsopgave koppelt of wanneer u een project maakt op basis van een prijsopgave, wordt de projectfase ingesteld op **Prijsopgave** en worden de geschatte begin- en einddatum bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="742a7-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="742a7-119">Als het project zich in de fase **Prijsopgave** bevindt, worden op het tabblad **Verkoop** van de pagina **Projectentiteit** details van de prijsopgave weergegeven.</span><span class="sxs-lookup"><span data-stu-id="742a7-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="742a7-120">Plannen</span><span class="sxs-lookup"><span data-stu-id="742a7-120">Plan</span></span>

<span data-ttu-id="742a7-121">Wanneer u een order binnenhaalt op basis van een prijsopgave die aan een project is gekoppeld en het project overgaat naar de fase **Contract**, wordt de projectfase bijgewerkt naar **Plannen**.</span><span class="sxs-lookup"><span data-stu-id="742a7-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="742a7-122">Als het project zich in de fase **Plannen** bevindt, worden op de pagina **Projectentiteit** de details van het contract weergegeven.</span><span class="sxs-lookup"><span data-stu-id="742a7-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="742a7-123">Leveren</span><span class="sxs-lookup"><span data-stu-id="742a7-123">Deliver</span></span>

<span data-ttu-id="742a7-124">Wanneer het projectplan is voltooid en u aan het project kunt beginnen, moet de projectmanager de projectfase bijwerken naar **Leveren** om aan te geven dat het project is gestart.</span><span class="sxs-lookup"><span data-stu-id="742a7-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="742a7-125">Voltooid</span><span class="sxs-lookup"><span data-stu-id="742a7-125">Complete</span></span> 

<span data-ttu-id="742a7-126">Wanneer het werk voor het project is voltooid, kan de projectmanager de fase bijwerken naar **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="742a7-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="742a7-127">Als u de projectfase bijwerkt naar **Voltooid**, geeft de projectmanager aan dat het werk voor 100 procent is voltooid, maar dat het project nog open wordt gehouden om eventuele openstaande tijdsvermeldingen of onkostenposten te kunnen vastleggen.</span><span class="sxs-lookup"><span data-stu-id="742a7-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="742a7-128">Sluiten</span><span class="sxs-lookup"><span data-stu-id="742a7-128">Close</span></span>

<span data-ttu-id="742a7-129">Wanneer alle transacties voor het project zijn vastgelegd, kan de projectmanager de fase bijwerken naar **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="742a7-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="742a7-130">Op dat moment kunnen er geen transacties meer worden vastgelegd en wordt het project ingesteld op alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="742a7-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
