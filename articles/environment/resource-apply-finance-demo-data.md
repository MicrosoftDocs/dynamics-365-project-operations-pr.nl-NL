---
title: Demogegevens uit Project Operations toepassen op een Finance-cloudomgeving
description: In dit onderwerp wordt uitgelegd hoe u demogegevens van Project Operations kunt toepassen op een gehoste cloudomgeving in Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1a94862d5a024eb1630f33c0c96699e8b4b49bf2
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948825"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="8465d-103">Demogegevens uit Project Operations toepassen op een Finance-cloudomgeving</span><span class="sxs-lookup"><span data-stu-id="8465d-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="8465d-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="8465d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

><span data-ttu-id="8465d-105">[Belangrijk] Dit onderwerp is alleen van toepassing op Microsoft Dynamics 365 Finance versie 10.0.13 en kan alleen worden uitgevoerd in een gehoste cloudomgeving.</span><span class="sxs-lookup"><span data-stu-id="8465d-105">[Important] This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="8465d-106">Voltooi de stappen in dit onderwerp **VOORDAT** u kwaliteitsupdates toepast op de omgeving.</span><span class="sxs-lookup"><span data-stu-id="8465d-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="8465d-107">Open in uw LCS-project de pagina **Omgevingsdetails**.</span><span class="sxs-lookup"><span data-stu-id="8465d-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="8465d-108">Deze bevat de details bevat die nodig zijn om verbinding te maken met de omgeving met behulp van Remote Desktop Protocol (RDP).</span><span class="sxs-lookup"><span data-stu-id="8465d-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Details van -omgevingen](./media/1EnvironmentDetails.png)

<span data-ttu-id="8465d-110">De eerste set gemarkeerde referenties zijn de referenties van het lokale account en bevatten een hyperlink naar de externe desktopverbinding.</span><span class="sxs-lookup"><span data-stu-id="8465d-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="8465d-111">De inloggegevens omvatten de gebruikersnaam en het wachtwoord van de omgevingsbeheerder.</span><span class="sxs-lookup"><span data-stu-id="8465d-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="8465d-112">De tweede set referenties wordt gebruikt om in deze omgeving in te loggen op SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8465d-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="8465d-113">Maak verbinding met de omgeving via de hyperlink in **Lokale accounts** en gebruik de **Lokale accountreferenties** voor de verificatie.</span><span class="sxs-lookup"><span data-stu-id="8465d-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="8465d-114">Ga naar **Internet Information Services** > **Toepassingsgroepen** > **AOSService** en stop de service.</span><span class="sxs-lookup"><span data-stu-id="8465d-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="8465d-115">U stopt de service op dit punt, zodat u kunt doorgaan met het vervangen van de SQL-database.</span><span class="sxs-lookup"><span data-stu-id="8465d-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![AOS stoppen](./media/2StopAOS.png)

4. <span data-ttu-id="8465d-117">Ga naar **Services** en stop de volgende twee items:</span><span class="sxs-lookup"><span data-stu-id="8465d-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="8465d-118">Microsoft Dynamics 365 Unified Operations: Batchbeheerservice</span><span class="sxs-lookup"><span data-stu-id="8465d-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="8465d-119">Microsoft Dynamics 365 Unified Operations: Raamwerk voor gegevensimport/-export</span><span class="sxs-lookup"><span data-stu-id="8465d-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Services stoppen](./media/3StopServices.png)

5. <span data-ttu-id="8465d-121">Open Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="8465d-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="8465d-122">Log in met SQL-serverreferenties en gebruik de axdbadmin-gebruiker en het wachtwoord van de LCS-pagina **Omgevingsdetails**.</span><span class="sxs-lookup"><span data-stu-id="8465d-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="8465d-124">Zoek in Object Explorer **Databases** naar **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="8465d-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="8465d-125">U vervangt de database door een nieuwe database in het [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="8465d-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="8465d-126">Kopieer het zipbestand naar de virtuele machine waarmee u op afstand verbinding hebt en pak de zipinhoud uit.</span><span class="sxs-lookup"><span data-stu-id="8465d-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="8465d-127">Klik met de rechtermuisknop in SQL Server Management Studio op **AxDB** en selecteer **Taken** > **Herstellen** > **Database**.</span><span class="sxs-lookup"><span data-stu-id="8465d-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Database herstellen](./media/5RestoreDatabase.png)

9. <span data-ttu-id="8465d-129">Selecteer **Bronapparaat** en navigeer naar het bestand dat is geëxtraheerd uit de zip die u hebt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="8465d-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Bronapparaten](./media/6SourceDevice.png)

10. <span data-ttu-id="8465d-131">Selecteer **Opties** en vervolgens **De bestaande database overschrijven** en **Bestaande verbindingen met de doeldatabase sluiten**.</span><span class="sxs-lookup"><span data-stu-id="8465d-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="8465d-132">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="8465d-132">Select **OK**.</span></span>

![Instellingen herstellen](./media/7RestoreSetting.png)

<span data-ttu-id="8465d-134">U ontvangt een bevestiging dat de AXDB-herstelbewerking is gelukt.</span><span class="sxs-lookup"><span data-stu-id="8465d-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="8465d-135">Nadat u deze bevestiging hebt ontvangen, kunt u SQL Services Management Studio sluiten.</span><span class="sxs-lookup"><span data-stu-id="8465d-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="8465d-136">Ga terug naar **Internet Information Services** > **Toepassingsgroepen** > **AOSService** en start de AOSService.</span><span class="sxs-lookup"><span data-stu-id="8465d-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="8465d-137">Ga naar **Services** en start de twee services die u eerder stopte.</span><span class="sxs-lookup"><span data-stu-id="8465d-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="8465d-138">Zoek het hulpprogramma AdminUserProvisioning op deze VM.</span><span class="sxs-lookup"><span data-stu-id="8465d-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="8465d-139">Kijk onder K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="8465d-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="8465d-140">Voer het .ext-bestand uit met uw gebruikersadres in het veld **E-mailadres**.</span><span class="sxs-lookup"><span data-stu-id="8465d-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="8465d-141">Selecteer **Indienen**.</span><span class="sxs-lookup"><span data-stu-id="8465d-141">Select **Submit**.</span></span>

![Gebruiker met beheerdersrechten inrichten](./media/8AdminUserProvisioning.png)

<span data-ttu-id="8465d-143">Dit duurt een paar minuten.</span><span class="sxs-lookup"><span data-stu-id="8465d-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="8465d-144">U ontvangt een bevestigingsbericht dat de gebruiker met beheerdersrechten met succes is bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="8465d-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="8465d-145">Voer ten slotte de opdrachtprompt uit als Beheerder en voer iisreset uit</span><span class="sxs-lookup"><span data-stu-id="8465d-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS opnieuw instellen](./media/9IISReset.png)

18. <span data-ttu-id="8465d-147">Sluit de externe bureaubladsessie en gebruik de LCS-pagina **Omgevingsdetails** om in te loggen op de omgeving en te bevestigen dat deze werkt zoals verwacht.</span><span class="sxs-lookup"><span data-stu-id="8465d-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
