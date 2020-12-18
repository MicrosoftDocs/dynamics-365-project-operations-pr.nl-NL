---
title: Configuratiegegevens in Common Data Service instellen en toepassen
description: Dit onderwerp bevat informatie over het instellen en toepassen van configuratiegegevens in Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642222"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="e770c-103">Configuratiegegevens in Common Data Service instellen en toepassen</span><span class="sxs-lookup"><span data-stu-id="e770c-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="e770c-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="e770c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="e770c-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="e770c-105">Prerequisites</span></span>

<span data-ttu-id="e770c-106">Voordat u begint met het configureren van gegevens in Common Data Service (CDS), moet aan de volgende voorwaarden worden voldaan:</span><span class="sxs-lookup"><span data-stu-id="e770c-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="e770c-107">Richt een CDS-omgeving en een Dynamics 365 Finance-omgeving in voor Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e770c-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="e770c-108">Informatie over rechtspersoon van Dynamics 365 Finance wordt gedeeld met de CDS-omgeving.</span><span class="sxs-lookup"><span data-stu-id="e770c-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="e770c-109">Dit betekent dat de entiteit **Bedrijf** in CDS de volgende bedrijfsrecords heeft:</span><span class="sxs-lookup"><span data-stu-id="e770c-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="e770c-110">THPM</span><span class="sxs-lookup"><span data-stu-id="e770c-110">THPM</span></span>
  - <span data-ttu-id="e770c-111">USPM</span><span class="sxs-lookup"><span data-stu-id="e770c-111">USPM</span></span>
  - <span data-ttu-id="e770c-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="e770c-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="e770c-113">Gegevens voor installatie en configuratie installeren</span><span class="sxs-lookup"><span data-stu-id="e770c-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="e770c-114">Download, deblokkeer en extraheer het [Installatie- en configuratiegegevenspakket](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="e770c-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="e770c-115">Navigeer naar de uitgepakte map en voer het uitvoerbare bestand *DataMigrationUtility* uit.</span><span class="sxs-lookup"><span data-stu-id="e770c-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="e770c-116">Op pagina 1 van de wizard Common Data Service Configuratiemigratie (CMT) selecteert u **Gegevens importeren** en vervolgens **Doorgaan**.</span><span class="sxs-lookup"><span data-stu-id="e770c-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Configuratiemigratie](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="e770c-118">Selecteer op pagina 2 van de CMT-wizard **Microsoft 365** als **Implementatietype**.</span><span class="sxs-lookup"><span data-stu-id="e770c-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="e770c-119">Schakel de selectievakjes **Een lijst met beschikbare organisaties weergeven** en **Geavanceerd weergeven** in.</span><span class="sxs-lookup"><span data-stu-id="e770c-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="e770c-120">Selecteer de regio van uw tenant, voer uw inloggegevens in en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="e770c-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Configuratie inloggen](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="e770c-122">Selecteer op pagina 3 uit de lijst met organisaties op de tenant de organisatie waarin u de demogegevens wilt importeren en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="e770c-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="e770c-123">Selecteer op pagina 4 het zipbestand *SampleSetupAndConfigData* in de uitgepakte map.</span><span class="sxs-lookup"><span data-stu-id="e770c-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selectie zipbestand](./media/3ZipFile.png)

![Selecteer een bestand](./media/4SelectAFile.png)

9. <span data-ttu-id="e770c-126">Selecteer nadat het zipbestand is geselecteerd **Gegevens importeren**.</span><span class="sxs-lookup"><span data-stu-id="e770c-126">After the zip file is selected, select **Import Data**.</span></span>

![Gegevens importeren](./media/5ImportData.png)

10. <span data-ttu-id="e770c-128">Het importeren duurt ongeveer twee tot tien minuten, afhankelijk van uw netwerksnelheid.</span><span class="sxs-lookup"><span data-stu-id="e770c-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="e770c-129">Sluit de CMT-wizard nadat het importeren is voltooid.</span><span class="sxs-lookup"><span data-stu-id="e770c-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="e770c-130">Controleer uw organisatie op gegevens in de volgende 19 entiteiten:</span><span class="sxs-lookup"><span data-stu-id="e770c-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="e770c-131">Valuta</span><span class="sxs-lookup"><span data-stu-id="e770c-131">Currency</span></span>
  - <span data-ttu-id="e770c-132">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="e770c-132">Organizational Unit</span></span>
  - <span data-ttu-id="e770c-133">Contact</span><span class="sxs-lookup"><span data-stu-id="e770c-133">Contact</span></span>
  - <span data-ttu-id="e770c-134">Belastinggroep</span><span class="sxs-lookup"><span data-stu-id="e770c-134">Tax Group</span></span>
  - <span data-ttu-id="e770c-135">Klantengroep</span><span class="sxs-lookup"><span data-stu-id="e770c-135">Customer Group</span></span>
  - <span data-ttu-id="e770c-136">Eenheid</span><span class="sxs-lookup"><span data-stu-id="e770c-136">Unit</span></span>
  - <span data-ttu-id="e770c-137">Eenhedengroep</span><span class="sxs-lookup"><span data-stu-id="e770c-137">Unit Group</span></span>
  - <span data-ttu-id="e770c-138">Prijslijst</span><span class="sxs-lookup"><span data-stu-id="e770c-138">Price List</span></span>
  - <span data-ttu-id="e770c-139">Prijslijst voor projectparameters</span><span class="sxs-lookup"><span data-stu-id="e770c-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="e770c-140">Factuurfrequentie</span><span class="sxs-lookup"><span data-stu-id="e770c-140">Invoice Frequency</span></span>
  - <span data-ttu-id="e770c-141">Categorie van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="e770c-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="e770c-142">Transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="e770c-142">Transaction Category</span></span>
  - <span data-ttu-id="e770c-143">Onkostencategorie</span><span class="sxs-lookup"><span data-stu-id="e770c-143">Expense Category</span></span>
  - <span data-ttu-id="e770c-144">Rolprijs</span><span class="sxs-lookup"><span data-stu-id="e770c-144">Role Price</span></span>
  - <span data-ttu-id="e770c-145">Prijs voor transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="e770c-145">Transaction Category Price</span></span>
  - <span data-ttu-id="e770c-146">Kenmerk</span><span class="sxs-lookup"><span data-stu-id="e770c-146">Characteristic</span></span>
  - <span data-ttu-id="e770c-147">Boekbare resource</span><span class="sxs-lookup"><span data-stu-id="e770c-147">Bookable Resource</span></span>
  - <span data-ttu-id="e770c-148">Toewijzing van categorie met boekbare resources</span><span class="sxs-lookup"><span data-stu-id="e770c-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="e770c-149">Kenmerk van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="e770c-149">Bookable Resource Characteristic</span></span>

![Import voltooid](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="e770c-151">Project Operations-configuraties bijwerken</span><span class="sxs-lookup"><span data-stu-id="e770c-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="e770c-152">Navigeer naar de CE-omgeving.</span><span class="sxs-lookup"><span data-stu-id="e770c-152">Navigate to the CE environment.</span></span> <span data-ttu-id="e770c-153">U kunt dit vinden door het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com/environments) te openen, de omgeving te selecteren en vervolgens **Omgeving openen** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="e770c-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Omgeving openen](./media/7OpenEnvironment.png)

2. <span data-ttu-id="e770c-155">Ga naar **Projecten** > **Resources** en selecteer **Nieuw** om een boekbare resource voor uw gebruiker te maken.</span><span class="sxs-lookup"><span data-stu-id="e770c-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Boekbare resources](./media/8BookableResources.png)

3. <span data-ttu-id="e770c-157">Selecteer op het tabblad **Algemeen** uw gebruiker met beheerdersrechten.</span><span class="sxs-lookup"><span data-stu-id="e770c-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="e770c-158">Controleer of de tijdzone overeenkomt met de zone waarin u zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="e770c-158">Verify that the time zone matches the one you are in.</span></span> 

![Nieuwe boekbare resource](./media/9NewBookableResource.png)

4. <span data-ttu-id="e770c-160">Op het tabblad **Planning**, in het veld **Bedrijf** kiest u het bedrijf **USPM** en selecteert u **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e770c-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Tabblad Planning](./media/10SchedulingTab.png)

