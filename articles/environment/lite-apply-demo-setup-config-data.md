---
title: Demogegevens voor installatie en configuratie toepassen - lite
description: Dit onderwerp bevat informatie over het toepassen van demo- en configuratiegegevens voor Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997145"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="f0461-103">Demogegevens voor installatie en configuratie toepassen voor Project Operations - lite</span><span class="sxs-lookup"><span data-stu-id="f0461-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="f0461-104">_\*\*Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="f0461-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="f0461-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="f0461-105">Prerequisites</span></span>

<span data-ttu-id="f0461-106">Voordat u met de configuratie begint, moet u een Common Data Service-omgeving (CDS) inrichten voor Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f0461-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="f0461-107">Instructies</span><span class="sxs-lookup"><span data-stu-id="f0461-107">Instructions</span></span>

1. <span data-ttu-id="f0461-108">Download het [Pakket met mastergegevens](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="f0461-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="f0461-109">Navigeer naar de map *ProjOpsSampleSetupData - CE: alleen CMT* en voer het uitvoerbare bestand *GegevensmigratieUtility* uit.</span><span class="sxs-lookup"><span data-stu-id="f0461-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="f0461-110">Op pagina 1 van de wizard Common Data Service Configuratiemigratie (CMT) selecteert u **Gegevens importeren** en vervolgens **Doorgaan**.</span><span class="sxs-lookup"><span data-stu-id="f0461-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Configuratiemigratie](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="f0461-112">Selecteer op pagina 2 van de CMT-wizard **Microsoft 365** als **Implementatietype**.</span><span class="sxs-lookup"><span data-stu-id="f0461-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="f0461-113">Schakel de selectievakjes **Een lijst met beschikbare organisaties weergeven** en **Geavanceerd weergeven** in.</span><span class="sxs-lookup"><span data-stu-id="f0461-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="f0461-114">Selecteer de regio van uw tenant, voer uw inloggegevens in en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="f0461-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Configuratie inloggen](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="f0461-116">Selecteer op pagina 3 uit de lijst met organisaties op de tenant de organisatie waarin u de demogegevens wilt importeren en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="f0461-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="f0461-117">Selecteer op pagina 4 het zipbestand *SampleSetupAndConfigData* in de uitgepakte map *ProjOpsSampleSetupData - CE: alleen CMT*.</span><span class="sxs-lookup"><span data-stu-id="f0461-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Zipbestand](./media/3ZipFile.png)

   ![Een bestand selecteren](./media/4SelectAFile.png)

9. <span data-ttu-id="f0461-120">Selecteer nadat het zipbestand is geselecteerd **Gegevens importeren**.</span><span class="sxs-lookup"><span data-stu-id="f0461-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Gegevens importeren](./media/5ImportData.png)

10. <span data-ttu-id="f0461-122">Het importeren duurt ongeveer twee tot tien minuten, afhankelijk van uw netwerksnelheid.</span><span class="sxs-lookup"><span data-stu-id="f0461-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="f0461-123">Sluit de CMT-wizard nadat het importeren is voltooid.</span><span class="sxs-lookup"><span data-stu-id="f0461-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="f0461-124">Controleer uw organisatie op gegevens in de volgende 18 entiteiten:</span><span class="sxs-lookup"><span data-stu-id="f0461-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="f0461-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="f0461-125">Currency</span></span>
    -   <span data-ttu-id="f0461-126">Account</span><span class="sxs-lookup"><span data-stu-id="f0461-126">Account</span></span>
    -   <span data-ttu-id="f0461-127">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="f0461-127">Organizational Unit</span></span>
    -   <span data-ttu-id="f0461-128">Contact</span><span class="sxs-lookup"><span data-stu-id="f0461-128">Contact</span></span>
    -   <span data-ttu-id="f0461-129">Eenheid</span><span class="sxs-lookup"><span data-stu-id="f0461-129">Unit</span></span>
    -   <span data-ttu-id="f0461-130">Eenhedengroep</span><span class="sxs-lookup"><span data-stu-id="f0461-130">Unit Group</span></span>
    -   <span data-ttu-id="f0461-131">Prijslijst</span><span class="sxs-lookup"><span data-stu-id="f0461-131">Price List</span></span>
    -   <span data-ttu-id="f0461-132">Prijslijst voor projectparameters</span><span class="sxs-lookup"><span data-stu-id="f0461-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="f0461-133">Factuurfrequentie</span><span class="sxs-lookup"><span data-stu-id="f0461-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="f0461-134">Categorie van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="f0461-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="f0461-135">Transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="f0461-135">Transaction Category</span></span>
    -   <span data-ttu-id="f0461-136">Onkostencategorie</span><span class="sxs-lookup"><span data-stu-id="f0461-136">Expense Category</span></span>
    -   <span data-ttu-id="f0461-137">Rolprijs</span><span class="sxs-lookup"><span data-stu-id="f0461-137">Role Price</span></span>
    -   <span data-ttu-id="f0461-138">Prijs voor transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="f0461-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="f0461-139">Kenmerk</span><span class="sxs-lookup"><span data-stu-id="f0461-139">Characteristic</span></span>
    -   <span data-ttu-id="f0461-140">Boekbare resource</span><span class="sxs-lookup"><span data-stu-id="f0461-140">Bookable Resource</span></span>
    -   <span data-ttu-id="f0461-141">Toewijzing van categorie met boekbare resources</span><span class="sxs-lookup"><span data-stu-id="f0461-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="f0461-142">Kenmerk van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="f0461-142">Bookable Resource Characteristic</span></span>

    ![Import voltooid](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
