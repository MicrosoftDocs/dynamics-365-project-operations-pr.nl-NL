---
title: Prestaties van projectfactuurvoorstellen
description: Dit onderwerp biedt informatie over prestatieverbeteringen voor projectfactuurvoorstellen.
author: Yowelle
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 78c924cba8107471a5f8e6d6a38265890d32d72b
ms.sourcegitcommit: 2350c6f3728067a8298adde640e6fdd5984eb077
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573553"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="edf7d-103">Prestaties van projectfactuurvoorstellen</span><span class="sxs-lookup"><span data-stu-id="edf7d-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="edf7d-104">Wanneer u een nieuw factuurvoorstel maakt, kunt u prestatieproblemen tegenkomen naarmate het aantal projecten en subprojecten toeneemt.</span><span class="sxs-lookup"><span data-stu-id="edf7d-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="edf7d-105">Om de prestaties te verbeteren, is er een functie beschikbaar die de tijd verkort die nodig is om een nieuw factuurvoorstel te maken voor geboekte projecttransacties.</span><span class="sxs-lookup"><span data-stu-id="edf7d-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="edf7d-106">Prestatieverbetering voor projectfactuurvoorstellen inschakelen</span><span class="sxs-lookup"><span data-stu-id="edf7d-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="edf7d-107">Voer de volgende stappen uit om de functie voor prestatieverbetering van projectfactuurvoorstellen in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="edf7d-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="edf7d-108">Ga naar **Functiebeheer** > **Alle**.</span><span class="sxs-lookup"><span data-stu-id="edf7d-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="edf7d-109">Zoek in de lijst met functies naar **Prestatieverbetering voor projectfactuurvoorstellen**.</span><span class="sxs-lookup"><span data-stu-id="edf7d-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="edf7d-110">Selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="edf7d-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="edf7d-111">Vernieuw de browser en maak een nieuw factuurvoorstel.</span><span class="sxs-lookup"><span data-stu-id="edf7d-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="edf7d-112">Prestatieverbetering voor projectfactuurvoorstellen uitschakelen</span><span class="sxs-lookup"><span data-stu-id="edf7d-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="edf7d-113">Voer de volgende stappen uit om de functie voor prestatieverbetering van projectfactuurvoorstellen uit te schakelen.</span><span class="sxs-lookup"><span data-stu-id="edf7d-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="edf7d-114">Ga naar **Functiebeheer** > **Alle**.</span><span class="sxs-lookup"><span data-stu-id="edf7d-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="edf7d-115">Zoek in de lijst met functies naar **Prestatieverbetering voor projectfactuurvoorstellen**.</span><span class="sxs-lookup"><span data-stu-id="edf7d-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="edf7d-116">Selecteer **Uitschakelen**.</span><span class="sxs-lookup"><span data-stu-id="edf7d-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="edf7d-117">Vernieuw de browser.</span><span class="sxs-lookup"><span data-stu-id="edf7d-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="edf7d-118">De prestaties van factuurvoorstellen kunnen niet worden toegepast wanneer factureringsregels zijn ingeschakeld of als er batchprocessen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="edf7d-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
