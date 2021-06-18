---
title: Een projectsjabloon maken
description: Informatie over een projectsjabloon maken in Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 148bf1d42b640ff7b58b13bb0c30c7e583d803c8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997235"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="bb35b-103">Een projectsjabloon maken (Project Service)</span><span class="sxs-lookup"><span data-stu-id="bb35b-103">Create a project template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="bb35b-104">Projectsjablonen besparen u tijd als uw bedrijf regelmatig op soortgelijke projecttypen biedt.</span><span class="sxs-lookup"><span data-stu-id="bb35b-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="bb35b-105">Ze bieden een standaardset van rollen en geschatte uren voor een type project.</span><span class="sxs-lookup"><span data-stu-id="bb35b-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="bb35b-106">Accountmanagers en projectmanagers kunnen projecten maken op basis van een projectsjabloon of ze kunnen de sjabloon kopiëren en een eigen project maken.</span><span class="sxs-lookup"><span data-stu-id="bb35b-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="bb35b-107">Onderdelen van een projectsjabloon</span><span class="sxs-lookup"><span data-stu-id="bb35b-107">Components of project template</span></span>
 <span data-ttu-id="bb35b-108">Een projectsjabloon bestaat uit drie onderdelen:</span><span class="sxs-lookup"><span data-stu-id="bb35b-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="bb35b-109">**Structuur voor werkspecificatie**: een structuur voor werkspecificatie in een projectsjabloon heeft dezelfde verzameling elementen als in het project.</span><span class="sxs-lookup"><span data-stu-id="bb35b-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="bb35b-110">U kunt een taakhiërarchie maken, rollen aan de taak koppelen, planningskenmerken definiëren, afhankelijkheden instellen en alle gegevens weergeven in Gantt.</span><span class="sxs-lookup"><span data-stu-id="bb35b-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="bb35b-111">De structuur voor werkspecificatie in projectsjablonen ondersteunt ook taakmodi voor elke taak.</span><span class="sxs-lookup"><span data-stu-id="bb35b-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="bb35b-112">Er is geen verschil tussen een projectsjabloon en een project bij het maken van een werkplanning.</span><span class="sxs-lookup"><span data-stu-id="bb35b-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="bb35b-113">**Projectschattingen**: projectschattingen in sjablonen werken op dezelfde manier als in projecten, behalve dat de prijslijsten standaard altijd worden ingesteld op de standaardkosten en de standaardverkoopprijslijsten die in de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-parameters zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="bb35b-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="bb35b-114">De rest van de functionaliteit is hetzelfde als in een project.</span><span class="sxs-lookup"><span data-stu-id="bb35b-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="bb35b-115">**Projectteamvorming**: als u een projectteam vormt voor een projectsjabloon, kunt u geen benoemde resource in een sjabloon boeken.</span><span class="sxs-lookup"><span data-stu-id="bb35b-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="bb35b-116">U kunt **Projectteam genereren** in de structuur voor werkspecificatie gebruiken om een set algemene resources te genereren.</span><span class="sxs-lookup"><span data-stu-id="bb35b-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="bb35b-117">U kunt ook de vereiste vaardigheden en deskundigheden voor algemene resources opgeven.</span><span class="sxs-lookup"><span data-stu-id="bb35b-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="bb35b-118">U kunt een algemene resource niet vervangen met een boekbare resource in projectsjablonen.</span><span class="sxs-lookup"><span data-stu-id="bb35b-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="bb35b-119">Een project maken op basis van een sjabloon</span><span class="sxs-lookup"><span data-stu-id="bb35b-119">Create a project from a template</span></span>  
 <span data-ttu-id="bb35b-120">U kunt een project op de volgende manieren op basis van een sjabloon maken:</span><span class="sxs-lookup"><span data-stu-id="bb35b-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="bb35b-121">Bij het maken van een project op basis van de prijsopgave kunt u een projectsjabloon in het projectformulier voor snelle invoer kiezen.</span><span class="sxs-lookup"><span data-stu-id="bb35b-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="bb35b-122">Wanneer u een project maakt door te klikken op **Nieuw project**, wordt het projectformulier weergegeven voordat u de record opslaat.</span><span class="sxs-lookup"><span data-stu-id="bb35b-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="bb35b-123">Vanaf hier kunt u klikken op het veld **Een sjabloon kiezen** om een keuze te maken in de lijst met vooraf gedefinieerde projectsjablonen in uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="bb35b-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="bb35b-124">Klik op **Projecten maken van een sjabloon** op de pagina **Projectsjabloon** om een project op basis van de sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="bb35b-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="bb35b-125">Onderdelen van een sjabloon kopiëren naar een project</span><span class="sxs-lookup"><span data-stu-id="bb35b-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="bb35b-126">Wanneer u onderdelen van een sjabloon naar een project kopieert, zijn er enkele dingen die u moet weten.</span><span class="sxs-lookup"><span data-stu-id="bb35b-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="bb35b-127">**Een structuur voor werkspecificatie kopiëren**: als u de structuur voor werkspecificatie van een projectsjabloon kopieert, worden als het project een andere projectkalender dan de sjabloon heeft, de werkuren van de agenda van het project toegepast op de planning van taken.</span><span class="sxs-lookup"><span data-stu-id="bb35b-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="bb35b-128">Hiermee wordt de planning aangepast aan de ondersteunende projectkalender.</span><span class="sxs-lookup"><span data-stu-id="bb35b-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="bb35b-129">Op dezelfde manier gebruikt de eerste taak in de structuur voor werkspecificatie de begindatum van het project, waardoor de rest van de planning van de taakhiërarchie wordt bijgewerkt op basis van de duur en de afhankelijkheden die in de structuur voor werkspecificatie van de sjabloon zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="bb35b-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="bb35b-130">**Projectschattingen kopiëren**: als u schattingsregels van meerdere projecten kopieert, worden prijslijsten bijgewerkt op basis van de eenheid die eigenaar is van het project voor de kostprijslijst en klant voor de verkoopprijslijst.</span><span class="sxs-lookup"><span data-stu-id="bb35b-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="bb35b-131">De kosten per eenheid en de verkoopprijzen worden bepaald aan de hand van deze prijslijsten in projecten die aan een verkoopentiteit zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="bb35b-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="bb35b-132">**Een projectteam kopiëren**: als u het projectteam op basis van een sjabloon kopieert naar een project, worden de algemene resources gekopieerd samen met de vaardigheden en de deskundigheden die in de sjabloon zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="bb35b-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="bb35b-133">Algemene resourcetoewijzingen worden ook onderhouden zoals in de projectsjabloon.</span><span class="sxs-lookup"><span data-stu-id="bb35b-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="bb35b-134">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bb35b-134">See Also</span></span>  
 [<span data-ttu-id="bb35b-135">Projectmanager-handleiding</span><span class="sxs-lookup"><span data-stu-id="bb35b-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]