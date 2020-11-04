---
title: De status van een project volgen
description: Informatie over de status van een project volgen in Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074650"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="0451d-103">De status van een project bijhouden (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0451d-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0451d-104">Gebruik de [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] om de voortgang van het project van een klant bij te houden.</span><span class="sxs-lookup"><span data-stu-id="0451d-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="0451d-105">Als overeenkomstenvoortgangen, het bijwerken van projecten fasen van het stadium van de overeenkomst te geven:</span><span class="sxs-lookup"><span data-stu-id="0451d-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="0451d-106">**Nieuw**</span><span class="sxs-lookup"><span data-stu-id="0451d-106">**New**</span></span>    | <span data-ttu-id="0451d-107">Wanneer u een project hebt gemaakt, is de fase ingesteld op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0451d-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="0451d-108">Als u de sjabloon van een project hebt gemaakt, in dit stadium een planning kan het project, schattingen, en teamgegevens hebben.</span><span class="sxs-lookup"><span data-stu-id="0451d-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="0451d-109">Anders, is het overzicht van het project zijn en moet u de rest projectmarketing het handmatig invoeren.</span><span class="sxs-lookup"><span data-stu-id="0451d-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="0451d-110">**Offerte**</span><span class="sxs-lookup"><span data-stu-id="0451d-110">**Quote**</span></span>   |      <span data-ttu-id="0451d-111">Wanneer u een project aan een offerte koppelt of het aanmaakt op basis van een offert, wordt de projectfase ingesteld op **Offerte** en de geschatte begin- en einddatum worden eveneens bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="0451d-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote** , and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="0451d-112">Wanneer het project in de prijsopgavefase is, ziet u de details op de offerte in op het **Verkoop** op de **Project**</span><span class="sxs-lookup"><span data-stu-id="0451d-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="0451d-113">**Plannen**</span><span class="sxs-lookup"><span data-stu-id="0451d-113">**Plan**</span></span>   |                                     <span data-ttu-id="0451d-114">Wanneer u een quote binnenhaalt aan een project is gekoppeld, en als de overeenkomstenvoortgangen aan de contractfase, updates van de projectfase op **Plannen**.</span><span class="sxs-lookup"><span data-stu-id="0451d-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="0451d-115">De weergave van contract details op het tabblad **Verkoop** op de pagina **Project**.</span><span class="sxs-lookup"><span data-stu-id="0451d-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="0451d-116">**Voltooien**</span><span class="sxs-lookup"><span data-stu-id="0451d-116">**Complete**</span></span> |                    <span data-ttu-id="0451d-117">Als het projectwerk is voltooid, kunt u de fase aan **Voltooien**</span><span class="sxs-lookup"><span data-stu-id="0451d-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="0451d-118">Als de projectfase is ingesteld om te voltooien, wordt deze met het werk begrepen volledige 100% is maar wordt het project voor de behandeling of tijd te kosten registreren vermeldingen open verdeeld.</span><span class="sxs-lookup"><span data-stu-id="0451d-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="0451d-119">**Sluiten**</span><span class="sxs-lookup"><span data-stu-id="0451d-119">**Close**</span></span>   |           <span data-ttu-id="0451d-120">Wanneer alle transacties op het project zijn geregistreerd en any u er niet als u verwacht zijn geregistreerd, kunt u de fase aan **Sluiten** handmatig instellen.</span><span class="sxs-lookup"><span data-stu-id="0451d-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="0451d-121">Wanneer het project is ingesteld op **Sluiten** , kunt u niet logboek any more transacties op het project en het project alleen worden gelezen.</span><span class="sxs-lookup"><span data-stu-id="0451d-121">When the project is set to **Close** , you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="0451d-122">Om de status van een project te houden</span><span class="sxs-lookup"><span data-stu-id="0451d-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="0451d-123">Ga naar **Project Service > Projecten**.</span><span class="sxs-lookup"><span data-stu-id="0451d-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="0451d-124">Klik op het project waaraan u wilt werken.</span><span class="sxs-lookup"><span data-stu-id="0451d-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="0451d-125">In de balk die boven aan het scherm wordt weergegeven, selecteert u de pijl-omlaag naast de projectnaam, en klikt u vervolgens op **Projectschattingen**.</span><span class="sxs-lookup"><span data-stu-id="0451d-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="0451d-126">Selecteer **Inspanningen bijhouden** of **Kosten bijhouden** in de vervolgkeuzelijst boven de takenlijst.</span><span class="sxs-lookup"><span data-stu-id="0451d-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="0451d-127">Dubbelklik op elke taak om deze te bewerken.</span><span class="sxs-lookup"><span data-stu-id="0451d-127">Double-click any task to edit it.</span></span> <span data-ttu-id="0451d-128">U kunt de voortgangsbalken in het Gantt-diagram ook of verplaatsen formaat wijzigen om de tijd en de voortgang van een taak wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0451d-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="0451d-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0451d-129">See Also</span></span>  
 [<span data-ttu-id="0451d-130">Projectmanager-handleiding</span><span class="sxs-lookup"><span data-stu-id="0451d-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
