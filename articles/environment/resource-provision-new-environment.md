---
title: Een nieuwe omgeving inrichten
description: Dit onderwerp bevat informatie over het inrichten van een nieuwe Project Operations-omgeving.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a43b947207b6d4276ef27ec996713bf3883e7906
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074451"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="282ec-103">Een nieuwe omgeving inrichten</span><span class="sxs-lookup"><span data-stu-id="282ec-103">Provision a new environment</span></span>

<span data-ttu-id="282ec-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="282ec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="282ec-105">Dit onderwerp bevat informatie over het inrichten van een nieuwe Dynamics 365 Project Operations-omgeving voor scenario's op basis van resources/niet-voorradige artikelen.</span><span class="sxs-lookup"><span data-stu-id="282ec-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="282ec-106">De geautomatiseerde inrichting van Project Operations in een LCS-project inschakelen</span><span class="sxs-lookup"><span data-stu-id="282ec-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="282ec-107">Gebruik de volgende stappen om de geautomatiseerde inrichtingsstroom van Project Operations voor uw LCS-project in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="282ec-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="282ec-108">Ga naar [LCS](https://lcs.dynamics.com/v2) en selecteer de tegel **Beheer previewfunctie**.</span><span class="sxs-lookup"><span data-stu-id="282ec-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="282ec-109">Selecteer **Project Operations** in de lijst **Previewfunctie** en selecteer vervolgens **Previewfunctie ingeschakeld** om Project Operations in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="282ec-109">In the **Preview feature** list, select **Project Operations Feature** , and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="282ec-110">Deze stap wordt slechts één keer per LCS-project uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="282ec-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="282ec-111">Een Project Operations-omgeving inrichten</span><span class="sxs-lookup"><span data-stu-id="282ec-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="282ec-112">Open een nieuwe implementatie van een Dynamics 365 Finance [demo-omgeving](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) of [sandbox-/productieomgeving](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="282ec-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="282ec-113">Volg de wizard **Omgeving inrichten**.</span><span class="sxs-lookup"><span data-stu-id="282ec-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="282ec-114">Zorg ervoor dat de geselecteerde applicatieversie 10.0.13 of hoger is.</span><span class="sxs-lookup"><span data-stu-id="282ec-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="282ec-115">Voor het inrichten van Project Operations selecteert u **Common Data Service** onder **Geavanceerde instellingen**.</span><span class="sxs-lookup"><span data-stu-id="282ec-115">To provision Project Operations, under **Advance settings** , select **Common Data Service**.</span></span> 
4. <span data-ttu-id="282ec-116">Schakel **Common Data Service-instelling** in door **Ja** te selecteren en voer vervolgens informatie in de vereiste velden in:</span><span class="sxs-lookup"><span data-stu-id="282ec-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="282ec-117">Meetcriterium</span><span class="sxs-lookup"><span data-stu-id="282ec-117">Name</span></span>
  - <span data-ttu-id="282ec-118">Regio</span><span class="sxs-lookup"><span data-stu-id="282ec-118">Region</span></span>
  - <span data-ttu-id="282ec-119">Taal</span><span class="sxs-lookup"><span data-stu-id="282ec-119">Language</span></span>
  - <span data-ttu-id="282ec-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="282ec-120">Currency</span></span>
 
5. <span data-ttu-id="282ec-121">Selecteer in het veld **Common Data Service-sjabloon** de optie **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="282ec-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="282ec-122">Selecteer het omgevingstype voor uw implementatie.</span><span class="sxs-lookup"><span data-stu-id="282ec-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="282ec-123">Met een proefversie op basis van een abonnement kunt u een CDS-omgeving gedurende 30 dagen implementeren.</span><span class="sxs-lookup"><span data-stu-id="282ec-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Instellingen voor implementatie](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="282ec-125">Selecteer **Akkoord** om de servicevoorwaarden te erkennen en selecteer vervolgens **Gereed** om terug te keren naar de implementatie-instellingen.</span><span class="sxs-lookup"><span data-stu-id="282ec-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Toestemming voor implementatie](./media/2DeploymentConsent.png)

