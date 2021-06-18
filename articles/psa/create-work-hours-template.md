---
title: Een werkurensjabloon maken
description: In dit onderwerp wordt beschreven hoe u een werkurensjabloon kunt maken in Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997190"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="d7a05-103">Een werkurensjabloon maken (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d7a05-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d7a05-104">Als u een project wilt maken en beheren, moet u een agendasjabloon op het project toepassen.</span><span class="sxs-lookup"><span data-stu-id="d7a05-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="d7a05-105">De agendasjabloon definieert de volgende projectkenmerken:</span><span class="sxs-lookup"><span data-stu-id="d7a05-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="d7a05-106">Werkuren, inclusief begin- en eindtijd</span><span class="sxs-lookup"><span data-stu-id="d7a05-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="d7a05-107">Werkdagen</span><span class="sxs-lookup"><span data-stu-id="d7a05-107">Working days</span></span>
- <span data-ttu-id="d7a05-108">Agenda-uitzonderingen zoals niet-werkdagen</span><span class="sxs-lookup"><span data-stu-id="d7a05-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="d7a05-109">De agendasjabloon die op een project wordt toegepast, is een kopie van de agendasjabloon die is gedefinieerd in de instellingen van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="d7a05-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="d7a05-110">Als u de agendasjabloon wijzigt, worden die wijzigingen niet doorgevoerd in de werktijden van het project.</span><span class="sxs-lookup"><span data-stu-id="d7a05-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="d7a05-111">Als u de werktijden van het project wilt wijzigen, moet een nieuwe sjabloon worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d7a05-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="d7a05-112">Als u een agendasjabloon voor uw organisatie wilt maken, zijn er twee belangrijke vereisten:</span><span class="sxs-lookup"><span data-stu-id="d7a05-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="d7a05-113">Definieer de gewenste werkuren van de sjabloon met behulp van een nieuwe of bestaande boekbare resource.</span><span class="sxs-lookup"><span data-stu-id="d7a05-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="d7a05-114">Maak een nieuwe agendasjabloon en koppel de sjabloon aan de boekbare resource.</span><span class="sxs-lookup"><span data-stu-id="d7a05-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="d7a05-115">**De werkuren van de sjabloon definiëren**</span><span class="sxs-lookup"><span data-stu-id="d7a05-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="d7a05-116">Ga naar **Resources** \> **Resources**.</span><span class="sxs-lookup"><span data-stu-id="d7a05-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="d7a05-117">Maak een nieuwe resource om naar te verwijzen in de agendasjabloon of selecteer een bestaande resource.</span><span class="sxs-lookup"><span data-stu-id="d7a05-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="d7a05-118">Selecteer het tabblad **Werkuren** van de resource en voer de instructies uit in [Werkuren instellen voor een resource](/dynamics365/field-service/set-work-hours-resource.md) om de agendaregels te configureren.</span><span class="sxs-lookup"><span data-stu-id="d7a05-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="d7a05-119">**Een nieuwe agendasjabloon maken**</span><span class="sxs-lookup"><span data-stu-id="d7a05-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="d7a05-120">Ga naar **Instellingen** \> **Agendasjabloon**.</span><span class="sxs-lookup"><span data-stu-id="d7a05-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="d7a05-121">Selecteer **Nieuw** en voer een naam, beschrijving en sjabloonresource in.</span><span class="sxs-lookup"><span data-stu-id="d7a05-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="d7a05-122">Wanneer in een agendasjabloon naar een resource wordt verwezen, wordt een kopie van de agenda van de resource aan de agendasjabloon gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="d7a05-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="d7a05-123">Als de werkuren van de gekopieerde sjabloon veranderen, worden die wijzigingen niet doorgevoerd in de agendasjabloon.</span><span class="sxs-lookup"><span data-stu-id="d7a05-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="d7a05-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d7a05-124">See Also</span></span>  
 [<span data-ttu-id="d7a05-125">Resources instellen</span><span class="sxs-lookup"><span data-stu-id="d7a05-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
