---
title: Projectuitgavencategorieën synchroniseren tussen Finance and Operations en Project Service Automation
description: In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om onkostencategorieën voor projecten te synchroniseren tussen Microsoft Dynamics 365 Finance en Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999845"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="c3911-103">Projectuitgavencategorieën synchroniseren tussen Finance and Operations en Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c3911-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c3911-104">In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om onkostencategorieën voor projecten te synchroniseren tussen Dynamics 365 Finance en Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c3911-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="c3911-105">Projecttaakintegratie, onkostentransactiecategorieën, uurschattingen, onkostenschattingen en functionaliteitsvergrendeling zijn beschikbaar in versie 8.0.</span><span class="sxs-lookup"><span data-stu-id="c3911-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="c3911-106">Integratie van werkelijke waarden is beschikbaar in versie 8.0.1 of hoger.</span><span class="sxs-lookup"><span data-stu-id="c3911-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="c3911-107">Als u Enterprise-editie 7.3.0 gebruikt nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, kunt u de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, uurramingen, onkostenramingen en werkelijke waarden te integreren en om functionaliteitsvergrendeling te configureren.</span><span class="sxs-lookup"><span data-stu-id="c3911-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="c3911-108">Als u de boekhoudingsverdelingen moet resetten, raden we u aan ook KB 4131710 te installeren.</span><span class="sxs-lookup"><span data-stu-id="c3911-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="c3911-109">Gegevensstroom voor Project Service Automation en Finance</span><span class="sxs-lookup"><span data-stu-id="c3911-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="c3911-110">De integratieoplossing van Project Service Automation en Finance gebruikt de functie Gegevensintegratie om gegevens tussen exemplaren van Project Service Automation en Finance te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="c3911-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="c3911-111">De integratiesjablonen die beschikbaar zijn met de functie Gegevensintegratie maken de stroom van gegevens over categorieën voor onkostentransacties tussen Project Service Automation en Finance mogelijk.</span><span class="sxs-lookup"><span data-stu-id="c3911-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="c3911-112">Bij het beheer van de projectonkostencategorieën in Finance, gaat de integratiestroom eerst van Finance naar Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c3911-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="c3911-113">De integratie-id's van de projectonkostencategorieën worden vervolgens bijgewerkt via synchronisatie van Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="c3911-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c3911-114">Bij het beheer van de projectonkostencategorieën in Project Service Automation, gaat de integratiestroom eerst van Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="c3911-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="c3911-115">De projectcategorieën moeten al in Finance zijn geconfigureerd vóór de synchronisatie vanuit Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c3911-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="c3911-116">Synchroniseer vervolgens van Finance terug naar Project Service Automation en vervolgens weer van Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="c3911-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="c3911-117">Op deze manier helpt u te garanderen dat de categorieën zijn gekoppeld en dat er geen duplicaten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c3911-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="c3911-118">Doorgaans worden de projectonkostencategorieën beheerd in Finance.</span><span class="sxs-lookup"><span data-stu-id="c3911-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="c3911-119">Als dit echter niet het geval is, of als er al onkostencategorieën zijn gemaakt in Project Service Automation, moet u eerst synchroniseren met behulp van de sjabloon Projectonkostentransactiecategorieën (PSA to Fin en Ops).</span><span class="sxs-lookup"><span data-stu-id="c3911-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="c3911-120">Synchroniseer vervolgens met behulp van de sjabloon Projectonkostentransactiecategorieën (Fin en Ops naar PSA).</span><span class="sxs-lookup"><span data-stu-id="c3911-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="c3911-121">U moet daarna de synchronisatie van Project Service Automation naar Finance nog een keer uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c3911-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="c3911-122">Als u eerst synchroniseert vanuit Project Service Automation, moet aan de volgende vereisten in Finance worden voldaan voordat de synchronisatie wordt uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="c3911-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="c3911-123">De gedeelde categorie die overeenkomt met de projectcategorie die is ingesteld in Project Service Automation moet bestaan en moet zijn ingeschakeld voor zowel **Project** als **Onkosten**.</span><span class="sxs-lookup"><span data-stu-id="c3911-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="c3911-124">Voor elke rechtspersoon van Finance waarmee moet worden geïntegreerd, moeten de volgende projectcategorieën bestaan:</span><span class="sxs-lookup"><span data-stu-id="c3911-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="c3911-125">**Projectcategorie** bestaat.</span><span class="sxs-lookup"><span data-stu-id="c3911-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="c3911-126">**Gebruik in Onkosten** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c3911-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="c3911-127">**Actief in journaal** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c3911-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="c3911-128">**Transactietype** ingesteld op **Onkosten**.</span><span class="sxs-lookup"><span data-stu-id="c3911-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="c3911-129">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance.</span><span class="sxs-lookup"><span data-stu-id="c3911-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="c3911-130">[![Gegevensstroom voor integratie van Project Service Automation met Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="c3911-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="c3911-131">Synchronisatie van projectonkostencategorieën van Finance naar Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c3911-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="c3911-132">Sjabloon en taak</span><span class="sxs-lookup"><span data-stu-id="c3911-132">Template and task</span></span>

<span data-ttu-id="c3911-133">U kunt toegang krijgen tot de sjabloon in het Microsoft Power Apps-beheercentrum door de optie **Projecten** te selecteren en vervolgens in de rechterbovenhoek **Nieuw project** te selecteren om openbare sjablonen te kiezen.</span><span class="sxs-lookup"><span data-stu-id="c3911-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c3911-134">De volgende sjabloon en onderliggende taak worden gebruikt om projectonkostencategorieën van Finance naar Project Service Automation te synchroniseren:</span><span class="sxs-lookup"><span data-stu-id="c3911-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="c3911-135">**Naam van de sjabloon in Gegevensintegratie:** projectonkostentransactiecategorieën (Fin en Ops naar PSA)</span><span class="sxs-lookup"><span data-stu-id="c3911-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="c3911-136">**Naam van de taak in het project:** synchroniseer categorieën met PSA</span><span class="sxs-lookup"><span data-stu-id="c3911-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="c3911-137">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="c3911-137">Entity set</span></span>

| <span data-ttu-id="c3911-138">Finance</span><span class="sxs-lookup"><span data-stu-id="c3911-138">Finance</span></span>                           | <span data-ttu-id="c3911-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c3911-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="c3911-140">Integratie-entiteit voor categorieën</span><span class="sxs-lookup"><span data-stu-id="c3911-140">Integration entity for categories</span></span> | <span data-ttu-id="c3911-141">Transactiecategorieën</span><span class="sxs-lookup"><span data-stu-id="c3911-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="c3911-142">Entiteitsstroom</span><span class="sxs-lookup"><span data-stu-id="c3911-142">Entity flow</span></span>

<span data-ttu-id="c3911-143">Projectonkostencategorieën worden beheerd in Finance en worden gesynchroniseerd met Project Service Automation als transactiecategorieën.</span><span class="sxs-lookup"><span data-stu-id="c3911-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="c3911-144">Power-query</span><span class="sxs-lookup"><span data-stu-id="c3911-144">Power Query</span></span>

<span data-ttu-id="c3911-145">Wanneer u synchroniseert met Project Service Automation, moet u Microsoft Power Query voor Excel gebruiken om het factureringstype voor de transactiecategorie in te stellen.</span><span class="sxs-lookup"><span data-stu-id="c3911-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="c3911-146">De sjabloon Projectonkostentransactiecategorieën (Fin en Ops naar PSA) biedt een standaardkolom en toewijzing.</span><span class="sxs-lookup"><span data-stu-id="c3911-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="c3911-147">Als u uw eigen sjabloon maakt, moet u een voorwaardelijke kolom toevoegen in Power Query.</span><span class="sxs-lookup"><span data-stu-id="c3911-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="c3911-148">Voer de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="c3911-148">Follow these steps.</span></span>

1. <span data-ttu-id="c3911-149">Klik op de pijl om de toewijzing van de taak voor projectonkostencategorieën te openen in de sjabloon Projectonkostentransactiecategorieën (Fin en Ops naar PSA).</span><span class="sxs-lookup"><span data-stu-id="c3911-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="c3911-150">Klik op de koppeling **Geavanceerde query's en filteren** om Power Query te openen.</span><span class="sxs-lookup"><span data-stu-id="c3911-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="c3911-151">Selecteer **Voorwaardelijke kolom toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c3911-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="c3911-152">Voer een naam in voor de nieuwe kolom, zoals **Factureringstype**.</span><span class="sxs-lookup"><span data-stu-id="c3911-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="c3911-153">Voer de volgende voorwaarde in: **als CATEGORYID niet gelijk is aan null, dan 19235001, anders null**.</span><span class="sxs-lookup"><span data-stu-id="c3911-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="c3911-154">Klik op **OK** in de kolom.</span><span class="sxs-lookup"><span data-stu-id="c3911-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="c3911-155">Zorg ervoor dat u deze nieuwe kolom op de toewijzingspagina toewijst.</span><span class="sxs-lookup"><span data-stu-id="c3911-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="c3911-156">De volgende afbeelding toont een voorbeeld van de toewijzing van sjabloontaken in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="c3911-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="c3911-157">De toewijzing toont de veldinformatie die wordt gesynchroniseerd van Finance naar Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c3911-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="c3911-158">[![Sjabloontoewijzing van projectonkostencategorie naar Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c3911-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="c3911-159">Synchronisatie van projectonkostencategorieën van Project Service Automation naar Finance</span><span class="sxs-lookup"><span data-stu-id="c3911-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="c3911-160">Sjabloon en taak</span><span class="sxs-lookup"><span data-stu-id="c3911-160">Template and task</span></span>

<span data-ttu-id="c3911-161">De volgende sjabloon en onderliggende taak worden gebruikt om projectonkostencategorieën van Project Service Automation naar Finance te synchroniseren:</span><span class="sxs-lookup"><span data-stu-id="c3911-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="c3911-162">**Naam van de sjabloon in Gegevensintegratie:** projectonkostentransactiecategorieën (PSA naar Fin en Ops)</span><span class="sxs-lookup"><span data-stu-id="c3911-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c3911-163">**Naam van de taak in het project:** synchroniseer categorieën met Fin Ops</span><span class="sxs-lookup"><span data-stu-id="c3911-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="c3911-164">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="c3911-164">Entity set</span></span>

| <span data-ttu-id="c3911-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c3911-165">Project Service Automation</span></span> | <span data-ttu-id="c3911-166">Finance</span><span class="sxs-lookup"><span data-stu-id="c3911-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="c3911-167">Transactiecategorieën</span><span class="sxs-lookup"><span data-stu-id="c3911-167">Transaction categories</span></span>     | <span data-ttu-id="c3911-168">Integratie-entiteit voor categorieën</span><span class="sxs-lookup"><span data-stu-id="c3911-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="c3911-169">Entiteitsstroom</span><span class="sxs-lookup"><span data-stu-id="c3911-169">Entity flow</span></span>

<span data-ttu-id="c3911-170">Projectonkostencategorieën worden beheerd in Finance en worden gesynchroniseerd met Project Service Automation als transactiecategorieën.</span><span class="sxs-lookup"><span data-stu-id="c3911-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="c3911-171">Bij de synchronisatie terug naar Finance wordt de projectcategorie bijgewerkt in Finance met de integratie-id's van Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c3911-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c3911-172">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="c3911-172">Template mapping in Data integration</span></span>

<span data-ttu-id="c3911-173">De volgende afbeelding toont een voorbeeld van de toewijzing van sjabloontaken in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="c3911-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="c3911-174">De toewijzing toont de veldinformatie die wordt gesynchroniseerd van Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="c3911-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c3911-175">[![Sjabloontoewijzing van Project Service Automation naar Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c3911-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]