7. <span data-ttu-id="282ec-127">Vul de overige verplichte velden in de wizard in en bevestig de implementatie.</span><span class="sxs-lookup"><span data-stu-id="282ec-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="282ec-128">Hoe lang het inrichten van de omgeving duurt, is afhankelijk van het type omgeving.</span><span class="sxs-lookup"><span data-stu-id="282ec-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="282ec-129">Het inrichten kan tot zes uur duren.</span><span class="sxs-lookup"><span data-stu-id="282ec-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="282ec-130">Nadat de implementatie met succes is voltooid, wordt de omgeving weergegeven als **Geïmplementeerd**.</span><span class="sxs-lookup"><span data-stu-id="282ec-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="282ec-131">Om te bevestigen dat de omgeving is geïmplementeerd selecteert u **Aanmelden** en meldt u zich aan bij de omgeving om te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="282ec-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Details van -omgevingen](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="282ec-133">Finance-demogegevens van Project Operations toepassen (optionele stap)</span><span class="sxs-lookup"><span data-stu-id="282ec-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="282ec-134">Finance-demogegevens van Project Operations toepassen op een Cloud Hosted Environment met servicerelease 10.0.13 zoals beschreven in [dit artikel](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="282ec-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="282ec-135">Updates toepassen op de Finance-omgeving</span><span class="sxs-lookup"><span data-stu-id="282ec-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="282ec-136">Project Operations vereist een Finance-omgeving met toepassingsversie **10.0.13 (10.0.569.20009)** of hoger.</span><span class="sxs-lookup"><span data-stu-id="282ec-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="282ec-137">Mogelijk moet u kwaliteitsupdates toepassen op uw Finance-omgeving om deze versie te ontvangen.</span><span class="sxs-lookup"><span data-stu-id="282ec-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="282ec-138">Selecteer in LCS op de pagina **Omgevingsdetails** in de sectie **Beschikbare updates** de optie **Updates weergeven**.</span><span class="sxs-lookup"><span data-stu-id="282ec-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Updates weergeven](./media/5ViewUpdates.png)

2. <span data-ttu-id="282ec-140">Selecteer **Pakket opslaan** op de pagina **Binaire updates**.</span><span class="sxs-lookup"><span data-stu-id="282ec-140">On the **Binary updates** page, select **Save package.**</span></span>

![Pakket opslaan](./media/6SavePackage.png)

3. <span data-ttu-id="282ec-142">Klik op **Alles selecteren** en selecteer **Pakket opslaan**.</span><span class="sxs-lookup"><span data-stu-id="282ec-142">Click **Select all** and then select **Save package**.</span></span>

![Updates evalueren en opslaan](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="282ec-144">Voer een naam en een beschrijving van het pakket in en selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="282ec-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="282ec-145">Afhankelijk van de internetverbinding kan dit proces enige tijd duren.</span><span class="sxs-lookup"><span data-stu-id="282ec-145">Depending on the internet connection, this process might take some time.</span></span>

![Pakket uploaden naar Activabibliotheek](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="282ec-147">Selecteer **Gereed** nadat het pakket is opgeslagen in de Activabibliotheek in uw LCS-project.</span><span class="sxs-lookup"><span data-stu-id="282ec-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="282ec-148">Het opslaan en valideren van het pakket kan ongeveer 15 minuten duren.</span><span class="sxs-lookup"><span data-stu-id="282ec-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="282ec-149">Als u de update wilt toepassen, navigeert u naar de pagina **Omgevingsdetails** in LCS en selecteert u **Onderhouden** > **Updates toepassen**.</span><span class="sxs-lookup"><span data-stu-id="282ec-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Omgevingen onderhouden](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="282ec-151">Selecteer in de lijst met updates het pakket dat u hebt gemaakt en selecteer **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="282ec-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Updates toepassen](./media/10ApplyUpdates.png)

<span data-ttu-id="282ec-153">Het onderhouden van de omgeving kan enige tijd duren.</span><span class="sxs-lookup"><span data-stu-id="282ec-153">Environment servicing will take some time.</span></span> <span data-ttu-id="282ec-154">Nadat het is voltooid, keert de omgeving terug naar de geïmplementeerde staat.</span><span class="sxs-lookup"><span data-stu-id="282ec-154">After it is complete, the environment will return to a deployed state.</span></span>

![Omgeving geïmplementeerd](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="282ec-156">Een verbinding voor twee keer wegschrijven tot stand brengen</span><span class="sxs-lookup"><span data-stu-id="282ec-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="282ec-157">Ga in uw LCS-project naar de pagina **Omgevingsdetails**.</span><span class="sxs-lookup"><span data-stu-id="282ec-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="282ec-158">Selecteer onder **Informatie over Common Data Service-omgeving** **Koppelen met CDS voor apps**.</span><span class="sxs-lookup"><span data-stu-id="282ec-158">Under **Common Data Service Environment Information** , select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="282ec-159">Selecteer nadat de koppeling is voltooid opnieuw **Koppelen met CDS voor apps**.</span><span class="sxs-lookup"><span data-stu-id="282ec-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="282ec-160">U wordt doorgestuurd naar Twee keer wegschrijven in Finance.</span><span class="sxs-lookup"><span data-stu-id="282ec-160">You will be redirected to Dual Write in Finance.</span></span>

![Koppeling naar CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="282ec-162">Selecteer **Oplossing toepassen** om toegang te krijgen tot de entiteiten die in de integratie worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="282ec-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Oplossingen toepassen](./media/13ApplySolutions.png)

5. <span data-ttu-id="282ec-164">Selecteer beide oplossingen, **Entiteitstoewijzing voor twee keer wegschrijven in Dynamics 365 Finance and Operations** en **Entiteitstoewijzingen voor twee keer wegschrijven in Dynamics 365 Project Operations** , en selecteer vervolgens **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="282ec-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps** , and then select **Apply**.</span></span>

![Oplossingen bevestigen](./media/14ConfirmSolutions.png)

<span data-ttu-id="282ec-166">Nadat de oplossingen zijn toegepast, worden de entiteiten voor twee keer wegschrijven op de omgeving toegepast.</span><span class="sxs-lookup"><span data-stu-id="282ec-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Oplossingen worden toegepast](./media/15ApplyingSolutions.png)

<span data-ttu-id="282ec-168">Nadat de entiteiten zijn toegepast, worden alle beschikbare toewijzingen in de omgeving weergegeven.</span><span class="sxs-lookup"><span data-stu-id="282ec-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Toewijzingen voor twee keer wegschrijven](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="282ec-170">Vernieuw de gegevensentiteiten na de update</span><span class="sxs-lookup"><span data-stu-id="282ec-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="282ec-171">Ga in Finance naar de werkruimte **Gegevensbeheer**.</span><span class="sxs-lookup"><span data-stu-id="282ec-171">In Finance, go to the **Data management** workspace.</span></span>

![Werkruimte Gegevensbeheer](./media/16DataManagement.png)

2. <span data-ttu-id="282ec-173">Selecteer de tegel **Raamwerkparameters**.</span><span class="sxs-lookup"><span data-stu-id="282ec-173">Select the **Framework parameters** tile.</span></span>

![Raamwerkparameters](./media/17FrameworkParameters.png)

3. <span data-ttu-id="282ec-175">Selecteer op de pagina **Entiteitsinstellingen** de optie **Entiteitslijst vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="282ec-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Entiteitslijst vernieuwen](./media/18RefreshEntityList.png)

<span data-ttu-id="282ec-177">Het vernieuwen duurt ongeveer 20 minuten.</span><span class="sxs-lookup"><span data-stu-id="282ec-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="282ec-178">U ontvangt een melding wanneer dit is voltooid.</span><span class="sxs-lookup"><span data-stu-id="282ec-178">You will receive an alert when it is complete.</span></span>

![Bevestiging vernieuwen](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="282ec-180">Toewijzingen voor twee keer wegschrijven uitvoeren in Project Operations</span><span class="sxs-lookup"><span data-stu-id="282ec-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="282ec-181">Ga in uw LCS-project naar de pagina **Omgevingsdetails**.</span><span class="sxs-lookup"><span data-stu-id="282ec-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="282ec-182">Selecteer onder **Informatie over Common Data Service-omgeving** **Koppelen met CDS voor apps.**</span><span class="sxs-lookup"><span data-stu-id="282ec-182">Under **Common Data Service Environment Information** , select **Link to CDS for Apps.**</span></span> <span data-ttu-id="282ec-183">Nadat u de koppeling hebt geselecteerd, wordt u doorgestuurd naar de lijst met entiteiten in de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="282ec-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="282ec-184">Start de toewijzingen volgens de beschrijving in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="282ec-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="282ec-185">Zorg ervoor dat u de volgorde volgt zoals vermeld.</span><span class="sxs-lookup"><span data-stu-id="282ec-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="282ec-186">**Entiteitstoewijzing**</span><span class="sxs-lookup"><span data-stu-id="282ec-186">**Entity Map**</span></span> | <span data-ttu-id="282ec-187">**Entiteit vernieuwen**</span><span class="sxs-lookup"><span data-stu-id="282ec-187">**Refresh entity**</span></span> | <span data-ttu-id="282ec-188">**Initiële synchronisatie**</span><span class="sxs-lookup"><span data-stu-id="282ec-188">**Initial sync**</span></span> | <span data-ttu-id="282ec-189">**Model voor initiële synchronisatie**</span><span class="sxs-lookup"><span data-stu-id="282ec-189">**Master for initial sync**</span></span> | <span data-ttu-id="282ec-190">**Vereisten voor uitvoeren**</span><span class="sxs-lookup"><span data-stu-id="282ec-190">**Run prerequisites**</span></span> | <span data-ttu-id="282ec-191">**Vereisten voor initiële synchronisatie**</span><span class="sxs-lookup"><span data-stu-id="282ec-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="282ec-192">**Rollen voor projectresources voor alle bedrijven (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="282ec-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="282ec-193">No</span><span class="sxs-lookup"><span data-stu-id="282ec-193">No</span></span> | <span data-ttu-id="282ec-194">Ja</span><span class="sxs-lookup"><span data-stu-id="282ec-194">Yes</span></span> | <span data-ttu-id="282ec-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="282ec-195">Common Data Service</span></span> | <span data-ttu-id="282ec-196">No</span><span class="sxs-lookup"><span data-stu-id="282ec-196">No</span></span> | <span data-ttu-id="282ec-197">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-197">N\A</span></span> |
| <span data-ttu-id="282ec-198">**Rechtspersonen (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="282ec-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="282ec-199">No</span><span class="sxs-lookup"><span data-stu-id="282ec-199">No</span></span> | <span data-ttu-id="282ec-200">Ja</span><span class="sxs-lookup"><span data-stu-id="282ec-200">Yes</span></span> | <span data-ttu-id="282ec-201">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="282ec-201">Finance and Operations apps</span></span> | <span data-ttu-id="282ec-202">No</span><span class="sxs-lookup"><span data-stu-id="282ec-202">No</span></span> | <span data-ttu-id="282ec-203">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-203">N\A</span></span> |
| <span data-ttu-id="282ec-204">**Werkelijke waarden voor integratie van Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="282ec-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="282ec-205">No</span><span class="sxs-lookup"><span data-stu-id="282ec-205">No</span></span> | <span data-ttu-id="282ec-206">No</span><span class="sxs-lookup"><span data-stu-id="282ec-206">No</span></span> | <span data-ttu-id="282ec-207">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-207">N\A</span></span> | <span data-ttu-id="282ec-208">Ja</span><span class="sxs-lookup"><span data-stu-id="282ec-208">Yes</span></span> | <span data-ttu-id="282ec-209">No</span><span class="sxs-lookup"><span data-stu-id="282ec-209">No</span></span> |
| <span data-ttu-id="282ec-210">**Projectcontractregels (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="282ec-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="282ec-211">No</span><span class="sxs-lookup"><span data-stu-id="282ec-211">No</span></span> | <span data-ttu-id="282ec-212">No</span><span class="sxs-lookup"><span data-stu-id="282ec-212">No</span></span> | <span data-ttu-id="282ec-213">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-213">N\A</span></span> | <span data-ttu-id="282ec-214">No</span><span class="sxs-lookup"><span data-stu-id="282ec-214">No</span></span> | <span data-ttu-id="282ec-215">No</span><span class="sxs-lookup"><span data-stu-id="282ec-215">No</span></span> |
| <span data-ttu-id="282ec-216">**Integratie-entiteit voor projecttransactierelaties (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="282ec-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="282ec-217">No</span><span class="sxs-lookup"><span data-stu-id="282ec-217">No</span></span> | <span data-ttu-id="282ec-218">No</span><span class="sxs-lookup"><span data-stu-id="282ec-218">No</span></span> | <span data-ttu-id="282ec-219">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-219">N\A</span></span> | <span data-ttu-id="282ec-220">No</span><span class="sxs-lookup"><span data-stu-id="282ec-220">No</span></span> | <span data-ttu-id="282ec-221">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-221">N\A</span></span> |
| <span data-ttu-id="282ec-222">**Mijlpalen voor de contractregel van Project Operations-integratie (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="282ec-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="282ec-223">No</span><span class="sxs-lookup"><span data-stu-id="282ec-223">No</span></span> | <span data-ttu-id="282ec-224">No</span><span class="sxs-lookup"><span data-stu-id="282ec-224">No</span></span> | <span data-ttu-id="282ec-225">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-225">N\A</span></span> | <span data-ttu-id="282ec-226">No</span><span class="sxs-lookup"><span data-stu-id="282ec-226">No</span></span> | <span data-ttu-id="282ec-227">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-227">N\A</span></span> |
| <span data-ttu-id="282ec-228">**Entiteit voor onkostenramingen van Project Operations-integratie (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="282ec-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="282ec-229">Geen</span><span class="sxs-lookup"><span data-stu-id="282ec-229">No</span></span> | <span data-ttu-id="282ec-230">Geen</span><span class="sxs-lookup"><span data-stu-id="282ec-230">No</span></span> | <span data-ttu-id="282ec-231">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-231">N\A</span></span> | <span data-ttu-id="282ec-232">Geen</span><span class="sxs-lookup"><span data-stu-id="282ec-232">No</span></span> | <span data-ttu-id="282ec-233">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-233">N\A</span></span> |
| <span data-ttu-id="282ec-234">**Entiteit voor exporteren van categorieën met projectonkosten voor Project Operations-integratie (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="282ec-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="282ec-235">Geen</span><span class="sxs-lookup"><span data-stu-id="282ec-235">No</span></span> | <span data-ttu-id="282ec-236">Geen</span><span class="sxs-lookup"><span data-stu-id="282ec-236">No</span></span> | <span data-ttu-id="282ec-237">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-237">N\A</span></span> | <span data-ttu-id="282ec-238">Geen</span><span class="sxs-lookup"><span data-stu-id="282ec-238">No</span></span> | <span data-ttu-id="282ec-239">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-239">N\A</span></span> |
| <span data-ttu-id="282ec-240">**Entiteit voor exporteren van projectkosten voor Project Operations-integratie (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="282ec-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="282ec-241">Ja</span><span class="sxs-lookup"><span data-stu-id="282ec-241">Yes</span></span> | <span data-ttu-id="282ec-242">No</span><span class="sxs-lookup"><span data-stu-id="282ec-242">No</span></span> | <span data-ttu-id="282ec-243">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-243">N\A</span></span> | <span data-ttu-id="282ec-244">No</span><span class="sxs-lookup"><span data-stu-id="282ec-244">No</span></span> | <span data-ttu-id="282ec-245">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-245">N\A</span></span> |
| <span data-ttu-id="282ec-246">**Entiteit voor tijdramingen van Project Operations-integratie (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="282ec-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="282ec-247">Ja</span><span class="sxs-lookup"><span data-stu-id="282ec-247">Yes</span></span> | <span data-ttu-id="282ec-248">No</span><span class="sxs-lookup"><span data-stu-id="282ec-248">No</span></span> | <span data-ttu-id="282ec-249">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-249">N\A</span></span> | <span data-ttu-id="282ec-250">No</span><span class="sxs-lookup"><span data-stu-id="282ec-250">No</span></span> | <span data-ttu-id="282ec-251">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="282ec-251">N\A</span></span> |


4. <span data-ttu-id="282ec-252">Als u de entiteit wilt vernieuwen, selecteert u de toewijzingsnaam en vervolgens **Entiteiten vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="282ec-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Toewijzing vernieuwen](./media/20RefreshMapping.png)

5. <span data-ttu-id="282ec-254">Voer de toewijzing uit nadat het vernieuwen is voltooid.</span><span class="sxs-lookup"><span data-stu-id="282ec-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="282ec-255">Voordat u de volgende toewijzing inschakelt, moet u controleren of de toewijzing in de tabel de status **In uitvoering** heeft.</span><span class="sxs-lookup"><span data-stu-id="282ec-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="282ec-256">Het uitvoeren van toewijzingen met een groot aantal vereisten kan enige tijd duren.</span><span class="sxs-lookup"><span data-stu-id="282ec-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="282ec-257">Om een toewijzing met vereisten uit te voeren, schakelt u de wisselknop **Gerelateerde entiteitstoewijzingen weergeven** in.</span><span class="sxs-lookup"><span data-stu-id="282ec-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="282ec-258">Als in de tabel bij **Vereisten voor initiële synchronisatie** **Nee** wordt aangegeven, controleert u of de markering **Initiële synchronisatie** op **Uit** staat voor alle vereiste toewijzingen voordat u deze uitvoert.</span><span class="sxs-lookup"><span data-stu-id="282ec-258">If the table indicates **Prerequisite initial sync** is **No** , verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Toewijzing uitvoeren](./media/21RunMap.png)

6. <span data-ttu-id="282ec-260">Controleer of alle projectgerelateerde toewijzingen de status actief hebben.</span><span class="sxs-lookup"><span data-stu-id="282ec-260">Validate all project related maps are in the running state.</span></span>

![Alle toewijzingen worden uitgevoerd](./media/22AllMapsRunning.png)

<span data-ttu-id="282ec-262">Uw Project Operations-omgeving is nu ingericht en geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="282ec-262">Your Project Operations environment is now provisioned and configured.</span></span>
