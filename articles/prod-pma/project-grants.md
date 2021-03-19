---
title: Projectsubsidies
description: In dit onderwerp wordt uitgelegd hoe u een subsidie kunt aanmaken of wijzigen.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: dfd91e859244cc03b9b358b057bded79eeea0182
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289363"
---
# <a name="project-grants"></a><span data-ttu-id="3d6a7-103">Projectsubsidies</span><span class="sxs-lookup"><span data-stu-id="3d6a7-103">Project grants</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d6a7-104">Een subsidie is een geldschenking voor een specifiek doel of project.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-104">A grant is a gift of money for a specific purpose or project.</span></span> <span data-ttu-id="3d6a7-105">Meestal zijn er beperkingen aan de manier waarop een subsidie kan worden besteed.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-105">Usually, there are restrictions on how a grant can be spent.</span></span> <span data-ttu-id="3d6a7-106">In Projectbeheer en financiële administratie kunt u subsidies invoeren en volgen, en hun relaties voor projecten en projectcontracten definiëren.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-106">In Project management and accounting, you can enter and track grants, and define their relationships to projects and project contracts.</span></span> <span data-ttu-id="3d6a7-107">U kunt bijvoorbeeld de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="3d6a7-107">For example, you can perform the following tasks:</span></span>

- <span data-ttu-id="3d6a7-108">Koppel subsidies aan projecten en financieringsbronnen via koppelingen naar de pagina's **Project** en **Projectcontractdetails**.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-108">Associate grants with projects and funding sources through links to the **Project** and **Project contract details** pages.</span></span>
- <span data-ttu-id="3d6a7-109">Voer wijzigingen in een subsidie in en volg ze bij de overgang van de ene status naar de andere.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-109">Enter and track changes to a grant as it moves from one status to another.</span></span>
- <span data-ttu-id="3d6a7-110">Voer kosten, aangevraagde bedragen en toegekende bedragen in en houd ze bij.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-110">Enter and track costs, requested amounts, and awarded amounts.</span></span>
- <span data-ttu-id="3d6a7-111">Maak hoofdsubsidies en koppel er subbedragen aan.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-111">Create master grants, and associate subgrants with them.</span></span>

<span data-ttu-id="3d6a7-112">U kunt een subsidie aanmaken door alle details in een nieuw record in te voeren, of u kunt de details van een bestaande subsidie kopiëren en deze vervolgens bijwerken.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-112">You can create a grant by entering all the details in a new record, or you can copy the details from an existing grant and then update them.</span></span>

## <a name="create-a-new-grant"></a><span data-ttu-id="3d6a7-113">Een nieuwe subsidie maken</span><span class="sxs-lookup"><span data-stu-id="3d6a7-113">Create a new grant</span></span>

