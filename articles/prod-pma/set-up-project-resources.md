---
title: Projectresources opzetten
description: Dit onderwerp bevat informatie over het instellen of aanvragen van projectresources.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288733"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="84135-103">Projectresources opzetten</span><span class="sxs-lookup"><span data-stu-id="84135-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84135-104">U moet een agenda opstellen en deze aan een medewerker of werknemer koppelen.</span><span class="sxs-lookup"><span data-stu-id="84135-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="84135-105">De agenda wordt gebruikt om het project en de werktijd van de resources die voor het project zijn gereserveerd in te plannen.</span><span class="sxs-lookup"><span data-stu-id="84135-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="84135-106">Tijdens het instellen van de agenda kunnen projectmanagers resourcenivellering uitvoeren als onderdeel van resource-optimalisatie.</span><span class="sxs-lookup"><span data-stu-id="84135-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="84135-107">Op basis van het agendaschema kunnen beperkingen worden opgelegd aan resources.</span><span class="sxs-lookup"><span data-stu-id="84135-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="84135-108">U kunt een agenda opzetten op de pagina **Agenda's**.</span><span class="sxs-lookup"><span data-stu-id="84135-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="84135-109">Wanneer u een werknemer instelt als projectresource, kunt u kiezen uit werknemers die werken in het bedrijf waarvoor u resources instelt.</span><span class="sxs-lookup"><span data-stu-id="84135-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="84135-110">U kunt ook werknemers van andere bedrijven in uw organisatie selecteren.</span><span class="sxs-lookup"><span data-stu-id="84135-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="84135-111">Deze werknemers worden intercompany-resources genoemd.</span><span class="sxs-lookup"><span data-stu-id="84135-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="84135-112">In de volgende procedures wordt uitgelegd hoe u een werknemer instelt als projectresource in uw bedrijf en hoe u een intercompany-projectresource instelt.</span><span class="sxs-lookup"><span data-stu-id="84135-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="84135-113">Een werknemer instellen als projectresource</span><span class="sxs-lookup"><span data-stu-id="84135-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="84135-114">Selecteer op de pagina **Werknemers** in de lijst **Werknemers** de werknemer die u toevoegt als een projectresource. Open vervolgens de werknemerrecord.</span><span class="sxs-lookup"><span data-stu-id="84135-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="84135-115">Selecteer in het actievenster de optie **Project** &gt; **Instelling** &gt; **Project instellen**.</span><span class="sxs-lookup"><span data-stu-id="84135-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="84135-116">Selecteer een agenda en sluit vervolgens de pagina.</span><span class="sxs-lookup"><span data-stu-id="84135-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="84135-117">U kunt ook standaardprojecten voor een resource specificeren als een soort toewijzing vooraf.</span><span class="sxs-lookup"><span data-stu-id="84135-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="84135-118">Toewijzingen vooraf kunnen worden gebruikt wanneer de resourcemanager of projectmanager van tevoren weet aan welke projecten de resource zal werken.</span><span class="sxs-lookup"><span data-stu-id="84135-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="84135-119">Toewijzingen vooraf kunnen ook plaatsvinden op verzoek van een projectsponsor of klant.</span><span class="sxs-lookup"><span data-stu-id="84135-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="84135-120">Als u een project vooraf wilt toewijzen, gaat u naar de pagina **Projecten toewijzen**, tabblad **Projecten** en selecteert u het juiste project in de lijst **Resterende projecten**.</span><span class="sxs-lookup"><span data-stu-id="84135-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="84135-121">Een intercompany-resource instellen</span><span class="sxs-lookup"><span data-stu-id="84135-121">Set up an intercompany resource</span></span>

<span data-ttu-id="84135-122">Wanneer u een werknemer instelt als intercompany-resource, moet u de instellingen zowel in het uitlenende bedrijf als in het lenende bedrijf uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="84135-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="84135-123">In het uitlenende bedrijf</span><span class="sxs-lookup"><span data-stu-id="84135-123">In the lending company</span></span>

