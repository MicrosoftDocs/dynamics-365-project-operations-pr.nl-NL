---
title: Configuratiegegevens in Common Data Service instellen en toepassen voor Project Operations
description: Dit onderwerp bevat informatie over het instellen en toepassen van configuratiegegevens in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074437"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="4b7fe-103">Configuratiegegevens in Common Data Service instellen en toepassen voor Project Operations</span><span class="sxs-lookup"><span data-stu-id="4b7fe-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="4b7fe-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="4b7fe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="4b7fe-105">Gegevens voor installatie en configuratie installeren</span><span class="sxs-lookup"><span data-stu-id="4b7fe-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="4b7fe-106">Download, deblokkeer en extraheer het [Installatie- en configuratiegegevenspakket](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="4b7fe-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="4b7fe-107">Navigeer naar de uitgepakte map en voer het uitvoerbare bestand *DataMigrationUtility* uit.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="4b7fe-108">Op pagina 1 van de wizard Common Data Service Configuratiemigratie (CMT) selecteert u **Gegevens importeren** en vervolgens **Doorgaan**.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Configuratiemigratie](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="4b7fe-110">Selecteer op pagina 2 van de CMT-wizard **Microsoft 365** als **Implementatietype**.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="4b7fe-111">Schakel de selectievakjes **Een lijst met beschikbare organisaties weergeven** en **Geavanceerd weergeven** in.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="4b7fe-112">Selecteer de regio van uw tenant, voer uw inloggegevens in en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Configuratie inloggen](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="4b7fe-114">Selecteer op pagina 3 uit de lijst met organisaties op de tenant de organisatie waarin u de demogegevens wilt importeren en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="4b7fe-115">Selecteer op pagina 4 het zipbestand *SampleSetupAndConfigData* in de uitgepakte map.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selectie zipbestand](./media/3ZipFile.png)

![Selecteer een bestand](./media/4SelectAFile.png)

9. <span data-ttu-id="4b7fe-118">Selecteer nadat het zipbestand is geselecteerd **Gegevens importeren**.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-118">After the zip file is selected, select **Import Data**.</span></span>

![Gegevens importeren](./media/5ImportData.png)

10. <span data-ttu-id="4b7fe-120">Het importeren duurt ongeveer twee tot tien minuten, afhankelijk van uw netwerksnelheid.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="4b7fe-121">Sluit de CMT-wizard nadat het importeren is voltooid.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="4b7fe-122">Controleer uw organisatie op gegevens in de volgende 19 entiteiten:</span><span class="sxs-lookup"><span data-stu-id="4b7fe-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="4b7fe-123">Valuta</span><span class="sxs-lookup"><span data-stu-id="4b7fe-123">Currency</span></span>
  - <span data-ttu-id="4b7fe-124">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="4b7fe-124">Organizational Unit</span></span>
  - <span data-ttu-id="4b7fe-125">Contact</span><span class="sxs-lookup"><span data-stu-id="4b7fe-125">Contact</span></span>
  - <span data-ttu-id="4b7fe-126">Belastinggroep</span><span class="sxs-lookup"><span data-stu-id="4b7fe-126">Tax Group</span></span>
  - <span data-ttu-id="4b7fe-127">Klantengroep</span><span class="sxs-lookup"><span data-stu-id="4b7fe-127">Customer Group</span></span>
  - <span data-ttu-id="4b7fe-128">Eenheid</span><span class="sxs-lookup"><span data-stu-id="4b7fe-128">Unit</span></span>
  - <span data-ttu-id="4b7fe-129">Eenhedengroep</span><span class="sxs-lookup"><span data-stu-id="4b7fe-129">Unit Group</span></span>
  - <span data-ttu-id="4b7fe-130">Prijslijst</span><span class="sxs-lookup"><span data-stu-id="4b7fe-130">Price List</span></span>
  - <span data-ttu-id="4b7fe-131">Prijslijst voor projectparameters</span><span class="sxs-lookup"><span data-stu-id="4b7fe-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="4b7fe-132">Factuurfrequentie</span><span class="sxs-lookup"><span data-stu-id="4b7fe-132">Invoice Frequency</span></span>
  - <span data-ttu-id="4b7fe-133">Categorie van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="4b7fe-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="4b7fe-134">Transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="4b7fe-134">Transaction Category</span></span>
  - <span data-ttu-id="4b7fe-135">Onkostencategorie</span><span class="sxs-lookup"><span data-stu-id="4b7fe-135">Expense Category</span></span>
  - <span data-ttu-id="4b7fe-136">Rolprijs</span><span class="sxs-lookup"><span data-stu-id="4b7fe-136">Role Price</span></span>
  - <span data-ttu-id="4b7fe-137">Prijs voor transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="4b7fe-137">Transaction Category Price</span></span>
  - <span data-ttu-id="4b7fe-138">Kenmerk</span><span class="sxs-lookup"><span data-stu-id="4b7fe-138">Characteristic</span></span>
  - <span data-ttu-id="4b7fe-139">Boekbare resource</span><span class="sxs-lookup"><span data-stu-id="4b7fe-139">Bookable Resource</span></span>
  - <span data-ttu-id="4b7fe-140">Toewijzing van categorie met boekbare resources</span><span class="sxs-lookup"><span data-stu-id="4b7fe-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="4b7fe-141">Kenmerk van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="4b7fe-141">Bookable Resource Characteristic</span></span>