1. <span data-ttu-id="3d6a7-114">Ga naar **Projectmanagement en financiële administratie** \> **Subsidies** \> **Subsidies**.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-114">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="3d6a7-115">Selecteer **Nieuw** \> **Subsidie**.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-115">Select **New** \> **Grant**.</span></span>
3. <span data-ttu-id="3d6a7-116">Voer op de pagina met subsidiedetails op het sneltabblad **Algemeen** in het veld **Subsidie-id** een alfanumerieke id in voor de subsidie.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-116">On the grant details page, on the **General** FastTab, in the **Grant ID** field, enter an alphanumeric identifier for the grant.</span></span>
4. <span data-ttu-id="3d6a7-117">Typ een naam voor de subsidie in het veld **Subsidie**.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-117">In the **Grant name** field, enter a name for the grant.</span></span>
5. <span data-ttu-id="3d6a7-118">Voeg in het veld **Omschrijving** details toe over de nieuwe subsidie.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-118">In the **Description** field, add details about the new grant.</span></span>

    <span data-ttu-id="3d6a7-119">De meeste andere velden op de pagina zijn optioneel en u kunt zo weinig of zo veel informatie invoeren als u wilt.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-119">Most of the other fields on the page are optional, and you can enter as little or as much information as you want.</span></span>

    <span data-ttu-id="3d6a7-120">De volgende lijst beschrijft de informatie die wordt gespecificeerd op elk sneltabblad van de pagina met subsidiedetails:</span><span class="sxs-lookup"><span data-stu-id="3d6a7-120">The following list describes the information that is specified on each FastTab of the grant details page:</span></span>

    - <span data-ttu-id="3d6a7-121">**Algemeen**: voer de naam, de status, de beschrijving, het doel en het bedrag van de subsidie in.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-121">**General** – Enter the grant name, status, description, purpose, and amount.</span></span>
    - <span data-ttu-id="3d6a7-122">**Contactgegevens**: voer details in over personeelsleden, de afdeling die de subsidie beheert en de subsidieontvanger of organisatiebron van de subsidie.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-122">**Contact information** – Enter details about staff members, the department that manages the grant, and the grant customer or organization source of the grant.</span></span> <span data-ttu-id="3d6a7-123">U kunt ook aangeven of uw organisatie een doorgeefentiteit is die de subsidie ontvangt en deze vervolgens doorgeeft aan een andere ontvanger.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-123">You can also indicate whether your organization is a pass-through entity that receives the grant and then passes it on to another recipient.</span></span> <span data-ttu-id="3d6a7-124">Selecteer **Toevoegen** om contactgegevens toe te voegen, zoals telefoonnummers en e-mailadressen voor de organisatie die de subsidie verstrekt.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-124">Select **Add** to add contact information such as telephone numbers and email addresses for the organization that provides the grant.</span></span>
    - <span data-ttu-id="3d6a7-125">**Datums en deadlines**: vul datums in die betrekking hebben op de subsidie en de subsidieaanvraag.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-125">**Dates and deadlines** – Enter dates that are related to the grant and the grant application.</span></span> <span data-ttu-id="3d6a7-126">Voorbeelden zijn de vervaldatum van de aanvraag, de datum van indiening en de datum waarop de subsidie wordt goedgekeurd of afgewezen.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-126">Examples include the application due date, the submission date, and the date when the grant is approved or rejected.</span></span>
    - <span data-ttu-id="3d6a7-127">**Bijbehorende projecten en projectcontracten**: u kunt alleen informatie op dit sneltabblad invoeren als het veld **Subsidiestatus** op het sneltabblad **Algemeen** is ingesteld op **Actief** of **Toegekend**.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-127">**Associated projects and project contracts** – You can enter information on this FastTab only if the **Grant status** field on the **General** FastTab is set to **Active** or **Awarded**.</span></span> <span data-ttu-id="3d6a7-128">Selecteer een van de volgende opties om de gerelateerde taak te voltooien:</span><span class="sxs-lookup"><span data-stu-id="3d6a7-128">Select among the following options to complete the related task:</span></span>

        - <span data-ttu-id="3d6a7-129">**Financieringsbron toevoegen**: voeg een nieuwe financieringsbron toe voor de subsidie.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-129">**Add funding source** – Add a new funding source for the grant.</span></span> <span data-ttu-id="3d6a7-130">U kunt nu alle details invoeren of u kunt de standaardinformatie gebruiken en deze later bijwerken.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-130">You can enter all the details now, or you can use default information and then update it later.</span></span>
        - <span data-ttu-id="3d6a7-131">**Projectcontract toevoegen**: toevoegen of bijwerken van projectcontractinformatie.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-131">**Add project contract** – Add or update project contract information.</span></span>
        - <span data-ttu-id="3d6a7-132">**Project toevoegen**: projectdetails toevoegen of bijwerken.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-132">**Add project** – Add or update project details.</span></span>

    - <span data-ttu-id="3d6a7-133">**Instellen**: voer details in over het afstemmen van de financiering, als deze informatie vereist is.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-133">**Setup** – Enter details about matching funds, if this information is required.</span></span> <span data-ttu-id="3d6a7-134">Veel organisaties die subsidies toekennen, eisen dat ontvangers een bepaald bedrag van hun eigen geld of middelen uitgeven, dat overeenkomt met het bedrag dat in de subsidie wordt toegekend.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-134">Many organizations that award grants require that recipients spend a specific amount of their own money or resources, to match the amount that is awarded in the grant.</span></span> <span data-ttu-id="3d6a7-135">In het veld **Lokaal project of tracking-id** kunt u een id invoeren die verschilt van de project-id.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-135">In the **Local project or tracking ID** field, you can enter an identifier that differs from the project identifier.</span></span>

        > [!NOTE]
        > <span data-ttu-id="3d6a7-136">Als een deel van de subsidie aan een andere organisatie wordt toegekend, stelt u de optie **Subontvanger** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-136">If part of the grant will be awarded to a different organization, set the **Subgrantor** option to **Yes**.</span></span> <span data-ttu-id="3d6a7-137">Voor subsidies die in de Verenigde Staten worden toegekend, kunt u aangeven of een subsidie zal worden toegekend onder een staatsmandaat of een federaal mandaat.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-137">For grants that are awarded in the United States, you can specify whether a grant will be awarded under a state mandate or a federal mandate.</span></span>

    - <span data-ttu-id="3d6a7-138">**Opnamegegevens**: informatie toevoegen of bijwerken over hoe vaak subsidiegelden kunnen worden opgenomen, gefactureerd of uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-138">**Drawdown details** – Add or update information about how often grant funds can be withdrawn, billed for, or spent.</span></span>

