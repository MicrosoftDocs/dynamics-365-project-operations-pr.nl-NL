---
title: Benoemde, boekbare resources boeken voor een projectteam en taken toewijzen
description: Dit onderwerp bevat informatie over hoe u benoemde resources voor projectteams kunt boeken en hen aan taken kunt toewijzen.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: d8a49b6ae8423cb99c710e40704475b4a71d3724
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145352"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="896ed-103">Benoemde, boekbare resources boeken voor een projectteam en taken toewijzen</span><span class="sxs-lookup"><span data-stu-id="896ed-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="896ed-104">U kunt een benoemde resource toevoegen aan uw projectteam door ze rechtstreeks voor het team te boeken.</span><span class="sxs-lookup"><span data-stu-id="896ed-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="896ed-105">U doet dit via de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="896ed-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="896ed-106">Ga in Project Service Automation naar **Projecten** en open het project waarvoor u boekt.</span><span class="sxs-lookup"><span data-stu-id="896ed-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="896ed-107">Klik op de pagina **Project** op het tabblad **Team** op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="896ed-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Een teamlid toevoegen via het tabblad Team](media/RM-how-to-1.png)

3. <span data-ttu-id="896ed-109">Selecteer de boekbare resource in het dialoogvenster **Snelle invoer: Projectteamlid**.</span><span class="sxs-lookup"><span data-stu-id="896ed-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="896ed-110">Het veld **Rol** wordt gevuld met de standaardrol van de resource, indien toegewezen.</span><span class="sxs-lookup"><span data-stu-id="896ed-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="896ed-111">Indien nodig kunt u de rol wijzigen.</span><span class="sxs-lookup"><span data-stu-id="896ed-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="896ed-112">Selecteer de begin- en einddatums voor de periode waarvoor de resource nodig is en selecteer de toewijzingsmethode van de capaciteit van de resource.</span><span class="sxs-lookup"><span data-stu-id="896ed-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="896ed-113">Als u wilt dat het teamlid een projectfiatteur is, selecteert u **Ja** in het veld **Projectfiatteur**.</span><span class="sxs-lookup"><span data-stu-id="896ed-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="896ed-114">Dit betekent dat het teamlid ingediende tijd- en onkostenposten voor dit project kan goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="896ed-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="896ed-115">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="896ed-115">Click **Save**.</span></span>

![Een teamlid toevoegen in het formulier voor snelle invoer](media/RM-how-to-2.png)


<span data-ttu-id="896ed-117">U kunt de geboekte resource nu toewijzen aan taken in het project.</span><span class="sxs-lookup"><span data-stu-id="896ed-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="896ed-118">Klik op de pagina **Project** op het tabblad **Planning** om taken aan de nieuwe resource toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="896ed-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="896ed-119">De resourcekiezer die wordt gestart vanuit het veld **Resources** in het taakraster bevat de teamleden die u kunt selecteren.</span><span class="sxs-lookup"><span data-stu-id="896ed-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Een teamlid toewijzen aan een taak op het tabblad Planning](media/RM-how-to-3.png)

<span data-ttu-id="896ed-121">In versie 3 voor Project Service Automation (PSA) zijn resourceboekingen en taaktoewijzingen niet nauw gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="896ed-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="896ed-122">Dit betekent dat u taken aan teamleden kunt toewijzen voor meer uren dan hun boekingen dekken in het project wanneer u de resourcekiezer in de planning gebruikt.</span><span class="sxs-lookup"><span data-stu-id="896ed-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="896ed-123">U kunt de verschillen tussen boekingen en toewijzingen voor teamleden op het tabblad **Team** of op het tabblad **Resourceafstemming** bekijken. U kunt ook de verschillen tussen boekingen en toewijzingen voor resources op een meer gedetailleerd niveau afstemmen.</span><span class="sxs-lookup"><span data-stu-id="896ed-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Het tabblad Afstemming van resources](media/RM-how-to-4.png)

<span data-ttu-id="896ed-125">U ook de resourcekiezer op het tabblad **Planning** gebruiken om boekbare resources te zoeken en te selecteren die nog geen deel uitmaken van het projectteam.</span><span class="sxs-lookup"><span data-stu-id="896ed-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="896ed-126">Deze worden weergegeven in de resourcekiezer als **Andere resources**.</span><span class="sxs-lookup"><span data-stu-id="896ed-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Een niet-teamlidresource toewijzen aan een taak](media/RM-how-to-5.png)

<span data-ttu-id="896ed-128">Wanneer u dit doet, wordt de resource toegevoegd aan het projectteam en toegewezen aan de taak, maar er worden geen boekingen gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="896ed-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Teamlid met toewijzingen en geen boekingen](media/RM-how-to-6.png)

<span data-ttu-id="896ed-130">U kunt de functie voor uitgebreid boeken van het tabblad **Afstemming** of het **planbord** gebruiken om de capaciteit van de resource voor het project te boeken.</span><span class="sxs-lookup"><span data-stu-id="896ed-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Boekingen voor een teamlid uitbreiden op het tabblad Afstemming van resources](media/RM-how-to-7.png)

<span data-ttu-id="896ed-132">Nadat een teamlid is geboekt voor uw project, kunt u Boekingen bijhouden of het planbord rechtstreeks gebruiken om hun boekingen te beheren.</span><span class="sxs-lookup"><span data-stu-id="896ed-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
