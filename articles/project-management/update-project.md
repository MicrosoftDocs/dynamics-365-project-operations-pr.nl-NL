---
title: Een project bijwerken
description: In dit onderwerp krijgt u informatie over het bijwerken van projecten in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074419"
---
# <a name="update-a-project"></a><span data-ttu-id="229d2-103">Een project bijwerken</span><span class="sxs-lookup"><span data-stu-id="229d2-103">Update a project</span></span>

<span data-ttu-id="229d2-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="229d2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="229d2-105">Hieronder vindt u een overzicht van de velden die kunnen worden bijgewerkt voor een project nadat het is gemaakt en alle toepasselijke implicaties van de updates.</span><span class="sxs-lookup"><span data-stu-id="229d2-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="229d2-106">Projectdetailvelden</span><span class="sxs-lookup"><span data-stu-id="229d2-106">Project detail fields</span></span>

- <span data-ttu-id="229d2-107">**Naam** : de naam van het project.</span><span class="sxs-lookup"><span data-stu-id="229d2-107">**Name** : The title of the project.</span></span>
- <span data-ttu-id="229d2-108">**Beschrijving** : een overzicht van het project.</span><span class="sxs-lookup"><span data-stu-id="229d2-108">**Description** : An overview of the project.</span></span>
- <span data-ttu-id="229d2-109">**Klant** : het bedrijf waaraan het project zal worden opgeleverd.</span><span class="sxs-lookup"><span data-stu-id="229d2-109">**Customer** : The company the project will be delivered to.</span></span>
- <span data-ttu-id="229d2-110">**Kalendersjabloon** : de werktijden van het project.</span><span class="sxs-lookup"><span data-stu-id="229d2-110">**Calendar template** : The working hours of the project.</span></span> <span data-ttu-id="229d2-111">Wanneer het veld wordt gewijzigd, wordt het volledige schema opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="229d2-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="229d2-112">**Valuta** : de valuta voor het project.</span><span class="sxs-lookup"><span data-stu-id="229d2-112">**Currency** : The currency for the project.</span></span> <span data-ttu-id="229d2-113">Dit veld wordt standaard ingesteld op basis van de valuta die is gedefinieerd in de contracterende eenheid.</span><span class="sxs-lookup"><span data-stu-id="229d2-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="229d2-114">Wanneer de contracterende eenheid wordt bijgewerkt, wordt het veld ook bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="229d2-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="229d2-115">**Contracterende eenheid** : de organisatie-eenheid die de bedrijfsgroep of divisie vertegenwoordigt die primair verantwoordelijk is voor het sluiten van de verkoop en het beheren van de levering van arbeid en diensten aan de klant.</span><span class="sxs-lookup"><span data-stu-id="229d2-115">**Contracting Unit** : The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="229d2-116">**Projectmanager** : het projectteamlid dat de bevoegdheid heeft om tijdinvoer en onkosten te beoordelen en goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="229d2-116">**Project Manager** : The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="229d2-117">Velden met schattingen</span><span class="sxs-lookup"><span data-stu-id="229d2-117">Estimate fields</span></span>

- <span data-ttu-id="229d2-118">**Geschatte startdatum** : de datum waarop het project begint.</span><span class="sxs-lookup"><span data-stu-id="229d2-118">**Estimated Start Date** : The date that the project will begin.</span></span> <span data-ttu-id="229d2-119">Wanneer dit veld wordt bijgewerkt, worden alle taken in het project proportioneel verplaatst met de nieuwe startdatum.</span><span class="sxs-lookup"><span data-stu-id="229d2-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="229d2-120">**Einddatum** : de datum waarop het project moet eindigen.</span><span class="sxs-lookup"><span data-stu-id="229d2-120">**Finish Date** : The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="229d2-121">**Inspanning** : de geschatte inspanning voor het project.</span><span class="sxs-lookup"><span data-stu-id="229d2-121">**Effort** : The estimated effort of the project.</span></span> <span data-ttu-id="229d2-122">Wanneer taken aan het project worden toegevoegd, kan dit veld niet langer worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="229d2-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="229d2-123">**Geschatte arbeidskosten** : de geschatte arbeidskosten van het project.</span><span class="sxs-lookup"><span data-stu-id="229d2-123">**Estimated Labor Cost** : The estimated labor cost of the project.</span></span> <span data-ttu-id="229d2-124">Wanneer arbeidskosten aan het project worden toegevoegd, kan dit veld niet langer worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="229d2-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="229d2-125">**Geschatte onkosten** : de geschatte onkosten van het project.</span><span class="sxs-lookup"><span data-stu-id="229d2-125">**Estimated Expenses** : The estimated expenses of the project.</span></span> <span data-ttu-id="229d2-126">Wanneer onkosten aan het project worden toegevoegd, kan dit veld niet langer worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="229d2-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="229d2-127">Velden met werkelijke projectgegevens</span><span class="sxs-lookup"><span data-stu-id="229d2-127">Project actual fields</span></span>
- <span data-ttu-id="229d2-128">**Werkelijke start** : de datum waarop het project is gestart.</span><span class="sxs-lookup"><span data-stu-id="229d2-128">**Actual Start** : The date that the project started.</span></span>
- <span data-ttu-id="229d2-129">**Werkelijk einde** : wordt bijgewerkt wanneer een project is voltooid.</span><span class="sxs-lookup"><span data-stu-id="229d2-129">**Actual Finish** : To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="229d2-130">Velden voor projectstatus</span><span class="sxs-lookup"><span data-stu-id="229d2-130">Project status fields</span></span>

- <span data-ttu-id="229d2-131">**Algemene projectstatus** : de algehele status van het project die wordt geleverd door de projectmanager.</span><span class="sxs-lookup"><span data-stu-id="229d2-131">**Overall Project Status** : The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="229d2-132">**Opmerkingen** : een beschrijving van de huidige status van het project, geleverd door de projectmanager.</span><span class="sxs-lookup"><span data-stu-id="229d2-132">**Comments** : A narrative regarding the current health of the project provided by the Project manager.</span></span>