## <a name="create-a-new-grant-from-a-copy"></a><span data-ttu-id="3d6a7-139">Een nieuwe subsidie maken op basis van een kopie</span><span class="sxs-lookup"><span data-stu-id="3d6a7-139">Create a new grant from a copy</span></span>

1. <span data-ttu-id="3d6a7-140">Ga naar **Projectmanagement en financiële administratie** \> **Subsidies** \> **Subsidies**.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-140">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="3d6a7-141">Selecteer **Nieuw** \> **Kopiëren van subsidie**.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-141">Select **New** \> **Copy from grant**.</span></span>
3. <span data-ttu-id="3d6a7-142">Voer een alfanumerieke identificatie en een naam in voor de nieuwe subsidie, en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-142">Enter an alphanumeric identifier and a name for the new grant, and then select **OK**.</span></span>
4. <span data-ttu-id="3d6a7-143">Bekijk op de pagina met subsidiegegevens de details van de gekopieerde subsidie en breng de nodige wijzigingen aan.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-143">On the grant details page, review the details of the copied grant, and make any changes that are required.</span></span> <span data-ttu-id="3d6a7-144">De meeste velden op de pagina zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-144">Most of the fields on the page are optional.</span></span>

## <a name="view-or-modify-grant-details"></a><span data-ttu-id="3d6a7-145">Details van subsidie bekijken of wijzigen</span><span class="sxs-lookup"><span data-stu-id="3d6a7-145">View or modify grant details</span></span>

1. <span data-ttu-id="3d6a7-146">Ga naar **Projectmanagement en financiële administratie** \> **Subsidies** \> **Subsidies**.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-146">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="3d6a7-147">Selecteer de subsidie die u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-147">Select the grant to modify.</span></span>
3. <span data-ttu-id="3d6a7-148">Ga naar het actievenster en selecteer op het tabblad **Subsidie** in de groep **Onderhouden** de optie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-148">On the Action Pane, on the **Grant** tab, in the **Maintain** group, select **Edit**.</span></span>
4. <span data-ttu-id="3d6a7-149">Bekijk de details van de subsidie en breng de nodige wijzigingen aan.</span><span class="sxs-lookup"><span data-stu-id="3d6a7-149">Review the grant details, and make any changes that are required.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]