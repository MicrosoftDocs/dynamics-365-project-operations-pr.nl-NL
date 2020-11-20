---
title: Verkoopschattingen en projecten
description: Dit onderwerp bevat informatie over hoe u kunt profiteren van de planning en schattingen in het verkoopproces.
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
ms.openlocfilehash: d8bb380519759659dc1b4151b62228a626ee7a26
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120672"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="4cf77-103">Verkoopschattingen en projecten</span><span class="sxs-lookup"><span data-stu-id="4cf77-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4cf77-104">Tijdens het verkoopproces kunt u verkoopschattingen maken door een project aan een verkoopprijsopgave te koppelen.</span><span class="sxs-lookup"><span data-stu-id="4cf77-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="4cf77-105">Op deze manier kan een deterministische schatting worden gemaakt tijdens het verkoopproces om te profiteren van de mogelijkheden voor projectplanning en -schatting.</span><span class="sxs-lookup"><span data-stu-id="4cf77-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="4cf77-106">Als de verkoop doorgaat, kan de planning die is gebruikt voor verkoopschattingsdoeleinden, worden gebruikt als basis voor verdere verfijning van het projectplan.</span><span class="sxs-lookup"><span data-stu-id="4cf77-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="4cf77-107">Een project koppelen aan een prijsopgaveregel</span><span class="sxs-lookup"><span data-stu-id="4cf77-107">Linking a project to a quote line</span></span>

<span data-ttu-id="4cf77-108">Wanneer u een op een project gebaseerde prijsopgaveregel maakt, kunt u een nieuw project maken of een bestaand project koppelen op de pagina **Prijsopgaveregel**.</span><span class="sxs-lookup"><span data-stu-id="4cf77-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Prijsopgaveregelformulier](media/project-8.png)
 
<span data-ttu-id="4cf77-110">Wanneer u een nieuw project maakt op basis van de details van de prijsopgaveregel, kunt u gebruikmaken van projectsjablonen.</span><span class="sxs-lookup"><span data-stu-id="4cf77-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="4cf77-111">Projectsjablonen zijn modelprojecten die standaardprojectplannen en financiële schattingen vertegenwoordigen die typisch zijn voor een organisatie.</span><span class="sxs-lookup"><span data-stu-id="4cf77-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="4cf77-112">Ze kunnen ook kopieën van projectplannen en schattingen van eerdere projecten vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="4cf77-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Prijsopgaveregeldetails](media/project-9.png)
  
<span data-ttu-id="4cf77-114">Wanneer u het project maakt op basis van de prijsopgave, wordt het project automatisch gekoppeld aan de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="4cf77-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="4cf77-115">Componenten van schattingen in een project</span><span class="sxs-lookup"><span data-stu-id="4cf77-115">Components of estimates in a project</span></span>

<span data-ttu-id="4cf77-116">Met een planning kunt u werk verdelen in taken, een hiërarchie van taken onderhouden, bepalen welke resources nodig zijn om een taak te voltooien en een schatting toewijzen van de inspanning die nodig is om een taak te voltooien.</span><span class="sxs-lookup"><span data-stu-id="4cf77-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="4cf77-117">U kunt de werkinspanning en de planningsschattingen definiëren met behulp van de velden op het tabblad **Planning** van de pagina **Project**.</span><span class="sxs-lookup"><span data-stu-id="4cf77-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="4cf77-118">Omdat er een prijslijst aan het project is gekoppeld, worden financiële schattingen berekend op basis van kost- en verkoopprijzen die zijn gedefinieerd in de prijslijst.</span><span class="sxs-lookup"><span data-stu-id="4cf77-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="4cf77-119">Schattingen importeren van een project in een prijsopgave</span><span class="sxs-lookup"><span data-stu-id="4cf77-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="4cf77-120">Nadat u projectschattingen hebt gedefinieerd, kunt u deze importeren in de prijsopgaveregel.</span><span class="sxs-lookup"><span data-stu-id="4cf77-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="4cf77-121">Selecteer op de pagina **Details van prijsopgaveregel** de optie **Importeren uit schatting** op het lint om projectschattingen op het niveau van transactietype, rol of taak samen te vatten.</span><span class="sxs-lookup"><span data-stu-id="4cf77-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
