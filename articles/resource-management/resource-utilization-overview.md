---
title: Overzicht van bestede uren van resource
description: Dit onderwerp bevat informatie over de bestede uren van resources in Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367930"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="8494a-103">Overzicht van bestede uren van resource</span><span class="sxs-lookup"><span data-stu-id="8494a-103">Resource utilization overview</span></span>

<span data-ttu-id="8494a-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="8494a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8494a-105">Resources kunnen een doelwaarde voor factureerbare bestede uren hebben.</span><span class="sxs-lookup"><span data-stu-id="8494a-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="8494a-106">Dit doel voor bestede uren is gedefinieerd als een kenmerk voor de standaardrol van een resource, of is ingesteld in de record van de individuele boekbare resource.</span><span class="sxs-lookup"><span data-stu-id="8494a-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="8494a-107">Berekeningen van bestede uren zijn gebaseerd op de werkelijke uren die resources hebben gerapporteerd door middel van goedgekeurde tijdsvermeldingen.</span><span class="sxs-lookup"><span data-stu-id="8494a-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="8494a-108">De volgende formules worden gebruikt om het gebruik te berekenen:</span><span class="sxs-lookup"><span data-stu-id="8494a-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="8494a-109">Factureerbare uren = Factureerbare werkelijke uren ÷ Resourcecapaciteit</span><span class="sxs-lookup"><span data-stu-id="8494a-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="8494a-110">Niet-factureerbare uren = Werkelijke tijd met factureringstype-ID = Niet-factureerbaar, Complementair of Niet beschikbaar ÷ Resourcecapaciteit</span><span class="sxs-lookup"><span data-stu-id="8494a-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="8494a-111">Intern = Werkelijke tijd zonder verkoopcontract ÷ Resourcecapaciteit</span><span class="sxs-lookup"><span data-stu-id="8494a-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="8494a-112">Resourcecapaciteit = Werkuren van resource – Afwezig – Niet-werkdagen</span><span class="sxs-lookup"><span data-stu-id="8494a-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="8494a-113">De weergave **Bestede uren van resource** vindt u in het deelvenster **Resources**.</span><span class="sxs-lookup"><span data-stu-id="8494a-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="8494a-114">Elke cel in het raster vertegenwoordigt het het percentage factureerbare uren van de resource in een periode, zoals een dag, week of maand.</span><span class="sxs-lookup"><span data-stu-id="8494a-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="8494a-115">De volgende formules worden gebruikt voor de kleur van de cellen:</span><span class="sxs-lookup"><span data-stu-id="8494a-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="8494a-116">**Groen**: factureerbare bestede uren >= doel voor bestede uren van resource</span><span class="sxs-lookup"><span data-stu-id="8494a-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="8494a-117">**Geel**: doel voor bestede uren - 20 <= factureerbare bestede uren < doel voor bestede uren</span><span class="sxs-lookup"><span data-stu-id="8494a-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="8494a-118">**Rood**: factureerbare bestede uren < doel voor bestede uren – 20</span><span class="sxs-lookup"><span data-stu-id="8494a-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="8494a-119">Omdat de weergave **Bestede uren van resource** is gebaseerd op het planbord, kunt u met de filtermogelijkheden van het planbord uw resultaten filteren.</span><span class="sxs-lookup"><span data-stu-id="8494a-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="8494a-120">Het raster vereist dat u een doelwaarde voor bestede uren instelt voor de rol of voor de individuele resource.</span><span class="sxs-lookup"><span data-stu-id="8494a-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="8494a-121">Dit kunt u doen in **Resources** > **Resourcerollen**.</span><span class="sxs-lookup"><span data-stu-id="8494a-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="8494a-122">Daarnaast moet een standaardrol worden toegewezen aan elke boekbare resource.</span><span class="sxs-lookup"><span data-stu-id="8494a-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="8494a-123">Ga naar **Resources** > **Resources**.</span><span class="sxs-lookup"><span data-stu-id="8494a-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="8494a-124">Controleer op het tabblad **Project Service** of een resourerol is gedefinieerd en of het veld **Is standaard** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8494a-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="8494a-125">U kunt extra rollen toevoegen waar **Is standaard** = **Nee**.</span><span class="sxs-lookup"><span data-stu-id="8494a-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="8494a-126">De rol waar **Is standaard** = **Ja**, wordt gebruikt voor het evalueren van de bestede uren van de resource ten opzichte van het doel voor die rol.</span><span class="sxs-lookup"><span data-stu-id="8494a-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="8494a-127">Op het tabblad **Project Service** kunt u ook een afzonderlijk doel voor bestede uren voor de resource instellen.</span><span class="sxs-lookup"><span data-stu-id="8494a-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="8494a-128">De berekening van de bestede uren gebruikt vervolgens die doelwaarde om te het doel van de resource te evalueren, in plaats van het doel van de standaardrol van de resource.</span><span class="sxs-lookup"><span data-stu-id="8494a-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="8494a-129">De bestede uren worden alleen voor een resource weergegeven als die resource goedgekeurde, factureerbare tijd heeft in de periode die wordt weergegeven in het raster.</span><span class="sxs-lookup"><span data-stu-id="8494a-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]