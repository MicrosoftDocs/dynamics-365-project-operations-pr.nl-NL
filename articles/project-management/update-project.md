---
title: Een project bijwerken
description: In dit onderwerp krijgt u informatie over het bijwerken van projecten in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131427"
---
# <a name="update-a-project"></a><span data-ttu-id="18913-103">Een project bijwerken</span><span class="sxs-lookup"><span data-stu-id="18913-103">Update a project</span></span>

<span data-ttu-id="18913-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="18913-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="18913-105">Hieronder vindt u een overzicht van de velden die kunnen worden bijgewerkt voor een project nadat het is gemaakt en alle toepasselijke implicaties van de updates.</span><span class="sxs-lookup"><span data-stu-id="18913-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="18913-106">Projectdetailvelden</span><span class="sxs-lookup"><span data-stu-id="18913-106">Project detail fields</span></span>

- <span data-ttu-id="18913-107">**Naam**: de naam van het project.</span><span class="sxs-lookup"><span data-stu-id="18913-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="18913-108">**Beschrijving**: een overzicht van het project.</span><span class="sxs-lookup"><span data-stu-id="18913-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="18913-109">**Klant**: het bedrijf waaraan het project zal worden opgeleverd.</span><span class="sxs-lookup"><span data-stu-id="18913-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="18913-110">**Kalendersjabloon**: de werktijden van het project.</span><span class="sxs-lookup"><span data-stu-id="18913-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="18913-111">Wanneer het veld wordt gewijzigd, wordt het volledige schema opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="18913-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="18913-112">**Valuta**: de valuta voor het project.</span><span class="sxs-lookup"><span data-stu-id="18913-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="18913-113">Dit veld wordt standaard ingesteld op basis van de valuta die is gedefinieerd in de contracterende eenheid.</span><span class="sxs-lookup"><span data-stu-id="18913-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="18913-114">Wanneer de contracterende eenheid wordt bijgewerkt, wordt het veld ook bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="18913-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="18913-115">**Contracterende eenheid**: de organisatie-eenheid die de bedrijfsgroep of divisie vertegenwoordigt die primair verantwoordelijk is voor het sluiten van de verkoop en het beheren van de levering van arbeid en diensten aan de klant.</span><span class="sxs-lookup"><span data-stu-id="18913-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="18913-116">**Projectmanager**: het projectteamlid dat de bevoegdheid heeft om tijdinvoer en onkosten te beoordelen en goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="18913-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="18913-117">Velden met schattingen</span><span class="sxs-lookup"><span data-stu-id="18913-117">Estimate fields</span></span>

- <span data-ttu-id="18913-118">**Geschatte startdatum**: de datum waarop het project begint.</span><span class="sxs-lookup"><span data-stu-id="18913-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="18913-119">Wanneer dit veld wordt bijgewerkt, worden alle taken in het project proportioneel verplaatst met de nieuwe startdatum.</span><span class="sxs-lookup"><span data-stu-id="18913-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="18913-120">**Einddatum**: de datum waarop het project moet eindigen.</span><span class="sxs-lookup"><span data-stu-id="18913-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="18913-121">**Inspanning**: de geschatte inspanning voor het project.</span><span class="sxs-lookup"><span data-stu-id="18913-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="18913-122">Wanneer taken aan het project worden toegevoegd, kan dit veld niet langer worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="18913-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="18913-123">**Geschatte arbeidskosten**: de geschatte arbeidskosten van het project.</span><span class="sxs-lookup"><span data-stu-id="18913-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="18913-124">Wanneer arbeidskosten aan het project worden toegevoegd, kan dit veld niet langer worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="18913-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="18913-125">**Geschatte onkosten**: de geschatte onkosten van het project.</span><span class="sxs-lookup"><span data-stu-id="18913-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="18913-126">Wanneer onkosten aan het project worden toegevoegd, kan dit veld niet langer worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="18913-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="18913-127">Velden met werkelijke projectgegevens</span><span class="sxs-lookup"><span data-stu-id="18913-127">Project actual fields</span></span>
- <span data-ttu-id="18913-128">**Werkelijke start**: de datum waarop het project is gestart.</span><span class="sxs-lookup"><span data-stu-id="18913-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="18913-129">**Werkelijk einde**: wordt bijgewerkt wanneer een project is voltooid.</span><span class="sxs-lookup"><span data-stu-id="18913-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="18913-130">Velden voor projectstatus</span><span class="sxs-lookup"><span data-stu-id="18913-130">Project status fields</span></span>

- <span data-ttu-id="18913-131">**Algemene projectstatus**: de algehele status van het project die wordt geleverd door de projectmanager.</span><span class="sxs-lookup"><span data-stu-id="18913-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="18913-132">**Opmerkingen**: een beschrijving van de huidige status van het project, geleverd door de projectmanager.</span><span class="sxs-lookup"><span data-stu-id="18913-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

