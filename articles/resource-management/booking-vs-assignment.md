---
title: Boekingen versus toewijzingen
description: Dit onderwerp biedt informatie over de verschillen tussen resourceboekingen en resourcetoewijzingen.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012760"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="76cce-103">Boekingen versus toewijzingen</span><span class="sxs-lookup"><span data-stu-id="76cce-103">Bookings vs assignments</span></span>

<span data-ttu-id="76cce-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="76cce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="76cce-105">Boekingen zijn de harde of zachte toewijzing van resources aan een project.</span><span class="sxs-lookup"><span data-stu-id="76cce-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="76cce-106">Een harde boeking verbruikt de capaciteit van een resource.</span><span class="sxs-lookup"><span data-stu-id="76cce-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="76cce-107">Boekingen vertegenwoordigen organisatieconcepten voor teams, zodat ze kunnen begrijpen hoe resources bij verschillende projecten worden ingezet.</span><span class="sxs-lookup"><span data-stu-id="76cce-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="76cce-108">Dynamics 365 Project Operations beschouwt boekingen als een concept op projectniveau.</span><span class="sxs-lookup"><span data-stu-id="76cce-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="76cce-109">In tegenstelling tot boekingen zijn toewijzingen de toezegging van resources voor projecttaken in de projectplanning.</span><span class="sxs-lookup"><span data-stu-id="76cce-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="76cce-110">De resources kunnen een naam hebben of generiek zijn.</span><span class="sxs-lookup"><span data-stu-id="76cce-110">The resources can be named or generic.</span></span>  <span data-ttu-id="76cce-111">Wanneer een resourcevereiste wordt afgeleid uit de projecttaaktoewijzingen, gebruikt Project Operations de inspanningscontouren van de resourcetoewijzing om de contouren van de details van resourcevereisten op te bouwen.</span><span class="sxs-lookup"><span data-stu-id="76cce-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="76cce-112">Een verwijzing naar de resourcetoewijzingen wordt echter niet gehandhaafd.</span><span class="sxs-lookup"><span data-stu-id="76cce-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="76cce-113">Updates van de boekingen die zijn afgeleid van de resourcevereiste werken geen resourcetoewijzingen bij.</span><span class="sxs-lookup"><span data-stu-id="76cce-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="76cce-114">Meestal is de som van de boekingen voor een resource gelijk aan de som van de toewijzingen van de resource voor een of meerdere taken.</span><span class="sxs-lookup"><span data-stu-id="76cce-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="76cce-115">In Project Operations is deze overeenkomst echter niet verplicht.</span><span class="sxs-lookup"><span data-stu-id="76cce-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="76cce-116">In de weergave **Afstemming** wordt aan een projectmanager getoond waar boekingen en toewijzingen van een resource niet overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="76cce-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]