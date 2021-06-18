---
title: Configuratiegegevens in Common Data Service instellen en toepassen
description: Dit onderwerp bevat informatie over het instellen en toepassen van configuratiegegevens in Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001285"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="0efd0-103">Configuratiegegevens in Common Data Service instellen en toepassen</span><span class="sxs-lookup"><span data-stu-id="0efd0-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="0efd0-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="0efd0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="0efd0-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="0efd0-105">Prerequisites</span></span>

<span data-ttu-id="0efd0-106">Voordat u begint met het configureren van gegevens in Common Data Service (CDS), moet aan de volgende voorwaarden worden voldaan:</span><span class="sxs-lookup"><span data-stu-id="0efd0-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="0efd0-107">Richt een CDS-omgeving en een Dynamics 365 Finance-omgeving in voor Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0efd0-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="0efd0-108">Informatie over rechtspersoon van Dynamics 365 Finance wordt gedeeld met de CDS-omgeving.</span><span class="sxs-lookup"><span data-stu-id="0efd0-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="0efd0-109">Dit betekent dat de entiteit **Bedrijf** in CDS de volgende bedrijfsrecords heeft:</span><span class="sxs-lookup"><span data-stu-id="0efd0-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="0efd0-110">THPM</span><span class="sxs-lookup"><span data-stu-id="0efd0-110">THPM</span></span>
  - <span data-ttu-id="0efd0-111">USPM</span><span class="sxs-lookup"><span data-stu-id="0efd0-111">USPM</span></span>
  - <span data-ttu-id="0efd0-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="0efd0-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="0efd0-113">Gegevens voor installatie en configuratie installeren</span><span class="sxs-lookup"><span data-stu-id="0efd0-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="0efd0-114">Download, deblokkeer en extraheer het [Installatie- en configuratiegegevenspakket](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="0efd0-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="0efd0-115">Navigeer naar de uitgepakte map en voer het uitvoerbare bestand *DataMigrationUtility* uit.</span><span class="sxs-lookup"><span data-stu-id="0efd0-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="0efd0-116">Op pagina 1 van de wizard Common Data Service Configuratiemigratie (CMT) selecteert u **Gegevens importeren** en vervolgens **Doorgaan**.</span><span class="sxs-lookup"><span data-stu-id="0efd0-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Configuratiemigratie](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="0efd0-118">Selecteer op pagina 2 van de CMT-wizard **Microsoft 365** als **Implementatietype**.</span><span class="sxs-lookup"><span data-stu-id="0efd0-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="0efd0-119">Schakel de selectievakjes **Een lijst met beschikbare organisaties weergeven** en **Geavanceerd weergeven** in.</span><span class="sxs-lookup"><span data-stu-id="0efd0-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="0efd0-120">Selecteer de regio van uw tenant, voer uw inloggegevens in en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="0efd0-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Configuratie inloggen](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="0efd0-122">Selecteer op pagina 3 uit de lijst met organisaties op de tenant de organisatie waarin u de demogegevens wilt importeren en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="0efd0-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="0efd0-123">Selecteer op pagina 4 het zipbestand *SampleSetupAndConfigData* in de uitgepakte map.</span><span class="sxs-lookup"><span data-stu-id="0efd0-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selectie zipbestand](./media/3ZipFile.png)

![Selecteer een bestand](./media/4SelectAFile.png)

9. <span data-ttu-id="0efd0-126">Selecteer nadat het zipbestand is geselecteerd **Gegevens importeren**.</span><span class="sxs-lookup"><span data-stu-id="0efd0-126">After the zip file is selected, select **Import Data**.</span></span>

![Gegevens importeren](./media/5ImportData.png)

10. <span data-ttu-id="0efd0-128">Het importeren duurt ongeveer twee tot tien minuten, afhankelijk van uw netwerksnelheid.</span><span class="sxs-lookup"><span data-stu-id="0efd0-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="0efd0-129">Sluit de CMT-wizard nadat het importeren is voltooid.</span><span class="sxs-lookup"><span data-stu-id="0efd0-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="0efd0-130">Controleer uw organisatie op gegevens in de volgende 26 entiteiten:</span><span class="sxs-lookup"><span data-stu-id="0efd0-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="0efd0-131">Valuta</span><span class="sxs-lookup"><span data-stu-id="0efd0-131">Currency</span></span>
  - <span data-ttu-id="0efd0-132">Rekeningschema</span><span class="sxs-lookup"><span data-stu-id="0efd0-132">Chart of Accounts</span></span>
  - <span data-ttu-id="0efd0-133">Fiscale kalender</span><span class="sxs-lookup"><span data-stu-id="0efd0-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="0efd0-134">Typen valutawisselkoers</span><span class="sxs-lookup"><span data-stu-id="0efd0-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="0efd0-135">Betalingsdag</span><span class="sxs-lookup"><span data-stu-id="0efd0-135">Payment Day</span></span>
  - <span data-ttu-id="0efd0-136">Betalingsschema</span><span class="sxs-lookup"><span data-stu-id="0efd0-136">Payment Schedule</span></span>
  - <span data-ttu-id="0efd0-137">Betalingsvoorwaarde</span><span class="sxs-lookup"><span data-stu-id="0efd0-137">Payment Term</span></span>
  - <span data-ttu-id="0efd0-138">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="0efd0-138">Organizational Unit</span></span>
  - <span data-ttu-id="0efd0-139">Contact</span><span class="sxs-lookup"><span data-stu-id="0efd0-139">Contact</span></span>
  - <span data-ttu-id="0efd0-140">Belastinggroep</span><span class="sxs-lookup"><span data-stu-id="0efd0-140">Tax Group</span></span>
  - <span data-ttu-id="0efd0-141">Klantengroep</span><span class="sxs-lookup"><span data-stu-id="0efd0-141">Customer Group</span></span>
  - <span data-ttu-id="0efd0-142">Leveranciersgroep</span><span class="sxs-lookup"><span data-stu-id="0efd0-142">Vendor Group</span></span>
  - <span data-ttu-id="0efd0-143">Eenheid</span><span class="sxs-lookup"><span data-stu-id="0efd0-143">Unit</span></span>
  - <span data-ttu-id="0efd0-144">Eenhedengroep</span><span class="sxs-lookup"><span data-stu-id="0efd0-144">Unit Group</span></span>
  - <span data-ttu-id="0efd0-145">Prijslijst</span><span class="sxs-lookup"><span data-stu-id="0efd0-145">Price List</span></span>
  - <span data-ttu-id="0efd0-146">Prijslijst voor projectparameters</span><span class="sxs-lookup"><span data-stu-id="0efd0-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="0efd0-147">Factuurfrequentie</span><span class="sxs-lookup"><span data-stu-id="0efd0-147">Invoice Frequency</span></span>
  - <span data-ttu-id="0efd0-148">Categorie van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="0efd0-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="0efd0-149">Transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="0efd0-149">Transaction Category</span></span>
  - <span data-ttu-id="0efd0-150">Onkostencategorie</span><span class="sxs-lookup"><span data-stu-id="0efd0-150">Expense Category</span></span>
  - <span data-ttu-id="0efd0-151">Rolprijs</span><span class="sxs-lookup"><span data-stu-id="0efd0-151">Role Price</span></span>
  - <span data-ttu-id="0efd0-152">Prijs voor transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="0efd0-152">Transaction Category Price</span></span>
  - <span data-ttu-id="0efd0-153">Kenmerk</span><span class="sxs-lookup"><span data-stu-id="0efd0-153">Characteristic</span></span>
  - <span data-ttu-id="0efd0-154">Boekbare resource</span><span class="sxs-lookup"><span data-stu-id="0efd0-154">Bookable Resource</span></span>
  - <span data-ttu-id="0efd0-155">Toewijzing van categorie met boekbare resources</span><span class="sxs-lookup"><span data-stu-id="0efd0-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="0efd0-156">Kenmerk van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="0efd0-156">Bookable Resource Characteristic</span></span>

![Import voltooid](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="0efd0-158">Project Operations-configuraties bijwerken</span><span class="sxs-lookup"><span data-stu-id="0efd0-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="0efd0-159">Navigeer naar de CE-omgeving.</span><span class="sxs-lookup"><span data-stu-id="0efd0-159">Navigate to the CE environment.</span></span> <span data-ttu-id="0efd0-160">U kunt dit vinden door het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com/environments) te openen, de omgeving te selecteren en vervolgens **Omgeving openen** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="0efd0-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Omgeving openen](./media/7OpenEnvironment.png)

2. <span data-ttu-id="0efd0-162">Ga naar **Projecten** > **Resources** en selecteer **Nieuw** om een boekbare resource voor uw gebruiker te maken.</span><span class="sxs-lookup"><span data-stu-id="0efd0-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Boekbare resources](./media/8BookableResources.png)

3. <span data-ttu-id="0efd0-164">Selecteer op het tabblad **Algemeen** uw gebruiker met beheerdersrechten.</span><span class="sxs-lookup"><span data-stu-id="0efd0-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="0efd0-165">Controleer of de tijdzone overeenkomt met de zone waarin u zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="0efd0-165">Verify that the time zone matches the one you are in.</span></span> 

![Nieuwe boekbare resource](./media/9NewBookableResource.png)

4. <span data-ttu-id="0efd0-167">Op het tabblad **Planning**, in het veld **Bedrijf** kiest u het bedrijf **USPM** en selecteert u **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0efd0-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Tabblad Planning](./media/10SchedulingTab.png)

