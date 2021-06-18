---
title: Resourcecapaciteit synchroniseren
description: Dit onderwerp bevat informatie over het synchroniseren van de capaciteit van een resource in meerdere agenda's en projecten.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997505"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="fc3e1-103">Resourcecapaciteit synchroniseren</span><span class="sxs-lookup"><span data-stu-id="fc3e1-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc3e1-104">De processen voor resourcesynchronisatie helpen garanderen dat informatie voor de agenda en de basisagenda naar beneden stroomt in de resourceplanning van het project.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="fc3e1-105">Als de agenda wordt gewijzigd, voeren de processen de vereiste updates uit in de planning van projectresources.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="fc3e1-106">De processen helpen ook de prestaties te verbeteren, omdat de resourcegegevens van de agenda van tevoren wordt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="fc3e1-107">Daarom vinden updates van gegevens over resourceplanning sneller plaats.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="fc3e1-108">We raden u aan de processen als batch te plannen in plaats van een voor een.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="fc3e1-109">Anders bestaat het risico dat iemand de inclusieve datums vergeet waarop de gegevens voor het laatst zijn gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="fc3e1-110">Als geen inclusieve datums worden gebruikt, kunnen er hiaten ontstaan tijdens de synchronisatie van de datum.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Agendasynchronisatie](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="fc3e1-112">Samenvoegen van resourcecapaciteit synchroniseren</span><span class="sxs-lookup"><span data-stu-id="fc3e1-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="fc3e1-113">Het synchronisatieproces is ontworpen om alle agendagegevens van resources te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="fc3e1-114">Deze informatie omvat basisagendagegevens over eventuele wijzigingen in de capaciteitstabel van de resourceagenda van het project.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="fc3e1-115">Als er nieuwe resources aan het project worden toegevoegd, zorgt synchronisatie ervoor dat de bijgewerkte agendagegevens beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="fc3e1-116">Deze synchronisatie kan op elk moment worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="fc3e1-117">We raden u aan een batch te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-117">We recommend that you use a batch.</span></span> <span data-ttu-id="fc3e1-118">De opties zijn beschikbaar tijdens het synchroniseren van capaciteitsreserveringen.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="fc3e1-119">Selecteer **Projectmanagement en financiële administratie** &gt; **Periodiek** &gt; **Capaciteitssynchronisatie** &gt; **Samenvoegen van resourcecapaciteit synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="fc3e1-120">Stel de opties in de volgende tabel in.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="fc3e1-121">Optie</span><span class="sxs-lookup"><span data-stu-id="fc3e1-121">Option</span></span>      | <span data-ttu-id="fc3e1-122">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="fc3e1-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="fc3e1-123">Periodecode</span><span class="sxs-lookup"><span data-stu-id="fc3e1-123">Period code</span></span> | <span data-ttu-id="fc3e1-124">Selecteer desgewenst de intervalcode van de grootboekdatum om de begin- en einddatums in te stellen voor het synchronisatieproces voor het samenvoegen van resourcecapaciteit.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="fc3e1-125">Begindatum</span><span class="sxs-lookup"><span data-stu-id="fc3e1-125">Start date</span></span>  | <span data-ttu-id="fc3e1-126">Voer de begindatum in voor het synchronisatieproces voor het samenvoegen van resourcecapaciteit.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="fc3e1-127">Einddatum</span><span class="sxs-lookup"><span data-stu-id="fc3e1-127">End date</span></span>    | <span data-ttu-id="fc3e1-128">Voer de einddatum in voor het synchronisatieproces voor het samenvoegen van resourcecapaciteit.</span><span class="sxs-lookup"><span data-stu-id="fc3e1-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="fc3e1-129">[![Synchronisatieproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="fc3e1-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]