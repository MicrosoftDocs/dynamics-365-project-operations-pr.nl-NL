---
title: Project Operations updaten in uw Finance-omgeving
description: Dit onderwerp bevat informatie over hoe u Project Operations updatet in uw Dynamics 365 Finance-omgeving.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011050"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="8d281-103">Project Operations updaten in uw Finance-omgeving</span><span class="sxs-lookup"><span data-stu-id="8d281-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="8d281-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="8d281-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="8d281-105">Dit onderwerp bevat informatie over hoe u Dynamics 365 Project Operations updatet in uw Dynamics 365 Finance-omgeving.</span><span class="sxs-lookup"><span data-stu-id="8d281-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="8d281-106">Er zijn drie procedures nodig om Project Operations te updaten naar Update 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="8d281-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="8d281-107">Het pakket importeren in uw preview-project</span><span class="sxs-lookup"><span data-stu-id="8d281-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="8d281-108">De update toepassen</span><span class="sxs-lookup"><span data-stu-id="8d281-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="8d281-109">Uw Dataverse-omgeving updaten</span><span class="sxs-lookup"><span data-stu-id="8d281-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="8d281-110">Het pakket importeren in uw LCS-project</span><span class="sxs-lookup"><span data-stu-id="8d281-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="8d281-111">Meld u aan bij [Lifecycle Services (LCS)](https://lcs.dynamics.com/) als projecteigenaar of omgevingsmanager.</span><span class="sxs-lookup"><span data-stu-id="8d281-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="8d281-112">Selecteer in de lijst met projecten uw LCS-project.</span><span class="sxs-lookup"><span data-stu-id="8d281-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="8d281-113">Open op de pagina **Project** in de groep **Omgevingen** de omgeving die u wilt updaten.</span><span class="sxs-lookup"><span data-stu-id="8d281-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="8d281-114">Controleer of de omgeving wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8d281-114">Verify that the environment is running.</span></span> <span data-ttu-id="8d281-115">Start de omgeving als deze niet is gestart.</span><span class="sxs-lookup"><span data-stu-id="8d281-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="8d281-116">Selecteer in de sectie **Nieuwe versie** onder **Beschikbare updates**, **Update weergeven** voor 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="8d281-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Update weergeven-knop](media/view-update.png)

6. <span data-ttu-id="8d281-118">Selecteer op de pagina **Binaire updates** **Pakket opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8d281-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="8d281-119">Selecteer op de pagina **Updates beoordelen en opslaan** **Pakket opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8d281-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="8d281-120">Voer in het deelvenster **Pakket opslaan in de assetbibliotheek** dat wordt geopend, de pakketnaam in en selecteer vervolgens **Pakket opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8d281-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="8d281-121">Wanneer LCS het pakket heeft opgeslagen, wordt de knop **Gereed** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="8d281-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="8d281-122">Selecteer **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="8d281-122">Select **Done**.</span></span> <span data-ttu-id="8d281-123">LCS controleert het pakket.</span><span class="sxs-lookup"><span data-stu-id="8d281-123">LCS will verify the package.</span></span> <span data-ttu-id="8d281-124">Verificatie kan enkele minuten of maximaal een uur duren.</span><span class="sxs-lookup"><span data-stu-id="8d281-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="8d281-125">De pakketupdate toepassen</span><span class="sxs-lookup"><span data-stu-id="8d281-125">Apply the package update</span></span>

1. <span data-ttu-id="8d281-126">Selecteer in LCS, op de pagina **Omgevingsgegevens** **Onderhouden** > **Updates toepassen**.</span><span class="sxs-lookup"><span data-stu-id="8d281-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="8d281-127">Selecteer in de lijst het pakket dat u eerder hebt opgeslagen en selecteer vervolgens **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="8d281-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="8d281-128">Selecteer **Ja** om te bevestigen dat u het pakket wilt implementeren.</span><span class="sxs-lookup"><span data-stu-id="8d281-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Dialoogvenster voor bevestigen van pakketimplementatie](media/confirm-package-deployment.png)

4. <span data-ttu-id="8d281-130">Selecteer **Ja** om te bevestigen dat u de toepassing wilt updaten.</span><span class="sxs-lookup"><span data-stu-id="8d281-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Dialoogvenster voor bevestigen van toepassingsupdate](media/confirm-application-update.png)

<span data-ttu-id="8d281-132">De implementatie en toepassingsupdate worden gestart.</span><span class="sxs-lookup"><span data-stu-id="8d281-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="8d281-133">Op de pagina **Omgevingsgegevens** wordt in de rechterbovenhoek de omgevingsstatus bijgewerkt naar **Onderhoud**.</span><span class="sxs-lookup"><span data-stu-id="8d281-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="8d281-134">Over ongeveer twee uur is de update voltooid.</span><span class="sxs-lookup"><span data-stu-id="8d281-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="8d281-135">De versie-informatie van de toepassing wordt bijgewerkt naar **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** en de omgevingsstatus wordt bijgewerkt naar **Geïmplementeerd**.</span><span class="sxs-lookup"><span data-stu-id="8d281-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="8d281-136">Uw Dataverse-omgeving updaten</span><span class="sxs-lookup"><span data-stu-id="8d281-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="8d281-137">Meld u aan bij het [Power Platform-beheercentrum](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="8d281-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="8d281-138">Zoek en open in de lijst de omgeving die u hebt gebruikt om Project Operations te installeren.</span><span class="sxs-lookup"><span data-stu-id="8d281-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="8d281-139">Selecteer op de pagina **Omgevingen** **Resource** > **Dynamics 365-apps**.</span><span class="sxs-lookup"><span data-stu-id="8d281-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="8d281-140">Zoek in de lijst **Microsoft Dynamics 365 Project Operations** en selecteer in de kolom **Status** **Update beschikbaar**.</span><span class="sxs-lookup"><span data-stu-id="8d281-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="8d281-141">Schakel het selectievakje **Ik ga akkoord met de servicevoorwaarden** in en selecteer vervolgens **Bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="8d281-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="8d281-142">De nieuwste versie van de oplossing wordt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="8d281-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="8d281-143">Nadat de installatie is voltooid, hebt u versie 4.5.0.134 geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="8d281-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="8d281-144">Nieuwe functies configureren</span><span class="sxs-lookup"><span data-stu-id="8d281-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="8d281-145">Toewijzing van twee keer wegschrijven inschakelen</span><span class="sxs-lookup"><span data-stu-id="8d281-145">Enable dual-write mapping</span></span>

<span data-ttu-id="8d281-146">Nadat u de update in de Finance en Dataverse-omgevingen hebt afgerond, kunt u de vereiste toewijzingen voor twee keer wegschrijven inschakelen.</span><span class="sxs-lookup"><span data-stu-id="8d281-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="8d281-147">Doorloop de volgend procedures om toewijzingen voor twee keer wegschrijven in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="8d281-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="8d281-148">De beveiligingsinstellingen in de Customer Engagement-omgeving bijwerken</span><span class="sxs-lookup"><span data-stu-id="8d281-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="8d281-149">Gegevenseenheden vernieuwen</span><span class="sxs-lookup"><span data-stu-id="8d281-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="8d281-150">De toewijzingen voor twee keer wegschrijven bijwerken en uitvoeren</span><span class="sxs-lookup"><span data-stu-id="8d281-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="8d281-151">De beveiligingsinstellingen in de Dataverse-omgeving bijwerken</span><span class="sxs-lookup"><span data-stu-id="8d281-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="8d281-152">De volgende updates van de beveiligingsbevoegdheden voor entiteiten zijn vereist als onderdeel van de update naar UR5.</span><span class="sxs-lookup"><span data-stu-id="8d281-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="8d281-153">Ga in uw Dataverse-omgeving naar **Instellingen** en selecteer in de groep **Systeem** **Beveiliging**.</span><span class="sxs-lookup"><span data-stu-id="8d281-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Dataverse-omgevingsinstellingen](media/Picture21.png)

