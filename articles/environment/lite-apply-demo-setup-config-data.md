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
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948817"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="4c5c3-103">Demo- en configuratiegegevens toepassen voor Project Operations Lite-implementatie, van deal tot proforma-facturering</span><span class="sxs-lookup"><span data-stu-id="4c5c3-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="4c5c3-104">_\*\*Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="4c5c3-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="4c5c3-105">Download het [Pakket met mastergegevens](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="4c5c3-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="4c5c3-106">Navigeer naar de map *ProjOpsDemoDataSetupAndMaster - Integrated CMT* en voer het uitvoerbare bestand *DataMigrationUtility* uit.</span><span class="sxs-lookup"><span data-stu-id="4c5c3-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="4c5c3-107">Op pagina 1 van de wizard Common Data Service Configuratiemigratie (CMT) selecteert u **Gegevens importeren** en vervolgens **Doorgaan**.</span><span class="sxs-lookup"><span data-stu-id="4c5c3-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Configuratiemigratie](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="4c5c3-109">Selecteer op pagina 2 van de CMT-wizard **Office 365** als **Implementatietype**.</span><span class="sxs-lookup"><span data-stu-id="4c5c3-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="4c5c3-110">Schakel de selectievakjes **Een lijst met beschikbare organisaties weergeven** en **Geavanceerd weergeven** in.</span><span class="sxs-lookup"><span data-stu-id="4c5c3-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="4c5c3-111">Selecteer de regio van uw tenant, voer uw inloggegevens in en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="4c5c3-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Configuratie inloggen](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="4c5c3-113">Selecteer op pagina 3 uit de lijst met organisaties op de tenant de organisatie waarin u de demogegevens wilt importeren en selecteer **Login**.</span><span class="sxs-lookup"><span data-stu-id="4c5c3-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="4c5c3-114">Selecteer op pagina 4 het zipbestand *MasterAndSetupData* in de uitgepakte map, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="4c5c3-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zipbestand](./media/3ZipFile.png)

![Selecteer een bestand](./media/4SelectAFile.png)

9. <span data-ttu-id="4c5c3-117">Selecteer nadat het zipbestand is geselecteerd **Gegevens importeren**.</span><span class="sxs-lookup"><span data-stu-id="4c5c3-117">After the zip file is selected, select **Import Data**.</span></span>

![Gegevens importeren](./media/5ImportData.png)

10. <span data-ttu-id="4c5c3-119">Het importeren duurt ongeveer twee tot tien minuten, afhankelijk van uw netwerksnelheid.</span><span class="sxs-lookup"><span data-stu-id="4c5c3-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="4c5c3-120">Sluit de CMT-wizard nadat het importeren is voltooid.</span><span class="sxs-lookup"><span data-stu-id="4c5c3-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="4c5c3-121">Controleer uw organisatie op gegevens in de volgende 20 entiteiten:</span><span class="sxs-lookup"><span data-stu-id="4c5c3-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="4c5c3-122">Valuta</span><span class="sxs-lookup"><span data-stu-id="4c5c3-122">Currency</span></span>
- <span data-ttu-id="4c5c3-123">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="4c5c3-123">Organizational Unit</span></span>
- <span data-ttu-id="4c5c3-124">Contact</span><span class="sxs-lookup"><span data-stu-id="4c5c3-124">Contact</span></span>
- <span data-ttu-id="4c5c3-125">Belastinggroep</span><span class="sxs-lookup"><span data-stu-id="4c5c3-125">Tax Group</span></span>
- <span data-ttu-id="4c5c3-126">Klantengroep</span><span class="sxs-lookup"><span data-stu-id="4c5c3-126">Customer Group</span></span>
- <span data-ttu-id="4c5c3-127">Eenheid</span><span class="sxs-lookup"><span data-stu-id="4c5c3-127">Unit</span></span>
- <span data-ttu-id="4c5c3-128">Eenhedengroep</span><span class="sxs-lookup"><span data-stu-id="4c5c3-128">Unit Group</span></span>
- <span data-ttu-id="4c5c3-129">Prijslijst</span><span class="sxs-lookup"><span data-stu-id="4c5c3-129">Price List</span></span>
- <span data-ttu-id="4c5c3-130">Prijslijst voor projectparameters</span><span class="sxs-lookup"><span data-stu-id="4c5c3-130">Project Parameter Price List</span></span>
- <span data-ttu-id="4c5c3-131">Factuurfrequentie</span><span class="sxs-lookup"><span data-stu-id="4c5c3-131">Invoice Frequency</span></span>
- <span data-ttu-id="4c5c3-132">Factuurfrequentiedetail</span><span class="sxs-lookup"><span data-stu-id="4c5c3-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="4c5c3-133">Categorie van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="4c5c3-133">Bookable Resource Category</span></span>
- <span data-ttu-id="4c5c3-134">Transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="4c5c3-134">Transaction Category</span></span>
- <span data-ttu-id="4c5c3-135">Onkostencategorie</span><span class="sxs-lookup"><span data-stu-id="4c5c3-135">Expense Category</span></span>
- <span data-ttu-id="4c5c3-136">Rolprijs</span><span class="sxs-lookup"><span data-stu-id="4c5c3-136">Role Price</span></span>
- <span data-ttu-id="4c5c3-137">Prijs voor transactiecategorie</span><span class="sxs-lookup"><span data-stu-id="4c5c3-137">Transaction Category Price</span></span>
- <span data-ttu-id="4c5c3-138">Kenmerk</span><span class="sxs-lookup"><span data-stu-id="4c5c3-138">Characteristic</span></span>
- <span data-ttu-id="4c5c3-139">Boekbare resource</span><span class="sxs-lookup"><span data-stu-id="4c5c3-139">Bookable Resource</span></span>
- <span data-ttu-id="4c5c3-140">Toewijzing van categorie met boekbare resources</span><span class="sxs-lookup"><span data-stu-id="4c5c3-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="4c5c3-141">Kenmerk van boekbare resources</span><span class="sxs-lookup"><span data-stu-id="4c5c3-141">Bookable Resource Characteristic</span></span>

![Import voltooid](./media/6CompleteImport.png)
