---
title: Een nieuwe omgeving inrichten
description: Dit onderwerp bevat informatie over het inrichten van een nieuwe Project Operations-omgeving.
author: sigitac
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d0712d9d5dfc6c35ccd07142ff5948f50e6a254c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995480"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="8c6c2-103">Een nieuwe omgeving inrichten</span><span class="sxs-lookup"><span data-stu-id="8c6c2-103">Provision a new environment</span></span>

<span data-ttu-id="8c6c2-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="8c6c2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8c6c2-105">Dit onderwerp bevat informatie over het inrichten van een nieuwe Dynamics 365 Project Operations-omgeving voor scenario's op basis van resources/niet-voorradige artikelen.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="8c6c2-106">De geautomatiseerde inrichting van Project Operations in een LCS-project inschakelen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="8c6c2-107">Gebruik de volgende stappen om de geautomatiseerde inrichtingsstroom van Project Operations voor uw LCS-project in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="8c6c2-108">Ga naar [LCS](https://lcs.dynamics.com/v2) en selecteer de tegel **Beheer previewfunctie**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="8c6c2-109">Selecteer **Project Operations** in de lijst **Previewfunctie** en selecteer vervolgens **Previewfunctie ingeschakeld** om Project Operations in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="8c6c2-110">Deze stap wordt slechts één keer per LCS-project uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="8c6c2-111">Een Project Operations-omgeving inrichten</span><span class="sxs-lookup"><span data-stu-id="8c6c2-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="8c6c2-112">Open een nieuwe implementatie van een Dynamics 365 Finance [demo-omgeving](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) of [sandbox-/productieomgeving](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="8c6c2-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="8c6c2-113">Volg de wizard **Omgeving inrichten**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8c6c2-114">Zorg ervoor dat de geselecteerde applicatieversie 10.0.13 of hoger is.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="8c6c2-115">Voor het inrichten van Project Operations selecteert u **Common Data Service** onder **Geavanceerde instellingen**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="8c6c2-116">Schakel **Common Data Service-instelling** in door **Ja** te selecteren en voer vervolgens informatie in de vereiste velden in:</span><span class="sxs-lookup"><span data-stu-id="8c6c2-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="8c6c2-117">Meetcriterium</span><span class="sxs-lookup"><span data-stu-id="8c6c2-117">Name</span></span>
  - <span data-ttu-id="8c6c2-118">Regio</span><span class="sxs-lookup"><span data-stu-id="8c6c2-118">Region</span></span>
  - <span data-ttu-id="8c6c2-119">Taal</span><span class="sxs-lookup"><span data-stu-id="8c6c2-119">Language</span></span>
  - <span data-ttu-id="8c6c2-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="8c6c2-120">Currency</span></span>
 
5. <span data-ttu-id="8c6c2-121">Selecteer in het veld **Common Data Service-sjabloon** de optie **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="8c6c2-122">Selecteer het omgevingstype voor uw implementatie.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="8c6c2-123">Met een proefversie op basis van een abonnement kunt u een CDS-omgeving gedurende 30 dagen implementeren.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Instellingen voor implementatie](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="8c6c2-125">Selecteer **Akkoord** om de servicevoorwaarden te erkennen en selecteer vervolgens **Gereed** om terug te keren naar de implementatie-instellingen.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Toestemming voor implementatie](./media/2DeploymentConsent.png)

