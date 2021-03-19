---
title: Wijzigingen op het gebied van resourcebeheer (Project Service Automation 3.x)
description: Dit onderwerp biedt informatie over de wijzigingen op het gebied van resourcebeheer.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f88d7309a5e1171629a72e749bfc01abb64c62a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284757"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="8e8a6-103">Wijzigingen op het gebied van resourcebeheer (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="8e8a6-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="8e8a6-104">De secties van dit onderwerp bevatten informatie over de wijzigingen die zijn doorgevoerd in het resourcebeheer-deel van Dynamics 365 Project Service Automation versie 3.x.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="8e8a6-105">Projectschattingen</span><span class="sxs-lookup"><span data-stu-id="8e8a6-105">Project estimates</span></span>

<span data-ttu-id="8e8a6-106">Projectschattingen zijn nu niet meer gebaseerd op de entiteit **msdyn\_projecttask** (**Projecttaak**), maar op de entiteit **msdyn\_resourceassignment** (**Resourcetoewijzing**).</span><span class="sxs-lookup"><span data-stu-id="8e8a6-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="8e8a6-107">Resourcetoewijzingen zijn de 'bron van waarheid' geworden voor taakplanning en prijzen.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="8e8a6-108">Regeltaken</span><span class="sxs-lookup"><span data-stu-id="8e8a6-108">Line tasks</span></span>

<span data-ttu-id="8e8a6-109">In PSA 3.x zijn lijntaken verouderd (afgeschaft).</span><span class="sxs-lookup"><span data-stu-id="8e8a6-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="8e8a6-110">Toewijzingen verwijzen nu naar de gehele taak in plaats van naar de regeltaken.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="8e8a6-111">In het volgende voorbeeld ziet u hoe een taak met de naam Testtaak wordt toegewezen aan de teamleden A en B in eerdere versies van PSA en in PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="8e8a6-112">**Vóór PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="8e8a6-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="8e8a6-113">Testtaak</span><span class="sxs-lookup"><span data-stu-id="8e8a6-113">Test task</span></span>

        - <span data-ttu-id="8e8a6-114">Testtaak – regeltaak 1</span><span class="sxs-lookup"><span data-stu-id="8e8a6-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="8e8a6-115">Toewijzing aan A</span><span class="sxs-lookup"><span data-stu-id="8e8a6-115">Assignment to A</span></span>

        - <span data-ttu-id="8e8a6-116">Testtaak – regeltaak 2</span><span class="sxs-lookup"><span data-stu-id="8e8a6-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="8e8a6-117">Toewijzing aan B</span><span class="sxs-lookup"><span data-stu-id="8e8a6-117">Assignment to B</span></span>

- <span data-ttu-id="8e8a6-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="8e8a6-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="8e8a6-119">Testtaak</span><span class="sxs-lookup"><span data-stu-id="8e8a6-119">Test task</span></span>

        - <span data-ttu-id="8e8a6-120">Toewijzing aan A</span><span class="sxs-lookup"><span data-stu-id="8e8a6-120">Assignment to A</span></span>
        - <span data-ttu-id="8e8a6-121">Toewijzing aan B</span><span class="sxs-lookup"><span data-stu-id="8e8a6-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="8e8a6-122">Niet-toegewezen toewijzing</span><span class="sxs-lookup"><span data-stu-id="8e8a6-122">Unassigned assignment</span></span>

