---
title: Werkschattingen opgeven voor een project tijdens het verkoopproces
description: Informatie over werkschattingen opgeven voor een project tijdens het verkoopproces in Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 7bd83b6872d437f1d074d6ea2336c751bdfdd9e6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120582"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="92ee2-103">Werkschattingen opgeven voor een project tijdens het verkoopproces (Project Service)</span><span class="sxs-lookup"><span data-stu-id="92ee2-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="92ee2-104">Tijdens het verkoopproces, kunt u verkopenschattingen van de grond af uitwerken met prijsopgaveregels.</span><span class="sxs-lookup"><span data-stu-id="92ee2-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="92ee2-105">De mogelijkheden voor [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] bieden een wetenschappelijkere en deterministische manier om verkopenschattingen te maken door werkitems op te splitsen en relevante kenmerken aan elkaar te koppelen die bijdragen aan schattingen voor het project in de structuur voor werkspecificatie.</span><span class="sxs-lookup"><span data-stu-id="92ee2-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="92ee2-106">Als u de verkoop binnenhaalt, kunt u de gekoppelde structuur voor werkspecificatie in uw projectplan gebruiken, en indien nodig verfijnen voor het voltooien van het project.</span><span class="sxs-lookup"><span data-stu-id="92ee2-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="92ee2-107">Een project koppelen aan een prijsopgaveregel</span><span class="sxs-lookup"><span data-stu-id="92ee2-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="92ee2-108">Bij het maken van een op Project gebaseerde prijsopgaveregel, kunt u een nieuw project maken vanaf de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="92ee2-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="92ee2-109">U kunt projectsjablonen vervolgens gebruiken, dat zijn pre-gevormde standaardprojectplannen en financiële ramingen die gelden voor uw organisatie, of een kopie van een projectplan en schattingen van een eerder project.</span><span class="sxs-lookup"><span data-stu-id="92ee2-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="92ee2-110">Wanneer u een project maakt, het kiezen van een projectsjabloon biedt een basis voor verfijning van het projectplan, schattingen, en de rolvereisten.</span><span class="sxs-lookup"><span data-stu-id="92ee2-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="92ee2-111">Door het project vanaf de offerte te maken, wordt het project automatisch gekoppeld aan de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="92ee2-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="92ee2-112">Project-schattingscomponenten</span><span class="sxs-lookup"><span data-stu-id="92ee2-112">Project estimate components</span></span>  
 <span data-ttu-id="92ee2-113">De structuur voor werkspecificatie in een project bevat een manier voor het opsplitsing van het werk in taken, het behouder van een hiërarchie van taken, en wijst een schatting van vereiste moeite voor het voltooien van elke taak.</span><span class="sxs-lookup"><span data-stu-id="92ee2-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="92ee2-114">U kunt ook rollen op een taak koppelen om een schatting van het type resource te geven dat is vereist om een taak en een planning te voltooien.</span><span class="sxs-lookup"><span data-stu-id="92ee2-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="92ee2-115">Met de structuur voor werkspecificatie kunt u schattingen maken van de werkinspanning en planning.</span><span class="sxs-lookup"><span data-stu-id="92ee2-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="92ee2-116">Standaard gebruikt het project standaardprijslijsten die u eerder gedefinieerd hebt.</span><span class="sxs-lookup"><span data-stu-id="92ee2-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="92ee2-117">De kost- en verkoopprijzen gedefinieerd in de prijslijsten helpen financiële ramingen voor de werkanalyse van het project te definiëren.</span><span class="sxs-lookup"><span data-stu-id="92ee2-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="92ee2-118">Als de project aan een prijsopgave is gekoppeld, en de prijsopgave een andere prijslijst dan de standaard heeft, wordt de prijslijst van prijsopgave gebruikt voor financiële ramingen.</span><span class="sxs-lookup"><span data-stu-id="92ee2-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="92ee2-119">Importerenschattingen van een project in een prijsopgave</span><span class="sxs-lookup"><span data-stu-id="92ee2-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="92ee2-120">Als u projectschattingen in het project hebt, kunt u deze schattingen in de prijsopgaveregel importeren:</span><span class="sxs-lookup"><span data-stu-id="92ee2-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="92ee2-121">In **De Details van de prijsopgaveregel**, klik op **Importeren uit schatting**.</span><span class="sxs-lookup"><span data-stu-id="92ee2-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="92ee2-122">Selecteer of u projectschattingen wilt importeren samengevat op transactietype, rol, of het niveau van werkspecificatieknooppunt.</span><span class="sxs-lookup"><span data-stu-id="92ee2-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="92ee2-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="92ee2-123">See Also</span></span>  
 [<span data-ttu-id="92ee2-124">Projectmanager-handleiding</span><span class="sxs-lookup"><span data-stu-id="92ee2-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
