---
title: Projecten en taken toewijzen aan een projectgebaseerde prijsopgaveregel
description: Dit onderwerp bevat informatie over het toewijzen van projecten en taken aan een projectgebaseerde taakregel.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272742"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="ad194-103">Projecten en taken toewijzen aan een projectgebaseerde prijsopgaveregel</span><span class="sxs-lookup"><span data-stu-id="ad194-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="ad194-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="ad194-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ad194-105">Op projectgebaseerde prijsopgaveregels kunt u de specifieke taken toewijzen van een project dat al aan een prijsopgaveregel is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="ad194-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="ad194-106">Wanneer u taken toewijst aan een prijsopgaveregel, zijn de volgende items die u op de prijsopgaveregel hebt gedefinieerd alleen van toepassing op die taken:</span><span class="sxs-lookup"><span data-stu-id="ad194-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="ad194-107">Factureringsmethode</span><span class="sxs-lookup"><span data-stu-id="ad194-107">Billing method</span></span>
- <span data-ttu-id="ad194-108">Opties voor toerekenbaarheid</span><span class="sxs-lookup"><span data-stu-id="ad194-108">Chargeability options</span></span>
- <span data-ttu-id="ad194-109">Niet-overschrijdingslimieten</span><span class="sxs-lookup"><span data-stu-id="ad194-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="ad194-110">Klanten</span><span class="sxs-lookup"><span data-stu-id="ad194-110">Customers</span></span>

<span data-ttu-id="ad194-111">U kunt bijvoorbeeld een project hebben waarbij de ene fase een vaste prijs heeft en voor alle andere fasen tijd en materiaal geldt.</span><span class="sxs-lookup"><span data-stu-id="ad194-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="ad194-112">In dit geval kunt u de eerste fase en alle onderliggende taken aan de prijsopgaveregel voor die fase koppelen met een factureringsmethode tegen een vaste prijs.</span><span class="sxs-lookup"><span data-stu-id="ad194-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="ad194-113">U kunt dan alle andere fasen aan de op tijd en materiaal gebaseerde prijsopgaveregel koppelen.</span><span class="sxs-lookup"><span data-stu-id="ad194-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="ad194-114">Taken koppelen aan projectgebaseerde prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="ad194-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="ad194-115">U kunt taken koppelen aan prijsopgaveregels van de volgende locaties:</span><span class="sxs-lookup"><span data-stu-id="ad194-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="ad194-116">Pagina **Project** > tabblad **Taakfacturering** (optimaal)</span><span class="sxs-lookup"><span data-stu-id="ad194-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="ad194-117">Pagina **Prijsopgaveregel** > tabblad **Toerekenbare taken**</span><span class="sxs-lookup"><span data-stu-id="ad194-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="ad194-118">Vanaf de pagina Project</span><span class="sxs-lookup"><span data-stu-id="ad194-118">From the Project page</span></span>

<span data-ttu-id="ad194-119">De pagina **Project** biedt de optimale voorzieningen voor het koppelen van taken aan offerteregels.</span><span class="sxs-lookup"><span data-stu-id="ad194-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="ad194-120">Gebruik deze pagina om meerdere taken te selecteren en ze allemaal, plus hun onderliggende taken, aan de geselecteerde prijsopgaveregel te koppelen.</span><span class="sxs-lookup"><span data-stu-id="ad194-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="ad194-121">Op het tabblad **Algemeen** van een projectgebaseerde prijsopgaveregel, controleert u of het veld **Project** is ingevuld.</span><span class="sxs-lookup"><span data-stu-id="ad194-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="ad194-122">Selecteer in het veld **Opgenomen taken** **Alleen geselecteerde taken**.</span><span class="sxs-lookup"><span data-stu-id="ad194-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="ad194-123">Sla de projectgebaseerde prijsopgaveregel op.</span><span class="sxs-lookup"><span data-stu-id="ad194-123">Save the project-based quote line.</span></span> <span data-ttu-id="ad194-124">Wanneer het formulier wordt vernieuwd, wordt het tabblad **Toerekenbare taken** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ad194-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="ad194-125">Selecteer op het tabblad **Algemeen** de koppeling voor het project in het veld **Project**.</span><span class="sxs-lookup"><span data-stu-id="ad194-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="ad194-126">Selecteer op de pagina **Project** het tabblad **Taakfacturering**.</span><span class="sxs-lookup"><span data-stu-id="ad194-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="ad194-127">Selecteer in het tweede raster, dat van toepassing is op taakspecifieke factureringsinstellingen, een of meer taken en selecteer vervolgens **Prijsopgaveregels koppelen**.</span><span class="sxs-lookup"><span data-stu-id="ad194-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="ad194-128">Selecteer in het dialoogvenster dat verschijnt een prijsopgaveregel die projectgebaseerde prijsopgaveregels in de prijsopgave weergeeft.</span><span class="sxs-lookup"><span data-stu-id="ad194-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="ad194-129">Geef in het veld **Factureringstype** aan of deze taken wel of niet toerekenbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="ad194-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="ad194-130">Schakel het selectievakje in om aan te geven of de koppeling onderliggende taken van de geselecteerde taken moet bevatten.</span><span class="sxs-lookup"><span data-stu-id="ad194-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="ad194-131">Als u het vakje selecteert, worden de onderliggende taken van de geselecteerde taken aan de prijsopgaveregel gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="ad194-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="ad194-132">Kies **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="ad194-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="ad194-133">Vanaf de pagina Prijsopgave</span><span class="sxs-lookup"><span data-stu-id="ad194-133">From the Quote line page</span></span>

