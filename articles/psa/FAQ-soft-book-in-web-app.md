---
title: Hoe kan ik resources 'zacht boeken' in appversie 2.x?
description: In dit artikel wordt beschreven hoe u leden van een projectteam zacht boekt met Project Service.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6bd13c448f4ce16fb93843df54f26cdd9bb884f4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146477"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="dc7f3-103">Hoe kan ik resources 'zacht boeken' in de webapp (Project Service-app v2.x)?</span><span class="sxs-lookup"><span data-stu-id="dc7f3-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="dc7f3-104">U kunt een resource voorlopig plannen of 'zacht boeken' voor een projectteam om te laten zien dat u van plan bent om de resource aan een project toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="dc7f3-105">Zachte boekingen verbruiken de beschikbare capaciteit van een resource niet.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="dc7f3-106">Zacht geboekte teamleden kunnen niet aan projecttaken worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="dc7f3-107">Alleen resources met de status Hard geboekt en het toewijzingstype Vastgelegd kunnen aan taken worden toegewezen (ervan uitgaand dat ze voldoende hard te boeken uren hebben voor de betreffende toewijzing).</span><span class="sxs-lookup"><span data-stu-id="dc7f3-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="dc7f3-108">Zacht geboekte projectteamleden worden in het raster Teamlid weergegeven met hun zacht geboekte uren in de kolom Zacht boeken.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="dc7f3-109">Ze worden ook weergegeven op het planbord.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-109">They also show up on the schedule board.</span></span> <span data-ttu-id="dc7f3-110">Zoals aangegeven verbruiken zachte boekingen geen capaciteit.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="dc7f3-111">U kunt een teamlid op drie manieren zacht boeken voor een project met Project Service-versie 2.x.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="dc7f3-112">U kunt zacht boeken via het planbord, de functie Boekingen bijhouden gebruiken of een algemene resource maken.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="dc7f3-113">Deze methoden worden hieronder beschreven.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="dc7f3-114">Zacht boeken via het planbord</span><span class="sxs-lookup"><span data-stu-id="dc7f3-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="dc7f3-115">Ga als volgt te werk om zacht te boeken via het planbord:</span><span class="sxs-lookup"><span data-stu-id="dc7f3-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="dc7f3-116">Open het planbord.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-116">Open the schedule board.</span></span>
2. <span data-ttu-id="dc7f3-117">Selecteer het tabblad Project in het onderste deelvenster Boekingsvereisten van het planbord.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="dc7f3-118">Zoek het project waarvoor u een resource zacht wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="dc7f3-119">Als u veel projecten hebt, klikt u op de kolomkop Project en gebruikt u vervolgens het filter om het project te zoeken.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="dc7f3-120">Klik op het project en sleep het naar het tijdraster van de resource.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="dc7f3-121">Het deelvenster Resourceboeking maken wordt rechts geopend.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="dc7f3-122">Pas de begin- en einddatum aan, selecteer de boekingsstatus Zacht en stel de uren in.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="dc7f3-123">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-123">Click Book.</span></span>
7. <span data-ttu-id="dc7f3-124">In het project wordt de resource nu als teamlid met de zacht geboekte uren weergegeven in de kolom Zacht boeken.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="dc7f3-125">U kunt deze resources niet toewijzen aan taken in de structuur voor werkspecificatie omdat alleen hard geboekte resources in het team kunnen worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="dc7f3-126">Zacht boeken via de functie Boekingen bijhouden</span><span class="sxs-lookup"><span data-stu-id="dc7f3-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="dc7f3-127">Ga als volgt te werk om zacht te boeken via Boekingen bijhouden:</span><span class="sxs-lookup"><span data-stu-id="dc7f3-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="dc7f3-128">Klik op Nieuw in het raster voor teamleden.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="dc7f3-129">Selecteer de te boeken resource, functie en datums.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="dc7f3-130">Selecteer een andere toewijzingsmethode dan Geen:</span><span class="sxs-lookup"><span data-stu-id="dc7f3-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="dc7f3-131">Volledige capaciteit</span><span class="sxs-lookup"><span data-stu-id="dc7f3-131">Full Capacity</span></span>
- <span data-ttu-id="dc7f3-132">Percentagecapaciteit</span><span class="sxs-lookup"><span data-stu-id="dc7f3-132">Percentage Capacity</span></span>
- <span data-ttu-id="dc7f3-133">Uren gelijkmatig verdelen</span><span class="sxs-lookup"><span data-stu-id="dc7f3-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="dc7f3-134">Uren vooraf laden</span><span class="sxs-lookup"><span data-stu-id="dc7f3-134">By Hours Front Load</span></span>
4. <span data-ttu-id="dc7f3-135">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-135">Click Save.</span></span> <span data-ttu-id="dc7f3-136">De resource in het teamraster en de uren worden weergegeven als hard geboekt.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="dc7f3-137">Houd de boekingen van de resource bij door te klikken op Boekingen bijhouden.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="dc7f3-138">Wanneer het planbord wordt geopend, vouwt u de resource uit om de boekingen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="dc7f3-139">De boeking wordt aangeduid als hard geboekt.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="dc7f3-140">Klik met de rechtermuisknop op de boeking en selecteer onder Status wijzigen de optie Zacht boeken en vervolgens Zacht.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="dc7f3-141">De boekingsstatus is nu Zacht.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="dc7f3-142">Wanneer u het planbord sluit, ziet u dat de uren voor de resource van Hard in Zacht zijn gewijzigd in het raster van het teamlid.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="dc7f3-143">Als u een resource hard boekt voor het team, vervolgens taken aan deze resource toewijst in de structuur van de werkspecificatie en ten slotte Boekingen onderhouden gebruikt om de status van Hard in Zacht te wijzigen, worden de toewijzingen voor die resource verwijderd, aangezien alleen hard geboekte resources aan taken kunnen worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="dc7f3-144">Zacht boeken door een algemene resource te maken</span><span class="sxs-lookup"><span data-stu-id="dc7f3-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="dc7f3-145">U kunt een zachte boeking maken door een algemeen resourceteamlid te maken, te voldoen aan een planbord- of resourceaanvraag en het type te wijzigen tijdens het boeken.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="dc7f3-146">Ga hiervoor als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="dc7f3-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="dc7f3-147">Wijs in de structuur voor werkspecificatie rollen toe aan de taken waarvoor u algemene teamleden wilt genereren.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="dc7f3-148">Klik op Projectteam genereren.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="dc7f3-149">Selecteer de algemene resource in het raster van het projectteamlid en klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="dc7f3-150">Selecteer de resource die u wilt boeken op het planbord.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="dc7f3-151">Wijzig de boekingsstatus in Zacht in het deelvenster Resourceboeking maken van het planbord.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="dc7f3-152">Klik op Boeken of Boeken en Afsluiten.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="dc7f3-153">Nadat u het planbord hebt gesloten, wordt de geselecteerde resource aan het team toegevoegd met zacht geboekte uren en toegewezen uren.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="dc7f3-154">Daarnaast blijft de algemene resource deel uitmaken van het team als indicatie dat de taken zijn toegewezen aan een zacht geboekt teamlid.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="dc7f3-155">Ga als volgt te werk wanneer u een zacht geboekte teamlidresource in een hard geboekt teamlid wilt wijzigen zodat u taken aan hem of haar kunt toewijzen:</span><span class="sxs-lookup"><span data-stu-id="dc7f3-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="dc7f3-156">Selecteer de resource en klik op Boekingen bijhouden.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="dc7f3-157">Wanneer het planbord wordt geopend, vouwt u de resource uit om de boekingen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="dc7f3-158">De boeking wordt gemarkeerd als Zacht.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="dc7f3-159">Klik met de rechtermuisknop op de boeking en selecteer onder Status wijzigen de optie Hard boeken en vervolgens Hard.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="dc7f3-160">De boekingsstatus is nu Hard.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="dc7f3-161">Wanneer u het planbord sluit, ziet u dat de uren voor de resource van Zacht in Hard zijn gewijzigd in het raster van het teamlid.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="dc7f3-162">U kunt de resource nu aan taken toewijzen (als de hard geboekte uren en de inspanningsuren van de taak voor toewijzing overeenkomen).</span><span class="sxs-lookup"><span data-stu-id="dc7f3-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="dc7f3-163">Als u de stappen in procedure 3 hierboven hebt uitgevoerd en de status van de zacht geboekte boekbare resource in hard wijzigt, wordt het algemene teamlid verwijderd uit het team.</span><span class="sxs-lookup"><span data-stu-id="dc7f3-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>
