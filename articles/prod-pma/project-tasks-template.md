---
title: Projecttaken rechtstreeks vanuit Project Service Automation met Finance and Operations synchroniseren
description: In dit onderwerp worden de sjabloon en onderliggende taak beschreven die worden gebruikt om projecttaken rechtstreeks vanuit Microsoft Dynamics 365 Project Service Automation te synchroniseren met Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074546"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="7e4e1-103">Projecttaken rechtstreeks vanuit Project Service Automation met Finance and Operations synchroniseren</span><span class="sxs-lookup"><span data-stu-id="7e4e1-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7e4e1-104">In dit onderwerp worden de sjabloon en onderliggende taak beschreven die worden gebruikt om projecttaken rechtstreeks vanuit Dynamics 365 Project Service Automation te synchroniseren met Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="7e4e1-105">Projecttaakintegratie, onkostentransactiecategorieën, uurschattingen, onkostenschattingen en functionaliteitsvergrendeling zijn beschikbaar in versie 8.0.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="7e4e1-106">Als u Enterprise-editie 7.3.0 gebruikt nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, kunt u de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, uurramingen, onkostenramingen en werkelijke waarden te integreren en om functionaliteitsvergrendeling te configureren.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="7e4e1-107">Als u de boekhoudingsverdelingen moet resetten, raden we u aan ook KB 4131710 te installeren.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="7e4e1-108">Integratie van werkelijke waarden is beschikbaar in versie 8.0.1 of hoger.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="7e4e1-109">Gegevensstroom voor Project Service Automation naar Finance</span><span class="sxs-lookup"><span data-stu-id="7e4e1-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="7e4e1-110">De integratieoplossing van Project Service Automation naar Finance gebruikt de functie Gegevensintegratie om gegevens tussen exemplaren van Project Service Automation en Finance te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="7e4e1-111">De integratiesjabloon die beschikbaar is met de functie Gegevensintegratie maakt de stroom van gegevens over projecttaken van Project Service Automation naar Finance mogelijk.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7e4e1-112">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="7e4e1-113">[![Gegevensstroom voor integratie van Project Service Automation met Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="7e4e1-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="7e4e1-114">Sjabloon en taak</span><span class="sxs-lookup"><span data-stu-id="7e4e1-114">Template and task</span></span>

<span data-ttu-id="7e4e1-115">U kunt toegang krijgen tot de sjabloon in het Microsoft Power Apps-beheercentrum door de optie **Projecten** te selecteren en vervolgens in de rechterbovenhoek **Nieuw project** te selecteren om openbare sjablonen te kiezen.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-115">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="7e4e1-116">De volgende sjabloon en onderliggende taak worden gebruikt om projecttaken van Project Service Automation naar Finance te synchroniseren:</span><span class="sxs-lookup"><span data-stu-id="7e4e1-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="7e4e1-117">**Naam van de sjabloon in Gegevensintegratie:** Projecttaken (PSA naar Fin en Ops)</span><span class="sxs-lookup"><span data-stu-id="7e4e1-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="7e4e1-118">**Naam van de taak in het project:** Projecttaken</span><span class="sxs-lookup"><span data-stu-id="7e4e1-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="7e4e1-119">Voordat synchronisatie van projecttaken kan plaatsvinden, moet u projectcontracten en projecten synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="7e4e1-120">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="7e4e1-120">Entity set</span></span>

| <span data-ttu-id="7e4e1-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7e4e1-121">Project Service Automation</span></span> | <span data-ttu-id="7e4e1-122">Finance</span><span class="sxs-lookup"><span data-stu-id="7e4e1-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="7e4e1-123">Projecttaken</span><span class="sxs-lookup"><span data-stu-id="7e4e1-123">Project Tasks</span></span>              | <span data-ttu-id="7e4e1-124">Integratie-entiteit voor projecttaak</span><span class="sxs-lookup"><span data-stu-id="7e4e1-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="7e4e1-125">Entiteitsstroom</span><span class="sxs-lookup"><span data-stu-id="7e4e1-125">Entity flow</span></span>

<span data-ttu-id="7e4e1-126">Projecttaken worden beheerd in Project Service Automation en worden gesynchroniseerd met Finance als projectactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="7e4e1-127">Vereisten en toewijzingsinstellingen</span><span class="sxs-lookup"><span data-stu-id="7e4e1-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="7e4e1-128">Voordat synchronisatie van projecttaken kan plaatsvinden, moet u projectcontracten en projecten synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="7e4e1-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="7e4e1-129">Power Query</span></span>

<span data-ttu-id="7e4e1-130">U moet Microsoft Power Query voor Excel gebruiken om gegevens te filteren als aan deze voorwaarde is voldaan:</span><span class="sxs-lookup"><span data-stu-id="7e4e1-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="7e4e1-131">U hebt resourcespecifieke records in een projecttaak.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="7e4e1-132">Volg deze richtlijn als u Power Query moet gebruiken:</span><span class="sxs-lookup"><span data-stu-id="7e4e1-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="7e4e1-133">De sjabloon Projecttaken (PSA naar Fin en Ops) heeft een standaardfilter dat resourcespecifieke records uitsluit van een projecttaak door het filter voor **IsLineTask** in te stellen op **False**.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="7e4e1-134">Als u uw eigen sjabloon maakt, moet u dit filter toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7e4e1-135">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="7e4e1-135">Template mapping in Data integration</span></span>

<span data-ttu-id="7e4e1-136">De volgende afbeelding toont een voorbeeld van de toewijzingen van sjabloontaken in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="7e4e1-137">De toewijzing toont de veldinformatie die wordt gesynchroniseerd van Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="7e4e1-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7e4e1-138">[![Sjabloontoewijzing](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="7e4e1-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
