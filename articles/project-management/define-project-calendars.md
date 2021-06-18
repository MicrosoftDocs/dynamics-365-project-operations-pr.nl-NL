---
title: Projectkalenders definiëren
description: Dit onderwerp biedt informatie over hoe u een agendasjabloon op een project kunt toepassen om de projectplanning bij te houden.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998990"
---
# <a name="define-project-calendars"></a><span data-ttu-id="51f79-103">Projectkalenders definiëren</span><span class="sxs-lookup"><span data-stu-id="51f79-103">Define project calendars</span></span>

<span data-ttu-id="51f79-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="51f79-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="51f79-105">Als u een project wilt maken en beheren, moet u een agendasjabloon op het project toepassen.</span><span class="sxs-lookup"><span data-stu-id="51f79-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="51f79-106">De agendasjabloon definieert de volgende projectkenmerken:</span><span class="sxs-lookup"><span data-stu-id="51f79-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="51f79-107">Werkuren, inclusief begin- en eindtijd</span><span class="sxs-lookup"><span data-stu-id="51f79-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="51f79-108">Werkdagen</span><span class="sxs-lookup"><span data-stu-id="51f79-108">Working days</span></span>
- <span data-ttu-id="51f79-109">Agenda-uitzonderingen zoals niet-werkdagen</span><span class="sxs-lookup"><span data-stu-id="51f79-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="51f79-110">De agendasjabloon die op een project wordt toegepast, is een kopie van de agendasjabloon die is gedefinieerd in de instellingen van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="51f79-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="51f79-111">Als u de agendasjabloon wijzigt, worden die wijzigingen niet doorgevoerd in de werktijden van het project.</span><span class="sxs-lookup"><span data-stu-id="51f79-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="51f79-112">Als u de werktijden van het project wilt wijzigen, moet een nieuwe sjabloon worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="51f79-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="51f79-113">Als u een agendasjabloon voor uw organisatie wilt maken, zijn er twee belangrijke vereisten:</span><span class="sxs-lookup"><span data-stu-id="51f79-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="51f79-114">Definieer de gewenste werkuren van de sjabloon met behulp van een nieuwe of bestaande boekbare resource.</span><span class="sxs-lookup"><span data-stu-id="51f79-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="51f79-115">Maak een nieuwe agendasjabloon en koppel de sjabloon aan de boekbare resource.</span><span class="sxs-lookup"><span data-stu-id="51f79-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="51f79-116">**De werkuren van de sjabloon definiëren**</span><span class="sxs-lookup"><span data-stu-id="51f79-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="51f79-117">Ga naar **Resources** \> **Resources**.</span><span class="sxs-lookup"><span data-stu-id="51f79-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="51f79-118">Maak een nieuwe resource om naar te verwijzen in de agendasjabloon of selecteer een bestaande resource.</span><span class="sxs-lookup"><span data-stu-id="51f79-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="51f79-119">Selecteer het tabblad **Werkuren** van de resource en voer de instructies uit in [Werkuren instellen voor een resource](/dynamics365/field-service/set-work-hours-resource.md) om de agendaregels te configureren.</span><span class="sxs-lookup"><span data-stu-id="51f79-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="51f79-120">**Een nieuwe agendasjabloon maken**</span><span class="sxs-lookup"><span data-stu-id="51f79-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="51f79-121">Ga naar **Instellingen** \> **Agendasjabloon**.</span><span class="sxs-lookup"><span data-stu-id="51f79-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="51f79-122">Selecteer **Nieuw** en voer een naam, beschrijving en sjabloonresource in.</span><span class="sxs-lookup"><span data-stu-id="51f79-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="51f79-123">Wanneer in een agendasjabloon naar een resource wordt verwezen, wordt een kopie van de agenda van de resource aan de agendasjabloon gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="51f79-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="51f79-124">Als de werkuren van de gekopieerde sjabloon veranderen, worden die wijzigingen niet doorgevoerd in de agendasjabloon.</span><span class="sxs-lookup"><span data-stu-id="51f79-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="51f79-125">U kunt nu de werksjabloon aan een sjabloon voor een projectkalender koppelen.</span><span class="sxs-lookup"><span data-stu-id="51f79-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

