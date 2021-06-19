---
title: Mobiele werkruimte Projecttijdinvoer
description: Dit onderwerp bevat informatie over de mobiele werkruimte Projecttijdinvoer. Met deze werkruimte kunnen gebruikers een project invoeren en tijd besparen door hun mobiele apparaat te gebruiken.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f087e15780272fd376a14b42ed9e00420f86a61f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009925"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="ebb20-104">Mobiele werkruimte Projecttijdinvoer</span><span class="sxs-lookup"><span data-stu-id="ebb20-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebb20-105">Dit onderwerp bevat informatie over de mobiele werkruimte **Projecttijdinvoer**.</span><span class="sxs-lookup"><span data-stu-id="ebb20-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="ebb20-106">Met deze werkruimte kunnen gebruikers een project invoeren en tijd besparen door hun mobiele apparaat te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ebb20-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="ebb20-107">Deze mobiele werkruimte is bedoeld om te worden gebruikt met de mobiele app Dynamics 365 Unified Ops.</span><span class="sxs-lookup"><span data-stu-id="ebb20-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="ebb20-108">Samenzicht</span><span class="sxs-lookup"><span data-stu-id="ebb20-108">Overview</span></span>
<span data-ttu-id="ebb20-109">Als onderdeel van hun dagelijkse werk zijn projectresources vaak ter plaatse of onderweg.</span><span class="sxs-lookup"><span data-stu-id="ebb20-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="ebb20-110">Met de mobiele werkruimte **Projecttijdinvoer** kunnen gebruikers hun factureerbare of niet-factureerbare tijd voor een project invoeren op het mobiele apparaat van hun keuze.</span><span class="sxs-lookup"><span data-stu-id="ebb20-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="ebb20-111">Daarom kunnen projectresources altijd en overal tijdregistraties uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="ebb20-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="ebb20-112">Ze kunnen ook tijdvermeldingen bekijken die al zijn vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="ebb20-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="ebb20-113">In de mobiele werkruimte **Projecttijdinvoer** kunnen gebruikers de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="ebb20-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="ebb20-114">Voor een geselecteerde datum het aantal uren invoeren dat u aan een specifieke taak hebt besteed.</span><span class="sxs-lookup"><span data-stu-id="ebb20-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="ebb20-115">Op projectnaam of klant zoeken om het project te vinden waarvoor u tijd wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="ebb20-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="ebb20-116">De categorie en activiteit opgeven voor de tijd die u hebt besteed.</span><span class="sxs-lookup"><span data-stu-id="ebb20-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="ebb20-117">De tijd registreren als factureerbaar of niet-factureerbaar voor het project.</span><span class="sxs-lookup"><span data-stu-id="ebb20-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="ebb20-118">Optioneel externe of interne opmerkingen invoeren.</span><span class="sxs-lookup"><span data-stu-id="ebb20-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ebb20-119">Vereisten</span><span class="sxs-lookup"><span data-stu-id="ebb20-119">Prerequisites</span></span>
<span data-ttu-id="ebb20-120">De vereisten verschillen, afhankelijk van de versie van Microsoft Dynamics 365 die is geïmplementeerd voor uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="ebb20-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="ebb20-121">Vereisten als u Dynamics 365 Finance gebruikt</span><span class="sxs-lookup"><span data-stu-id="ebb20-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="ebb20-122">Als Finance is geïmplementeerd voor uw organisatie, moet het systeembeheerder de mobiele werkruimte **Projecttijdinvoer** publiceren.</span><span class="sxs-lookup"><span data-stu-id="ebb20-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="ebb20-123">Zie [Een mobiele werkruimte publiceren](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace) voor instructies.</span><span class="sxs-lookup"><span data-stu-id="ebb20-123">For instructions, see [Publish a mobile workspace](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="ebb20-124">Vereisten als u versie 1611 met platformupdate 3 of hoger gebruikt</span><span class="sxs-lookup"><span data-stu-id="ebb20-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="ebb20-125">Als versie 1611 met platformupdate 3 of hoger is geïmplementeerd voor uw organisatie, moet de systeembeheerder aan de volgende vereisten voldoen.</span><span class="sxs-lookup"><span data-stu-id="ebb20-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ebb20-126">Vereisten</span><span class="sxs-lookup"><span data-stu-id="ebb20-126">Prerequisite</span></span></th>
<th><span data-ttu-id="ebb20-127">Rol</span><span class="sxs-lookup"><span data-stu-id="ebb20-127">Role</span></span></th>
<th><span data-ttu-id="ebb20-128">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ebb20-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="ebb20-129">Implementeer KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="ebb20-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="ebb20-130">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="ebb20-130">System administrator</span></span></td>
<td><span data-ttu-id="ebb20-131">KB 4018050 is een X++-update of metagegevenshotfix die de mobiele werkruimte <strong>Projecttijdinvoer</strong> bevat.</span><span class="sxs-lookup"><span data-stu-id="ebb20-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="ebb20-132">Als de systeembeheerder KB 4018050 wil implementeren, moeten deze stappen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ebb20-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="ebb20-133"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download de metagegevenshotfix vanuit Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="ebb20-133"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="ebb20-134"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installeer de metagegevenshotfix</a>.</span><span class="sxs-lookup"><span data-stu-id="ebb20-134"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="ebb20-135"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Maak een implementeerbaar pakket</a> dat de modellen <strong>ApplicationSuite</strong> en <strong>projectMobile</strong> bevat en upload vervolgens het implementeerbare pakket naar LCS.</span><span class="sxs-lookup"><span data-stu-id="ebb20-135"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="ebb20-136"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Pas het implementeerbare pakket toe</a>.</span><span class="sxs-lookup"><span data-stu-id="ebb20-136"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebb20-137">Publiceer de mobiele werkruimte <strong>Projecttijdinvoer</strong>.</span><span class="sxs-lookup"><span data-stu-id="ebb20-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="ebb20-138">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="ebb20-138">System administrator</span></span></td>
<td><span data-ttu-id="ebb20-139">Zie <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Een mobiele werkruimte publiceren</a>.</span><span class="sxs-lookup"><span data-stu-id="ebb20-139">See <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="ebb20-140">De mobiele app downloaden en installeren</span><span class="sxs-lookup"><span data-stu-id="ebb20-140">Download and install the mobile app</span></span>

