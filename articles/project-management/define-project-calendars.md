---
title: Projectkalenders definiëren
description: Dit onderwerp bevat informatie over het gebruik van een projectkalender om de projectplanning bij te houden.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074738"
---
# <a name="define-project-calendars"></a><span data-ttu-id="57e05-103">Projectkalenders definiëren</span><span class="sxs-lookup"><span data-stu-id="57e05-103">Define project calendars</span></span>

<span data-ttu-id="57e05-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="57e05-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="57e05-105">Als u een projectplanning wilt maken, maakt u een sjabloon voor een projectkalender waarin het aantal werkuren per dag en eventuele sluitingsdagen van het bedrijf worden aangegeven.</span><span class="sxs-lookup"><span data-stu-id="57e05-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="57e05-106">Als u een sjabloon voor een projectkalender wilt maken, koppelt u een werksjabloon aan het veld **Kalendersjabloon** voor het project.</span><span class="sxs-lookup"><span data-stu-id="57e05-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="57e05-107">Voer deze stappen uit om een werksjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="57e05-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="57e05-108">Selecteer in het linkernavigatievenster de optie **Resources**.</span><span class="sxs-lookup"><span data-stu-id="57e05-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="57e05-109">Open op de lijstpagina **Resources** een gebruikersrecord en selecteer vervolgens **Werkuren weergeven**.</span><span class="sxs-lookup"><span data-stu-id="57e05-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="57e05-110">Zorg ervoor dat u pop-ups op de browserpagina toestaat.</span><span class="sxs-lookup"><span data-stu-id="57e05-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="57e05-111">Op deze manier kunt u de werkuren zien die voor de resource zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="57e05-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="57e05-112">Selecteer op het tabblad **Maandweergave** de optie **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="57e05-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="57e05-113">Er wordt een lijst met drie opties weergegeven:</span><span class="sxs-lookup"><span data-stu-id="57e05-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="57e05-114">Nieuwe weekplanning</span><span class="sxs-lookup"><span data-stu-id="57e05-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="57e05-115">Werkplanning voor één dag</span><span class="sxs-lookup"><span data-stu-id="57e05-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="57e05-116">Verlof</span><span class="sxs-lookup"><span data-stu-id="57e05-116">Time Off</span></span>

4. <span data-ttu-id="57e05-117">Selecteer **Nieuwe weekplanning** en stel vervolgens de opties voor deze resourceplanning in.</span><span class="sxs-lookup"><span data-stu-id="57e05-117">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="57e05-118">U kunt een terugkerende weekplanning, parameters voor dagelijkse uren, sluitingsdagen van het bedrijf en meer instellen.</span><span class="sxs-lookup"><span data-stu-id="57e05-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="57e05-119">Stel het datumbereik in, selecteer **Opslaan** en selecteer vervolgens **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="57e05-119">Set the date range, select **Save** , and then select **Close**.</span></span> 
6. <span data-ttu-id="57e05-120">Ga terug naar de lijstpagina **Resources** en selecteer de resource waarvoor u de werkuren wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="57e05-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="57e05-121">Selecteer **Agenda instellen als** om de werksjabloon in te stellen.</span><span class="sxs-lookup"><span data-stu-id="57e05-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="57e05-122">Voer in het dialoogvenster **Werksjabloon** een naam voor de werksjabloon in en selecteer **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="57e05-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="57e05-123">U kunt nu de werksjabloon aan een sjabloon voor een projectkalender koppelen.</span><span class="sxs-lookup"><span data-stu-id="57e05-123">You can now associate the work template with a project calendar template.</span></span>
