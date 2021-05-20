---
title: Planningsmodi
description: Dit onderwerp biedt informatie over planningsmodi.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981429"
---
# <a name="scheduling-modes"></a><span data-ttu-id="be143-103">Planningsmodi</span><span class="sxs-lookup"><span data-stu-id="be143-103">Scheduling modes</span></span>

<span data-ttu-id="be143-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="be143-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="be143-105">Dynamics 365 Project Operations biedt organisaties de mogelijkheid om te definiëren hoe zij wijzigingen in sleutelvariabelen in taken binnen de structuur voor werkspecificatie beheren.</span><span class="sxs-lookup"><span data-stu-id="be143-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="be143-106">Op basis van de specifieke behoeften van de organisatie kunnen projectmanagers wijzigingen aanbrengen in de planningsmodus wanneer een project wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="be143-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="be143-107">Er zijn drie planningsmodi beschikbaar in Project Operations:</span><span class="sxs-lookup"><span data-stu-id="be143-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="be143-108">Vaste duur (dit is de standaardmodus)</span><span class="sxs-lookup"><span data-stu-id="be143-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="be143-109">Vast werk</span><span class="sxs-lookup"><span data-stu-id="be143-109">Fixed work</span></span>
  - <span data-ttu-id="be143-110">Vaste eenheden</span><span class="sxs-lookup"><span data-stu-id="be143-110">Fixed units</span></span>

<span data-ttu-id="be143-111">De waarden die worden beïnvloed door de definitie van een specifieke planningsmodus, worden bepaald door de volgende formule:</span><span class="sxs-lookup"><span data-stu-id="be143-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="be143-112">Inspanning (*Werk*) = Duur x Eenheden</span><span class="sxs-lookup"><span data-stu-id="be143-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="be143-113">Wanneer u de planningsmodus van een project definieert, stelt u een van deze waarden in, die dan niet kunnen worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="be143-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="be143-114">Als u deze waarde als een constante aanhoudt, krijgt die waarde een prioriteit, waardoor het systeem wordt geïnformeerd dat deze niet moet worden gewijzigd wanneer de andere twee waarden veranderen.</span><span class="sxs-lookup"><span data-stu-id="be143-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="be143-115">De volgende tabel bevat informatie over de gevolgen van het selecteren van een specifieke modus.</span><span class="sxs-lookup"><span data-stu-id="be143-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="be143-116">**In deze taak**</span><span class="sxs-lookup"><span data-stu-id="be143-116">**In this task**</span></span>             | <span data-ttu-id="be143-117">**Als u eenheden herziet**</span><span class="sxs-lookup"><span data-stu-id="be143-117">**If you revise units**</span></span>   | <span data-ttu-id="be143-118">**Als u duur herziet**</span><span class="sxs-lookup"><span data-stu-id="be143-118">**If you revise duration**</span></span> | <span data-ttu-id="be143-119">**Als u inspanning herziet**</span><span class="sxs-lookup"><span data-stu-id="be143-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="be143-120">Taak met vaste eenheden</span><span class="sxs-lookup"><span data-stu-id="be143-120">Fixed units task</span></span>     | <span data-ttu-id="be143-121">Duur wordt opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="be143-121">Duration is recalculated.</span></span> | <span data-ttu-id="be143-122">Inspanning wordt opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="be143-122">Effort is recalculated.</span></span>    | <span data-ttu-id="be143-123">Duur wordt opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="be143-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="be143-124">Taak met vaste inspanning</span><span class="sxs-lookup"><span data-stu-id="be143-124">Fixed effort task</span></span>    | <span data-ttu-id="be143-125">Duur wordt opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="be143-125">Duration is recalculated.</span></span> | <span data-ttu-id="be143-126">Eenheden worden opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="be143-126">Units are recalculated.</span></span>    | <span data-ttu-id="be143-127">Duur wordt opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="be143-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="be143-128">Taak met vaste duur</span><span class="sxs-lookup"><span data-stu-id="be143-128">Fixed duration task</span></span>  | <span data-ttu-id="be143-129">Inspanning wordt opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="be143-129">Effort is recalculated.</span></span>   | <span data-ttu-id="be143-130">Inspanning wordt opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="be143-130">Effort is recalculated.</span></span>    | <span data-ttu-id="be143-131">Eenheden worden opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="be143-131">Units are recalculated.</span></span>   |

<span data-ttu-id="be143-132">Zie [Het taaktype wijzigen voor een nauwkeurigere planning](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72) voor meer informatie over de implicaties van een bepaalde modus.</span><span class="sxs-lookup"><span data-stu-id="be143-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="be143-133">In het onderwerp wordt de term **Werk** gebruikt in plaats van **Inspanning**.</span><span class="sxs-lookup"><span data-stu-id="be143-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="be143-134">De planningsmodus van de organisatie wijzigen</span><span class="sxs-lookup"><span data-stu-id="be143-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="be143-135">Voer de volgende stappen uit om de planningsmodus van een organisatie te definiëren.</span><span class="sxs-lookup"><span data-stu-id="be143-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="be143-136">Ga naar **Instellingen** \> **Algemeen** \> **Parameters** en selecteer vervolgens de projectparameter.</span><span class="sxs-lookup"><span data-stu-id="be143-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="be143-137">Selecteer op de pagina **Projectparameters** de standaardplanningsmodus voor de organisatie en definieer vervolgens de mogelijkheid voor de projectmanager om de instelling te overschrijven bij het maken van een nieuw project.</span><span class="sxs-lookup"><span data-stu-id="be143-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="be143-138">De instelling voor de planningsmodus wijzigen in een project</span><span class="sxs-lookup"><span data-stu-id="be143-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="be143-139">Als een organisatie de projectmanager toestaat om de standaardplanningsmodus te overschrijven, kan de projectmanager die wijziging doorvoeren bij het maken van een nieuw project.</span><span class="sxs-lookup"><span data-stu-id="be143-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="be143-140">Nadat het project is opgeslagen, kan de planningsmodus echter niet meer worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="be143-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="be143-141">Gekopieerde projecten</span><span class="sxs-lookup"><span data-stu-id="be143-141">Copied projects</span></span>

<span data-ttu-id="be143-142">Omdat een project wordt gemaakt wanneer de actie voor het kopiëren van een project wordt uitgevoerd, kan de projectmanager de planningsmodus niet instellen.</span><span class="sxs-lookup"><span data-stu-id="be143-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="be143-143">Het bestemmingsproject zal altijd standaard de modus gebruiken die op organisatieniveau is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="be143-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="be143-144">Gekopieerde taken</span><span class="sxs-lookup"><span data-stu-id="be143-144">Copied tasks</span></span>

<span data-ttu-id="be143-145">Wanneer een taak van het ene project naar het andere wordt gekopieerd, neemt de taak de planningsmodus van het bestemmingsproject over.</span><span class="sxs-lookup"><span data-stu-id="be143-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