<span data-ttu-id="ebb20-141">De mobiele app Finance and Operations downloaden en installeren:</span><span class="sxs-lookup"><span data-stu-id="ebb20-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="ebb20-142">Voor Android-telefoons</span><span class="sxs-lookup"><span data-stu-id="ebb20-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="ebb20-143">Voor iPhones</span><span class="sxs-lookup"><span data-stu-id="ebb20-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="ebb20-144">Aanmelden bij de mobiele app</span><span class="sxs-lookup"><span data-stu-id="ebb20-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="ebb20-145">Start de app op uw mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="ebb20-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="ebb20-146">Voer uw URL voor Dynamics 365 in.</span><span class="sxs-lookup"><span data-stu-id="ebb20-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="ebb20-147">Wanneer u zich voor het eerst aanmeldt, wordt u om uw gebruikersnaam en wachtwoord gevraagd.</span><span class="sxs-lookup"><span data-stu-id="ebb20-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="ebb20-148">Voer uw referenties in.</span><span class="sxs-lookup"><span data-stu-id="ebb20-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="ebb20-149">Nadat u zich hebt aangemeld, worden de beschikbare werkruimten voor uw bedrijf weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ebb20-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="ebb20-150">Merk op dat als uw systeembeheerder later een nieuwe werkruimte publiceert, u de lijst met mobiele werkruimten moet vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="ebb20-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="ebb20-151">[![Slepen om te vernieuwen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="ebb20-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="ebb20-152">Tijd invoeren met de mobiele werkruimte Projecttijdinvoer</span><span class="sxs-lookup"><span data-stu-id="ebb20-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="ebb20-153">Selecteer op uw mobiele apparaat de werkruimte **Projecttijdinvoer**.</span><span class="sxs-lookup"><span data-stu-id="ebb20-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="ebb20-154">Selecteer **Tijdinvoer**.</span><span class="sxs-lookup"><span data-stu-id="ebb20-154">Select **Time entry**.</span></span> <span data-ttu-id="ebb20-155">De agendadatums voor de huidige week worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ebb20-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="ebb20-156">Selecteer voor een geselecteerde datum **Acties** &gt; **Nieuwe invoer**.</span><span class="sxs-lookup"><span data-stu-id="ebb20-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="ebb20-157">Voer het aantal vast te leggen uren in.</span><span class="sxs-lookup"><span data-stu-id="ebb20-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="ebb20-158">Selecteer het project voor de tijdinvoer.</span><span class="sxs-lookup"><span data-stu-id="ebb20-158">Select the project for the time entry.</span></span> <span data-ttu-id="ebb20-159">Een lijst toont de projecten die in uw app zijn geladen voor offline gebruik.</span><span class="sxs-lookup"><span data-stu-id="ebb20-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="ebb20-160">Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen.</span><span class="sxs-lookup"><span data-stu-id="ebb20-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="ebb20-161">Zie [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ebb20-161">For more information, see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
6.  <span data-ttu-id="ebb20-162">Als uw project niet in de lijst staat, selecteert u **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="ebb20-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="ebb20-163">Zoek op naam of schakel over naar zoeken op projectnaam of klant.</span><span class="sxs-lookup"><span data-stu-id="ebb20-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="ebb20-164">Selecteer een categorie.</span><span class="sxs-lookup"><span data-stu-id="ebb20-164">Select a category.</span></span> <span data-ttu-id="ebb20-165">Een lijst toont de categorieën die in uw app zijn geladen voor offline gebruik.</span><span class="sxs-lookup"><span data-stu-id="ebb20-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="ebb20-166">Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen.</span><span class="sxs-lookup"><span data-stu-id="ebb20-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="ebb20-167">Zie [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ebb20-167">For more information, see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
8.  <span data-ttu-id="ebb20-168">Als uw categorie niet in de lijst staat, selecteert u **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="ebb20-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="ebb20-169">Zoek op categorie of schakel over naar zoeken op categorienaam.</span><span class="sxs-lookup"><span data-stu-id="ebb20-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="ebb20-170">Selecteer een activiteit.</span><span class="sxs-lookup"><span data-stu-id="ebb20-170">Select an activity.</span></span> <span data-ttu-id="ebb20-171">Een lijst toont de activiteiten die in uw app zijn geladen voor offline gebruik.</span><span class="sxs-lookup"><span data-stu-id="ebb20-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="ebb20-172">Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen.</span><span class="sxs-lookup"><span data-stu-id="ebb20-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="ebb20-173">Zie [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ebb20-173">For more information, see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
10. <span data-ttu-id="ebb20-174">Als uw activiteit niet in de lijst staat, selecteert u **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="ebb20-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="ebb20-175">Zoek op activiteitnummer of schakel over naar zoeken op doel.</span><span class="sxs-lookup"><span data-stu-id="ebb20-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="ebb20-176">Selecteer de regeleigenschap.</span><span class="sxs-lookup"><span data-stu-id="ebb20-176">Select the line property.</span></span>
12. <span data-ttu-id="ebb20-177">Optioneel: voer eventuele externe en interne opmerkingen in.</span><span class="sxs-lookup"><span data-stu-id="ebb20-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="ebb20-178">Selecteer **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="ebb20-178">Select **Done**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]