---
title: Prestaties van projectresourceplanning
description: Dit onderwerp bevat informatie over hoe de prestaties van resourceplanning bij een groot aantal projecten kunnen worden verbeterd.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010015"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="41f64-103">Prestaties van projectresourceplanning</span><span class="sxs-lookup"><span data-stu-id="41f64-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="41f64-104">Prestatieproblemen met betrekking tot resourceplanning kunnen optreden wanneer het om duizenden projecten gaat.</span><span class="sxs-lookup"><span data-stu-id="41f64-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="41f64-105">Om de prestaties van de resourceplanning te verbeteren, is er een functie beschikbaar waarmee gebruikers het resourcebeschikbaarheidsformulier sneller kunnen starten.</span><span class="sxs-lookup"><span data-stu-id="41f64-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="41f64-106">Met name wordt hiermee het synchronisatieproces van de resourcecapaciteit overgeslagen en wordt de tabel **ResprojectResource** gebruikt om het zoeken naar resources te versnellen.</span><span class="sxs-lookup"><span data-stu-id="41f64-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="41f64-107">Houd er rekening mee dat de tabel **ResRollup** wordt niet meer gebruikt.</span><span class="sxs-lookup"><span data-stu-id="41f64-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41f64-108">Als er een afhankelijkheidsrelatie is met het synchronisatieproces van de resourcecapaciteit of de tabel **ResprojectResource**, gebruik deze functie dan niet.</span><span class="sxs-lookup"><span data-stu-id="41f64-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="41f64-109">Prestatieverbeteringen van resourceplanning inschakelen</span><span class="sxs-lookup"><span data-stu-id="41f64-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="41f64-110">Voer de volgende stappen uit om prestatieverbeteringen voor resourceplanning in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="41f64-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="41f64-111">Ga naar **Functiebeheer** > **Alles** en zoek in de lijst met functies naar **Functie voor prestatieverbeteringen van projectresources inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="41f64-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="41f64-112">Selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="41f64-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="41f64-113">Als u de functie niet in de lijst kunt vinden, selecteert u **Controleren op updates** om de lijst te vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="41f64-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="41f64-114">Vernieuw uw browser en ga naar **Projectmanagement en financiële administratie** > **Periodiek** > **Projectresources** > **Capaciteit van resourcekalenders voor alle bedrijven synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="41f64-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="41f64-115">Stel **Bestaande capaciteitsrecords verwijderen** in op **Ja** om eerdere gegevens te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="41f64-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="41f64-116">Als u incrementele gegevens wilt genereren, stelt u dit in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="41f64-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="41f64-117">Selecteer in het veld **Periodecode** de periode waarin gegevens moeten worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="41f64-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="41f64-118">Als u een periodecode selecteert, hoeft u geen begin- en einddatum te definiëren.</span><span class="sxs-lookup"><span data-stu-id="41f64-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="41f64-119">Als u het veld **Periodecode** leeglaat, selecteert u specifieke start- en einddatums om gegevens te genereren.</span><span class="sxs-lookup"><span data-stu-id="41f64-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="41f64-120">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="41f64-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="41f64-121">Hiermee worden algemene gegevens gegenereerd voor de tabel **ResCalendarCapacity** voor alle bedrijven in uw omgeving, dus de batchtaak hoeft maar in één rechtspersoon te worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="41f64-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="41f64-122">De gegevens in deze batchtaak zijn nodig om de resourcecapaciteit te berekenen via de bijbehorende kalender.</span><span class="sxs-lookup"><span data-stu-id="41f64-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="41f64-123">Ga naar **Projectmanagement en financiële administratie** > **Periodiek** > **Projectresources** > **Projectresources invullen voor alle bedrijven** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="41f64-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="41f64-124">Dit is het gegevensupgradescript voor algemene gegevens in de tabellen **ResProjectResource**, **ResCalendarDateTimeRange** en **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="41f64-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="41f64-125">Waarden voor het veld **PSAPRojSchedRole.RootActivity** worden ook bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="41f64-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="41f64-126">Als dit niet wordt uitgevoerd, ontvangt u een waarschuwing wanneer u bewerkingen voor resourceplanning probeert uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="41f64-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="41f64-127">Prestatieverbeteringen van resourceplanning uitschakelen</span><span class="sxs-lookup"><span data-stu-id="41f64-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="41f64-128">Ga naar **Functiebeheer** > **Alles** en zoek naar **Functie voor prestatieverbeteringen van projectresources inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="41f64-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="41f64-129">Selecteer de functie en vervolgens de knop **Uitschakelen**.</span><span class="sxs-lookup"><span data-stu-id="41f64-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="41f64-130">Vernieuw de browser.</span><span class="sxs-lookup"><span data-stu-id="41f64-130">Refresh your browser.</span></span>
4. <span data-ttu-id="41f64-131">Ga naar **Projectmanagement en boekhouding** > **Periodiek** > **Capaciteitssynchronisatie** > **Samenvoegen van resourcecapaciteit synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="41f64-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="41f64-132">Stel op de pagina **Synchronisatie van capaciteitsopbouw** de optie **Bestaande capaciteitsrecords verwijderen** in op **Ja** om eerdere gegevens te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="41f64-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="41f64-133">Als u incrementele gegevens wilt genereren, stelt u dit in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="41f64-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="41f64-134">Selecteer in het veld **Periodecode** de periode waarin gegevens moeten worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="41f64-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="41f64-135">Als u een periodecode selecteert, hoeft u geen begin- en einddatum te definiëren.</span><span class="sxs-lookup"><span data-stu-id="41f64-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="41f64-136">Als u het veld **Periodecode** leeglaat, selecteert u specifieke start- en einddatums om gegevens te genereren.</span><span class="sxs-lookup"><span data-stu-id="41f64-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="41f64-137">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="41f64-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="41f64-138">Hiermee worden algemene gegevens gegenereerd voor de tabel **ResRollup** voor alle bedrijven in uw omgeving, dus de batchtaak hoeft maar in één rechtspersoon te worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="41f64-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="41f64-139">Deze batchtaak is vereist voor alle weergaven voor **Beschikbaarheid van resources**.</span><span class="sxs-lookup"><span data-stu-id="41f64-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="41f64-140">Als deze batchtaak niet wordt uitgevoerd, worden de gegevens voor **ResRollup** tijdens de uitvoering gegenereerd, wat even kan duren.</span><span class="sxs-lookup"><span data-stu-id="41f64-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]