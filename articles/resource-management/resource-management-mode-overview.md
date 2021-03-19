---
title: Overzicht van resourcebeheermodi
description: In dit onderwerp krijgt u informatie over functionaliteit voor resourcebeheer in Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279447"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="04753-103">Overzicht van resourcebeheermodi</span><span class="sxs-lookup"><span data-stu-id="04753-103">Resource management modes overview</span></span>

<span data-ttu-id="04753-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="04753-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="04753-105">Dynamics 365 Project Operations ondersteunt twee modi zodat u de algehele boekingsstroom kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="04753-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="04753-106">De beheermodus wordt gedefinieerd als een projectparameter en kan worden gewijzigd als uw bedrijfsbehoeften veranderen.</span><span class="sxs-lookup"><span data-stu-id="04753-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="04753-107">Centrale modus</span><span class="sxs-lookup"><span data-stu-id="04753-107">Central mode</span></span>
<span data-ttu-id="04753-108">Voor organisaties die de toewijzing van resources aan projecten centraal regelen, vormt de modus Centraal een manier waarmee projectmanagers resourcevereisten op projectniveau kunnen definiëren.</span><span class="sxs-lookup"><span data-stu-id="04753-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="04753-109">Het voldoen aan de resourcevereisten wordt gedelegeerd aan een resourcemanager.</span><span class="sxs-lookup"><span data-stu-id="04753-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="04753-110">Projectmanagers kunnen resources accepteren of weigeren die door de resourcemanager worden voorgesteld.</span><span class="sxs-lookup"><span data-stu-id="04753-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Centrale modus](./media/resource-management-central.png)

<span data-ttu-id="04753-112">Om resources te beheren met de Centrale modus, zie:</span><span class="sxs-lookup"><span data-stu-id="04753-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="04753-113">Algemene, boekbare resources toewijzen aan een taak en resourcevereisten genereren</span><span class="sxs-lookup"><span data-stu-id="04753-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="04753-114">Benoemde resources boeken op basis van resourcevereisten</span><span class="sxs-lookup"><span data-stu-id="04753-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="04753-115">Een resourceaanvraag indienen</span><span class="sxs-lookup"><span data-stu-id="04753-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="04753-116">Een resourceaanvraag afhandelen</span><span class="sxs-lookup"><span data-stu-id="04753-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="04753-117">Een voorgestelde projectresource in een resourceaanvraag accepteren of afwijzen</span><span class="sxs-lookup"><span data-stu-id="04753-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="04753-118">Hybride modus</span><span class="sxs-lookup"><span data-stu-id="04753-118">Hybrid mode</span></span>
<span data-ttu-id="04753-119">In organisaties die flexibiliteit bij de toewijzing van resources nodig hebben, kunnen in de hybride modus zowel projectmanagers als resourcemanagers resources boeken.</span><span class="sxs-lookup"><span data-stu-id="04753-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybride modus](./media/resource-management-hybrid.png)

<span data-ttu-id="04753-121">Naast het ondersteunde proces in de centrale modus vindt u in de volgende onderwerpen informatie om alle andere ondersteunde boekingsstromen in de hybride modus te beheren:</span><span class="sxs-lookup"><span data-stu-id="04753-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="04753-122">Een resource rechtstreeks boeken voor een project:</span><span class="sxs-lookup"><span data-stu-id="04753-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="04753-123">Benoemde, boekbare resources boeken voor een projectteam en taken toewijzen</span><span class="sxs-lookup"><span data-stu-id="04753-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="04753-124">Een resource boeken op basis van een resourcevereiste:</span><span class="sxs-lookup"><span data-stu-id="04753-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="04753-125">Algemene, boekbare resources toewijzen aan een taak en resourcevereisten genereren</span><span class="sxs-lookup"><span data-stu-id="04753-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="04753-126">Benoemde resources boeken op basis van resourcevereisten</span><span class="sxs-lookup"><span data-stu-id="04753-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]