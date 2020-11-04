---
title: Demogegevens voor installatie en configuratie toepassen
description: Dit onderwerp bevat informatie over het toepassen van demo- en configuratiegegevens voor Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074429"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="c22d8-103">Demo- en configuratiegegevens toepassen voor Project Operations Lite-implementatie, van deal tot proforma-facturering</span><span class="sxs-lookup"><span data-stu-id="c22d8-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="c22d8-104">_\*\*Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="c22d8-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="c22d8-105">Download het [Pakket met mastergegevens](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="c22d8-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="c22d8-106">Navigeer naar de map *ProjOpsDemoDataSetupAndMaster - Integrated CMT* en voer het uitvoerbare bestand *DataMigrationUtility* uit.</span><span class="sxs-lookup"><span data-stu-id="c22d8-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="c22d8-107">Op pagina 1 van de wizard Common Data Service Configuratiemigratie (CMT) selecteert u **Gegevens importeren** en vervolgens **Doorgaan**.</span><span class="sxs-lookup"><span data-stu-id="c22d8-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Configuratiemigratie](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="c22d8-109">Selecteer op pagina 2 van de CMT-wizard **Microsoft 365** als **Implementatietype**.</span><span class="sxs-lookup"><span data-stu-id="c22d8-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="c22d8-110">Schakel de selectievakjes **Een lijst met beschikbare organisaties weergeven** en **Geavanceerd weergeven** in.</span><span class="sxs-lookup"><span data-stu-id="c22d8-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="c22d8-111">Selecteer de regio van uw tenant, voer uw inloggegevens in en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="c22d8-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Configuratie inloggen](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="c22d8-113">Selecteer op pagina 3 uit de lijst met organisaties op de tenant de organisatie waarin u de demogegevens wilt importeren en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="c22d8-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="c22d8-114">Selecteer op pagina 4 het zipbestand *MasterAndSetupData* in de uitgepakte map, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="c22d8-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zipbestand](./media/3ZipFile.png)

![Selecteer een bestand](./media/4SelectAFile.png)

9. <span data-ttu-id="c22d8-117">Selecteer nadat het zipbestand is geselecteerd **Gegevens importeren**.</span><span class="sxs-lookup"><span data-stu-id="c22d8-117">After the zip file is selected, select **Import Data**.</span></span>

![Gegevens importeren](./media/5ImportData.png)

10. <span data-ttu-id="c22d8-119">Het importeren duurt ongeveer twee tot tien minuten, afhankelijk van uw netwerksnelheid.</span><span class="sxs-lookup"><span data-stu-id="c22d8-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="c22d8-120">Sluit de CMT-wizard nadat het importeren is voltooid.</span><span class="sxs-lookup"><span data-stu-id="c22d8-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="c22d8-121">Controleer uw organisatie op gegevens in de volgende 20 entiteiten:</span><span class="sxs-lookup"><span data-stu-id="c22d8-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="c22d8-122">Valuta</span><span class="sxs-lookup"><span data-stu-id="c22d8-122">Currency</span></span>
- <span data-ttu-id="c22d8-123">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="c22d8-123">Organizational Unit</span></span>
- <span data-ttu-id="c22d8-124">Contact</span><span class="sxs-lookup"><span data-stu-id="c22d8-124">Contact</span></span>
- <span data-ttu-id="c22d8-125">Belastinggroep</span><span class="sxs-lookup"><span data-stu-id="c22d8-125">Tax Group</span></span>
- <span data-ttu-id="c22d8-126">Klantengroep</span><span class="sxs-lookup"><span data-stu-id="c22d8-126">Customer Group</span></span>
- <span data-ttu-id="c22d8-127">Eenheid</span><span class="sxs-lookup"><span data-stu-id="c22d8-127">Unit</span></span>
- <span data-ttu-id="c22d8-128">Eenhedengroep</span><span class="sxs-lookup"><span data-stu-id="c22d8-128">Unit Group</span></span>
- <span data-ttu-id="c22d8-129">Prijslijst</span><span class="sxs-lookup"><span data-stu-id="c22d8-129">Price List</span></span>
- <span data-ttu-id="c22d8-130">Prijslijst voor projectparameters</span><span class="sxs-lookup"><span data-stu-id="c22d8-130">Project Parameter Price List</span></span>
- <span data-ttu-id="c22d8-131">Factuurfrequentie</span><span class="sxs-lookup"><span data-stu-id="c22d8-131">Invoice Frequency</span></span>
- <span data-ttu-id="c22d8-132">Factuurfrequentiedetail</span><span class="sxs-lookup"><span data-stu-id="c22d8-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="c22d8-133">Categorie van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="c22d8-133">Bookable Resource Category</span></span>
- <span data-ttu-id="c22d8-134">Transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="c22d8-134">Transaction Category</span></span>
- <span data-ttu-id="c22d8-135">Onkostencategorie</span><span class="sxs-lookup"><span data-stu-id="c22d8-135">Expense Category</span></span>
- <span data-ttu-id="c22d8-136">Rolprijs</span><span class="sxs-lookup"><span data-stu-id="c22d8-136">Role Price</span></span>
- <span data-ttu-id="c22d8-137">Prijs voor transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="c22d8-137">Transaction Category Price</span></span>
- <span data-ttu-id="c22d8-138">Kenmerk</span><span class="sxs-lookup"><span data-stu-id="c22d8-138">Characteristic</span></span>
- <span data-ttu-id="c22d8-139">Boekbare resource</span><span class="sxs-lookup"><span data-stu-id="c22d8-139">Bookable Resource</span></span>
- <span data-ttu-id="c22d8-140">Toewijzing van categorie met boekbare resources</span><span class="sxs-lookup"><span data-stu-id="c22d8-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="c22d8-141">Kenmerk van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="c22d8-141">Bookable Resource Characteristic</span></span>

![Import voltooid](./media/6CompleteImport.png)