<span data-ttu-id="8e8a6-123">In PSA 3.x is een niet-toegewezen toewijzing een toewijzing die is toegewezen aan een **NULL**-teamlid en een **NULL**-resource.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="8e8a6-124">Niet-toegewezen toewijzingen kunnen in een aantal scenario's optreden:</span><span class="sxs-lookup"><span data-stu-id="8e8a6-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="8e8a6-125">Als een taak is gemaakt maar nog niet is toegewezen aan een teamlid, wordt altijd een niet-toegewezen toewijzing gemaakt.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="8e8a6-126">Als alle toegewezen gebruikers van een taak worden verwijderd, wordt een niet-toegewezen toewijzing voor die taak opnieuw gemaakt.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="8e8a6-127">Planningsvelden in de entiteit Projecttaak</span><span class="sxs-lookup"><span data-stu-id="8e8a6-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="8e8a6-128">De velden in de entiteit **msdyn\_projecttask** zijn afgeschaft of verplaatst naar de entiteit **msdyn\_resourceassignment**, of er wordt nu naar verwezen vanuit de entiteit **msdyn\_projectteam** (**Projectteamlid**).</span><span class="sxs-lookup"><span data-stu-id="8e8a6-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="8e8a6-129">Afgeschaft veld op msdyn\_projecttask (Projecttaak)</span><span class="sxs-lookup"><span data-stu-id="8e8a6-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="8e8a6-130">Nieuw veld op msdyn\_resourceassignment (Resourcetoewijzing)</span><span class="sxs-lookup"><span data-stu-id="8e8a6-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="8e8a6-131">Opmerking</span><span class="sxs-lookup"><span data-stu-id="8e8a6-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="8e8a6-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="8e8a6-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="8e8a6-133">Geen</span><span class="sxs-lookup"><span data-stu-id="8e8a6-133">None</span></span> | |
| <span data-ttu-id="8e8a6-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="8e8a6-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="8e8a6-135">Geen</span><span class="sxs-lookup"><span data-stu-id="8e8a6-135">None</span></span> | |
| <span data-ttu-id="8e8a6-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="8e8a6-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="8e8a6-137">Geen</span><span class="sxs-lookup"><span data-stu-id="8e8a6-137">None</span></span> | |
| <span data-ttu-id="8e8a6-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="8e8a6-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="8e8a6-139">Geen</span><span class="sxs-lookup"><span data-stu-id="8e8a6-139">None</span></span> | |
| <span data-ttu-id="8e8a6-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="8e8a6-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="8e8a6-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="8e8a6-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="8e8a6-142">De indeling van de gegevensstructuur JavaScript Object Notation (JSON) die is opgeslagen in het veld, is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="8e8a6-143">Planningscontour</span><span class="sxs-lookup"><span data-stu-id="8e8a6-143">Schedule contour</span></span>

<span data-ttu-id="8e8a6-144">De planningscontour is opgeslagen in het veld **Gepland werk** (**\_msdyn plannedwork**) van elke entiteit van het type **Resourcetoewijzing** (**\_msdyn ResourceAssignment**).</span><span class="sxs-lookup"><span data-stu-id="8e8a6-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="8e8a6-145">Structuur</span><span class="sxs-lookup"><span data-stu-id="8e8a6-145">Structure</span></span>

<span data-ttu-id="8e8a6-146">De nieuwe structuur van de planningscontour bestaat uit flexibele tijdsegmenten die voor elke dag van de planning zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="8e8a6-147">Elke tijdsectie heeft de volgende eigenschappen:</span><span class="sxs-lookup"><span data-stu-id="8e8a6-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="8e8a6-148">**Begin**: het begin van de werkuren voor de dag, volgens de projectagenda.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="8e8a6-149">**Eind**: het einde van de werkuren voor de dag, volgens de projectagenda.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="8e8a6-150">**Uren**: het aantal uren dat is toegewezen op de dag.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="8e8a6-151">**Voorbeeld**</span><span class="sxs-lookup"><span data-stu-id="8e8a6-151">**Example**</span></span>

<span data-ttu-id="8e8a6-152">In dit voorbeeld wordt een projectagenda gebruikt waarin de werkdag loopt van 9 uur tot 17 uur in de tijdzone UTC-8.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="8e8a6-153">Automatisch plannen en handmatig plannen</span><span class="sxs-lookup"><span data-stu-id="8e8a6-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="8e8a6-154">Als een taak automatisch wordt gepland, worden de uren vooraf geladen en kan de duur van de taak worden verminderd.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="8e8a6-155">**Voorbeeld**</span><span class="sxs-lookup"><span data-stu-id="8e8a6-155">**Example**</span></span>

<span data-ttu-id="8e8a6-156">De volgende taak wordt automatisch gepland voor 18 uur gedurende drie dagen (3 december 2018 tot en met 5 december 2018).</span><span class="sxs-lookup"><span data-stu-id="8e8a6-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="8e8a6-157">Als een taak handmatig wordt gepland, worden de uren gelijkmatig verdeeld over alle datums.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="8e8a6-158">**Voorbeeld**</span><span class="sxs-lookup"><span data-stu-id="8e8a6-158">**Example**</span></span>

