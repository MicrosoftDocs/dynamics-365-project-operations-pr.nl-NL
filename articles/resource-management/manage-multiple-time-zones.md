---
title: Tijdzones beheren
description: Wanneer een project wordt gemaakt, is de tijdzone ervan gebaseerd op de tijdzone die is gedefinieerd in de toegepaste werkurensjabloon.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074502"
---
# <a name="manage-time-zones"></a><span data-ttu-id="ed26f-103">Tijdzones beheren</span><span class="sxs-lookup"><span data-stu-id="ed26f-103">Manage time zones</span></span>

<span data-ttu-id="ed26f-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="ed26f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="ed26f-105">Projecten</span><span class="sxs-lookup"><span data-stu-id="ed26f-105">Projects</span></span>

<span data-ttu-id="ed26f-106">Wanneer een project wordt gemaakt, is de tijdzone gebaseerd op de tijdzone die is gedefinieerd in de toegepaste werkurensjabloon.</span><span class="sxs-lookup"><span data-stu-id="ed26f-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="ed26f-107">In het **Project** zijn de datums altijd relatief ten opzichte van de tijdzone van de gebruiker die is aangemeld op elk tabblad, behalve het tabblad **Taak**. Wanneer u de structuur voor werkspecificatie bekijkt, worden de datums altijd weergegeven in de tijdzone van het project.</span><span class="sxs-lookup"><span data-stu-id="ed26f-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="ed26f-108">Opdrachten</span><span class="sxs-lookup"><span data-stu-id="ed26f-108">Tasks</span></span>

<span data-ttu-id="ed26f-109">Wanneer een taak wordt gemaakt, worden de starttijd, eindtijd en uren/dag bepaald door de werkuren van het project.</span><span class="sxs-lookup"><span data-stu-id="ed26f-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="ed26f-110">Als een taak bijvoorbeeld is gemaakt met een project met tijdzone -8 PST en de volgende werkuren: 9:00 uur tot 17:00 uur van maandag tot vrijdag, zal elke taak die zonder toewijzing wordt gemaakt, de starttijd en eindtijd van de projectkalender respecteren.</span><span class="sxs-lookup"><span data-stu-id="ed26f-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="ed26f-111">Resources beheren met tijdzones</span><span class="sxs-lookup"><span data-stu-id="ed26f-111">Manage resources with time zones</span></span>

<span data-ttu-id="ed26f-112">Voor nauwkeurige en voorspelbare resultaten bij gebruik van **Boeking uitbreiden** , zijn er twee belangrijke voorwaarden waaraan moet worden voldaan:</span><span class="sxs-lookup"><span data-stu-id="ed26f-112">For accurate and predictable results when using **Extend Booking** , there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="ed26f-113">De gebruiker moet de tijdzone van zijn apparaat configureren zodat deze overeenkomt met de tijdzone die is gedefinieerd in **Persoonlijke instellingen** van het systeem.</span><span class="sxs-lookup"><span data-stu-id="ed26f-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Tijdzone-instellingen in Windows 10](media/reconcile-assignments-03.png)

  ![Tijdzone-instellingen in Persoonlijke instellingen](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="ed26f-116">De boekbare resource moet ten minste één minuut werktijd hebben die overlapt met de contouren waarmee de aangevraagde uitbreiding wordt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="ed26f-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="ed26f-117">Bijvoorbeeld de volgende resources met werktijden die vallen tussen 9.00 en 19.00 uur.</span><span class="sxs-lookup"><span data-stu-id="ed26f-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Vergelijking van resourcecontouren](media/reconcile-assignments-05.png)

<span data-ttu-id="ed26f-119">In de onderstaande tabel ziet u het volgende:</span><span class="sxs-lookup"><span data-stu-id="ed26f-119">The following table shows:</span></span>

- <span data-ttu-id="ed26f-120">Een sjabloon van een projectagenda</span><span class="sxs-lookup"><span data-stu-id="ed26f-120">A project calendar template</span></span>
- <span data-ttu-id="ed26f-121">Resource A: Deze resource heeft dezelfde agenda en bevindt zich in dezelfde tijdzone als het project.</span><span class="sxs-lookup"><span data-stu-id="ed26f-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="ed26f-122">De starttijd van de boekingen is 09.00 uur.</span><span class="sxs-lookup"><span data-stu-id="ed26f-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="ed26f-123">Resource B: deze resource bevindt zich in een andere tijdzone dan het project en begint om 7:00 uur in zijn tijdzone.</span><span class="sxs-lookup"><span data-stu-id="ed26f-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="ed26f-124">De boekingen beginnen echter om 09:00 uur, omdat dit de vroegste starttijd van de toewijzingscontour is.</span><span class="sxs-lookup"><span data-stu-id="ed26f-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="ed26f-125">Resources C en D: de resources bevinden zich in verschillende tijdzones, beide verschillend van elkaar en van het project, en hun boekingen beginnen niet eerder dan hun respectievelijke beschikbare starttijden.</span><span class="sxs-lookup"><span data-stu-id="ed26f-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="ed26f-126">Entiteit</span><span class="sxs-lookup"><span data-stu-id="ed26f-126">Entity</span></span>  |<span data-ttu-id="ed26f-127">Agenda</span><span class="sxs-lookup"><span data-stu-id="ed26f-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="ed26f-128">Sjabloon van projectagenda</span><span class="sxs-lookup"><span data-stu-id="ed26f-128">Project calendar template</span></span>   | ![projectagenda](media/reconcile-assignments-06.png) |
|<span data-ttu-id="ed26f-130">Resource A</span><span class="sxs-lookup"><span data-stu-id="ed26f-130">Resource A</span></span>  | ![Agenda van resource A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="ed26f-132">Resource B</span><span class="sxs-lookup"><span data-stu-id="ed26f-132">Resource B</span></span>  |  ![Agenda van resource B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="ed26f-134">Resource C</span><span class="sxs-lookup"><span data-stu-id="ed26f-134">Resource C</span></span>  |  ![Agenda van resource C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="ed26f-136">Resource D</span><span class="sxs-lookup"><span data-stu-id="ed26f-136">Resource D</span></span>  | ![Agenda van resource D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="ed26f-138">In de weergave **Afstemming** worden de resourcetoewijzingen en de bijbehorende boekingstekorten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ed26f-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Afstemmingsweergave vóór uitbreiding](media/reconcile-assignments-10.png)

<span data-ttu-id="ed26f-140">Nadat de functie voor het uitbreiden van boekingen is gebruikt voor elke resource, worden boekingen verlengd voor elke resource omdat de werkuren van elke resource de contouren van het tekort overlappen.</span><span class="sxs-lookup"><span data-stu-id="ed26f-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Afstemmingsweergave na uitbreiding van de boeking](media/reconcile-assignments-11.png) 

<span data-ttu-id="ed26f-142">Merk op dat de details van de boekingen verschillen laten zien in de starttijd van de boekingen.</span><span class="sxs-lookup"><span data-stu-id="ed26f-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="ed26f-143">De boekingen starten niet eerder dan de starttijd van de toewijzingscontour en niet eerder dan de beschikbare starttijd van de resource.</span><span class="sxs-lookup"><span data-stu-id="ed26f-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Nieuwe boekingen van de resources in het planbord](media/reconcile-assignments-12.png)
