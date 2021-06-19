---
title: Overzicht van Project Service Automation
description: In dit onderwerp wordt informatie verstrekt over de oplossing voor integratie van Dynamics 365 Project Service Automation naar Dynamics 365 Finance.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ca459b99881b612e4656be112c8a2e420b4196e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005875"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="6cfb8-103">Overzicht van Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6cfb8-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6cfb8-104">De integratieoplossing van Project Service Automation naar Finance gebruikt de functie Gegevensintegratie om gegevens tussen exemplaren van Dynamics 365 Finance en Dynamics 365 Project Service Automation via Common Data Service te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="6cfb8-105">De integratiesjablonen die beschikbaar zijn met de functie Gegevensintegratie maken de stroom van projecten, projectcontracten, projectcontractregels en mijlpalen voor projectcontractregels, projecttaken, onkostentransactiecategorieën, uurschattingen en onkostenschattingen vanuit Project Service Automation naar Finance mogelijk.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="6cfb8-106">Als u versie 7.3.0 gebruikt, moet u KB 4074835 installeren.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="6cfb8-107">U kunt dan projecten met een vaste prijs integreren.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="6cfb8-108">Als u versie 7.3.0 gebruikt en u transactiekosten overbrengt vanuit Project Service Automation, moet u KB 4345320 installeren om deze kosten in de projectfactuur op te nemen.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="6cfb8-109">Als u versie 8.0 gebruikt, kunt u projecttaakintegratie, onkostentransactiecategorieën, uurschattingen, onkostenschattingen en functionaliteitsvergrendeling gebruiken.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="6cfb8-110">Als u versie 8.0.1 of hoger gebruikt, kunt u werkelijke waarden synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="6cfb8-111">Voordat u Project Service Automation Finance kunt integreren, moet u de integratieparameters van Project Service Automation configureren.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="6cfb8-112">Zie [Integratieparameters voor Project Service Automation](PSA-parameters.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="6cfb8-113">Deze integratieoplossing maakt directe synchronisatie mogelijk in de volgende scenario's:</span><span class="sxs-lookup"><span data-stu-id="6cfb8-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="6cfb8-114">Onderhoud projectcontracten in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="6cfb8-115">Maak projecten in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="6cfb8-116">Onderhoud projectcontractregels in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="6cfb8-117">Onderhoud mijlpalen voor projectcontractregels in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="6cfb8-118">Onderhoud projecttaken in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="6cfb8-119">Onderhoud onkostentransactiecategorieën in Finance en synchroniseer ze rechtstreeks vanuit Finance naar Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="6cfb8-120">Maak schattingen van projecturen in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="6cfb8-121">Maak schattingen van projectonkosten in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="6cfb8-122">Maak werkelijke waarden voor projecttijd, onkosten en tarieven in Project Service Automation en maak projecttransacties in het integratiejournaal van Project Service Automation, zodat ze in Finance kunnen worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="6cfb8-123">Gegevenssynchronisatie</span><span class="sxs-lookup"><span data-stu-id="6cfb8-123">Data synchronization</span></span>

<span data-ttu-id="6cfb8-124">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd als onderdeel van de integratie tussen Project Service Automation en Finance.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="6cfb8-125">Niet alle sjablonen zijn momenteel beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-125">Not all templates are currently available.</span></span> <span data-ttu-id="6cfb8-126">Sjablonen worden vrijgegeven zodra ze zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="6cfb8-127">[![Integratie van Project Service Automation met Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="6cfb8-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="6cfb8-128">Systeemvereisten voor Finance</span><span class="sxs-lookup"><span data-stu-id="6cfb8-128">System requirements for Finance</span></span>

<span data-ttu-id="6cfb8-129">Als u de integratieoplossing Project Service Automation naar Finance wilt gebruiken, moet u Enterprise-editie 7.3 met platformupdate 12 of hoger installeren.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="6cfb8-130">Systeemvereisten voor Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6cfb8-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="6cfb8-131">Als u de integratieoplossing Project Service Automation naar Finance wilt gebruiken, moet u de volgende onderdelen installeren:</span><span class="sxs-lookup"><span data-stu-id="6cfb8-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="6cfb8-132">Dynamics 365 Project Service Automation versie 9.0.0.0 of later</span><span class="sxs-lookup"><span data-stu-id="6cfb8-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="6cfb8-133">Oplossing Van prospect tot contanten voor Dynamics 365 Sales, versie 1.14.0.0 (v14) of hoger</span><span class="sxs-lookup"><span data-stu-id="6cfb8-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="6cfb8-134">Project Service Automation naar Finance-oplossing voor Dynamics 365 Project Service Automation versie 1.0.0.0 of hoger</span><span class="sxs-lookup"><span data-stu-id="6cfb8-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="6cfb8-135">Installeer de integratieoplossing Project Service Automation naar Finance in uw Project Service Automation-exemplaar</span><span class="sxs-lookup"><span data-stu-id="6cfb8-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="6cfb8-136">Download de integratieoplossing Project Service Automation naar Finance vanuit het [Microsoft-downloadcentrum](https://www.microsoft.com/download/details.aspx?id=57016) en volg de instructies die bij de oplossing zijn geleverd.</span><span class="sxs-lookup"><span data-stu-id="6cfb8-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]