<span data-ttu-id="8e8a6-159">De volgende taak wordt handmatig gepland voor 18 uur gedurende drie dagen (3 december 2018 tot en met 5 december 2018).</span><span class="sxs-lookup"><span data-stu-id="8e8a6-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="8e8a6-160">Toewijzingseenheid</span><span class="sxs-lookup"><span data-stu-id="8e8a6-160">Assignment unit</span></span>

<span data-ttu-id="8e8a6-161">De toewijzingseenheid is afgeschaft in PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="8e8a6-162">De inspanningsuren van een taak worden nu gelijkelijk verdeeld, per dag, tussen alle toegewezen resources.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="8e8a6-163">**Voorbeeld**</span><span class="sxs-lookup"><span data-stu-id="8e8a6-163">**Example**</span></span>

<span data-ttu-id="8e8a6-164">In dit voorbeeld wordt de taak toegewezen aan twee resources en automatisch gepland voor 36 uur gedurende drie dagen (3 december 2018 tot en met 5 december 2018).</span><span class="sxs-lookup"><span data-stu-id="8e8a6-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="8e8a6-165">Toewijzing 1:</span><span class="sxs-lookup"><span data-stu-id="8e8a6-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="8e8a6-166">Toewijzing 2:</span><span class="sxs-lookup"><span data-stu-id="8e8a6-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="8e8a6-167">Prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="8e8a6-167">Pricing dimensions</span></span>

<span data-ttu-id="8e8a6-168">In PSA 3.x zijn resourcespecifieke dimensievelden voor prijzen (zoals **Rol** en **Organisatie-eenheid**) verwijderd uit de entiteit **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="8e8a6-169">Deze velden kunnen nu worden opgehaald uit het bijbehorende projectteamlid (**msdyn\_projectteam**) van de resourcetoewijzing (**msdyn\_resourceassignment**) wanneer projectschattingen worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="8e8a6-170">Er is een nieuw veld, **msdyn\_organizationalunit**, toegevoegd aan de entiteit **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="8e8a6-171">Afgeschaft veld op msdyn\_projecttask (Projecttaak)</span><span class="sxs-lookup"><span data-stu-id="8e8a6-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="8e8a6-172">Veld van msdyn\_projectteam (Projectteamlid) dat in plaats daarvan wordt gebruikt</span><span class="sxs-lookup"><span data-stu-id="8e8a6-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="8e8a6-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="8e8a6-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="8e8a6-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="8e8a6-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="8e8a6-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="8e8a6-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="8e8a6-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="8e8a6-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="8e8a6-177">Contouren</span><span class="sxs-lookup"><span data-stu-id="8e8a6-177">Contours</span></span>

<span data-ttu-id="8e8a6-178">De contourvelden voor prijzen en schattingen zijn afgeschaft voor de entiteit **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="8e8a6-179">Ze zijn verplaatst naar de entiteit **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="8e8a6-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="8e8a6-180">Afgeschaft veld op msdyn\_projecttask (Projecttaak)</span><span class="sxs-lookup"><span data-stu-id="8e8a6-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="8e8a6-181">Nieuw veld op msdyn\_resourceassignment (Resourcetoewijzing)</span><span class="sxs-lookup"><span data-stu-id="8e8a6-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="8e8a6-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="8e8a6-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="8e8a6-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="8e8a6-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="8e8a6-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="8e8a6-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="8e8a6-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="8e8a6-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="8e8a6-186">De volgende velden zijn toegevoegd aan de entiteit **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="8e8a6-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="8e8a6-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="8e8a6-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="8e8a6-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="8e8a6-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="8e8a6-189">De volgende velden voor geplande, werkelijke en resterende kosten en verkopen zijn niet veranderd voor de entiteit **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="8e8a6-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="8e8a6-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="8e8a6-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="8e8a6-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="8e8a6-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="8e8a6-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="8e8a6-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="8e8a6-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="8e8a6-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="8e8a6-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="8e8a6-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="8e8a6-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="8e8a6-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]