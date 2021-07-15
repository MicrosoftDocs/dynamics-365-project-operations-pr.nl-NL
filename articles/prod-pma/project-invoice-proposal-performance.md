---
title: Prestaties van projectfactuurvoorstellen
description: Dit onderwerp biedt informatie over prestatieverbeteringen voor projectfactuurvoorstellen.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269784"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="ce24a-103">Prestaties van projectfactuurvoorstellen</span><span class="sxs-lookup"><span data-stu-id="ce24a-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce24a-104">Wanneer u een nieuw factuurvoorstel maakt, kunt u prestatieproblemen tegenkomen naarmate het aantal projecten en subprojecten toeneemt.</span><span class="sxs-lookup"><span data-stu-id="ce24a-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="ce24a-105">Om de prestaties te verbeteren, is er een functie beschikbaar die de tijd verkort die nodig is om een nieuw factuurvoorstel te maken voor geboekte projecttransacties.</span><span class="sxs-lookup"><span data-stu-id="ce24a-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="ce24a-106">Prestatieverbetering voor projectfactuurvoorstellen inschakelen</span><span class="sxs-lookup"><span data-stu-id="ce24a-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="ce24a-107">Voer de volgende stappen uit om de functie voor prestatieverbetering van projectfactuurvoorstellen in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="ce24a-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="ce24a-108">Ga naar **Functiebeheer** > **Alle**.</span><span class="sxs-lookup"><span data-stu-id="ce24a-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="ce24a-109">Zoek in de lijst met functies naar **Prestatieverbetering voor projectfactuurvoorstellen**.</span><span class="sxs-lookup"><span data-stu-id="ce24a-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="ce24a-110">Selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="ce24a-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="ce24a-111">Vernieuw de browser en maak een nieuw factuurvoorstel.</span><span class="sxs-lookup"><span data-stu-id="ce24a-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="ce24a-112">Prestatieverbetering voor projectfactuurvoorstellen uitschakelen</span><span class="sxs-lookup"><span data-stu-id="ce24a-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="ce24a-113">Voer de volgende stappen uit om de functie voor prestatieverbetering van projectfactuurvoorstellen uit te schakelen.</span><span class="sxs-lookup"><span data-stu-id="ce24a-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="ce24a-114">Ga naar **Functiebeheer** > **Alle**.</span><span class="sxs-lookup"><span data-stu-id="ce24a-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="ce24a-115">Zoek in de lijst met functies naar **Prestatieverbetering voor projectfactuurvoorstellen**.</span><span class="sxs-lookup"><span data-stu-id="ce24a-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="ce24a-116">Selecteer **Uitschakelen**.</span><span class="sxs-lookup"><span data-stu-id="ce24a-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="ce24a-117">Vernieuw de browser.</span><span class="sxs-lookup"><span data-stu-id="ce24a-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="ce24a-118">Factuurvoorstelprestaties kunnen niet worden toegepast wanneer factureringsregels zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ce24a-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="ce24a-119">Tijdens het batchproces om factuurvoorstellen te maken, splitst het aantal subtakende taken in een maximum aantal op basis van het aantal contracten met factureerbare transacties, ongeacht wat u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="ce24a-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="ce24a-120">Als u bijvoorbeeld **3** invoert voor het aantal subtaken voor het maken van factuurvoorstellen in batch en er zijn slechts twee contracten met factureerbare transacties, worden er slechts twee subtaken gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ce24a-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
