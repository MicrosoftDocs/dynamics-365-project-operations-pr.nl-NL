---
title: Werk plannen in Microsoft Project met de invoegtoepassing Project Service | MicrosoftDocs
description: Dit onderwerp bevat informatie over het toevoegen, configureren en gebruiken van de Microsoft project-invoegtoepassing voor Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074694"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="2bcbd-103">Werk plannen in Microsoft Project met de invoegtoepassing Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2bcbd-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="2bcbd-104">Met [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] is het eenvoudiger om uw projectplanning op te zetten, inclusief de schattingen.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-104">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="2bcbd-105">U kunt het werk definiëren zodat kosten, arbeid, en verkopenwaarde helder zijn wanneer het uiteindelijke voorstel wordt ingediend.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="2bcbd-106">Nu kunt u [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] installeren en al het planningwerk uitvoeren in uw vertrouwde [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-omgeving.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="2bcbd-107">U kunt profiteren van de robuuste plannings- en beheersmogelijkheden van [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] en vervolgens uw projectplan bijwerken in Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="2bcbd-108">Als u de functie voor SharePoint-documentbeheer wilt gebruiken om uw [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-bestanden voor [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projecten op te slaan, moet uw [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-beheerder documentbeheer inschakelen.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="2bcbd-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is alleen compatibel met [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="2bcbd-110">De invoegtoepassing downloaden en installeren</span><span class="sxs-lookup"><span data-stu-id="2bcbd-110">Download and install the add-in</span></span>  
 <span data-ttu-id="2bcbd-111">Houd uw aanmeldingsgegevens voor [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] bij de hand.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="2bcbd-112">U hebt deze informatie nodig om vanuit [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] verbinding te maken met [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="2bcbd-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="2bcbd-113">Download vanuit het Downloadcentrum de invoegtoepassing voor uw ondersteunde versie van Project Service, [v2.X](https://go.microsoft.com/fwlink/?linkid=828268) of [v3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="2bcbd-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="2bcbd-114">Klik op de downloadkoppeling.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-114">Click the download link.</span></span>  

3.  <span data-ttu-id="2bcbd-115">Als de download klaar is, klikt u op **Ja** om de invoegtoepassing te installeren.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="2bcbd-116">De invoegtoepassing configureren</span><span class="sxs-lookup"><span data-stu-id="2bcbd-116">Configure the add-in</span></span>  

1. <span data-ttu-id="2bcbd-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] en klik op het tabblad **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="2bcbd-118">Klik op **Verbinding maken**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="2bcbd-119">Voer uw aanmeldingsgegevens in en klik op **Aanmelden**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="2bcbd-120">Nu kunt u de invoegtoepassing gebruiken.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="2bcbd-121">Lezen uit een sjabloon</span><span class="sxs-lookup"><span data-stu-id="2bcbd-121">Read from a template</span></span>  
 <span data-ttu-id="2bcbd-122">Begin uw project te plannen door een sjabloon in te lezen die u in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] hebt gemaakt en naar [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] hebt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2bcbd-123">[Een projectsjabloon maken (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="2bcbd-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="2bcbd-124">Klik op het tabblad **Project Service** op **Lezen** > **Projectsjabloon van Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="2bcbd-125">Kies een projectsjabloon in de lijst en klik op **Openen**</span><span class="sxs-lookup"><span data-stu-id="2bcbd-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="2bcbd-126">Standaard zijn de taken die uit de sjabloon naar Project gekopieerd worden, ingesteld als handmatig gepland.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="2bcbd-127">Rollen in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] toewijzen aan projectresources</span><span class="sxs-lookup"><span data-stu-id="2bcbd-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="2bcbd-128">Open een project en klik op het **Taak** -lint.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="2bcbd-129">Klik op het menu **Gantt-diagram** en kies **Resourceblad**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="2bcbd-130">Klik op het Resourceblad op het vervolgkeuzemenu **Project-service resourcerol** en kies een rol uit Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="2bcbd-131">Resources toewijzen aan uw project</span><span class="sxs-lookup"><span data-stu-id="2bcbd-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="2bcbd-132">Selecteer op het tabblad Project Service een rij en klik op **Resources zoeken**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="2bcbd-133">Selecteer in het scherm **Resource boeken** de resource die u wilt gebruiken voor het project.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="2bcbd-134">Klik achtereenvolgens op **Boeken** en op **OK**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="2bcbd-135">Uw project publiceren</span><span class="sxs-lookup"><span data-stu-id="2bcbd-135">Publish your project</span></span>  
<span data-ttu-id="2bcbd-136">Wanneer de projectplanning is voltooid, moet u het project importeren in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en het publiceren.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="2bcbd-137">Het project wordt geïmporteerd in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="2bcbd-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="2bcbd-138">De processen voor het genereren van prijzen en teams worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="2bcbd-139">Open het project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en controleer of het team, de projectschattingen en de structuur voor werkspecificatie zijn gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="2bcbd-140">In de onderstaande tabel kunt u zien waar u de resultaten kunt vinden:</span><span class="sxs-lookup"><span data-stu-id="2bcbd-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="2bcbd-141">**Gantt-diagram**</span><span class="sxs-lookup"><span data-stu-id="2bcbd-141">**Gantt Chart**</span></span>   | <span data-ttu-id="2bcbd-142">Importbewerkingen in het [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] scherm **Structuur voor werkspecificatie**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="2bcbd-143">**Resourceblad**</span><span class="sxs-lookup"><span data-stu-id="2bcbd-143">**Resource Sheet**</span></span> |   <span data-ttu-id="2bcbd-144">Importbewerkingen in het [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] scherm **Projectteamleden**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="2bcbd-145">**Gebruik gebruiken**</span><span class="sxs-lookup"><span data-stu-id="2bcbd-145">**Use Usage**</span></span>    |    <span data-ttu-id="2bcbd-146">Importbewerkingen in het [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] scherm **Projectschattingen**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="2bcbd-147">**Uw project importeren en publiceren**</span><span class="sxs-lookup"><span data-stu-id="2bcbd-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="2bcbd-148">Klik op het tabblad **Project Service** op **Publiceren** > **Nieuw Project Service Automation-project**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="2bcbd-149">Voer in het dialoogvenster **Publiceren naar een nieuw project in Project Service** de **Projectnaam** in en selecteer de **Klant**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="2bcbd-150">Schakel eventueel de optie **Projectplan aan Project Service Automation koppelen** in om het planbestand uit Project aan Project Service Automation te koppelen.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="2bcbd-151">Klik op **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-151">Click **Publish**.</span></span>  

   <span data-ttu-id="2bcbd-152">Wanneer het Project-bestand aan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] wordt gekoppeld, wordt het Project-bestand het hooftbestand en wordt de structuur voor werkspecificatie in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ingesteld op alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="2bcbd-153">Als u wijzigingen wilt aanbrengen in het projectplan, moet u dat doen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] en deze als updates publiceren naar [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="2bcbd-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="2bcbd-154">Een geïmporteerd project bewerken</span><span class="sxs-lookup"><span data-stu-id="2bcbd-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="2bcbd-155">U hebt twee manieren om wijzigingen door te voeren in een projectplan dat is geïmporteerd in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]:</span><span class="sxs-lookup"><span data-stu-id="2bcbd-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="2bcbd-156">Open het hoofdbestand in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] en bewerk het.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="2bcbd-157">Het bestand ontkoppelen en het rechtstreeks in Project Service bewerken.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="2bcbd-158">Projecten die zijn geüpload vanuit [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] zijn standaard vergrendeld en kunnen alleen in Project worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="2bcbd-159">Als u het bestand wilt bewerken in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], moet u het eerst ontkoppelen.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="2bcbd-160">Bewerken in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="2bcbd-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="2bcbd-161">Klik in het hoofdmenu op **Project Service** > **Projecten**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="2bcbd-162">Open in de lijst met projecten het project dat u hebt gemaakt in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="2bcbd-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="2bcbd-163">Klik in het lint op **Openen in MS Project**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="2bcbd-164">Hiermee wordt het gekoppelde hoofdbestand geopend in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="2bcbd-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="2bcbd-165">Een bestand ontkoppelen en het in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service bewerken</span><span class="sxs-lookup"><span data-stu-id="2bcbd-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="2bcbd-166">Klik in het hoofdmenu op **Project Service** > **Projecten**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="2bcbd-167">Open in de lijst met projecten het project dat u hebt gemaakt in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="2bcbd-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="2bcbd-168">Klik in het lint op **Koppeling met MS Project verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="2bcbd-169">Een Project-bestand uploaden naar SharePoint of Office Groepen</span><span class="sxs-lookup"><span data-stu-id="2bcbd-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="2bcbd-170">U kunt uw Project-bestand uploaden naar SharePoint. U vindt het vervolgens bij de gekoppelde documenten voor uw [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-project.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="2bcbd-171">Uw beheerder moet het SharePoint-documentbeheer configureren en inschakelen voor de entiteit Project.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="2bcbd-172">U kunt uw Project-bestand ook uploaden naar [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], als Office Groepen is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="2bcbd-173">Een bestand uploaden voor SharePoint</span><span class="sxs-lookup"><span data-stu-id="2bcbd-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="2bcbd-174">Klik in het hoofdmenu op **Project Service** > **Uploaden**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="2bcbd-175">Selecteer **Aan projectdocumenten voor Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="2bcbd-176">Selecteer in het dialoogvenster **Openen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] inschakelen** de waarde **Ja** of **Nee**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="2bcbd-177">Als u op **Ja** klikt, kunt u in Project Service Automation de knop **Openen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** selecteren. Hiermee wordt [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] gestart en kunt u het Project-bestand laden vanuit de SharePoint-documentbibliotheek.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="2bcbd-178">Als u op **Nee** klikt, werkt de koppeling voor de knop **Openen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** niet.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="2bcbd-179">U vindt het [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-bestand in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] onder **Documenten** voor het specifieke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-project.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="2bcbd-180">Een bestand uploaden naar Office Groepen</span><span class="sxs-lookup"><span data-stu-id="2bcbd-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="2bcbd-181">Klik in het hoofdmenu op **Project Service** > **Uploaden**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="2bcbd-182">Selecteer **Aan projectdocumenten voor Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="2bcbd-183">Selecteer in het dialoogvenster **Openen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] inschakelen** de waarde **Ja** of **Nee**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="2bcbd-184">Als u op **Ja** klikt, kunt u in Project Service Automation de knop **Openen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** selecteren. Hiermee wordt [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] gestart en kunt u het Project-bestand laden vanuit de SharePoint-documentbibliotheek.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="2bcbd-185">Als u op **Nee** klikt, werkt de koppeling voor de knop **Openen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** niet.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="2bcbd-186">U vindt het [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-bestand in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] onder **Documenten** voor het specifieke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-project.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="2bcbd-187">Uw project publiceren als een sjabloon</span><span class="sxs-lookup"><span data-stu-id="2bcbd-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="2bcbd-188">U kunt uw project opslaan en opnieuw gebruiken door het op te slaan als projectsjabloon in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="2bcbd-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="2bcbd-189">Projectsjablonen zijn herbruikbare projectplannen in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="2bcbd-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2bcbd-190">[Een projectsjabloon maken (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="2bcbd-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="2bcbd-191">Klik op het tabblad **Project Service** op **Publiceren** > **Nieuwe Project Service Automation-projectsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="2bcbd-192">Voer in het dialoogvenster **Publiceren naar een nieuwe Project Service-projectsjabloon** de **Naam van de projectsjabloon** in.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="2bcbd-193">Schakel eventueel de optie **Projectplan aan Project Service Automation koppelen** in om het Project-bestand aan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] te koppelen.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="2bcbd-194">Klik op **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-194">Click **Publish**.</span></span>  

<span data-ttu-id="2bcbd-195">Wanneer het Project-bestand aan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] wordt gekoppeld, wordt het Project-bestand het hooftbestand en wordt de structuur voor werkspecificatie in de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-sjabloon ingesteld op alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="2bcbd-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="2bcbd-196">Als u wijzigingen wilt aanbrengen in het projectplan, moet u dat doen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] en deze als updates publiceren naar [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="2bcbd-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="2bcbd-197">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2bcbd-197">See Also</span></span>  
 [<span data-ttu-id="2bcbd-198">Projectmanager-handleiding</span><span class="sxs-lookup"><span data-stu-id="2bcbd-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