<span data-ttu-id="ad194-134">U kunt projecttaken koppelen aan prijsopgaveregels uit het tabblad **Toerekenbare taken** op de pagina **Prijsopgaveregel**.</span><span class="sxs-lookup"><span data-stu-id="ad194-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="ad194-135">De optimale plaats om projecttaken aan prijsopgaveregels te koppelen is op het tabblad **Taakfacturering** op de pagina **Project**.</span><span class="sxs-lookup"><span data-stu-id="ad194-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="ad194-136">Als u taken uit het tabblad **Toerekenbare taken** op de pagina **Prijsopgaveregel** koppelt, moet u elk project handmatig koppelen.</span><span class="sxs-lookup"><span data-stu-id="ad194-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="ad194-137">Op het tabblad **Algemeen** van een projectgebaseerde prijsopgaveregel, controleert u of een project is geselecteerd in het veld **Project**.</span><span class="sxs-lookup"><span data-stu-id="ad194-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="ad194-138">Selecteer in het veld **Opgenomen taken** **Alleen geselecteerde taken**.</span><span class="sxs-lookup"><span data-stu-id="ad194-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="ad194-139">Sla de projectgebaseerde prijsopgaveregel op.</span><span class="sxs-lookup"><span data-stu-id="ad194-139">Save the project-based quote line.</span></span> <span data-ttu-id="ad194-140">Wanneer het formulier wordt vernieuwd, wordt het tabblad **Toerekenbare taken** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ad194-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="ad194-141">Op het tabblad **Toerekenbare taken** selecteert u **Een taak voor een prijsopgaveregel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ad194-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="ad194-142">Selecteer de taak op de pagina **Taak voor prijsopgaveregel** in het veld **Taken** en selecteer **Opslaan** in het veld **Factureringstype**.</span><span class="sxs-lookup"><span data-stu-id="ad194-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="ad194-143">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ad194-143">Close the page.</span></span> <span data-ttu-id="ad194-144">De geselecteerde taak wordt nu gekoppeld aan de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="ad194-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="ad194-145">Taken loskoppelen van projectgebaseerde prijsopgaveregels</span><span class="sxs-lookup"><span data-stu-id="ad194-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="ad194-146">Vanaf de pagina Project</span><span class="sxs-lookup"><span data-stu-id="ad194-146">From the Project page</span></span>

<span data-ttu-id="ad194-147">Deze methode biedt de optimale voorzieningen voor het loskoppelen van taken van offerteregels.</span><span class="sxs-lookup"><span data-stu-id="ad194-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="ad194-148">Gebruik deze pagina om meerdere taken te selecteren en ze allemaal, plus hun onderliggende taken, los te koppelen van de geselecteerde prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="ad194-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="ad194-149">Op het tabblad **Algemeen** van een projectgebaseerde prijsopgaveregel, selecteert u de projectkoppeling in het veld **Project**.</span><span class="sxs-lookup"><span data-stu-id="ad194-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="ad194-150">Selecteer op de pagina **Project** het tabblad **Taakfacturering**.</span><span class="sxs-lookup"><span data-stu-id="ad194-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="ad194-151">Selecteer in het tweede raster, dat van toepassing is op taakspecifieke factureringsinstellingen, een of meer taken en selecteer vervolgens **Prijsopgaveregels loskoppelen**.</span><span class="sxs-lookup"><span data-stu-id="ad194-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="ad194-152">Selecteer een prijsopgaveregel in het dialoogvenster dat verschijnt.</span><span class="sxs-lookup"><span data-stu-id="ad194-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="ad194-153">Schakel het selectievakje in om aan te geven of de koppeling ook moet worden verwijderd uit onderliggende taken van de geselecteerde taken.</span><span class="sxs-lookup"><span data-stu-id="ad194-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="ad194-154">Als u het vakje selecteert, worden ook de onderliggende taken van de geselecteerde taken losgekoppeld van de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="ad194-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="ad194-155">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad194-155">Select **OK**.</span></span> <span data-ttu-id="ad194-156">Een waarschuwingsbericht informeert u dat als u deze koppeling verwijdert, eventuele werkelijke waarden die eerder voor de taak zijn geregistreerd, kunnen worden teruggedraaid.</span><span class="sxs-lookup"><span data-stu-id="ad194-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="ad194-157">Selecteer **OK** om door te gaan en de koppeling tussen de taak en de projectgebaseerde prijsopgaveregel te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="ad194-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="ad194-158">Vanaf de pagina Prijsopgave</span><span class="sxs-lookup"><span data-stu-id="ad194-158">From the Quote line page</span></span>

<span data-ttu-id="ad194-159">U kunt projecttaken ook loskoppelen van prijsopgaveregels via het tabblad **Toerekenbare taken** op de pagina **Prijsopgaveregel**.</span><span class="sxs-lookup"><span data-stu-id="ad194-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="ad194-160">Op het tabblad **Toerekenbare taken** selecteert u **Een taak voor een prijsopgaveregel verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="ad194-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="ad194-161">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad194-161">Select **OK**.</span></span> <span data-ttu-id="ad194-162">Een waarschuwingsbericht informeert u dat als u deze koppeling verwijdert, eventuele werkelijke waarden die eerder voor de taak zijn geregistreerd, kunnen worden teruggedraaid.</span><span class="sxs-lookup"><span data-stu-id="ad194-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="ad194-163">Selecteer **OK** om door te gaan en de koppeling tussen de taak en de projectgebaseerde prijsopgaveregel te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="ad194-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="ad194-164">Met deze procedure verwijdert u de taak niet uit het project.</span><span class="sxs-lookup"><span data-stu-id="ad194-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="ad194-165">U verwijdert alleen de taakkoppeling van de projectgebaseerde prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="ad194-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]