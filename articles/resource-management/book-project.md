---
title: Boeken voor een project
description: Dit onderwerp bevat informatie over hoe u een resources voor een project boekt.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908041"
---
# <a name="book-to-a-project"></a><span data-ttu-id="b3e37-103">Boeken voor een project</span><span class="sxs-lookup"><span data-stu-id="b3e37-103">Book to a project</span></span>

<span data-ttu-id="b3e37-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="b3e37-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b3e37-105">Er zijn momenten waarop een projectmanager of resourcemanager een resource aan een project moet toewijzen zonder dat een specifieke vereiste wordt gedefinieerd voor algemeen teamleden.</span><span class="sxs-lookup"><span data-stu-id="b3e37-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="b3e37-106">Dit kan op een van drie manieren worden bereikt.</span><span class="sxs-lookup"><span data-stu-id="b3e37-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="b3e37-107">Boeken vanuit het raster voor teamleden</span><span class="sxs-lookup"><span data-stu-id="b3e37-107">Book from the team member grid</span></span>
- <span data-ttu-id="b3e37-108">Boeken vanaf het planbord</span><span class="sxs-lookup"><span data-stu-id="b3e37-108">Book from the schedule board</span></span>
- <span data-ttu-id="b3e37-109">Boeken vanuit het formulier **Project**</span><span class="sxs-lookup"><span data-stu-id="b3e37-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="b3e37-110">Boeken vanuit het raster voor teamleden</span><span class="sxs-lookup"><span data-stu-id="b3e37-110">Book from the team member grid</span></span>

<span data-ttu-id="b3e37-111">Als uw organisatie in de hybride modus voor de toewijzing van resources werkt, kan de projectmanager een resource rechtstreeks naar het project boeken door de volgende stappen uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b3e37-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="b3e37-112">Ga vanuit het project naar het raster voor teamleden en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="b3e37-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="b3e37-113">Geef de positienaam en de rol van de resource op.</span><span class="sxs-lookup"><span data-stu-id="b3e37-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="b3e37-114">Selecteer de boekbare resource in de beschikbare zoekopdracht.</span><span class="sxs-lookup"><span data-stu-id="b3e37-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="b3e37-115">Wanneer u de resource hebt geselecteerd, geeft u de volgende veldgegevens op om de resource te boeken:</span><span class="sxs-lookup"><span data-stu-id="b3e37-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="b3e37-116">Begindatum</span><span class="sxs-lookup"><span data-stu-id="b3e37-116">Start date</span></span>
    - <span data-ttu-id="b3e37-117">Einddatum</span><span class="sxs-lookup"><span data-stu-id="b3e37-117">Finish date</span></span>
    - <span data-ttu-id="b3e37-118">Toewijzingsmethode</span><span class="sxs-lookup"><span data-stu-id="b3e37-118">Allocation method</span></span>
    - <span data-ttu-id="b3e37-119">Uren, indien van toepassing</span><span class="sxs-lookup"><span data-stu-id="b3e37-119">Hours, if applicable</span></span>
    - <span data-ttu-id="b3e37-120">Projectfiatteur</span><span class="sxs-lookup"><span data-stu-id="b3e37-120">Project approver</span></span>

6. <span data-ttu-id="b3e37-121">**Opslaan en sluiten** selecteren</span><span class="sxs-lookup"><span data-stu-id="b3e37-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="b3e37-122">Boeken vanaf het planbord</span><span class="sxs-lookup"><span data-stu-id="b3e37-122">Book from the schedule board</span></span>

<span data-ttu-id="b3e37-123">Wanneer een resourcemanager een resource rechtstreeks naar een project moet boeken, kan hij/zij het planbord en de projectvereiste gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b3e37-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="b3e37-124">De projectvereiste is een resourcevereiste die altijd kan worden gebruikt voor boekingen.</span><span class="sxs-lookup"><span data-stu-id="b3e37-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="b3e37-125">Voer de volgende stappen uit om rechtstreeks van het planbord naar een project te boeken.</span><span class="sxs-lookup"><span data-stu-id="b3e37-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="b3e37-126">Navigeer naar het planbord en filter op de linkerpagina op de resources die u overweegt voor de vereiste.</span><span class="sxs-lookup"><span data-stu-id="b3e37-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="b3e37-127">Selecteer in het onderste deelvenster het tabblad **Project** om een lijst met projectvereisten te bekijken.</span><span class="sxs-lookup"><span data-stu-id="b3e37-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="b3e37-128">Sleep de vereiste naar een resource en definieer de volgende gegevens:</span><span class="sxs-lookup"><span data-stu-id="b3e37-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="b3e37-129">Begindatum</span><span class="sxs-lookup"><span data-stu-id="b3e37-129">Start date</span></span>
    - <span data-ttu-id="b3e37-130">Einddatum</span><span class="sxs-lookup"><span data-stu-id="b3e37-130">Finish date</span></span>
    - <span data-ttu-id="b3e37-131">Boekingsstatus</span><span class="sxs-lookup"><span data-stu-id="b3e37-131">Booking status</span></span>
    - <span data-ttu-id="b3e37-132">Boekingsmethode</span><span class="sxs-lookup"><span data-stu-id="b3e37-132">Booking method</span></span>
    - <span data-ttu-id="b3e37-133">Duur</span><span class="sxs-lookup"><span data-stu-id="b3e37-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="b3e37-134">Boeken vanuit het formulier Project</span><span class="sxs-lookup"><span data-stu-id="b3e37-134">Book from the Project form</span></span>

<span data-ttu-id="b3e37-135">Als projectmanager moet u mogelijk een resource naar een project boeken, maar kent u alleen de criteria in plaats van de naam van de resource.</span><span class="sxs-lookup"><span data-stu-id="b3e37-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="b3e37-136">Voer de volgende stappen uit om de planningsassistent te gebruiken om een resource te vinden op basis van de beschikbare attributen van de resource.</span><span class="sxs-lookup"><span data-stu-id="b3e37-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="b3e37-137">Navigeer naar het project en selecteer **Boeken** om de planningsassistent te openen.</span><span class="sxs-lookup"><span data-stu-id="b3e37-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="b3e37-138">Gebruik de filters aan de linkerkant van de planningsassistent om de criteria te verfijnen en selecteer **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="b3e37-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="b3e37-139">Op basis van de resources die in de resultaten worden geretourneerd, kunt u een resource boeken.</span><span class="sxs-lookup"><span data-stu-id="b3e37-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="b3e37-140">Met deze methode maakt u geen boekingen voor de resource.</span><span class="sxs-lookup"><span data-stu-id="b3e37-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="b3e37-141">In plaats daarvan wordt de resource toegevoegd aan het team.</span><span class="sxs-lookup"><span data-stu-id="b3e37-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="b3e37-142">Nadat het teamlid aan het project is toegevoegd, kan de projectmanager de opties voor boekingen onderhouden en verlengen gebruiken om de vereiste boekingen aan de resource toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b3e37-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
