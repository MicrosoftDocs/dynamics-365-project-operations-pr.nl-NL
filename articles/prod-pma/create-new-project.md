---
title: Een nieuw project maken
description: Dit onderwerp bevat informatie over het maken van een nieuw project.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006235"
---
# <a name="create-a-new-project"></a><span data-ttu-id="875fb-103">Een nieuw project maken</span><span class="sxs-lookup"><span data-stu-id="875fb-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="875fb-104">Voer de volgende stappen uit om een nieuw project te maken.</span><span class="sxs-lookup"><span data-stu-id="875fb-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="875fb-105">Selecteer op de pagina **Projectmanagement** de optie **Nieuw project** en voer de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="875fb-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="875fb-106">**Projecttype:** Tijd en materiaal</span><span class="sxs-lookup"><span data-stu-id="875fb-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="875fb-107">**Naam van project:** XYZ-upgrade fase 2</span><span class="sxs-lookup"><span data-stu-id="875fb-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="875fb-108">**Projectgroep:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="875fb-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="875fb-109">**Projectcontract-id:** 00000002</span><span class="sxs-lookup"><span data-stu-id="875fb-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="875fb-110">Selecteer **Project maken**.</span><span class="sxs-lookup"><span data-stu-id="875fb-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="875fb-111">Een resource toewijzen aan een project</span><span class="sxs-lookup"><span data-stu-id="875fb-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="875fb-112">Selecteer op de pagina **Werknemers** in de lijst **Werknemers** de record voor de werknemer voor wie u eerder competenties hebt ingesteld en open de werknemerrecord.</span><span class="sxs-lookup"><span data-stu-id="875fb-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="875fb-113">Ga naar het actievenster op het tabblad **Project** en selecteer in de groep **Instelling** de optie **Projecten toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="875fb-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="875fb-114">Filter op de pagina **Projectopdrachten voor resourcevalidatie**, op het tabblad **Projecten**, in het veld **Het project toevoegen aan geselecteerde projecten**, op het project **XYZ-upgrade fase 2**.</span><span class="sxs-lookup"><span data-stu-id="875fb-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="875fb-115">Selecteer in het deelvenster **Resterende projecten** een project en selecteer vervolgens de pijlknop om het toe te voegen aan het deelvenster **Geselecteerde projecten**.</span><span class="sxs-lookup"><span data-stu-id="875fb-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="875fb-116">U kunt desgewenst ook categorieën aan een resource toewijzen.</span><span class="sxs-lookup"><span data-stu-id="875fb-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="875fb-117">Het categorietype is **Kosten** of **Omzet**.</span><span class="sxs-lookup"><span data-stu-id="875fb-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="875fb-118">Het categorietype wordt bepaald door uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="875fb-118">The category type is determined by your organization.</span></span> <span data-ttu-id="875fb-119">Als er geen categorieën zijn toegewezen aan een resource, zoekt Finance de standaardcategorie voor uurprijzen voor kosten en omzet.</span><span class="sxs-lookup"><span data-stu-id="875fb-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="875fb-120">Projectresource- en rolkenmerken instellen</span><span class="sxs-lookup"><span data-stu-id="875fb-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="875fb-121">Een projectmanager kan de functionaliteit voor het toewijzen van resources aan projecten gebruiken om de rollen te creëren die nodig zijn voor het project.</span><span class="sxs-lookup"><span data-stu-id="875fb-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="875fb-122">Rollen kunnen worden gebruikt als bevestigde resources nog onbekend zijn bij het reserveren van resources.</span><span class="sxs-lookup"><span data-stu-id="875fb-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="875fb-123">Rollen kunnen tijdelijk worden gereserveerd als geplande resources, zodat u kunt doorgaan met de projectplanningsfasen.</span><span class="sxs-lookup"><span data-stu-id="875fb-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="875fb-124">[![Voorbeeld van een rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="875fb-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="875fb-125">**Scenario:** Contoso is ingehuurd om een tijd- en materiaalproject te voltooien dat een goedgekeurd projectcharter heeft.</span><span class="sxs-lookup"><span data-stu-id="875fb-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="875fb-126">De junior projectmanager is nog bezig met het afronden van het bereik van het project.</span><span class="sxs-lookup"><span data-stu-id="875fb-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="875fb-127">De resourcemanager identificeert momenteel specifieke resources die zullen worden gereserveerd om aan het nieuwe project te werken.</span><span class="sxs-lookup"><span data-stu-id="875fb-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="875fb-128">Vanwege de cruciale aard van het project heeft de projectsponsor de senior projectmanager gevraagd een van de rollen op zich te nemen.</span><span class="sxs-lookup"><span data-stu-id="875fb-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="875fb-129">De resourcemanager moet de nieuwe resource verwerven en de rol in het systeem definiëren voor het geval de junior projectmanager de resourcegegevens nodig heeft tijdens de projectplanning.</span><span class="sxs-lookup"><span data-stu-id="875fb-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="875fb-130">De volgende stappen laten zien hoe de resourcemanager de rol van senior projectmanager kan instellen en hieraan resourcekenmerken kan koppelen.</span><span class="sxs-lookup"><span data-stu-id="875fb-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="875fb-131">Later kan de rol worden gebruikt om te zoeken naar beschikbare resources die passen bij de vereiste resourcecompetenties.</span><span class="sxs-lookup"><span data-stu-id="875fb-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="875fb-132">Selecteer op de pagina **Rollen instellen** de optie **Nieuw** en voer de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="875fb-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="875fb-133">**Rol-id:** Senior projectmanager</span><span class="sxs-lookup"><span data-stu-id="875fb-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="875fb-134">**Beschrijving:** Senior projectmanager</span><span class="sxs-lookup"><span data-stu-id="875fb-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="875fb-135">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="875fb-135">Select **Create**.</span></span>
3. <span data-ttu-id="875fb-136">Selecteer de rol **Senior projectmanager** en selecteer vervolgens **Kenmerken configureren**.</span><span class="sxs-lookup"><span data-stu-id="875fb-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="875fb-137">Selecteer in het veld **Kenmerktype** de optie **Vaardigheid**.</span><span class="sxs-lookup"><span data-stu-id="875fb-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="875fb-138">Voer in het veld **Beschikbare kenmerken** de vaardigheid in waarnaar u wilt zoeken.</span><span class="sxs-lookup"><span data-stu-id="875fb-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="875fb-139">Selecteer in het veld **Kenmerktype** de optie **Certificaat**.</span><span class="sxs-lookup"><span data-stu-id="875fb-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="875fb-140">Voer in het veld **Beschikbare kenmerken** het certificaattype in waarnaar u wilt zoeken.</span><span class="sxs-lookup"><span data-stu-id="875fb-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="875fb-141">Een projectresource toewijzen aan een project</span><span class="sxs-lookup"><span data-stu-id="875fb-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="875fb-142">Selecteer op de pagina **Alle projecten** het project **XYZ-upgrade fase 2**.</span><span class="sxs-lookup"><span data-stu-id="875fb-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="875fb-143">Selecteer op het tabblad **Projectteam en planning** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="875fb-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="875fb-144">Selecteer in het veld **Rol** de optie **Teamlid**.</span><span class="sxs-lookup"><span data-stu-id="875fb-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="875fb-145">Selecteer **Boeken vanuiit agenda**.</span><span class="sxs-lookup"><span data-stu-id="875fb-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="875fb-146">Selecteer op de pagina **Beschikbaarheid van resources** de optie **Instellingen weergeven**.</span><span class="sxs-lookup"><span data-stu-id="875fb-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="875fb-147">Voer op de pagina **Weergave-instellingen aanpassen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="875fb-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="875fb-148">**Indeling voor datumbereikweergave:** Dag</span><span class="sxs-lookup"><span data-stu-id="875fb-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="875fb-149">**Beschrijvingen van beschikbaarheid weergeven:** Ja</span><span class="sxs-lookup"><span data-stu-id="875fb-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="875fb-150">**Resterende capaciteit weergeven:** Ja</span><span class="sxs-lookup"><span data-stu-id="875fb-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="875fb-151">Selecteer een resource in de lijst met resources.</span><span class="sxs-lookup"><span data-stu-id="875fb-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="875fb-152">Selecteer **Hard boeken** en **Volledige capaciteit**.</span><span class="sxs-lookup"><span data-stu-id="875fb-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="875fb-153">Een standaardrol aan een resource toewijzen</span><span class="sxs-lookup"><span data-stu-id="875fb-153">Assign a resource to a default role</span></span>

