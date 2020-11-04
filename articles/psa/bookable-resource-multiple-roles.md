---
title: Een schatting van verkopen en kosten van projecten maken wanneer een boekbare resource meerdere rollen in een project vervult
description: Dit onderwerp biedt informatie over hoe prijsdimensies kunnen worden gebruikt om prijzen en kosten te ondersteunen voor een resource die meerdere rollen in een project vervult.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074616"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="17c2c-103">Een schatting van verkopen en kosten van projecten maken wanneer een boekbare resource meerdere rollen in een project vervult</span><span class="sxs-lookup"><span data-stu-id="17c2c-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="17c2c-104">Projectgebaseerde bedrijven hebben vaak behoefte aan één resource om meerdere rollen in een project uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="17c2c-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="17c2c-105">Voor elk van deze rollen kunnen verschillende prijzen en kosten worden ingesteld, wat betekent dat de tijd van dezelfde resource aan het project een andere financiële schatting kan krijgen, afhankelijk van de rekening en kostentarieven voor elk van de rollen.</span><span class="sxs-lookup"><span data-stu-id="17c2c-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="17c2c-106">In Project Service Automation kunnen de waarden in de teamlidrecord voor de genoemde resource worden ingesteld en kunnen verschillende overschrijvingen worden uitgevoerd voor elk van de taken waaraan het teamlid is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="17c2c-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="17c2c-107">In het volgende voorbeeld wordt uitgelegd hoe door een eenvoudige overschrijving van deze waarde een resource meerdere rollen in een project kan hebben met verschillende kosten- en factureringstarieven.</span><span class="sxs-lookup"><span data-stu-id="17c2c-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="17c2c-108">Taken maken</span><span class="sxs-lookup"><span data-stu-id="17c2c-108">Create tasks</span></span>
<span data-ttu-id="17c2c-109">Maak twee projecttaken van elk 40 uur: Taak A en Taak B. Selecteer Taak A als een voorgaande taak van Taak B.</span><span class="sxs-lookup"><span data-stu-id="17c2c-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="17c2c-110">Rol en organisatie-eenheid instellen voor een algemeen projectteamlid</span><span class="sxs-lookup"><span data-stu-id="17c2c-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="17c2c-111">Selecteer op de pagina **Planning** de rij **Taak** voor Taak A.</span><span class="sxs-lookup"><span data-stu-id="17c2c-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="17c2c-112">Selecteer in het veld **Resources** de optie **Maken** in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="17c2c-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="17c2c-113">Geef op de pagina **Snelle invoer voor teamleden** de kenmerken op van het algemene teamlid dat deze taak kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="17c2c-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="17c2c-114">Selecteer de juiste rol en organisatie-eenheid en selecteer vervolgens **Opslaan en sluiten**.</span><span class="sxs-lookup"><span data-stu-id="17c2c-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="17c2c-115">Er wordt een algemeen teamlid gemaakt en toegewezen aan deze taak.</span><span class="sxs-lookup"><span data-stu-id="17c2c-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="17c2c-116">Herhaal deze stappen voor taak B en zorg ervoor dat de rol en organisatie-eenheid van het algemene teamlid dat voor taak B is gemaakt, afwijken van die voor taak A.</span><span class="sxs-lookup"><span data-stu-id="17c2c-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="17c2c-117">Rol en organisatie-eenheid instellen voor een projecttaak</span><span class="sxs-lookup"><span data-stu-id="17c2c-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="17c2c-118">Nadat u taak A hebt gemaakt, selecteert u de taak en vervolgens selecteert u **Taak bewerken**.</span><span class="sxs-lookup"><span data-stu-id="17c2c-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="17c2c-119">Zoek op de pagina **Taakdetails** naar de velden **Rol** en **Organisatie-eenheid** en voeg de waarden toe die vereist zijn voor een resource die deze taak zou uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="17c2c-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="17c2c-120">Als u deze scenario's voltooit met demogegevens van Project Service Automation, selecteert u **Adviesleider** voor de rol en **Fabrikam US** als de organisatie-eenheid.</span><span class="sxs-lookup"><span data-stu-id="17c2c-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="17c2c-121">Selecteer Taak B en selecteer vervolgens **Taak bewerken**.</span><span class="sxs-lookup"><span data-stu-id="17c2c-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="17c2c-122">Zoek op de pagina **Taakdetails** naar de velden **Rol** en **Organisatie-eenheid** en voeg de waarden toe die vereist zijn voor een resource die deze taak zou uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="17c2c-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="17c2c-123">Zorg ervoor dat de waarden in de velden **Rol** en **Organisatie-eenheid** verschillen voor Taak B en Taak A.</span><span class="sxs-lookup"><span data-stu-id="17c2c-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="17c2c-124">Als u deze scenario's voltooit met demogegevens van Project Service Automation, selecteert u **Netwerktechnicus** voor de rol en **Fabrikam US** als de organisatie-eenheid.</span><span class="sxs-lookup"><span data-stu-id="17c2c-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="17c2c-125">Sla op en sluit de pagina **Taakdetails**.</span><span class="sxs-lookup"><span data-stu-id="17c2c-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="17c2c-126">Teamlid en gedrag van schattingen</span><span class="sxs-lookup"><span data-stu-id="17c2c-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="17c2c-127">Selecteer op de pagina **Taakdetails** voor **Teamlid** de twee algemene teamleden en selecteer vervolgens **Vereisten genereren**.</span><span class="sxs-lookup"><span data-stu-id="17c2c-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="17c2c-128">Vervolgens worden er resourcevereisten gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="17c2c-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="17c2c-129">Selecteer de teamlidrij voor **Adviesleider** en selecteer vervolgens **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="17c2c-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="17c2c-130">Het planbord wordt geopend en er wordt een resource voor die vereiste geboekt.</span><span class="sxs-lookup"><span data-stu-id="17c2c-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="17c2c-131">Selecteer de teamlidrij voor **Netwerktechnicus** en selecteer vervolgens **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="17c2c-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="17c2c-132">Het planbord wordt geopend en dezelfde resource wordt voor die vereiste geboekt.</span><span class="sxs-lookup"><span data-stu-id="17c2c-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="17c2c-133">Het raster Teamlid</span><span class="sxs-lookup"><span data-stu-id="17c2c-133">Team Member grid</span></span> 
<span data-ttu-id="17c2c-134">In het raster **Teamlid** zijn de twee generieke teamlidrecords verwijderd en vervangen door één resource.</span><span class="sxs-lookup"><span data-stu-id="17c2c-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="17c2c-135">Er is één set waarden voor die resource met een standaardverzameling waarden voor **Rol** en **Organisatie-eenheid**.</span><span class="sxs-lookup"><span data-stu-id="17c2c-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="17c2c-136">Wanneer u de rij van die teamlidrecord uitvouwt, kunt u voor beide taken verschillende toewijzingen in de teamlidrecord zien.</span><span class="sxs-lookup"><span data-stu-id="17c2c-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="17c2c-137">Elke toewijzingsrij bevat taakspecifieke waarden voor **Rol** en **Organisatie-eenheid**.</span><span class="sxs-lookup"><span data-stu-id="17c2c-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="17c2c-138">Het raster Schattingen</span><span class="sxs-lookup"><span data-stu-id="17c2c-138">Estimates grid</span></span> 
<span data-ttu-id="17c2c-139">Wanneer u naar het raster **Schattingen** navigeert, ziet u dat de toewijzingen voor dezelfde resource verschillend zijn geprijsd.</span><span class="sxs-lookup"><span data-stu-id="17c2c-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="17c2c-140">De toewijzing voor de resource voor Taak A wordt geprijsd met de kenmerkwaarde **Adviesleider** voor **Rol**.</span><span class="sxs-lookup"><span data-stu-id="17c2c-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="17c2c-141">De toewijzing voor dezelfde resource voor Taak B wordt geprijsd met de kenmerkwaarde **Netwerktechnicus** voor **Rol**.</span><span class="sxs-lookup"><span data-stu-id="17c2c-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