1. <span data-ttu-id="84135-124">Controleer in Finance of het uitlenende bedrijf is geselecteerd en voltooi vervolgens de procedure in de vorige sectie, "Een werknemer instellen als projectresource".</span><span class="sxs-lookup"><span data-stu-id="84135-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="84135-125">Selecteer **Nieuw** op de pagina **Intercompany-boekhouding**.</span><span class="sxs-lookup"><span data-stu-id="84135-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="84135-126">Selecteer het uitlenende bedrijf in het veld **Id van rechtspersoon**.</span><span class="sxs-lookup"><span data-stu-id="84135-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="84135-127">Vul de resterende velden in en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="84135-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="84135-128">Selecteer **Nieuw** op de pagina **Verrekenprijs**.</span><span class="sxs-lookup"><span data-stu-id="84135-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="84135-129">Selecteer het juiste bedrijf in het veld **Lenende rechtspersoon**.</span><span class="sxs-lookup"><span data-stu-id="84135-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="84135-130">Als u aan het lenende bedrijf alleen de resource wilt uitlenen die u aan het begin van deze sectie in het veld **Resource** hebt gemaakt, selecteert u e naam van de resource die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="84135-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="84135-131">Als u alle resources in het uitlenende bedrijf ter beschikking wilt stellen aan het lenende bedrijf, laat u het veld **Resource** leeg.</span><span class="sxs-lookup"><span data-stu-id="84135-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="84135-132">Stel op de pagina **Parameters voor Projectmanagement en financiële administratie**, op het tabblad **Intercompany**, de optie **Intercompany-resourceplanning en urenstaten inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="84135-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="84135-133">In het lenende bedrijf</span><span class="sxs-lookup"><span data-stu-id="84135-133">In the borrowing company</span></span>

- <span data-ttu-id="84135-134">Voer op de pagina **Lijst met resources**, in het zoekfilter de naam in van de resource die u voor het uitlenende bedrijf hebt gemaakt, om te controleren of de naam is opgenomen in de resourcelijst voor het lenende bedrijf.</span><span class="sxs-lookup"><span data-stu-id="84135-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="84135-135">Aanvragen van projectresources</span><span class="sxs-lookup"><span data-stu-id="84135-135">Request project resources</span></span>
<span data-ttu-id="84135-136">Met de functionaliteit voor het plannen van projectresources kunnen resourcemanagers alleen bemande resources verdelen over opdrachten of projecten.</span><span class="sxs-lookup"><span data-stu-id="84135-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="84135-137">Als u deze functionaliteit wilt inschakelen, voert u de volgende taken uit of controleert u of deze zijn voltooid:</span><span class="sxs-lookup"><span data-stu-id="84135-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="84135-138">Nummerreeksen instellen.</span><span class="sxs-lookup"><span data-stu-id="84135-138">Set up number sequences.</span></span>
- <span data-ttu-id="84135-139">Werkstromen voor projectbeheer en boekhouding instellen.</span><span class="sxs-lookup"><span data-stu-id="84135-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="84135-140">Werkstromen voor resourceaanvragen inschakelen.</span><span class="sxs-lookup"><span data-stu-id="84135-140">Enable resource request workflows.</span></span>

<span data-ttu-id="84135-141">Nadat de voorgaande taken zijn voltooid, kunt u naar behoefte de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="84135-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="84135-142">Een resourceaanvraag op basis van een voorlopig geboekte bemande resource.</span><span class="sxs-lookup"><span data-stu-id="84135-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="84135-143">Resourceaanvragen bewaken.</span><span class="sxs-lookup"><span data-stu-id="84135-143">Monitor resource requests.</span></span>
- <span data-ttu-id="84135-144">Resourceaanvragen afhandelen.</span><span class="sxs-lookup"><span data-stu-id="84135-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="84135-145">Een bemande resource aanvragen vanuit een WBS.</span><span class="sxs-lookup"><span data-stu-id="84135-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="84135-146">Resources voor een project zonder dat u een bemande resource hoeft aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="84135-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]