---
title: Demogegevens voor installatie en configuratie toepassen - lite
description: Dit onderwerp bevat informatie over het toepassen van demo- en configuratiegegevens voor Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401257"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="c6797-103">Demogegevens voor installatie en configuratie toepassen voor Project Operations - lite</span><span class="sxs-lookup"><span data-stu-id="c6797-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="c6797-104">_\*\*Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="c6797-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c6797-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="c6797-105">Prerequisites</span></span>

<span data-ttu-id="c6797-106">Voordat u met de configuratie begint, moet u een Common Data Service-omgeving (CDS) inrichten voor Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c6797-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="c6797-107">Instructies</span><span class="sxs-lookup"><span data-stu-id="c6797-107">Instructions</span></span>

1. <span data-ttu-id="c6797-108">Download het [Pakket met mastergegevens](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="c6797-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="c6797-109">Navigeer naar de map *ProjOpsDemoDataSetupAndMaster - Integrated CMT* en voer het uitvoerbare bestand *DataMigrationUtility* uit.</span><span class="sxs-lookup"><span data-stu-id="c6797-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="c6797-110">Op pagina 1 van de wizard Common Data Service Configuratiemigratie (CMT) selecteert u **Gegevens importeren** en vervolgens **Doorgaan**.</span><span class="sxs-lookup"><span data-stu-id="c6797-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Configuratiemigratie](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="c6797-112">Selecteer op pagina 2 van de CMT-wizard **Microsoft 365** als **Implementatietype**.</span><span class="sxs-lookup"><span data-stu-id="c6797-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="c6797-113">Schakel de selectievakjes **Een lijst met beschikbare organisaties weergeven** en **Geavanceerd weergeven** in.</span><span class="sxs-lookup"><span data-stu-id="c6797-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="c6797-114">Selecteer de regio van uw tenant, voer uw inloggegevens in en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="c6797-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Configuratie inloggen](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="c6797-116">Selecteer op pagina 3 uit de lijst met organisaties op de tenant de organisatie waarin u de demogegevens wilt importeren en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="c6797-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="c6797-117">Selecteer op pagina 4 het zipbestand *MasterAndSetupData* in de uitgepakte map, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="c6797-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zipbestand](./media/3ZipFile.png)

![Selecteer een bestand](./media/4SelectAFile.png)

9. <span data-ttu-id="c6797-120">Selecteer nadat het zipbestand is geselecteerd **Gegevens importeren**.</span><span class="sxs-lookup"><span data-stu-id="c6797-120">After the zip file is selected, select **Import Data**.</span></span>

![Gegevens importeren](./media/5ImportData.png)

10. <span data-ttu-id="c6797-122">Het importeren duurt ongeveer twee tot tien minuten, afhankelijk van uw netwerksnelheid.</span><span class="sxs-lookup"><span data-stu-id="c6797-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="c6797-123">Sluit de CMT-wizard nadat het importeren is voltooid.</span><span class="sxs-lookup"><span data-stu-id="c6797-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="c6797-124">Controleer uw organisatie op gegevens in de volgende 20 entiteiten:</span><span class="sxs-lookup"><span data-stu-id="c6797-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="c6797-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="c6797-125">Currency</span></span>
-   <span data-ttu-id="c6797-126">Account</span><span class="sxs-lookup"><span data-stu-id="c6797-126">Account</span></span>
-   <span data-ttu-id="c6797-127">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="c6797-127">Organizational Unit</span></span>
-   <span data-ttu-id="c6797-128">Contact</span><span class="sxs-lookup"><span data-stu-id="c6797-128">Contact</span></span>
-   <span data-ttu-id="c6797-129">Belastinggroep</span><span class="sxs-lookup"><span data-stu-id="c6797-129">Tax Group</span></span>
-   <span data-ttu-id="c6797-130">Klantengroep</span><span class="sxs-lookup"><span data-stu-id="c6797-130">Customer Group</span></span>
-   <span data-ttu-id="c6797-131">Eenheid</span><span class="sxs-lookup"><span data-stu-id="c6797-131">Unit</span></span>
-   <span data-ttu-id="c6797-132">Eenhedengroep</span><span class="sxs-lookup"><span data-stu-id="c6797-132">Unit Group</span></span>
-   <span data-ttu-id="c6797-133">Prijslijst</span><span class="sxs-lookup"><span data-stu-id="c6797-133">Price List</span></span>
-   <span data-ttu-id="c6797-134">Prijslijst voor projectparameters</span><span class="sxs-lookup"><span data-stu-id="c6797-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="c6797-135">Factuurfrequentie</span><span class="sxs-lookup"><span data-stu-id="c6797-135">Invoice Frequency</span></span>
-   <span data-ttu-id="c6797-136">Categorie van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="c6797-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="c6797-137">Transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="c6797-137">Transaction Category</span></span>
-   <span data-ttu-id="c6797-138">Onkostencategorie</span><span class="sxs-lookup"><span data-stu-id="c6797-138">Expense Category</span></span>
-   <span data-ttu-id="c6797-139">Rolprijs</span><span class="sxs-lookup"><span data-stu-id="c6797-139">Role Price</span></span>
-   <span data-ttu-id="c6797-140">Prijs voor transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="c6797-140">Transaction Category Price</span></span>
-   <span data-ttu-id="c6797-141">Kenmerk</span><span class="sxs-lookup"><span data-stu-id="c6797-141">Characteristic</span></span>
-   <span data-ttu-id="c6797-142">Boekbare resource</span><span class="sxs-lookup"><span data-stu-id="c6797-142">Bookable Resource</span></span>
-   <span data-ttu-id="c6797-143">Toewijzing van categorie met boekbare resources</span><span class="sxs-lookup"><span data-stu-id="c6797-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="c6797-144">Kenmerk van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="c6797-144">Bookable Resource Characteristic</span></span>

![Import voltooid](./media/6CompleteImport.png)
