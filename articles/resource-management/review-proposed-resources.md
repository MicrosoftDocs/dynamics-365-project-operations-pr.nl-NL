---
title: Voorgestelde resources beoordelen
description: Dit onderwerp bevat informatie over hoe u projectresources kunt voorstellen.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401167"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="94eca-103">Voorgestelde resources beoordelen</span><span class="sxs-lookup"><span data-stu-id="94eca-103">Review proposed resources</span></span>

<span data-ttu-id="94eca-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="94eca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="94eca-105">Resourcemanagers kunnen een resource voorstellen aan de projectmanager door middel van een resourceaanvraag.</span><span class="sxs-lookup"><span data-stu-id="94eca-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="94eca-106">Selecteer in het aanvraagraster of in de aanvraag zelf **Resources zoeken**.</span><span class="sxs-lookup"><span data-stu-id="94eca-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="94eca-107">Selecteer op de pagina **Planningsassistent** de resource en selecteer vervolgens in het deelvenster **Resourceboeking maken** in het veld **Boekingsstatus** de optie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="94eca-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="94eca-108">De volgende statusupdates worden uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="94eca-108">The following status updates occur:</span></span>

- <span data-ttu-id="94eca-109">Op de pagina **Planningsassistent** worden de statusindicatoren bijgewerkt om aan te geven dat de boeking wordt voorgesteld en niet hard geboekt is.</span><span class="sxs-lookup"><span data-stu-id="94eca-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="94eca-110">Op de resourceaanvraag wordt de status gewijzigd in **Moet worden geëvalueerd**.</span><span class="sxs-lookup"><span data-stu-id="94eca-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="94eca-111">Op het tabblad **Team** van het project wordt de **Aanvraagstatus** van het algemene teamlid gewijzigd in **Moet worden geëvalueerd**.</span><span class="sxs-lookup"><span data-stu-id="94eca-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="94eca-112">De projectmanager kan het voorstel accepteren of afwijzen.</span><span class="sxs-lookup"><span data-stu-id="94eca-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="94eca-113">Wanneer resourcemanagers resourceaanvragen verwerken, kunnen ze een van de volgende benaderingen gebruiken:</span><span class="sxs-lookup"><span data-stu-id="94eca-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="94eca-114">Stel meerdere resources voor om aan de vraag te voldoen, als er niet een enkele resource beschikbaar is om de vereiste uren te vervullen.</span><span class="sxs-lookup"><span data-stu-id="94eca-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="94eca-115">Voorgestelde uren worden vervolgens verdeeld over meerdere resources, die kunnen voldoen aan de vereiste uren.</span><span class="sxs-lookup"><span data-stu-id="94eca-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="94eca-116">In dit scenario kunnen de uren niet overlappen.</span><span class="sxs-lookup"><span data-stu-id="94eca-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="94eca-117">Stel minder resources voor dan nodig is.</span><span class="sxs-lookup"><span data-stu-id="94eca-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="94eca-118">In dit scenario is de voorgestelde resourcecapaciteit minder dan de vereiste uren die de aanvrager heeft opgegeven.</span><span class="sxs-lookup"><span data-stu-id="94eca-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="94eca-119">Wanneer de aanvrager de voorgestelde resources accepteert, wordt er daarom een niet-vervulde resourcevereiste gemaakt om de overblijvende vraag vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="94eca-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="94eca-120">Boek meerdere resources om aan de vraag te voldoen, als er niet één enkele resource beschikbaar is om het werk te voltooien.</span><span class="sxs-lookup"><span data-stu-id="94eca-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="94eca-121">Boek minder resources dan vereist.</span><span class="sxs-lookup"><span data-stu-id="94eca-121">Book fewer resources than are required.</span></span> <span data-ttu-id="94eca-122">In dit scenario zijn de geboekte uren minder dan de vereiste uren.</span><span class="sxs-lookup"><span data-stu-id="94eca-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="94eca-123">Het systeem begeleidt u bij het voorstellen van resources in plaats van boekingen, zodat de aanvrager de resterende vraag kan controleren en volgen.</span><span class="sxs-lookup"><span data-stu-id="94eca-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="94eca-124">Resourcebeschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="94eca-124">Resource availability</span></span>

<span data-ttu-id="94eca-125">Het is essentieel dat resourcemanagers de beschikbaarheid van resources kunnen bekijken en boekingen kunnen bijwerken.</span><span class="sxs-lookup"><span data-stu-id="94eca-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="94eca-126">In sommige gevallen is er geen formele vraag (resourceaanvraag), maar moet een resourcemanager reageren op een niet-geplande vraag die binnenkomt via kanalen zoals een e-mail, telefoongesprek of chat.</span><span class="sxs-lookup"><span data-stu-id="94eca-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="94eca-127">Resourcemanagers gebruiken het planbord om resources en boekingen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="94eca-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="94eca-128">Werkuren van een resource worden gebruikt als basis voor het berekenen van de beschikbaarheid van een resource.</span><span class="sxs-lookup"><span data-stu-id="94eca-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="94eca-129">Resourceboekingen verbruiken de capaciteit van de resources.</span><span class="sxs-lookup"><span data-stu-id="94eca-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="94eca-130">Het planbord gebruikt kleuren en arcering om boekingen, beschikbaarheid en overboekingen weer te geven, en ook de status van boekingen.</span><span class="sxs-lookup"><span data-stu-id="94eca-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="94eca-131">Met een instelling in de instellingen van het planbord kunt u een legenda laten weergeven.</span><span class="sxs-lookup"><span data-stu-id="94eca-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="94eca-132">Als er naast een individuele boekbare resource op het planbord een pijl naar rechts wordt weergegeven, kan de resource worden uitgevouwen om details weer te geven van het werk waarvoor de resource is geboekt.</span><span class="sxs-lookup"><span data-stu-id="94eca-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="94eca-133">Omdat Dynamics 365 Project Operations de Universal Resource Scheduling-engine gebruikt kunt u, als ook Dynamics 365 Field Service is geïnstalleerd, de details van resourceboekingen weergeven voor projecten, werkorders en andere entiteiten waarnaar u de planning hebt uitgebreid.</span><span class="sxs-lookup"><span data-stu-id="94eca-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="94eca-134">Als u meer details voor een individuele resource wilt weergeven, klikt u er met de rechtermuisknop op om de resourcekaart te openen.</span><span class="sxs-lookup"><span data-stu-id="94eca-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>