7. <span data-ttu-id="8c6c2-127">Optioneel - Pas demogegevens toe op de omgeving.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="8c6c2-128">Ga naar **Geavanceerde instellingen**, selecteer **SQL-databaseconfiguratie aanpassen** en stel **Een gegevensset opgeven voor de toepassingsdatabase** in op **Demo**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="8c6c2-129">Vul de overige verplichte velden in de wizard in en bevestig de implementatie.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="8c6c2-130">De tijd die nodig is om de omgeving in te richten, is afhankelijk van het omgevingstype.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="8c6c2-131">Het inrichten kan tot zes uur duren.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="8c6c2-132">Nadat de implementatie met succes is voltooid, wordt de omgeving weergegeven als **Geïmplementeerd**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="8c6c2-133">Selecteer om te bevestigen dat de omgeving met succes is geïmplementeerd **Aanmelden** en meld u aan bij de omgeving om te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Details van -omgevingen](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="8c6c2-135">Updates toepassen op de Finance-omgeving</span><span class="sxs-lookup"><span data-stu-id="8c6c2-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="8c6c2-136">Project Operations vereist een Finance-omgeving met toepassingsversie **10.0.13 (10.0.569.20009)** of hoger.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="8c6c2-137">Mogelijk moet u kwaliteitsupdates toepassen op uw Finance-omgeving om deze versie te ontvangen.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="8c6c2-138">Selecteer in LCS op de pagina **Omgevingsdetails** in de sectie **Beschikbare updates** de optie **Updates weergeven**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Updates weergeven](./media/5ViewUpdates.png)

2. <span data-ttu-id="8c6c2-140">Selecteer **Pakket opslaan** op de pagina **Binaire updates**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-140">On the **Binary updates** page, select **Save package.**</span></span>

![Pakket opslaan](./media/6SavePackage.png)

3. <span data-ttu-id="8c6c2-142">Klik op **Alles selecteren** en selecteer **Pakket opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-142">Click **Select all** and then select **Save package**.</span></span>

![Updates evalueren en opslaan](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="8c6c2-144">Voer een naam en een beschrijving van het pakket in en selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="8c6c2-145">Afhankelijk van de internetverbinding kan dit proces enige tijd duren.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-145">Depending on the internet connection, this process might take some time.</span></span>

![Pakket uploaden naar Activabibliotheek](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="8c6c2-147">Selecteer **Gereed** nadat het pakket is opgeslagen in de Activabibliotheek in uw LCS-project.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="8c6c2-148">Het opslaan en valideren van het pakket kan ongeveer 15 minuten duren.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="8c6c2-149">Als u de update wilt toepassen, navigeert u naar de pagina **Omgevingsdetails** in LCS en selecteert u **Onderhouden** > **Updates toepassen**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Omgevingen onderhouden](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="8c6c2-151">Selecteer in de lijst met updates het pakket dat u hebt gemaakt en selecteer **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Updates toepassen](./media/10ApplyUpdates.png)

<span data-ttu-id="8c6c2-153">Het onderhouden van de omgeving kan enige tijd duren.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-153">Environment servicing will take some time.</span></span> <span data-ttu-id="8c6c2-154">Nadat het is voltooid, keert de omgeving terug naar de geïmplementeerde staat.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-154">After it is complete, the environment will return to a deployed state.</span></span>

![Omgeving geïmplementeerd](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="8c6c2-156">Een verbinding voor twee keer wegschrijven tot stand brengen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="8c6c2-157">Ga in uw LCS-project naar de pagina **Omgevingsdetails**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8c6c2-158">Selecteer onder **Informatie over Common Data Service-omgeving** **Koppelen met CDS voor apps**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="8c6c2-159">Selecteer nadat de koppeling is voltooid opnieuw **Koppelen met CDS voor apps**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="8c6c2-160">U wordt doorgestuurd naar Twee keer wegschrijven in Finance.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-160">You will be redirected to Dual Write in Finance.</span></span>

![Koppeling naar CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="8c6c2-162">Selecteer **Oplossing toepassen** om toegang te krijgen tot de entiteiten die in de integratie worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Oplossingen toepassen](./media/13ApplySolutions.png)

5. <span data-ttu-id="8c6c2-164">Selecteer beide oplossingen, **Dynamics 365 Finance and Operations-entiteitstoewijzing voor twee keer wegschrijven** en **Dynamics 365 Project Operations-entiteitstoewijzingen voor twee keer wegschrijven** en selecteer vervolgens **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Oplossingen bevestigen](./media/14ConfirmSolutions.png)

<span data-ttu-id="8c6c2-166">Nadat de oplossingen zijn toegepast, worden de entiteiten voor twee keer wegschrijven op de omgeving toegepast.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Oplossingen worden toegepast](./media/15ApplyingSolutions.png)

<span data-ttu-id="8c6c2-168">Nadat de entiteiten zijn toegepast, worden alle beschikbare toewijzingen in de omgeving weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Toewijzingen voor twee keer wegschrijven](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="8c6c2-170">Vernieuw de gegevensentiteiten na de update</span><span class="sxs-lookup"><span data-stu-id="8c6c2-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="8c6c2-171">Ga in Finance naar de werkruimte **Gegevensbeheer**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-171">In Finance, go to the **Data management** workspace.</span></span>

![Werkruimte Gegevensbeheer](./media/16DataManagement.png)

2. <span data-ttu-id="8c6c2-173">Selecteer de tegel **Raamwerkparameters**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-173">Select the **Framework parameters** tile.</span></span>

![Raamwerkparameters](./media/17FrameworkParameters.png)

3. <span data-ttu-id="8c6c2-175">Selecteer op de pagina **Entiteitsinstellingen** de optie **Entiteitslijst vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Entiteitslijst vernieuwen](./media/18RefreshEntityList.png)

