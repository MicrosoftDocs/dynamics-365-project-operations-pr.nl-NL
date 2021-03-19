---
title: Voldoen aan algemene resourcevereisten
description: Dit onderwerp bevat informatie over het boeken van benoemde resources voor een algemene resourcevereiste.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279582"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="9255b-103">Voldoen aan algemene resourcevereisten</span><span class="sxs-lookup"><span data-stu-id="9255b-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="9255b-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="9255b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9255b-105">U een kunt benoemde resource boeken om een algemene resource met een resourcevereiste te vervangen.</span><span class="sxs-lookup"><span data-stu-id="9255b-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="9255b-106">Selecteer op de pagina **Projecten** het tabblad **Team**.</span><span class="sxs-lookup"><span data-stu-id="9255b-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="9255b-107">Selecteer in de lijst de algemene resource met een resourcevereiste en selecteer vervolgens **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="9255b-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="9255b-108">Of open de resourcevereiste en selecteer vervolgens **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="9255b-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="9255b-109">Selecteer op de pagina **Planningsassistent** een benoemde resource die u wilt boeken voor uw projectteam, en selecteer vervolgens **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="9255b-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="9255b-110">Wanneer de boeking is voltooid door een benoemde resource, wordt de algemene resource vervangen door de benoemde resource.</span><span class="sxs-lookup"><span data-stu-id="9255b-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="9255b-111">De toewijzingen in de planning worden ook bijgewerkt met de benoemde resource.</span><span class="sxs-lookup"><span data-stu-id="9255b-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="9255b-112">Een algemene resource vervullen met meerdere benoemde resources</span><span class="sxs-lookup"><span data-stu-id="9255b-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="9255b-113">Het voldoen aan een vereiste voor een algemene resource met meerdere benoemde resources is vergelijkbaar met het toewijzen van een één benoemde resource.</span><span class="sxs-lookup"><span data-stu-id="9255b-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="9255b-114">Er is bijvoorbeeld een taak met een duur van vijf dagen en 120 uur werk.</span><span class="sxs-lookup"><span data-stu-id="9255b-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="9255b-115">Deze taak kan niet worden voltooid door één resource met een normale 40-urige werkweek.</span><span class="sxs-lookup"><span data-stu-id="9255b-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="9255b-116">De vereiste heeft betrekking op 120 uur aan robotica-engineering gedurende vijf dagen, wat neerkomt op 24 uur per dag.</span><span class="sxs-lookup"><span data-stu-id="9255b-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="9255b-117">Dit is een voorbeeld van wanneer er meerdere benoemde resources nodig zijn om te voldoen aan een algemene resourceaanvraag.</span><span class="sxs-lookup"><span data-stu-id="9255b-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="9255b-118">U moet meerdere resources boeken om aan de vereiste te voldoen.</span><span class="sxs-lookup"><span data-stu-id="9255b-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="9255b-119">Het belangrijkste verschil in dit scenario is dat de algemene resource in het team blijft dat is toegewezen aan de taak terwijl de geboekte benoemde resourceteamleden niet worden toegewezen als onderdeel van de positie.</span><span class="sxs-lookup"><span data-stu-id="9255b-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="9255b-120">De projectmanager kan het werk naar behoefte toewijzen aan de benoemde resources.</span><span class="sxs-lookup"><span data-stu-id="9255b-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="9255b-121">De weergave **Afstemming** biedt een projectmanager overzicht van de boekingen voor meerdere resources naar taaktoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="9255b-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="9255b-122">Dit gebeurt niet automatisch omdat in elk scenario's dat complexer is dan het eenvoudige bovenstaande scenario, bijvoorbeeld als de vereiste bestaat uit een reeks taken, door het systeem moet worden verondersteld wat de intentie van de projectmanager is als het gaat om het toewijzen van resources.</span><span class="sxs-lookup"><span data-stu-id="9255b-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="9255b-123">Omdat het systeem de intentie niet begrijpt, is de kans groot dat de veronderstellingen van het systeem verschillen van de intentie van de projectmanager wat leidt tot een onjuist of onvoorspelbaar resultaat.</span><span class="sxs-lookup"><span data-stu-id="9255b-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="9255b-124">Het voorspelbare resultaat is dat de algemene resource toegewezen blijft totdat de projectmanager opzettelijk toewijzingen maakt, st met behulp van de weergave **Afstemming**.</span><span class="sxs-lookup"><span data-stu-id="9255b-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]