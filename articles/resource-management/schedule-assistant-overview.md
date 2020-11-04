---
title: Overzicht van planningsassistent
description: Dit onderwerp biedt informatie over het werken met de planningsassistent om resources te boeken.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074420"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="98b73-103">Overzicht van planningsassistent</span><span class="sxs-lookup"><span data-stu-id="98b73-103">Schedule assistant overview</span></span>

<span data-ttu-id="98b73-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="98b73-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="98b73-105">De planningsassistent wordt gebruikt om resources te boeken op basis van de vereisten die zijn gedefinieerd door de projectmanager.</span><span class="sxs-lookup"><span data-stu-id="98b73-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="98b73-106">De planningsassistent werkt met de parameters in de resourcevereiste om de resource te vinden.</span><span class="sxs-lookup"><span data-stu-id="98b73-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="98b73-107">De planningsassistent beveelt resources aan die voldoen aan relevante vereisten, zoals tijdvensters of benodigde vaardigheden.</span><span class="sxs-lookup"><span data-stu-id="98b73-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="98b73-108">Nadat geschikte resources zijn geïdentificeerd, kan de resource- of projectmanager de resource voor het werk boeken.</span><span class="sxs-lookup"><span data-stu-id="98b73-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="98b73-109">Vereisten</span><span class="sxs-lookup"><span data-stu-id="98b73-109">Prerequisites</span></span>

<span data-ttu-id="98b73-110">De planningsassistent is onderdeel van de Universal Resource Scheduling-oplossing.</span><span class="sxs-lookup"><span data-stu-id="98b73-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="98b73-111">Deze oplossing wordt samen met Dynamics 365 Project Operations, Dynamics 365 Field Service en Dynamics 365 Customer Service geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="98b73-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="98b73-112">Afstemming van vereisten en resources</span><span class="sxs-lookup"><span data-stu-id="98b73-112">Matching requirements and resources</span></span>

<span data-ttu-id="98b73-113">Een gegenereerde resourcevereiste wordt gebaseerd op details zoals:</span><span class="sxs-lookup"><span data-stu-id="98b73-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="98b73-114">Kenmerken</span><span class="sxs-lookup"><span data-stu-id="98b73-114">Characteristics</span></span>
-   <span data-ttu-id="98b73-115">Functies</span><span class="sxs-lookup"><span data-stu-id="98b73-115">Roles</span></span>
-   <span data-ttu-id="98b73-116">Business units</span><span class="sxs-lookup"><span data-stu-id="98b73-116">Business units</span></span>
-   <span data-ttu-id="98b73-117">Resourcevoorkeuren</span><span class="sxs-lookup"><span data-stu-id="98b73-117">Resource preferences</span></span>
-   <span data-ttu-id="98b73-118">Inspanningscontouren</span><span class="sxs-lookup"><span data-stu-id="98b73-118">Effort contours</span></span>
-   <span data-ttu-id="98b73-119">Tijdzone</span><span class="sxs-lookup"><span data-stu-id="98b73-119">Time zone</span></span>

<span data-ttu-id="98b73-120">De planningsassistent gebruikt deze details om resources te filteren.</span><span class="sxs-lookup"><span data-stu-id="98b73-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="98b73-121">De planningsassistent starten</span><span class="sxs-lookup"><span data-stu-id="98b73-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="98b73-122">Er zijn twee manieren waarop de planningsassistent wordt gestart.</span><span class="sxs-lookup"><span data-stu-id="98b73-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="98b73-123">Als u de hybride modus gebruikt, kunt u in het teamlidraster elk teamlid met een niet-vervulde resourcevereiste selecteren en vervolgens **Boeken** selecteren.</span><span class="sxs-lookup"><span data-stu-id="98b73-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="98b73-124">Als u de centrale modus gebruikt, wordt de resource gezocht en geselecteerd door de resourcemanager.</span><span class="sxs-lookup"><span data-stu-id="98b73-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="98b73-125">Filters voor planningsassistent</span><span class="sxs-lookup"><span data-stu-id="98b73-125">Schedule assistant filters</span></span>

<span data-ttu-id="98b73-126">Nadat de planningsassistent is uitgevoerd, worden de details van de resourcevereiste weergegeven als gefilterde waarden in het linkerdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="98b73-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="98b73-127">De resourcemanager of de projectmanager kan de resultaten verfijnen door filters aan te passen aan de planningsbehoeften.</span><span class="sxs-lookup"><span data-stu-id="98b73-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="98b73-128">Het filterpaneel toont werkgerelateerde opties, waaronder:</span><span class="sxs-lookup"><span data-stu-id="98b73-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="98b73-129">Begin- en einddatum voor werk</span><span class="sxs-lookup"><span data-stu-id="98b73-129">Work start and end</span></span>
-   <span data-ttu-id="98b73-130">Kenmerken</span><span class="sxs-lookup"><span data-stu-id="98b73-130">Characteristics</span></span>
-   <span data-ttu-id="98b73-131">Functies</span><span class="sxs-lookup"><span data-stu-id="98b73-131">Roles</span></span>
-   <span data-ttu-id="98b73-132">Organisatie-eenheden</span><span class="sxs-lookup"><span data-stu-id="98b73-132">Organizational units</span></span>
-   <span data-ttu-id="98b73-133">Bedrijf voor resources</span><span class="sxs-lookup"><span data-stu-id="98b73-133">Resourcing company</span></span>
-   <span data-ttu-id="98b73-134">Resourcetypen</span><span class="sxs-lookup"><span data-stu-id="98b73-134">Resource types</span></span>
-   <span data-ttu-id="98b73-135">Geprefereerde resources</span><span class="sxs-lookup"><span data-stu-id="98b73-135">Preferred resources</span></span>