2. <span data-ttu-id="8d281-155">Selecteer **Beveiligingsrollen**.</span><span class="sxs-lookup"><span data-stu-id="8d281-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="8d281-156">Selecteer uit de lijst met rollen **Twee keer wegschrijven app-gebruiker** en selecteer het tabblad **Aangepaste entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="8d281-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="8d281-157">Controleer of de rol de machtigingen **Lezen** en **Toevoegen aan** heeft voor:</span><span class="sxs-lookup"><span data-stu-id="8d281-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="8d281-158">**Type valutawisselkoers**</span><span class="sxs-lookup"><span data-stu-id="8d281-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="8d281-159">**Rekeningschema**</span><span class="sxs-lookup"><span data-stu-id="8d281-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="8d281-160">**Fiscale kalender**</span><span class="sxs-lookup"><span data-stu-id="8d281-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="8d281-161">**Grootboek**</span><span class="sxs-lookup"><span data-stu-id="8d281-161">**Ledger**</span></span>

5. <span data-ttu-id="8d281-162">Ga nadat de beveiligingsrol is bijgewerkt naar **Instellingen** > **Beveiliging** > **Teams**.</span><span class="sxs-lookup"><span data-stu-id="8d281-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="8d281-163">Controleer of de rol **twee keer wegschrijven app-gebruiker** is toegepast op het team.</span><span class="sxs-lookup"><span data-stu-id="8d281-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="8d281-164">Gegevensentiteiten uit de update vernieuwen</span><span class="sxs-lookup"><span data-stu-id="8d281-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="8d281-165">Open in uw Finance-omgeving de werkruimte **Gegevensbeheer** en vervolgens de pagina **Framework-parameters**.</span><span class="sxs-lookup"><span data-stu-id="8d281-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="8d281-166">Selecteer op het tabblad **Entiteitsinstellingen** **Entiteitenlijst vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="8d281-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="8d281-167">Selecteer **Sluiten** om het vernieuwen van de entiteit te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="8d281-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="8d281-168">Dit proces neemt ongeveer 20 minuten in beslag.</span><span class="sxs-lookup"><span data-stu-id="8d281-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="8d281-169">U krijgt een melding wanneer het vernieuwen is voltooid.</span><span class="sxs-lookup"><span data-stu-id="8d281-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="8d281-170">Toewijzingen voor twee keer wegschrijven bijwerken</span><span class="sxs-lookup"><span data-stu-id="8d281-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="8d281-171">Selecteer in de werkruimte **Gegevensbeheer** **Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="8d281-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="8d281-172">Selecteer **Oplossingen toepassen**, selecteer beide oplossingen in de lijst en selecteer vervolgens **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="8d281-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="8d281-173">Selecteer op de pagina **Twee keer wegschrijven** de volgende tabeltoewijzingen en selecteer vervolgens **Stoppen**.</span><span class="sxs-lookup"><span data-stu-id="8d281-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="8d281-174">**Werkelijke waarden voor integratie van Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="8d281-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="8d281-175">**Projectonkostencategorieën voor integratie van Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="8d281-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="8d281-176">**Werkelijke waarden voor projectonkosten exportentiteit voor integratie van Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="8d281-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="8d281-177">Pas op de pagina **Versie tabeltoewijzing** een nieuwe versie van de toewijzing toe op elk van de drie entiteiten.</span><span class="sxs-lookup"><span data-stu-id="8d281-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="8d281-178">Selecteer uitvoeren op de pagina **Twee keer wegschrijven** om de toewijzingen opnieuw op te starten.</span><span class="sxs-lookup"><span data-stu-id="8d281-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="8d281-179">Selecteer in de lijst met toewijzingen de toewijzing **Grootboek (msdyn_ledgers)** met alle vereisten en schakel het selectievakje **Eerste synchronisatie** in.</span><span class="sxs-lookup"><span data-stu-id="8d281-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="8d281-180">Selecteer in het veld **Master voor eerste synchronisatie** **Finance and Operations-apps** en selecteer vervolgens **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="8d281-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Synchronisatie van grootboektoewijzing](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]