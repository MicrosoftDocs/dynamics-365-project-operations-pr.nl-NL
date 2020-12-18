---
title: Projectsjablonen ontwikkelen met Project kopiëren
description: Dit onderwerp bevat informatie over het maken van projectsjablonen met de aangepaste actie Project kopiëren.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642402"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="4cbc5-103">Projectsjablonen ontwikkelen met Project kopiëren</span><span class="sxs-lookup"><span data-stu-id="4cbc5-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="4cbc5-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="4cbc5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4cbc5-105">Dynamics 365 Project Operations ondersteunt de mogelijkheid om een project te kopiëren en eventuele toewijzingen terug te zetten naar de algemene resources die de rol vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="4cbc5-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="4cbc5-106">Klanten kunnen deze functionaliteit gebruiken om eenvoudige projectsjablonen te maken.</span><span class="sxs-lookup"><span data-stu-id="4cbc5-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="4cbc5-107">Als u **Project kopiëren** selecteert, wordt de status van het doelproject bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="4cbc5-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="4cbc5-108">Gebruik **Reden van status** om te bepalen wanneer de kopieeractie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="4cbc5-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="4cbc5-109">Door **Project kopiëren** te selecteren, wordt ook de begindatum van het project bijgewerkt naar de huidige begindatum als er geen streefdatum wordt gedetecteerd in de doelprojectentiteit.</span><span class="sxs-lookup"><span data-stu-id="4cbc5-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="4cbc5-110">Aangepaste actie Project kopiëren</span><span class="sxs-lookup"><span data-stu-id="4cbc5-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="4cbc5-111">Meetcriterium</span><span class="sxs-lookup"><span data-stu-id="4cbc5-111">Name</span></span> 

<span data-ttu-id="4cbc5-112">**msdyn_CopyprojectV2**</span><span class="sxs-lookup"><span data-stu-id="4cbc5-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="4cbc5-113">Invoerparameters</span><span class="sxs-lookup"><span data-stu-id="4cbc5-113">Input parameters</span></span>
<span data-ttu-id="4cbc5-114">Er zijn drie invoerparameters:</span><span class="sxs-lookup"><span data-stu-id="4cbc5-114">There are three input parameters:</span></span>

| <span data-ttu-id="4cbc5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cbc5-115">Parameter</span></span>          | <span data-ttu-id="4cbc5-116">Type</span><span class="sxs-lookup"><span data-stu-id="4cbc5-116">Type</span></span>   | <span data-ttu-id="4cbc5-117">Waarden</span><span class="sxs-lookup"><span data-stu-id="4cbc5-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="4cbc5-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="4cbc5-118">ProjectCopyOption</span></span>  | <span data-ttu-id="4cbc5-119">String</span><span class="sxs-lookup"><span data-stu-id="4cbc5-119">String</span></span> | <span data-ttu-id="4cbc5-120">**{"removeNamedResources":true}** of **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="4cbc5-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="4cbc5-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="4cbc5-121">SourceProject</span></span>      | <span data-ttu-id="4cbc5-122">Entiteitverwijzing</span><span class="sxs-lookup"><span data-stu-id="4cbc5-122">Entity Reference</span></span> | <span data-ttu-id="4cbc5-123">Bronproject</span><span class="sxs-lookup"><span data-stu-id="4cbc5-123">Source Project</span></span> |
| <span data-ttu-id="4cbc5-124">Doel</span><span class="sxs-lookup"><span data-stu-id="4cbc5-124">Target</span></span>             | <span data-ttu-id="4cbc5-125">Entiteitverwijzing</span><span class="sxs-lookup"><span data-stu-id="4cbc5-125">Entity Reference</span></span> | <span data-ttu-id="4cbc5-126">Doelproject</span><span class="sxs-lookup"><span data-stu-id="4cbc5-126">Target Project</span></span> |


- <span data-ttu-id="4cbc5-127">**{"clearTeamsAndAssignments":true}**: het standaardgedrag voor Project for the Web; hiermee worden alle toewijzingen en teamleden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="4cbc5-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="4cbc5-128">**{"removeNamedResources":true}**: het standaardgedrag voor Project Operations; hiermee worden toewijzingen teruggezet naar algemene resources.</span><span class="sxs-lookup"><span data-stu-id="4cbc5-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="4cbc5-129">Zie [Web-API -acties gebruiken](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions) voor meer standaardwaarden voor acties.</span><span class="sxs-lookup"><span data-stu-id="4cbc5-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="4cbc5-130">Te kopiëren velden opgeven</span><span class="sxs-lookup"><span data-stu-id="4cbc5-130">Specify fields to copy</span></span> 
<span data-ttu-id="4cbc5-131">Wanneer de actie wordt aangeroepen, wordt met **Project kopiëren** de projectweergave **Projectkolommen kopiëren** gecontroleerd om te bepalen welke velden moeten worden gekopieerd wanneer het project wordt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="4cbc5-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