5. <span data-ttu-id="0efd0-169">Selecteer het tabblad **Werkuren**.</span><span class="sxs-lookup"><span data-stu-id="0efd0-169">Select the **Work hours** tab.</span></span>  

![Werkuren](./media/11WorkHours.png)

6. <span data-ttu-id="0efd0-171">Dubbelklik op een waarde in de kalender en selecteer **Bewerken** > **Alle gebeurtenissen in de reeks**.</span><span class="sxs-lookup"><span data-stu-id="0efd0-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Werkagenda](./media/12WorkCalendar.png)

7. <span data-ttu-id="0efd0-173">Verander werkuren in een werkdag van acht (8) uur, markeer weekends als vrije dagen en zorg ervoor dat de tijdzone overeenkomt met de uwe.</span><span class="sxs-lookup"><span data-stu-id="0efd0-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="0efd0-174">Selecteer **Opslaan en sluiten**.</span><span class="sxs-lookup"><span data-stu-id="0efd0-174">Select **Save and close**.</span></span>

![Agenda bijwerken](./media/13UpdateCalendar.png)

9. <span data-ttu-id="0efd0-176">Ga naar **Instellingen** > **Agendasjablonen** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0efd0-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Agendasjablonen](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="0efd0-178">Voer een naam in, selecteer de sjabloonresource die u hebt gemaakt en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0efd0-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Agendasjabloon opslaan](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="0efd0-180">Ga naar **Parameters** en dubbelklik op de record.</span><span class="sxs-lookup"><span data-stu-id="0efd0-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projectparameters](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="0efd0-182">Werk de volgende velden bij:</span><span class="sxs-lookup"><span data-stu-id="0efd0-182">Update the following fields:</span></span>

 - <span data-ttu-id="0efd0-183">**Standaardbedrijf**: USPM</span><span class="sxs-lookup"><span data-stu-id="0efd0-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="0efd0-184">**Standaardorganisatie-eenheid**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="0efd0-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="0efd0-185">**Factuurfrequentie**: zevende en laatste dag</span><span class="sxs-lookup"><span data-stu-id="0efd0-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="0efd0-186">**Werkuursjabloon**: ga naar de sjabloon die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0efd0-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="0efd0-187">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0efd0-187">Select **Save**.</span></span> 

![Bijgewerkte projectparameters](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