<span data-ttu-id="8c6c2-177">Het vernieuwen duurt ongeveer 20 minuten.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="8c6c2-178">U ontvangt een melding wanneer dit is voltooid.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-178">You will receive an alert when it is complete.</span></span>

![Bevestiging vernieuwen](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="8c6c2-180">Beveiligingsinstellingen bijwerken in Project Operations in Dataverse</span><span class="sxs-lookup"><span data-stu-id="8c6c2-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="8c6c2-181">Ga naar Project Operations in uw Dataverse-omgeving.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="8c6c2-182">Ga naar **Instellingen** > **Beveiliging** > **Beveiligingsrollen**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="8c6c2-183">Selecteer op de pagina **Beveiligingsrollen** in de lijst met rollen **Twee keer wegschrijven app-gebruiker** en selecteer het tabblad **Aangepaste entiteiten**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="8c6c2-184">Controleer of de rol de machtigingen **Lezen** en **Toevoegen aan** heeft voor:</span><span class="sxs-lookup"><span data-stu-id="8c6c2-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="8c6c2-185">**Type valutawisselkoers**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="8c6c2-186">**Rekeningschema**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="8c6c2-187">**Fiscale kalender**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="8c6c2-188">**Grootboek**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-188">**Ledger**</span></span>

5. <span data-ttu-id="8c6c2-189">Ga nadat de beveiligingsrol is bijgewerkt naar **Instellingen** > **Beveiliging** > **Teams** en selecteer het standaardteam in de teamweergave **Lokale bedrijfseigenaar**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="8c6c2-190">Selecteer **Rollen beheren** en controleer of de beveiligingsbevoegdheid **twee keer wegschrijven app-gebruiker** is toegepast op dit team.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="8c6c2-191">Toewijzingen voor twee keer wegschrijven uitvoeren in Project Operations</span><span class="sxs-lookup"><span data-stu-id="8c6c2-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="8c6c2-192">Ga in uw LCS-project naar de pagina **Omgevingsdetails**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8c6c2-193">Selecteer onder **Informatie over Common Data Service-omgeving** **Koppelen met CDS voor apps.**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="8c6c2-194">Nadat u de koppeling hebt geselecteerd, wordt u doorgestuurd naar de lijst met entiteiten in de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="8c6c2-195">Start de toewijzingen volgens de beschrijving in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="8c6c2-196">Zorg ervoor dat u de volgorde volgt zoals vermeld.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="8c6c2-197">**Entiteitstoewijzing**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-197">**Entity Map**</span></span> | <span data-ttu-id="8c6c2-198">**Entiteit vernieuwen**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-198">**Refresh entity**</span></span> | <span data-ttu-id="8c6c2-199">**Initiële synchronisatie**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-199">**Initial sync**</span></span> | <span data-ttu-id="8c6c2-200">**Model voor initiële synchronisatie**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-200">**Master for initial sync**</span></span> | <span data-ttu-id="8c6c2-201">**Vereisten voor uitvoeren**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-201">**Run prerequisites**</span></span> | <span data-ttu-id="8c6c2-202">**Vereisten voor initiële synchronisatie**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="8c6c2-203">**Rollen voor projectresources voor alle bedrijven (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="8c6c2-204">Geen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-204">No</span></span> | <span data-ttu-id="8c6c2-205">Ja</span><span class="sxs-lookup"><span data-stu-id="8c6c2-205">Yes</span></span> | <span data-ttu-id="8c6c2-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8c6c2-206">Common Data Service</span></span> | <span data-ttu-id="8c6c2-207">Geen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-207">No</span></span> | <span data-ttu-id="8c6c2-208">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-208">N\A</span></span> |
| <span data-ttu-id="8c6c2-209">**Rechtspersonen (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="8c6c2-210">Geen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-210">No</span></span> | <span data-ttu-id="8c6c2-211">Ja</span><span class="sxs-lookup"><span data-stu-id="8c6c2-211">Yes</span></span> | <span data-ttu-id="8c6c2-212">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="8c6c2-212">Finance and Operations apps</span></span> | <span data-ttu-id="8c6c2-213">Geen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-213">No</span></span> | <span data-ttu-id="8c6c2-214">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-214">N\A</span></span> |
| <span data-ttu-id="8c6c2-215">**Grootboek (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="8c6c2-216">Geen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-216">No</span></span> | <span data-ttu-id="8c6c2-217">Ja</span><span class="sxs-lookup"><span data-stu-id="8c6c2-217">Yes</span></span> | <span data-ttu-id="8c6c2-218">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="8c6c2-218">Finance and Operations apps</span></span> | <span data-ttu-id="8c6c2-219">Ja</span><span class="sxs-lookup"><span data-stu-id="8c6c2-219">Yes</span></span> | <span data-ttu-id="8c6c2-220">Ja, Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="8c6c2-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="8c6c2-221">**Werkelijke waarden voor integratie van Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="8c6c2-222">Geen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-222">No</span></span> | <span data-ttu-id="8c6c2-223">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-223">No</span></span> | <span data-ttu-id="8c6c2-224">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-224">N\A</span></span> | <span data-ttu-id="8c6c2-225">Ja</span><span class="sxs-lookup"><span data-stu-id="8c6c2-225">Yes</span></span> | <span data-ttu-id="8c6c2-226">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-226">No</span></span> |
| <span data-ttu-id="8c6c2-227">**Projectcontractregels (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="8c6c2-228">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-228">No</span></span> | <span data-ttu-id="8c6c2-229">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-229">No</span></span> | <span data-ttu-id="8c6c2-230">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-230">N\A</span></span> | <span data-ttu-id="8c6c2-231">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-231">No</span></span> | <span data-ttu-id="8c6c2-232">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-232">No</span></span> |
| <span data-ttu-id="8c6c2-233">**Integratie-entiteit voor projecttransactierelaties (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="8c6c2-234">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-234">No</span></span> | <span data-ttu-id="8c6c2-235">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-235">No</span></span> | <span data-ttu-id="8c6c2-236">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-236">N\A</span></span> | <span data-ttu-id="8c6c2-237">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-237">No</span></span> | <span data-ttu-id="8c6c2-238">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-238">N\A</span></span> |
| <span data-ttu-id="8c6c2-239">**Mijlpalen voor de contractregel van Project Operations-integratie (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="8c6c2-240">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-240">No</span></span> | <span data-ttu-id="8c6c2-241">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-241">No</span></span> | <span data-ttu-id="8c6c2-242">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-242">N\A</span></span> | <span data-ttu-id="8c6c2-243">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-243">No</span></span> | <span data-ttu-id="8c6c2-244">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-244">N\A</span></span> |
| <span data-ttu-id="8c6c2-245">**Entiteit voor onkostenramingen van Project Operations-integratie (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="8c6c2-246">Geen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-246">No</span></span> | <span data-ttu-id="8c6c2-247">Geen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-247">No</span></span> | <span data-ttu-id="8c6c2-248">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-248">N\A</span></span> | <span data-ttu-id="8c6c2-249">Geen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-249">No</span></span> | <span data-ttu-id="8c6c2-250">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-250">N\A</span></span> |
| <span data-ttu-id="8c6c2-251">**Entiteit voor exporteren van categorieën met projectonkosten voor Project Operations-integratie (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="8c6c2-252">Geen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-252">No</span></span> | <span data-ttu-id="8c6c2-253">Geen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-253">No</span></span> | <span data-ttu-id="8c6c2-254">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-254">N\A</span></span> | <span data-ttu-id="8c6c2-255">Geen</span><span class="sxs-lookup"><span data-stu-id="8c6c2-255">No</span></span> | <span data-ttu-id="8c6c2-256">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-256">N\A</span></span> |
| <span data-ttu-id="8c6c2-257">**Entiteit voor exporteren van projectkosten voor Project Operations-integratie (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="8c6c2-258">Ja</span><span class="sxs-lookup"><span data-stu-id="8c6c2-258">Yes</span></span> | <span data-ttu-id="8c6c2-259">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-259">No</span></span> | <span data-ttu-id="8c6c2-260">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-260">N\A</span></span> | <span data-ttu-id="8c6c2-261">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-261">No</span></span> | <span data-ttu-id="8c6c2-262">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-262">N\A</span></span> |
| <span data-ttu-id="8c6c2-263">**Entiteit voor tijdramingen van Project Operations-integratie (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="8c6c2-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="8c6c2-264">Ja</span><span class="sxs-lookup"><span data-stu-id="8c6c2-264">Yes</span></span> | <span data-ttu-id="8c6c2-265">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-265">No</span></span> | <span data-ttu-id="8c6c2-266">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-266">N\A</span></span> | <span data-ttu-id="8c6c2-267">No</span><span class="sxs-lookup"><span data-stu-id="8c6c2-267">No</span></span> | <span data-ttu-id="8c6c2-268">n.v.t.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-268">N\A</span></span> |


4. <span data-ttu-id="8c6c2-269">Als u de entiteit wilt vernieuwen, selecteert u de toewijzingsnaam en vervolgens **Entiteiten vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Toewijzing vernieuwen](./media/20RefreshMapping.png)

5. <span data-ttu-id="8c6c2-271">Voer de toewijzing uit nadat het vernieuwen is voltooid.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="8c6c2-272">Voordat u de volgende toewijzing inschakelt, moet u controleren of de toewijzing in de tabel de status **In uitvoering** heeft.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="8c6c2-273">Het uitvoeren van toewijzingen met een groot aantal vereisten kan enige tijd duren.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="8c6c2-274">Om een toewijzing met vereisten uit te voeren, schakelt u de wisselknop **Gerelateerde entiteitstoewijzingen weergeven** in.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="8c6c2-275">Als in de tabel bij **Vereisten voor initiële synchronisatie** **Nee** wordt aangegeven, controleert u of de markering **Initiële synchronisatie** op **Uit** staat voor alle vereiste toewijzingen voordat u deze uitvoert.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Toewijzing uitvoeren](./media/21RunMap.png)

6. <span data-ttu-id="8c6c2-277">Controleer of alle projectgerelateerde toewijzingen de status actief hebben.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-277">Validate all project related maps are in the running state.</span></span>

![Alle toewijzingen worden uitgevoerd](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="8c6c2-279">Configuratiegegevens in CDS toepassen voor Project Operations (optioneel)</span><span class="sxs-lookup"><span data-stu-id="8c6c2-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="8c6c2-280">Als u demogegevens hebt toegepast op de Finance-omgeving raadpleegt u [Configuratiegegevens instellen en toepassen in Common Data Service voor Project Operations](resource-apply-pro-setup-config-data.md) om demogegevens toe te passen in de CDS-omgeving.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="8c6c2-281">Uw Project Operations-omgeving is nu ingericht en geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]