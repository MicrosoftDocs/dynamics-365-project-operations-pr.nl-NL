---
title: Projectinstellingen
description: In dit onderwerp krijgt u informatie over instellingen voor projectbeheer.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074727"
---
# <a name="project-settings"></a><span data-ttu-id="85b9d-103">Projectinstellingen</span><span class="sxs-lookup"><span data-stu-id="85b9d-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="85b9d-104">Gebruik de volgende instellingen voor toegang tot de functies voor projectplanning.</span><span class="sxs-lookup"><span data-stu-id="85b9d-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="85b9d-105">Werksjabloon</span><span class="sxs-lookup"><span data-stu-id="85b9d-105">Work template</span></span>

<span data-ttu-id="85b9d-106">Als u een projectplanning wilt maken, maakt u een sjabloon voor een projectagenda waarin het aantal werkuren per dag en eventuele sluitingsdagen van het bedrijf worden aangegeven.</span><span class="sxs-lookup"><span data-stu-id="85b9d-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="85b9d-107">Als u een sjabloon voor een projectagenda wilt maken, koppelt u een werksjabloon aan het veld **Agendasjabloon** voor het project.</span><span class="sxs-lookup"><span data-stu-id="85b9d-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="85b9d-108">Voer deze stappen uit om een werksjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="85b9d-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="85b9d-109">Klik in PSA in het linkernavigatiedeelvenster op **Resources**.</span><span class="sxs-lookup"><span data-stu-id="85b9d-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="85b9d-110">Open op de lijstpagina **Resources** een gebruikersrecord en selecteer vervolgens **Werkuren weergeven**.</span><span class="sxs-lookup"><span data-stu-id="85b9d-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="85b9d-111">Zorg ervoor dat u pop-ups op de browserpagina toestaat.</span><span class="sxs-lookup"><span data-stu-id="85b9d-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="85b9d-112">Op deze manier kunt u de werkuren zien die voor de resource zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="85b9d-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="85b9d-113">Klik op het tabblad **Maandweergave** op **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="85b9d-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="85b9d-114">Er wordt een lijst met drie opties weergegeven:</span><span class="sxs-lookup"><span data-stu-id="85b9d-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="85b9d-115">Nieuwe weekplanning</span><span class="sxs-lookup"><span data-stu-id="85b9d-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="85b9d-116">Werkplanning voor één dag</span><span class="sxs-lookup"><span data-stu-id="85b9d-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="85b9d-117">Vrije tijd</span><span class="sxs-lookup"><span data-stu-id="85b9d-117">Time Off</span></span>

> ![Instellingsopties](media/project-13.png)

4. <span data-ttu-id="85b9d-119">Selecteer **Nieuwe weekplanning** en stel vervolgens de opties voor deze resourceplanning in.</span><span class="sxs-lookup"><span data-stu-id="85b9d-119">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="85b9d-120">U kunt een terugkerende weekplanning, parameters voor dagelijkse uren, sluitingsdagen van het bedrijf en meer instellen.</span><span class="sxs-lookup"><span data-stu-id="85b9d-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="85b9d-121">Stel het datumbereik in, selecteer **Opslaan** en klik vervolgens op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="85b9d-121">Set the date range, select **Save** , and then click **Close**.</span></span> 
6. <span data-ttu-id="85b9d-122">Ga terug naar de lijstpagina **Resources** en selecteer de resource waarvoor u de werkuren wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="85b9d-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="85b9d-123">Selecteer **Agenda instellen als** om de werksjabloon in te stellen.</span><span class="sxs-lookup"><span data-stu-id="85b9d-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="85b9d-124">Voer in het dialoogvenster **Werksjabloon** een naam voor de werksjabloon in en selecteer **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="85b9d-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="85b9d-125">U kunt nu de werksjabloon aan een sjabloon voor een projectagenda koppelen.</span><span class="sxs-lookup"><span data-stu-id="85b9d-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="85b9d-126">Resourcerollen</span><span class="sxs-lookup"><span data-stu-id="85b9d-126">Resource roles</span></span>

<span data-ttu-id="85b9d-127">De term *resourerol* verwijst naar de reeks vaardigheden, competenties en certificeringen die een persoon moet hebben om een specifieke reeks taken voor een project te kunnen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="85b9d-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="85b9d-128">In PSA kunt u de kosten en factuurtarieven van de tijd van een resource bepalen op basis van de rol waaraan de resource is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="85b9d-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="85b9d-129">Elke organisatie moet deze rollen instellen met behulp van de linkernavigatiebalk in het menu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="85b9d-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="85b9d-130">Elke organisatie moet deze rollen instellen op de pagina **Actieve resourcecategorieën**.</span><span class="sxs-lookup"><span data-stu-id="85b9d-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="85b9d-131">Als u deze pagina wilt openen, selecteert u in het linkernavigatiedeelvenster de optie **Resourcerollen**.</span><span class="sxs-lookup"><span data-stu-id="85b9d-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="85b9d-132">Prijslijsten</span><span class="sxs-lookup"><span data-stu-id="85b9d-132">Price lists</span></span>

<span data-ttu-id="85b9d-133">Met prijslijsten kunt u kosten en verkoopprijzen voor resourcerollen, onkostencategorieën, producten en andere elementen in een organisatie instellen.</span><span class="sxs-lookup"><span data-stu-id="85b9d-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="85b9d-134">Voordat u financiële schattingen instelt voor het werk dat voor een project moet worden geleverd, moet u een achterliggende lijst met kosten en een verkoopprijzen maken.</span><span class="sxs-lookup"><span data-stu-id="85b9d-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="85b9d-135">In de parametersectie moet u ook een standaardlijst met kosten en verkoopprijzen instellen die van toepassing is op alle projecten die in de organisatie worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="85b9d-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="85b9d-136">Zorg ervoor dat u op de pagina **Actieve projectparameters** een standaardlijst met kosten en verkoopprijzen instelt.</span><span class="sxs-lookup"><span data-stu-id="85b9d-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
