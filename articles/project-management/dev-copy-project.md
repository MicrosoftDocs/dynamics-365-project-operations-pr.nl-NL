---
title: Projectsjablonen ontwikkelen met Project kopiëren
description: Dit onderwerp bevat informatie over het maken van projectsjablonen met de aangepaste actie Project kopiëren.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 27847575e2d6ec9af77d24f756b13d3aeb0efea7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286917"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="22797-103">Projectsjablonen ontwikkelen met Project kopiëren</span><span class="sxs-lookup"><span data-stu-id="22797-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="22797-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="22797-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="22797-105">Dynamics 365 Project Operations ondersteunt de mogelijkheid om een project te kopiëren en eventuele toewijzingen terug te zetten naar de algemene resources die de rol vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="22797-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="22797-106">Klanten kunnen deze functionaliteit gebruiken om eenvoudige projectsjablonen te maken.</span><span class="sxs-lookup"><span data-stu-id="22797-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="22797-107">Als u **Project kopiëren** selecteert, wordt de status van het doelproject bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="22797-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="22797-108">Gebruik **Reden van status** om te bepalen wanneer de kopieeractie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="22797-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="22797-109">Door **Project kopiëren** te selecteren, wordt ook de begindatum van het project bijgewerkt naar de huidige begindatum als er geen streefdatum wordt gedetecteerd in de doelprojectentiteit.</span><span class="sxs-lookup"><span data-stu-id="22797-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="22797-110">Aangepaste actie Project kopiëren</span><span class="sxs-lookup"><span data-stu-id="22797-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="22797-111">Meetcriterium</span><span class="sxs-lookup"><span data-stu-id="22797-111">Name</span></span> 

<span data-ttu-id="22797-112">**msdyn_CopyprojectV2**</span><span class="sxs-lookup"><span data-stu-id="22797-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="22797-113">Invoerparameters</span><span class="sxs-lookup"><span data-stu-id="22797-113">Input parameters</span></span>
<span data-ttu-id="22797-114">Er zijn drie invoerparameters:</span><span class="sxs-lookup"><span data-stu-id="22797-114">There are three input parameters:</span></span>

| <span data-ttu-id="22797-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="22797-115">Parameter</span></span>          | <span data-ttu-id="22797-116">Type</span><span class="sxs-lookup"><span data-stu-id="22797-116">Type</span></span>   | <span data-ttu-id="22797-117">Waarden</span><span class="sxs-lookup"><span data-stu-id="22797-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="22797-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="22797-118">ProjectCopyOption</span></span>  | <span data-ttu-id="22797-119">String</span><span class="sxs-lookup"><span data-stu-id="22797-119">String</span></span> | <span data-ttu-id="22797-120">**{"removeNamedResources":true}** of **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="22797-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="22797-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="22797-121">SourceProject</span></span>      | <span data-ttu-id="22797-122">Entiteitverwijzing</span><span class="sxs-lookup"><span data-stu-id="22797-122">Entity Reference</span></span> | <span data-ttu-id="22797-123">Bronproject</span><span class="sxs-lookup"><span data-stu-id="22797-123">Source Project</span></span> |
| <span data-ttu-id="22797-124">Doel</span><span class="sxs-lookup"><span data-stu-id="22797-124">Target</span></span>             | <span data-ttu-id="22797-125">Entiteitverwijzing</span><span class="sxs-lookup"><span data-stu-id="22797-125">Entity Reference</span></span> | <span data-ttu-id="22797-126">Doelproject</span><span class="sxs-lookup"><span data-stu-id="22797-126">Target Project</span></span> |


- <span data-ttu-id="22797-127">**{"clearTeamsAndAssignments":true}**: het standaardgedrag voor Project for the Web; hiermee worden alle toewijzingen en teamleden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="22797-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="22797-128">**{"removeNamedResources":true}**: het standaardgedrag voor Project Operations; hiermee worden toewijzingen teruggezet naar algemene resources.</span><span class="sxs-lookup"><span data-stu-id="22797-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="22797-129">Zie [Web-API -acties gebruiken](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions) voor meer standaardwaarden voor acties.</span><span class="sxs-lookup"><span data-stu-id="22797-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="22797-130">Te kopiëren velden opgeven</span><span class="sxs-lookup"><span data-stu-id="22797-130">Specify fields to copy</span></span> 
<span data-ttu-id="22797-131">Wanneer de actie wordt aangeroepen, wordt met **Project kopiëren** de projectweergave **Projectkolommen kopiëren** gecontroleerd om te bepalen welke velden moeten worden gekopieerd wanneer het project wordt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="22797-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="22797-132">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="22797-132">Example</span></span>
<span data-ttu-id="22797-133">Het volgende voorbeeld laat zien hoe u de aangepaste actie **CopyProject** kunt aanroepen met de parameter **removeNamedResources** ingesteld.</span><span class="sxs-lookup"><span data-stu-id="22797-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]