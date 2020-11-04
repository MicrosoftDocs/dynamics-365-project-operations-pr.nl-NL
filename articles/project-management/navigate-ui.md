---
title: Navigeren door de gebruikersinterface
description: Dit onderwerp biedt informatie over projectmanagement in Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ff624a13ec88ae64dba18715fbe9b94353b070e8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074482"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="30560-103">Navigeren door de gebruikersinterface</span><span class="sxs-lookup"><span data-stu-id="30560-103">Navigating the user interface</span></span>

<span data-ttu-id="30560-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="30560-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="30560-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="30560-105">Overview</span></span>

<span data-ttu-id="30560-106">Het hoofdprojectformulier is onderverdeeld in verschillende tabbladen.</span><span class="sxs-lookup"><span data-stu-id="30560-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="30560-107">Elk tabblad vertegenwoordigt een ander detailniveau binnen het project.</span><span class="sxs-lookup"><span data-stu-id="30560-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="30560-108">**Overzicht** : geeft een beschrijving van het project en voegt zowel de geplande als de werkelijke projectprestaties samen.</span><span class="sxs-lookup"><span data-stu-id="30560-108">**Summary** : Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Overzichtstabblad en velden](media/navigation7.png)

- <span data-ttu-id="30560-110">**Taken** : bevat de details over de structuur voor werkspecificatie die wordt weergegeven door een rasterweergave, bordweergave en een ganttdiagram.</span><span class="sxs-lookup"><span data-stu-id="30560-110">**Tasks** : Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Taaktabblad en velden](media/navigation8.png)

- <span data-ttu-id="30560-112">**Team** : geeft details over de projectdeelnemers.</span><span class="sxs-lookup"><span data-stu-id="30560-112">**Team** : Provides details regarding the project participants.</span></span> <span data-ttu-id="30560-113">De toegewezen inspanning van elk teamlid wordt ook in deze weergave samengevat.</span><span class="sxs-lookup"><span data-stu-id="30560-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Teamtabblad en velden](media/navigation9.png)

- <span data-ttu-id="30560-115">**Resourcetoewijzingen** : bevat een gefaseerd overzicht van de inspanning voor elke resource in een project.</span><span class="sxs-lookup"><span data-stu-id="30560-115">**Resource assignments** : Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Het tabblad Resourcetoewijzingen en velden](media/navigation10.png)

- <span data-ttu-id="30560-117">**Afstemming van resources** : biedt een tijdgefaseerd overzicht van de verschillen tussen de toewijzingen van elke genoemde resource en hun boekingen.</span><span class="sxs-lookup"><span data-stu-id="30560-117">**Resource reconciliation** : Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Het tabblad Afstemming van resources en velden](media/navigation11.png)

- <span data-ttu-id="30560-119">**Schattingen** : biedt een gefaseerd overzicht van de kosten en verkoopramingen van een project.</span><span class="sxs-lookup"><span data-stu-id="30560-119">**Estimates** : Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Tabblad Schattingen en velden](media/navigation12.png)

- <span data-ttu-id="30560-121">**Volgen** : bevat een weergave met de voortgang van taken in de structuur voor werkspecificatie voor inspanning, kosten en verkoop.</span><span class="sxs-lookup"><span data-stu-id="30560-121">**Tracking** : Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Tabblad Volgen en velden](media/navigation13.png)

- <span data-ttu-id="30560-123">**Verkoop** : bevat diepe koppelingen naar prijsopgaven en contracten die aan het project zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="30560-123">**Sales** : Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="30560-124">**Kostenramingen** : bevat een raster dat projectkosten definieert op basis van organisatorische kostencategorieën.</span><span class="sxs-lookup"><span data-stu-id="30560-124">**Expense Estimates** : Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Tabblad Kostenramingen en velden](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="30560-126">Rasterinstellingen</span><span class="sxs-lookup"><span data-stu-id="30560-126">Grid controls</span></span>

<span data-ttu-id="30560-127">Hieronder volgt een beknopt overzicht van de gebruikelijke instellingen op de verschillende tabbladen voor projectplanning.</span><span class="sxs-lookup"><span data-stu-id="30560-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="30560-128">Vernieuwen</span><span class="sxs-lookup"><span data-stu-id="30560-128">Refresh</span></span>

<span data-ttu-id="30560-129">**Vernieuwen** : haalt de laatste gegevens van de server op als er wijzigingen zijn opgetreden nadat het raster is geladen.</span><span class="sxs-lookup"><span data-stu-id="30560-129">**Refresh** : Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Knop Vernieuwen](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="30560-131">Groeperen op</span><span class="sxs-lookup"><span data-stu-id="30560-131">Group by</span></span>

<span data-ttu-id="30560-132">**Groeperen op** : werkt de groepering van de rijen in het raster bij om bronnen, rollen of categorieën weer te geven op basis van de behoeften van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="30560-132">**Group by** : Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Knop Groeperen op](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="30560-134">Vorige/Volgende</span><span class="sxs-lookup"><span data-stu-id="30560-134">Previous/Next</span></span>

<span data-ttu-id="30560-135">**Vorige**/**Volgende** : werkt de zichtbare tijdsperioden bij op de tijdgebonden rasters.</span><span class="sxs-lookup"><span data-stu-id="30560-135">**Previous**/**Next** : Update the visible time periods on the time-phased grids.</span></span>

![Knoppen Vorige en Volgende](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="30560-137">Tijdschaal</span><span class="sxs-lookup"><span data-stu-id="30560-137">Timescale</span></span>

<span data-ttu-id="30560-138">**Tijdschaal** : wijzigt de samengevoegde tijdgebonden gegevens op basis van dagen, weken, maanden en jaren.</span><span class="sxs-lookup"><span data-stu-id="30560-138">**Timescale** : Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Knop Tijdschaal](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="30560-140">Uitbreiden</span><span class="sxs-lookup"><span data-stu-id="30560-140">Expand</span></span>

<span data-ttu-id="30560-141">**Uitbreiden** : geeft het zichtbare raster weer op volledig scherm, zodat u extra rollen kunt zien.</span><span class="sxs-lookup"><span data-stu-id="30560-141">**Expand** : Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Knop Uitvouwen](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="30560-143">Tijdsfasering op</span><span class="sxs-lookup"><span data-stu-id="30560-143">Time-phase by</span></span>

<span data-ttu-id="30560-144">**Tijdsfasering op** : werkt de groepering van de rijen in het raster bij om kostenramingen voor verkoopramingen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="30560-144">**Time-phase by** : Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="30560-145">Dit besturingselement is ook van toepassing op het script voor ramingen en het raster voor het bijhouden van de gegevens.</span><span class="sxs-lookup"><span data-stu-id="30560-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Knop Tijdsfasering op](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="30560-147">Kolom toevoegen</span><span class="sxs-lookup"><span data-stu-id="30560-147">Add column</span></span>

<span data-ttu-id="30560-148">**Kolom toevoegen** : hiermee kan de gebruiker de zichtbare kolommen in het raster definiëren.</span><span class="sxs-lookup"><span data-stu-id="30560-148">**Add column** : Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="30560-149">Alleen eenvoudige kolommen kunnen worden toegevoegd aan de rasters in het formulier **Projectplanning**.</span><span class="sxs-lookup"><span data-stu-id="30560-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Knop Kolom toevoegen](media/navigation5.png)
