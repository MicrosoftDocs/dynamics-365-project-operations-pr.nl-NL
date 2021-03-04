---
title: Algemene boekbare resources toewijzen aan een taak en projectteam
description: Dit onderwerp bevat informatie over het boeken van algemene resources aan taken en projectteams.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 684167f0a68872ef871fbaa06c5161e78045c9a5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145397"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="1cb1e-103">Algemene, boekbare resources toewijzen aan een taak en resourcevereisten genereren</span><span class="sxs-lookup"><span data-stu-id="1cb1e-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1cb1e-104">U kunt niet alleen benoemde of echte resources boeken en toewijzen aan uw project, maar u kunt ook algemene resources toewijzen aan projecttaken.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="1cb1e-105">Deze resources kunnen fungeren als tijdelijke aanduidingen voor benoemde resources totdat u klaar bent om benoemde resources voor uw project te kiezen.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="1cb1e-106">Open in Project Service Automation (PSA) de pagina **Project** en voer op het tabblad **Planning** de positienaam van de algemene resource in de cel **Resource** van de planning in.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="1cb1e-107">Of klik op het pictogram **Resource** in de cel en voer vervolgens in de resourcekiezer de naam in van de algemene resource die u wilt maken.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Een algemeen teamlid maken en toewijzen](media/RM-how-to-9.png)

<span data-ttu-id="1cb1e-109">Het deelvenster **Snelle invoer: Projectteamlid** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="1cb1e-110">Voer de rol en organisatie-eenheid van het algemene resourceteamlid in en klik vervolgens op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Algemeen teamlid snel maken](media/RM-how-to-10.png)

3. <span data-ttu-id="1cb1e-112">Nadat u het nieuwe algemene resourceteamlid hebt gemaakt, wordt dit lid toegewezen aan de taak.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="1cb1e-113">U kunt deze algemene resource blijven toewijzen aan andere taken in de taakplanning.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Bestaand algemeen teamlid toewijzen aan taken](media/RM-how-to-11.png)

4. <span data-ttu-id="1cb1e-115">Nadat u de algemene resource hebt toegewezen, kunt u een resourcevereiste genereren en hieraan voldoen door direct een resourceaanvraag te boeken of in te dienen bij een resourcemanager.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Een vereiste voor een algemeen teamlid genereren](media/RM-how-to-12.png)

<span data-ttu-id="1cb1e-117">In het raster van teamleden kunt u de resourcekiezer niet alleen gebruiken op de hierboven beschreven wijze, maar ook direct algemene resources toevoegen.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="1cb1e-118">De resources worden toegevoegd met een resourcevereiste die is gebaseerd op de begin- en einddatums en toewijzingsmethode die is opgegeven in het deelvenster **Snelle invoer: Projectteamlid**.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="1cb1e-119">U ziet een verschil als u het algemene teamlid rechtstreeks toevoegt en vervolgens meer taken toewijst aan de algemene resource dan er vereiste uren om te dekken zijn.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="1cb1e-120">Klik op **Vereiste genereren** om de vereiste opnieuw te genereren om de vereiste uren af te stemmen met toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="1cb1e-121">U kunt ook op de koppeling **Resourcevereiste** in het teamraster klikken om de vereiste te openen en vaardigheden, voorkeursresources en dergelijke toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Resourcevereiste](media/RM-how-to-13.png)

