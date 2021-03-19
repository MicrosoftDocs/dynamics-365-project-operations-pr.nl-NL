---
title: Projectsjablonen
description: Dit onderwerp bevat informatie over het gebruik van projectsjablonen om snel projectinstellingen te kunnen configureren.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: d9d208ebcef127062428afdadde2c54eb07ea505
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283587"
---
# <a name="project-templates"></a><span data-ttu-id="3fe1e-103">Projectsjablonen</span><span class="sxs-lookup"><span data-stu-id="3fe1e-103">Project templates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3fe1e-104">Een projectsjabloon is een vooraf gedefinieerd kader dat u in staat stelt snel en eenvoudig een project te starten.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="3fe1e-105">U kunt een vooraf gedefinieerde sjabloon gebruiken om met één klik een nieuw project te maken.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="3fe1e-106">Voor projecten moet u de vereisten voor projectsjablonen definiëren.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="3fe1e-107">U moet een projectagenda definiëren voor elke projectsjabloon en rollen en prijslijsten moeten vooraf worden gedefinieerd in de organisatie, zodat de onderdelen van de sjabloon nuttige gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="3fe1e-108">Een projectsjabloon bestaat uit drie onderdelen: een planning, projectschattingen en projectteamleden.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="3fe1e-109">Planning</span><span class="sxs-lookup"><span data-stu-id="3fe1e-109">Schedule</span></span>

<span data-ttu-id="3fe1e-110">Een planning in een projectsjabloon heeft dezelfde set elementen als een planning in een project.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="3fe1e-111">U kunt een taakhiërarchie maken, rollen aan taken koppelen, planningskenmerken definiëren en afhankelijkheden instellen.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="3fe1e-112">Een planning in een projectsjabloon ondersteunt ook de taakmodi voor elke taak.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="3fe1e-113">Daarom wordt ook de planningsengine ondersteund.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="3fe1e-114">U moet een projectagenda koppelen aan het project.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="3fe1e-115">Wanneer u een werkplanning maakt, is er geen verschil tussen een projectsjabloon en een project.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="3fe1e-116">Projectschattingen</span><span class="sxs-lookup"><span data-stu-id="3fe1e-116">Project estimates</span></span>

<span data-ttu-id="3fe1e-117">Projectschattingen in een projectsjabloon werken op dezelfde manier als projectschattingen in een project.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="3fe1e-118">De kosten en verkoopprijzen worden echter opgehaald uit de standaardlijsten met kosten en verkoopprijzen die in de parameters zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="3fe1e-119">Een project maken op basis van een sjabloon</span><span class="sxs-lookup"><span data-stu-id="3fe1e-119">Creating a project from a template</span></span>
 
<span data-ttu-id="3fe1e-120">Er zijn verschillende manieren om een project te maken op basis van een projectsjabloon:</span><span class="sxs-lookup"><span data-stu-id="3fe1e-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="3fe1e-121">Wanneer u een project maakt op basis van een prijsopgave, kunt u een projectsjabloon selecteren in het dialoogvenster **Snelle invoer: Project**.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Het dialoogvenster Snelle invoer: Project](media/project-11.png)

- <span data-ttu-id="3fe1e-123">Wanneer u een project maakt door **Nieuw project** te selecteren, wordt de pagina **Project** weergegeven voordat de record wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="3fe1e-124">Selecteer in het veld **Een sjabloon kiezen** een van de vooraf gedefinieerde projectsjablonen in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="3fe1e-125">Gebruik **Een project maken op basis van een sjabloon** op de pagina **Sjabloonentiteit**.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="3fe1e-126">Onderdelen van een sjabloon kopiëren naar een project</span><span class="sxs-lookup"><span data-stu-id="3fe1e-126">Copying components of template to project</span></span>

<span data-ttu-id="3fe1e-127">Wanneer u de onderdelen van een projectsjabloon naar een project kopieert, kunnen er enkele overschrijvingen plaatsvinden, afhankelijk van de instellingen in het project.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="3fe1e-128">De planning kopiëren</span><span class="sxs-lookup"><span data-stu-id="3fe1e-128">Copying the schedule</span></span>

<span data-ttu-id="3fe1e-129">Wanneer u de planning van een projectsjabloon kopieert, maar het project een andere projectagenda heeft dan de sjabloon, worden de werkuren van de agenda van het project toegepast op de taakplanning.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="3fe1e-130">Op deze manier wordt de planning aangepast, zodat deze overeenkomt met de achterliggende projectagenda.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="3fe1e-131">Zo wordt door de eerste taak in de planning ook de begindatum van het project overgenomen en wordt de planning van het resterende deel van de hiërarchie bijgewerkt op basis van de duur en de afhankelijkheden die in de sjabloon zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="3fe1e-132">Projectschattingen kopiëren</span><span class="sxs-lookup"><span data-stu-id="3fe1e-132">Copying project estimates</span></span> 

<span data-ttu-id="3fe1e-133">Wanneer u meerdere projectschattingsregels kopieert, worden de prijslijsten bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="3fe1e-134">Voor de kostprijslijst zijn deze updates gebaseerd op de eenheid die eigenaar is van het project.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="3fe1e-135">Voor de verkoopprijslijst zijn deze updates gebaseerd op de klant.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="3fe1e-136">Bij projecten die zijn gekoppeld aan een verkoopentiteit, worden de kosten per eenheid en de verkoopprijzen bepaald aan de hand van deze prijslijsten.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="3fe1e-137">Een projectteam kopiëren</span><span class="sxs-lookup"><span data-stu-id="3fe1e-137">Copying a project team</span></span>

<span data-ttu-id="3fe1e-138">Wanneer een projectteam van een projectsjabloon naar een project wordt gekopieerd, worden de algemene resources gekopieerd, samen met de vaardigheden en deskundigheden die in de sjabloon zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="3fe1e-139">Algemene resourcetoewijzingen worden ook onderhouden, net zoals in de projectsjabloon.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="3fe1e-140">Benoemde resources worden niet ondersteund in projectsjablonen.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-140">Named resources aren't supported in project templates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]