---
title: Resourcekalenders definiëren
description: Dit onderwerp biedt informatie over het definiëren van de werkuurkalenders voor resources in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: daa49cf8ba9ba005a16777f590c4c06d024de529
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123912"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="37c61-103">Resourcekalenders definiëren</span><span class="sxs-lookup"><span data-stu-id="37c61-103">Define resource calendars</span></span>

<span data-ttu-id="37c61-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="37c61-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="37c61-105">Elke boekbare resource die aan een project werkt, moet een werkurenkalender hebben om zijn/haar beschikbaarheid te bepalen.</span><span class="sxs-lookup"><span data-stu-id="37c61-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="37c61-106">De werkuren voor een resource kunnen op twee manieren worden gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="37c61-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="37c61-107">Individuele kalenderregels voor een resource opgeven</span><span class="sxs-lookup"><span data-stu-id="37c61-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="37c61-108">Een bestaande kalendersjabloon toepassen voor de resource</span><span class="sxs-lookup"><span data-stu-id="37c61-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="37c61-109">De werkuren van een resource opgeven</span><span class="sxs-lookup"><span data-stu-id="37c61-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="37c61-110">Selecteer **Resources** in het menu **Resources**.</span><span class="sxs-lookup"><span data-stu-id="37c61-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="37c61-111">Selecteer in de rasterweergave de toepasselijke **boekbare resource**.</span><span class="sxs-lookup"><span data-stu-id="37c61-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="37c61-112">Op de pagina **Resourcedetails** selecteert u het tabblad **Werkuren**. Standaard wordt de kalender met boekbare resources ingesteld op de werkuren van de sjabloon voor standaardwerkuren die voor de organisatie is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="37c61-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="37c61-113">Klik om de werktijden bij te werken met de rechtermuisknop op de startdatum van de voorgestelde kalenderregel die moet worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="37c61-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="37c61-114">Gebruik het kalenderregelmenu om een kalenderregel te definiëren voor een specifieke dag, de rest van de reeks of de hele kalender.</span><span class="sxs-lookup"><span data-stu-id="37c61-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="37c61-115">Als de optie is geselecteerd, kunt u het volgende opgeven:</span><span class="sxs-lookup"><span data-stu-id="37c61-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="37c61-116">De dag van de week waarvoor de werktijden gelden.</span><span class="sxs-lookup"><span data-stu-id="37c61-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="37c61-117">De werktijden op elke dag.</span><span class="sxs-lookup"><span data-stu-id="37c61-117">The working times within each day.</span></span>
    - <span data-ttu-id="37c61-118">De tijdzone voor de kalenderregel.</span><span class="sxs-lookup"><span data-stu-id="37c61-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="37c61-119">Indien van toepassing kan ook niet-werktijd worden opgegeven voor de regel.</span><span class="sxs-lookup"><span data-stu-id="37c61-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="37c61-120">Een kalendersjabloon toepassen op een resource</span><span class="sxs-lookup"><span data-stu-id="37c61-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="37c61-121">Selecteer **Resources** in het menu **Resources**.</span><span class="sxs-lookup"><span data-stu-id="37c61-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="37c61-122">Selecteer maximaal 25 **boekbare resources** om bij te werken in de rasterweergave.</span><span class="sxs-lookup"><span data-stu-id="37c61-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="37c61-123">Selecteer **Kalender instellen** om een dialoogvenster met een lijst met beschikbare werkuursjablonen te openen.</span><span class="sxs-lookup"><span data-stu-id="37c61-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="37c61-124">Selecteer de gewenste sjabloon en selecteer vervolgens **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="37c61-124">Select the template you want to use, and then select **Apply**.</span></span>