5. <span data-ttu-id="e770c-162">Selecteer het tabblad **Werkuren**.</span><span class="sxs-lookup"><span data-stu-id="e770c-162">Select the **Work hours** tab.</span></span>  

![Werkuren](./media/11WorkHours.png)

6. <span data-ttu-id="e770c-164">Dubbelklik op een waarde in de kalender en selecteer **Bewerken** > **Alle gebeurtenissen in de reeks**.</span><span class="sxs-lookup"><span data-stu-id="e770c-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Werkagenda](./media/12WorkCalendar.png)

7. <span data-ttu-id="e770c-166">Verander werkuren in een werkdag van acht (8) uur, markeer weekends als vrije dagen en zorg ervoor dat de tijdzone overeenkomt met de uwe.</span><span class="sxs-lookup"><span data-stu-id="e770c-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="e770c-167">Selecteer **Opslaan en sluiten**.</span><span class="sxs-lookup"><span data-stu-id="e770c-167">Select **Save and close**.</span></span>

![Agenda bijwerken](./media/13UpdateCalendar.png)

9. <span data-ttu-id="e770c-169">Ga naar **Instellingen** > **Agendasjablonen** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e770c-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Agendasjablonen](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="e770c-171">Voer een naam in, selecteer de sjabloonresource die u hebt gemaakt en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e770c-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Agendasjabloon opslaan](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="e770c-173">Ga naar **Parameters** en dubbelklik op de record.</span><span class="sxs-lookup"><span data-stu-id="e770c-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projectparameters](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="e770c-175">Werk de volgende velden bij:</span><span class="sxs-lookup"><span data-stu-id="e770c-175">Update the following fields:</span></span>

 - <span data-ttu-id="e770c-176">**Standaardbedrijf**: USPM</span><span class="sxs-lookup"><span data-stu-id="e770c-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="e770c-177">**Standaard organisatie-eenheid**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="e770c-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="e770c-178">**Factuurfrequentie**: zevende en laatste dag</span><span class="sxs-lookup"><span data-stu-id="e770c-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="e770c-179">**Werkuursjabloon**: ga naar de sjabloon die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e770c-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="e770c-180">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e770c-180">Select **Save**.</span></span> 

![Bijgewerkte projectparameters](./media/17UpdatedProjectParameters.png)