<span data-ttu-id="875fb-154">Als hulpmiddel voor project- of resourcemanagers kan verder worden ingezoomd op de resources die kunnen worden gereserveerd voor een project.</span><span class="sxs-lookup"><span data-stu-id="875fb-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="875fb-155">U kunt een standaardrol koppelen aan een bestaande resource of een nieuw verworven resource.</span><span class="sxs-lookup"><span data-stu-id="875fb-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="875fb-156">Toen Daniel bijvoorbeeld werd aangenomen, had hij de ervaring en vaardigheden om de rol van bedrijfsanalist te vervullen.</span><span class="sxs-lookup"><span data-stu-id="875fb-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="875fb-157">De resourcemanager heeft deze rol als standaardrol toegewezen aan Daniel.</span><span class="sxs-lookup"><span data-stu-id="875fb-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="875fb-158">Daarom heeft de resourcemanager Daniel toegevoegd aan een pool van bedrijfsanalisten die beschikbaar zijn om aan projecten te werken.</span><span class="sxs-lookup"><span data-stu-id="875fb-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="875fb-159">Tijdens het reserveren van resources kunnen projectmanagers de rolresources filteren die beschikbaar zijn om aan projecten te werken.</span><span class="sxs-lookup"><span data-stu-id="875fb-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="875fb-160">Ze kunnen deze informatie als één criterium gebruiken wanneer ze besluitvormingsanalyses op meerdere criteria uitvoeren tijdens het vervullen van resources.</span><span class="sxs-lookup"><span data-stu-id="875fb-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="875fb-161">Zij kunnen ook andere resourcekenmerken aan het filter toevoegen om te zoeken naar resources met specifieke vaardigheden, opleiding en ervaring voor een bepaald project.</span><span class="sxs-lookup"><span data-stu-id="875fb-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="875fb-162">**Scenario:** Er is een goedgekeurd project gestart en de rol van senior projectmanager is tijdens de projectplanningsfase gereserveerd als een geplande resource.</span><span class="sxs-lookup"><span data-stu-id="875fb-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="875fb-163">De resourcemanager heeft nu een resource verworven om de rol van senior projectmanager te vervullen.</span><span class="sxs-lookup"><span data-stu-id="875fb-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="875fb-164">Selecteer op de pagina **Resourcelijst** de naam **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="875fb-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="875fb-165">Selecteer op de pagina **Resourcerol** de optie **Nieuw** en voer de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="875fb-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="875fb-166">**Ingangsdaum:** Voer de huidige datum in.</span><span class="sxs-lookup"><span data-stu-id="875fb-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="875fb-167">**Vervaldatum:** Voer **Nooit** in.</span><span class="sxs-lookup"><span data-stu-id="875fb-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="875fb-168">**Rol:** Voer **Senior projectmanager** in.</span><span class="sxs-lookup"><span data-stu-id="875fb-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="875fb-169">Selecteer **Opslaan** en sluit vervolgens de pagina.</span><span class="sxs-lookup"><span data-stu-id="875fb-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="875fb-170">Voeg op het tabblad **Competenties** de vaardigheid **ProjectMgmt** en het certificaat **PMP** in.</span><span class="sxs-lookup"><span data-stu-id="875fb-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]