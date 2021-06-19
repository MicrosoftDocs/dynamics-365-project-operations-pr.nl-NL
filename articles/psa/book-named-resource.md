---
title: Benoemde resources boeken op basis van resourcevereisten
description: Dit onderwerp bevat informatie over het boeken van benoemde resources voor een algemene resourcevereiste.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: c2f97107de938975491770ab4e2ed18a3145d0e3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013390"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="2a724-103">Benoemde resources boeken op basis van resourcevereisten</span><span class="sxs-lookup"><span data-stu-id="2a724-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2a724-104">U een kunt benoemde resource boeken om een algemene resource met een resourcevereiste te vervangen.</span><span class="sxs-lookup"><span data-stu-id="2a724-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="2a724-105">Klik in Project Service Automation (PSA) op de pagina **Projecten** op het tabblad **Team**.</span><span class="sxs-lookup"><span data-stu-id="2a724-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="2a724-106">Selecteer de algemene resource met een resourcevereiste in de lijst en klik vervolgens op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="2a724-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="2a724-107">Of open de resourcevereiste en klik op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="2a724-107">Or, open the resource requirement and then click **Book**.</span></span>


![Een algemeen teamlid boeken](media/RM-how-to-14.png)


3. <span data-ttu-id="2a724-109">Selecteer op de pagina **Planningsassistent** een benoemde resource die u wilt boeken naar uw projectteam en klik vervolgens op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="2a724-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Een algemeen teamlid boeken via de planningsassistent](media/RM-how-to-15.png)

<span data-ttu-id="2a724-111">Wanneer de boeking is voltooid door een benoemde resource, wordt de algemene resource vervangen door de benoemde resource.</span><span class="sxs-lookup"><span data-stu-id="2a724-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Benoemd teamlid dat een algemeen teamlid vervangt](media/RM-how-to-16.png)

<span data-ttu-id="2a724-113">De toewijzingen in de planning worden ook bijgewerkt met de benoemde resource.</span><span class="sxs-lookup"><span data-stu-id="2a724-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Benoemd teamlid dat is toegewezen aan projecttaken](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="2a724-115">Een algemene resource vervullen met meerdere benoemde resources</span><span class="sxs-lookup"><span data-stu-id="2a724-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="2a724-116">Het voldoen aan een vereiste voor een algemene resource met meerdere benoemde resources is vergelijkbaar met het toewijzen van een één benoemde resource.</span><span class="sxs-lookup"><span data-stu-id="2a724-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="2a724-117">Er is bijvoorbeeld een taak met een duur van vijf dagen en 120 uur werk.</span><span class="sxs-lookup"><span data-stu-id="2a724-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="2a724-118">Deze taak kan niet worden voltooid door één resource met een normale 40-urige werkweek.</span><span class="sxs-lookup"><span data-stu-id="2a724-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Een taak van 120 uur werk in vijf dagen](media/RM-how-to-21.png)

<span data-ttu-id="2a724-120">De vereiste heeft betrekking op 120 uur aan robotica-engineering gedurende vijf dagen, wat neerkomt op 24 uur per dag.</span><span class="sxs-lookup"><span data-stu-id="2a724-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Vereiste per dag](media/RM-how-to-22.png)

<span data-ttu-id="2a724-122">Dit is een voorbeeld van wanneer er meerdere benoemde resources nodig zijn om te voldoen aan een algemene resourceaanvraag.</span><span class="sxs-lookup"><span data-stu-id="2a724-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="2a724-123">U moet meerdere resources boeken om aan de vereiste te voldoen.</span><span class="sxs-lookup"><span data-stu-id="2a724-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Meerdere resources boeken om aan de vereiste te voldoen](media/RM-how-to-23.png)

<span data-ttu-id="2a724-125">Het belangrijkste verschil in dit scenario is dat de algemene resource in het team blijft dat is toegewezen aan de taak terwijl de geboekte benoemde resourceteamleden niet worden toegewezen als onderdeel van de positie.</span><span class="sxs-lookup"><span data-stu-id="2a724-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="2a724-126">De projectmanager kan het werk naar behoefte toewijzen aan de benoemde resources.</span><span class="sxs-lookup"><span data-stu-id="2a724-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="2a724-127">De weergave **Afstemming** biedt een projectmanager overzicht van de boekingen voor meerdere resources naar taaktoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="2a724-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="2a724-128">Dit gebeurt niet automatisch omdat in complexere scenario's dan het bovenstaande voorbeeld, bijvoorbeeld waar de vereiste bestaat uit een bundel taken, moet worden aangenomen wat de intentie van de projectmanager is voor het toewijzen.</span><span class="sxs-lookup"><span data-stu-id="2a724-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="2a724-129">Omdat het systeem de intentie niet begrijpt, kunnen de veronderstellingen waarschijnlijk anders zijn dan bedoeld en zal er een onjuist of onvoorspelbaar resultaat optreden.</span><span class="sxs-lookup"><span data-stu-id="2a724-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="2a724-130">Het voorspelbare resultaat is dat de algemene resource toegewezen blijft totdat de projectmanager opzettelijk toewijzingen maakt, st met behulp van de weergave **Afstemming**.</span><span class="sxs-lookup"><span data-stu-id="2a724-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]