![Import voltooid](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="4b7fe-143">Project Operations-configuraties bijwerken</span><span class="sxs-lookup"><span data-stu-id="4b7fe-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="4b7fe-144">Navigeer naar de CE-omgeving.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-144">Navigate to the CE environment.</span></span> <span data-ttu-id="4b7fe-145">U kunt dit vinden door het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com/environments) te openen, de omgeving te selecteren en vervolgens **Omgeving openen** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Omgeving openen](./media/7OpenEnvironment.png)

2. <span data-ttu-id="4b7fe-147">Ga naar **Projecten** > **Resources** en selecteer **Nieuw** om een boekbare resource voor uw gebruiker te maken.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Boekbare resources](./media/8BookableResources.png)

3. <span data-ttu-id="4b7fe-149">Selecteer op het tabblad **Algemeen** uw gebruiker met beheerdersrechten.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="4b7fe-150">Controleer of de tijdzone overeenkomt met de zone waarin u zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-150">Verify that the time zone matches the one you are in.</span></span> 

![Nieuwe boekbare resource](./media/9NewBookableResource.png)

4. <span data-ttu-id="4b7fe-152">Op het tabblad **Planning** , in het veld **Bedrijf** kiest u het bedrijf **USPM** en selecteert u **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Tabblad Planning](./media/10SchedulingTab.png)

5. <span data-ttu-id="4b7fe-154">Selecteer het tabblad **Werkuren**.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-154">Select the **Work hours** tab.</span></span>  

![Werkuren](./media/11WorkHours.png)

6. <span data-ttu-id="4b7fe-156">Dubbelklik op een waarde in de kalender en selecteer **Bewerken** > **Alle gebeurtenissen in de reeks**.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Werkagenda](./media/12WorkCalendar.png)

7. <span data-ttu-id="4b7fe-158">Verander werkuren in een werkdag van acht (8) uur, markeer weekends als vrije dagen en zorg ervoor dat de tijdzone overeenkomt met de uwe.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="4b7fe-159">Selecteer **Opslaan en sluiten**.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-159">Select **Save and close**.</span></span>

![Agenda bijwerken](./media/13UpdateCalendar.png)

9. <span data-ttu-id="4b7fe-161">Ga naar **Instellingen** > **Agendasjablonen** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Agendasjablonen](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="4b7fe-163">Voer een naam in, selecteer de sjabloonresource die u hebt gemaakt en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Agendasjabloon opslaan](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="4b7fe-165">Ga naar **Parameters** en dubbelklik op de record.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projectparameters](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="4b7fe-167">Werk de volgende velden bij:</span><span class="sxs-lookup"><span data-stu-id="4b7fe-167">Update the following fields:</span></span>

 - <span data-ttu-id="4b7fe-168">**Standaardbedrijf** : USPM</span><span class="sxs-lookup"><span data-stu-id="4b7fe-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="4b7fe-169">**Standaard organisatie-eenheid** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="4b7fe-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="4b7fe-170">**Factuurfrequentie** : zevende en laatste dag</span><span class="sxs-lookup"><span data-stu-id="4b7fe-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="4b7fe-171">**Werkuursjabloon** : ga naar de sjabloon die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="4b7fe-172">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="4b7fe-172">Select **Save**.</span></span> 

![Bijgewerkte projectparameters](./media/17UpdatedProjectParameters.png)
