---
title: Aanvullende parametersinstellingen configureren
description: Informatie over aanvullende parametersinstellingen configureren in Project Service
author: JohnPBurrows
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
ms.openlocfilehash: 5ce7ffd635b10689c8295d9349966450f11282d1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129357"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="e3668-103">Aanvullende parametersinstellingen configureren (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e3668-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e3668-104">Nadat u de items in eerdere onderwerpen hebt geconfigureerd, moet u aanvullende projectparameters instellen voor die gebruik in uw projecten.</span><span class="sxs-lookup"><span data-stu-id="e3668-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="e3668-105">Toen u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] voor het eerst installeerde, hebt u een parameterinstelling gemaakt om eerst alle records te maken die voor [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="e3668-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="e3668-106">Nu gaat u terug en configureert u extra velden voor deze instellingen.</span><span class="sxs-lookup"><span data-stu-id="e3668-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="e3668-107">U moet de volgende instellingen hebben geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="e3668-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="e3668-108">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="e3668-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="e3668-109">Factuurfrequentie</span><span class="sxs-lookup"><span data-stu-id="e3668-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="e3668-110">Werkurensjabloon</span><span class="sxs-lookup"><span data-stu-id="e3668-110">Work hours template</span></span>  
  
-   <span data-ttu-id="e3668-111">Prijslijst</span><span class="sxs-lookup"><span data-stu-id="e3668-111">Price list</span></span>  
 
<span data-ttu-id="e3668-112">In deze stap geeft u ook aan welk soort resourcetoewijzing u wenst:</span><span class="sxs-lookup"><span data-stu-id="e3668-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="e3668-113">**Centraal**</span><span class="sxs-lookup"><span data-stu-id="e3668-113">**Central**.</span></span> <span data-ttu-id="e3668-114">Alleen resourcebeheerders kunnen resource toewijzen aan projecten.</span><span class="sxs-lookup"><span data-stu-id="e3668-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="e3668-115">**Hybride**</span><span class="sxs-lookup"><span data-stu-id="e3668-115">**Hybrid**.</span></span> <span data-ttu-id="e3668-116">Resourcebeheerders, projectmanagers en accountmanagers kunnen resources toewijzen aan projecten.</span><span class="sxs-lookup"><span data-stu-id="e3668-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="e3668-117">Als u projectparameters wilt instellen:</span><span class="sxs-lookup"><span data-stu-id="e3668-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="e3668-118">Ga naar **Project Service > Parameters**.</span><span class="sxs-lookup"><span data-stu-id="e3668-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="e3668-119">Klik op de parameterinstelling die u wilt configureren (de instelling die u hebt gemaakt toen u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] voor het eerst installeerde), of klik op **Nieuw** om een nieuwe parameterinstelling te maken.</span><span class="sxs-lookup"><span data-stu-id="e3668-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="e3668-120">Stel in het gebied **Algemeen** alle opties voor uw projectparameters in.</span><span class="sxs-lookup"><span data-stu-id="e3668-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="e3668-121">Klik in het gebied **Prijslijst** op **+** om een prijslijst toe te voegen, selecteer een prijslijst in de vervolgkeuzelijst **Prijslijst voor projectparameters** en klik vervolgens op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e3668-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="e3668-122">Klik rechtsonder in het scherm op de knop **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e3668-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="e3668-123">Om Project Service correct te laten functioneren, moet de projectparameterrecord worden onderhouden.</span><span class="sxs-lookup"><span data-stu-id="e3668-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="e3668-124">Deze record mag niet worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="e3668-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="e3668-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e3668-125">See Also</span></span>  
 [<span data-ttu-id="e3668-126">Resources configureren</span><span class="sxs-lookup"><span data-stu-id="e3668-126">Set up resources</span></span>](../psa/set-up-resources.md)
