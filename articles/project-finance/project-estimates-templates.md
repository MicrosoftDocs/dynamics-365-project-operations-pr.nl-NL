---
title: Projectschattingen rechtstreeks vanuit Project Service Automation met Finance and Operations synchroniseren
description: In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om schattingen van projecturen en projectonkosten rechtstreeks vanuit Microsoft Dynamics 365 Project Service Automation te synchroniseren met Dynamics 365 Finance.
author: KimANelson
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
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750743"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="ea650-103">Projectschattingen rechtstreeks vanuit Project Service Automation met Finance and Operations synchroniseren</span><span class="sxs-lookup"><span data-stu-id="ea650-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ea650-104">In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om schattingen van projecturen en projectonkosten rechtstreeks vanuit Dynamics 365 Project Service Automation te synchroniseren met Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ea650-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="ea650-105">Projecttaakintegratie, onkostentransactiecategorieën, uurschattingen, onkostenschattingen en functionaliteitsvergrendeling is beschikbaar in versie 8.0.</span><span class="sxs-lookup"><span data-stu-id="ea650-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="ea650-106">Integratie van werkelijke waarden is beschikbaar in versie 8.0.1 of hoger.</span><span class="sxs-lookup"><span data-stu-id="ea650-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="ea650-107">Gegevensstroom voor Project Service Automation naar Finance</span><span class="sxs-lookup"><span data-stu-id="ea650-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="ea650-108">De integratieoplossing van Project Service Automation naar Finance gebruikt de functie Gegevensintegratie om gegevens tussen exemplaren van Project Service Automation en Finance te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="ea650-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="ea650-109">De integratiesjablonen die beschikbaar zijn met de functie Gegevensintegratie maken de stroom van gegevens over schattingen van projecturen en projectonkosten van Project Service Automation naar Finance mogelijk.</span><span class="sxs-lookup"><span data-stu-id="ea650-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ea650-110">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance.</span><span class="sxs-lookup"><span data-stu-id="ea650-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="ea650-111">[![Gegevensstroom voor integratie van Project Service Automation met Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="ea650-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="ea650-112">Projectuurschattingen</span><span class="sxs-lookup"><span data-stu-id="ea650-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="ea650-113">Sjabloon en taken</span><span class="sxs-lookup"><span data-stu-id="ea650-113">Template and tasks</span></span>

<span data-ttu-id="ea650-114">U kunt toegang krijgen tot de beschikbare sjablonen door in het Microsoft Power Apps-beheercentrum de optie **Projecten** te selecteren en vervolgens in de rechterbovenhoek **Nieuw project** te selecteren om openbare sjablonen te kiezen.</span><span class="sxs-lookup"><span data-stu-id="ea650-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ea650-115">De volgende sjabloon en onderliggende taken worden gebruikt om projectuurschattingen van Project Service Automation naar Finance te synchroniseren:</span><span class="sxs-lookup"><span data-stu-id="ea650-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="ea650-116">**Naam van de sjabloon in Gegevensintegratie:** projectuurschattingen (PSA naar Fin en Ops)</span><span class="sxs-lookup"><span data-stu-id="ea650-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="ea650-117">**Naam van de taken in het project:**</span><span class="sxs-lookup"><span data-stu-id="ea650-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="ea650-118">Transactierelaties</span><span class="sxs-lookup"><span data-stu-id="ea650-118">Transaction relationships</span></span>
    - <span data-ttu-id="ea650-119">Onkostenschattingen</span><span class="sxs-lookup"><span data-stu-id="ea650-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="ea650-120">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="ea650-120">Entity set</span></span>

| <span data-ttu-id="ea650-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ea650-121">Project Service Automation</span></span> | <span data-ttu-id="ea650-122">Finance</span><span class="sxs-lookup"><span data-stu-id="ea650-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="ea650-123">Projecttaken</span><span class="sxs-lookup"><span data-stu-id="ea650-123">Project tasks</span></span>              | <span data-ttu-id="ea650-124">Integratie-entiteit voor projectuurschattingen</span><span class="sxs-lookup"><span data-stu-id="ea650-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="ea650-125">Entiteitsstroom</span><span class="sxs-lookup"><span data-stu-id="ea650-125">Entity flow</span></span>

<span data-ttu-id="ea650-126">Projectuurschattingen worden beheerd in Project Service Automation en worden gesynchroniseerd met Finance als projectuurprognoses.</span><span class="sxs-lookup"><span data-stu-id="ea650-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ea650-127">Vereisten</span><span class="sxs-lookup"><span data-stu-id="ea650-127">Prerequisites</span></span>

<span data-ttu-id="ea650-128">Voordat synchronisatie van projectuurschattingen kan plaatsvinden, moet u projecten, projecttaken en transactiecategorieën voor projectonkosten synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="ea650-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="ea650-129">Power-query</span><span class="sxs-lookup"><span data-stu-id="ea650-129">Power Query</span></span>

<span data-ttu-id="ea650-130">In de sjabloon voor projectuurschattingen moet u Microsoft Power Query voor Excel gebruiken om deze taken uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="ea650-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="ea650-131">Stel de standaard prognosemodel-id in die wordt gebruikt wanneer de integratie nieuwe uurprognoses maakt.</span><span class="sxs-lookup"><span data-stu-id="ea650-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="ea650-132">Filter alle resourcespecifieke records in de taak die niet in de uurprognoses kunnen worden geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="ea650-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="ea650-133">Filter eventuele lege transactiecategorierijen uit.</span><span class="sxs-lookup"><span data-stu-id="ea650-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="ea650-134">Als u deze taak niet voltooit, kan dit leiden tot onjuiste uurprognoses.</span><span class="sxs-lookup"><span data-stu-id="ea650-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="ea650-135">Stel de standaard prognosemodel-id in.</span><span class="sxs-lookup"><span data-stu-id="ea650-135">Set the default forecast model ID</span></span>

<span data-ttu-id="ea650-136">U kunt de standaard prognosemodel-id in de sjabloon bijwerken door op de pijl **Toewijzen** te klikken om de toewijzing te openen.</span><span class="sxs-lookup"><span data-stu-id="ea650-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="ea650-137">Selecteer vervolgens de koppeling **Geavanceerde query's en filteren**.</span><span class="sxs-lookup"><span data-stu-id="ea650-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="ea650-138">Als u de standaardsjabloon Projectuurschattingen (PSA naar Fin en Ops) gebruikt, selecteert u **Ingevoegde voorwaarde** in de lijst **Toegepaste stappen**.</span><span class="sxs-lookup"><span data-stu-id="ea650-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="ea650-139">Vervang in de vermelding **Functie** **O\_prognose** door de naam van de prognosemodel-id die moet worden gebruikt met de integratie.</span><span class="sxs-lookup"><span data-stu-id="ea650-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="ea650-140">De standaardsjabloon heeft een prognosemodel-id op basis van de demogegevens.</span><span class="sxs-lookup"><span data-stu-id="ea650-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="ea650-141">Als u een nieuwe sjabloon maakt, moet u deze kolom toevoegen.</span><span class="sxs-lookup"><span data-stu-id="ea650-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="ea650-142">Selecteer in Power Query de optie **Voorwaardelijke kolom toevoegen** en voer een naam in voor de nieuwe kolom, zoals **Model-id**.</span><span class="sxs-lookup"><span data-stu-id="ea650-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="ea650-143">Voer de voorwaarde voor de kolom in, waarbij, als Projecttaak niet null is, \<voer prognosemodel-id in\>; anders null.</span><span class="sxs-lookup"><span data-stu-id="ea650-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="ea650-144">Resourcespecifieke records uitfilteren</span><span class="sxs-lookup"><span data-stu-id="ea650-144">Filter out resource-specific records</span></span>

<span data-ttu-id="ea650-145">De sjabloon Projectuurschattingen (PSA naar Fin en Ops) heeft een standaardfilter dat alle resourcespecifieke records verwijdert.</span><span class="sxs-lookup"><span data-stu-id="ea650-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="ea650-146">Als u uw eigen sjabloon maakt, moet u dit filter toevoegen.</span><span class="sxs-lookup"><span data-stu-id="ea650-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="ea650-147">Selecteer de koppeling **Geavanceerde query's en filteren** om te filteren op de kolom **msdyn\_islinetask** zodat alleen records **False** worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="ea650-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="ea650-148">Lege transactiecategorierijen uitfilteren</span><span class="sxs-lookup"><span data-stu-id="ea650-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="ea650-149">U moet een filter toevoegen om rijen met lege transactiecategorieën te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="ea650-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="ea650-150">Deze taak is vereist, ongeacht of u de standaardsjabloon gebruikt of uw eigen sjabloon maakt.</span><span class="sxs-lookup"><span data-stu-id="ea650-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="ea650-151">Dit filter verwijdert alle overzichtsrijen uit Project Service Automation die ertoe kunnen leiden dat de uurprognoses in Finance onjuist zijn.</span><span class="sxs-lookup"><span data-stu-id="ea650-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="ea650-152">Selecteer de koppeling **Geavanceerde query's en filteren** om null-records in de kolom **msdyn\_transactioncategory\_value** uit te filteren.</span><span class="sxs-lookup"><span data-stu-id="ea650-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ea650-153">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="ea650-153">Template mapping in Data integration</span></span>

<span data-ttu-id="ea650-154">De volgende afbeelding toont een voorbeeld van de toewijzing van sjabloontaken in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="ea650-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="ea650-155">De toewijzing toont de veldinformatie die wordt gesynchroniseerd van Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="ea650-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ea650-156">[![Sjabloontoewijzing](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ea650-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="ea650-157">Projectonkostenschattingen</span><span class="sxs-lookup"><span data-stu-id="ea650-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="ea650-158">Sjabloon en taken</span><span class="sxs-lookup"><span data-stu-id="ea650-158">Template and tasks</span></span>

<span data-ttu-id="ea650-159">De volgende sjabloon en onderliggende taken worden gebruikt om projectonkostenschattingen van Project Service Automation naar Finance te synchroniseren:</span><span class="sxs-lookup"><span data-stu-id="ea650-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="ea650-160">**Naam van de sjabloon in Gegevensintegratie:** projectonkostenschattingen (PSA naar Fin en Ops)</span><span class="sxs-lookup"><span data-stu-id="ea650-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="ea650-161">**Naam van de taken in het project:**</span><span class="sxs-lookup"><span data-stu-id="ea650-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="ea650-162">Transactierelaties</span><span class="sxs-lookup"><span data-stu-id="ea650-162">Transaction relationships</span></span> 
    - <span data-ttu-id="ea650-163">Onkostenschattingen</span><span class="sxs-lookup"><span data-stu-id="ea650-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="ea650-164">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="ea650-164">Entity set</span></span>

| <span data-ttu-id="ea650-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ea650-165">Project Service Automation</span></span> | <span data-ttu-id="ea650-166">Finance</span><span class="sxs-lookup"><span data-stu-id="ea650-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="ea650-167">Transactieverbindingen</span><span class="sxs-lookup"><span data-stu-id="ea650-167">Transaction Connections</span></span>    | <span data-ttu-id="ea650-168">Integratie-entiteit voor projecttransactierelaties</span><span class="sxs-lookup"><span data-stu-id="ea650-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="ea650-169">Schattingsregels</span><span class="sxs-lookup"><span data-stu-id="ea650-169">Estimate Lines</span></span>             | <span data-ttu-id="ea650-170">Integratie-entiteit voor projectonkostenschattingen</span><span class="sxs-lookup"><span data-stu-id="ea650-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="ea650-171">Entiteitsstroom</span><span class="sxs-lookup"><span data-stu-id="ea650-171">Entity flow</span></span>

<span data-ttu-id="ea650-172">Projectonkostenschattingen worden beheerd in Project Service Automation en worden gesynchroniseerd met Finance als projectonkostenprognoses.</span><span class="sxs-lookup"><span data-stu-id="ea650-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ea650-173">Vereisten</span><span class="sxs-lookup"><span data-stu-id="ea650-173">Prerequisites</span></span>

<span data-ttu-id="ea650-174">Voordat synchronisatie van projectonkostenschattingen kan plaatsvinden, moet u projecten, projecttaken en transactiecategorieën voor projectonkosten synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="ea650-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="ea650-175">Power-query</span><span class="sxs-lookup"><span data-stu-id="ea650-175">Power Query</span></span>

<span data-ttu-id="ea650-176">In de sjabloon voor projectonkostenschattingen moet u Power Query gebruiken om de volgende taken uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="ea650-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="ea650-177">Filter om alleen records voor onkostenramingen op te nemen.</span><span class="sxs-lookup"><span data-stu-id="ea650-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="ea650-178">Stel de standaard prognosemodel-id in die wordt gebruikt wanneer de integratie nieuwe uurprognoses maakt.</span><span class="sxs-lookup"><span data-stu-id="ea650-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="ea650-179">Transformeer de factureringstypen.</span><span class="sxs-lookup"><span data-stu-id="ea650-179">Transform the billing types.</span></span>
- <span data-ttu-id="ea650-180">Transformeer de transactietypen.</span><span class="sxs-lookup"><span data-stu-id="ea650-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="ea650-181">Filteren om alleen regels voor kostenschattingen op te nemen</span><span class="sxs-lookup"><span data-stu-id="ea650-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="ea650-182">De sjabloon projectonkostenschattingen (PSA naar Fin en Ops) heeft een standaardfilter dat alleen onkostenregels in de integratie opneemt.</span><span class="sxs-lookup"><span data-stu-id="ea650-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="ea650-183">Als u uw eigen sjabloon maakt, moet u dit filter toevoegen.</span><span class="sxs-lookup"><span data-stu-id="ea650-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="ea650-184">Selecteer de taak **Transactierelaties** en klik vervolgens op de pijl **Toewijzen** om de toewijzing te openen.</span><span class="sxs-lookup"><span data-stu-id="ea650-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="ea650-185">Selecteer de koppeling **Geavanceerde query's en filteren**.</span><span class="sxs-lookup"><span data-stu-id="ea650-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="ea650-186">Filter de kolom **msdyn\_transactiontype1** zodat deze alleen **msdyn\_estimateline** bevat.</span><span class="sxs-lookup"><span data-stu-id="ea650-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="ea650-187">Stel de standaard prognosemodel-id in.</span><span class="sxs-lookup"><span data-stu-id="ea650-187">Set the default forecast model ID</span></span>

<span data-ttu-id="ea650-188">U kunt de standaard prognosemodel-id in de sjabloon bijwerken door de taak **Onkostenschattingen** te selecteren en vervolgens op de pijl **Toewijzen** te klikken om de toewijzing te openen.</span><span class="sxs-lookup"><span data-stu-id="ea650-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="ea650-189">Selecteer de koppeling **Geavanceerde query's en filteren**.</span><span class="sxs-lookup"><span data-stu-id="ea650-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="ea650-190">Als u de standaardsjabloon voor projectonkostenschattingen (PSA naar Fin en Ops) in Power Query gebruikt, selecteert u de eerste optie **Ingevoegde voorwaarde** in de sectie **Toegepaste stappen**.</span><span class="sxs-lookup"><span data-stu-id="ea650-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="ea650-191">Vervang in de vermelding **Functie** **O\_prognose** door de naam van de prognosemodel-id die moet worden gebruikt met de integratie.</span><span class="sxs-lookup"><span data-stu-id="ea650-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="ea650-192">De standaardsjabloon heeft een prognosemodel-id op basis van de demogegevens.</span><span class="sxs-lookup"><span data-stu-id="ea650-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="ea650-193">Als u een nieuwe sjabloon maakt, moet u deze kolom toevoegen.</span><span class="sxs-lookup"><span data-stu-id="ea650-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="ea650-194">Selecteer in Power Query de optie **Voorwaardelijke kolom toevoegen** en voer een naam in voor de nieuwe kolom, zoals **Model-id**.</span><span class="sxs-lookup"><span data-stu-id="ea650-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="ea650-195">Voer de voorwaarde voor de kolom in, waarbij, als Schattingsregel-id niet null is, \<voer prognosemodel-id in\>; anders null.</span><span class="sxs-lookup"><span data-stu-id="ea650-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="ea650-196">De factureringstypen transformeren</span><span class="sxs-lookup"><span data-stu-id="ea650-196">Transform the billing types</span></span>

<span data-ttu-id="ea650-197">De sjabloon Projectonkostenschattingen (PSA naar Fin en Ops) bevat een voorwaardelijke kolom die wordt gebruikt om de factureringstypen te transformeren die tijdens de integratie van Project Service Automation worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="ea650-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="ea650-198">Als u uw eigen sjabloon maakt, moet u deze voorwaardelijke kolom toevoegen.</span><span class="sxs-lookup"><span data-stu-id="ea650-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="ea650-199">Selecteer de koppeling **Geavanceerde query's en filteren** en selecteer vervolgens **Voorwaardelijke kolom toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ea650-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="ea650-200">Voer een naam in voor de nieuwe kolom, zoals **Factureringstype**.</span><span class="sxs-lookup"><span data-stu-id="ea650-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="ea650-201">Voer daarna de volgende voorwaarde in:</span><span class="sxs-lookup"><span data-stu-id="ea650-201">Then enter the following condition:</span></span>

<span data-ttu-id="ea650-202">If **msdyn\_billingtype** = 192350000, then **Niet-toerekenbaar**</span><span class="sxs-lookup"><span data-stu-id="ea650-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="ea650-203">else if **msdyn\_billingtype** = 192350001, then **Toerekenbaar**</span><span class="sxs-lookup"><span data-stu-id="ea650-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="ea650-204">else if **msdyn\_billingtype** = 192350002, then **Gratis**</span><span class="sxs-lookup"><span data-stu-id="ea650-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="ea650-205">else **Niet beschikbaar**</span><span class="sxs-lookup"><span data-stu-id="ea650-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="ea650-206">De transactietypen transformeren</span><span class="sxs-lookup"><span data-stu-id="ea650-206">Transform the transaction types</span></span>

<span data-ttu-id="ea650-207">De sjabloon Projectonkostenschattingen (PSA naar Fin en Ops) bevat een voorwaardelijke kolom die wordt gebruikt om de transactietypen te transformeren die tijdens de integratie van Project Service Automation worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="ea650-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="ea650-208">Als u uw eigen sjabloon maakt, moet u deze voorwaardelijke kolom toevoegen.</span><span class="sxs-lookup"><span data-stu-id="ea650-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="ea650-209">Selecteer de koppeling **Geavanceerde query's en filteren** en selecteer vervolgens **Voorwaardelijke kolom toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ea650-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="ea650-210">Voer een naam in voor de nieuwe kolom, zoals **Transactietype**.</span><span class="sxs-lookup"><span data-stu-id="ea650-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="ea650-211">Voer daarna de volgende voorwaarde in:</span><span class="sxs-lookup"><span data-stu-id="ea650-211">Then enter the following condition:</span></span>

<span data-ttu-id="ea650-212">If **msdyn\_transactiontypecode** = 192350000, then **Kosten**</span><span class="sxs-lookup"><span data-stu-id="ea650-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="ea650-213">else if **msdyn\_transactiontypecode** = 192350005, then **Verkoop**</span><span class="sxs-lookup"><span data-stu-id="ea650-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="ea650-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="ea650-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ea650-215">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="ea650-215">Template mapping in Data integration</span></span>

<span data-ttu-id="ea650-216">De volgende afbeeldingen laten voorbeelden zien van de toewijzingen van sjabloontaken in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="ea650-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="ea650-217">De toewijzing toont de veldinformatie die wordt gesynchroniseerd van Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="ea650-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ea650-218">[![Sjabloontoewijzing](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ea650-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="ea650-219">[![Sjabloontoewijzing](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ea650-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
