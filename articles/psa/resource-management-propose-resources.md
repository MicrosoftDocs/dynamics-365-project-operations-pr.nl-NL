---
title: Projectresources voorstellen
description: Dit onderwerp bevat informatie over het voorstellen van projectresources.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 18d7dcd95806841c952ea621ec65b513ef614958
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074783"
---
# <a name="propose-project-resources"></a><span data-ttu-id="f2a89-103">Projectresources voorstellen</span><span class="sxs-lookup"><span data-stu-id="f2a89-103">Propose project resources</span></span>

<span data-ttu-id="f2a89-104">Resourcemanagers kunnen een resource voorstellen aan de projectmanager door middel van een resourceaanvraag.</span><span class="sxs-lookup"><span data-stu-id="f2a89-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="f2a89-105">Selecteer in het aanvraagraster of in de aanvraag zelf **Resources zoeken**.</span><span class="sxs-lookup"><span data-stu-id="f2a89-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="f2a89-106">Selecteer op de pagina **Planningsassistent** de resource en selecteer vervolgens in het deelvenster **Resourceboeking maken** in het veld **Boekingsstatus** de optie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="f2a89-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Voorgestelde resource geselecteerd](media/Resource-Management-image62.png)

<span data-ttu-id="f2a89-108">De volgende statusupdates worden uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="f2a89-108">The following status updates occur:</span></span>

- <span data-ttu-id="f2a89-109">Op de pagina **Planningsassistent** worden de statusindicatoren bijgewerkt om aan te geven dat de boeking wordt voorgesteld en niet hard geboekt is.</span><span class="sxs-lookup"><span data-stu-id="f2a89-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Statusindicatoren voor voorgestelde boeking op de pagina Planningsassistent](media/Resource-Management-image63.png)

- <span data-ttu-id="f2a89-111">Op de resourceaanvraag wordt de status gewijzigd in **Moet worden geëvalueerd**.</span><span class="sxs-lookup"><span data-stu-id="f2a89-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Status van resourceaanvraag wordt gewijzigd in Moet worden geëvalueerd](media/Resource-Management-image64.png)

- <span data-ttu-id="f2a89-113">Op het tabblad **Team** van het project wordt de **Aanvraagstatus** van het algemene teamlid gewijzigd in **Moet worden geëvalueerd**.</span><span class="sxs-lookup"><span data-stu-id="f2a89-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Aanvraagstatus van algemeen teamlid op het tabblad Team gewijzigd in Moet worden geëvalueerd](media/Resource-Management-image48.png)

<span data-ttu-id="f2a89-115">De projectmanager kan het voorstel accepteren of afwijzen.</span><span class="sxs-lookup"><span data-stu-id="f2a89-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="f2a89-116">Wanneer resourcemanagers resourceaanvragen verwerken, kunnen ze een van de volgende benaderingen gebruiken:</span><span class="sxs-lookup"><span data-stu-id="f2a89-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="f2a89-117">Stel meerdere resources voor om aan de vraag te voldoen, als er niet een enkele resource beschikbaar is om de vereiste uren te vervullen.</span><span class="sxs-lookup"><span data-stu-id="f2a89-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="f2a89-118">Voorgestelde uren worden vervolgens verdeeld over meerdere resources, die kunnen voldoen aan de vereiste uren.</span><span class="sxs-lookup"><span data-stu-id="f2a89-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="f2a89-119">In dit scenario kunnen de uren niet overlappen.</span><span class="sxs-lookup"><span data-stu-id="f2a89-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="f2a89-120">Stel minder resources voor dan nodig is.</span><span class="sxs-lookup"><span data-stu-id="f2a89-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="f2a89-121">In dit scenario is de voorgestelde resourcecapaciteit minder dan de vereiste uren die de aanvrager heeft opgegeven.</span><span class="sxs-lookup"><span data-stu-id="f2a89-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="f2a89-122">Wanneer de aanvrager de voorgestelde resources accepteert, wordt er daarom een niet-vervulde resourcevereiste gemaakt om de overblijvende vraag vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="f2a89-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="f2a89-123">Boek meerdere resources om aan de vraag te voldoen, als er niet één enkele resource beschikbaar is om het werk te voltooien.</span><span class="sxs-lookup"><span data-stu-id="f2a89-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="f2a89-124">Boek minder resources dan vereist.</span><span class="sxs-lookup"><span data-stu-id="f2a89-124">Book fewer resources than are required.</span></span> <span data-ttu-id="f2a89-125">In dit scenario zijn de geboekte uren minder dan de vereiste uren.</span><span class="sxs-lookup"><span data-stu-id="f2a89-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="f2a89-126">Het systeem begeleidt u bij het voorstellen van resources in plaats van boekingen, zodat de aanvrager de resterende vraag kan controleren en volgen.</span><span class="sxs-lookup"><span data-stu-id="f2a89-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="f2a89-127">Factureerbare uren</span><span class="sxs-lookup"><span data-stu-id="f2a89-127">Billable utilization</span></span>

<span data-ttu-id="f2a89-128">Resources kunnen een doelwaarde voor factureerbare bestede uren hebben.</span><span class="sxs-lookup"><span data-stu-id="f2a89-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="f2a89-129">Dit doel voor bestede uren is gedefinieerd als een kenmerk voor de standaardrol van een resource, of is ingesteld in de record van de individuele boekbare resource.</span><span class="sxs-lookup"><span data-stu-id="f2a89-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="f2a89-130">Berekeningen van bestede uren zijn gebaseerd op de werkelijke uren die resources hebben gerapporteerd door middel van goedgekeurde tijdsvermeldingen.</span><span class="sxs-lookup"><span data-stu-id="f2a89-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="f2a89-131">De volgende formules worden gebruikt om het gebruik te berekenen:</span><span class="sxs-lookup"><span data-stu-id="f2a89-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="f2a89-132">Factureerbare uren = Factureerbare werkelijke uren ÷ Resourcecapaciteit</span><span class="sxs-lookup"><span data-stu-id="f2a89-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="f2a89-133">Niet-factureerbare uren = Werkelijke tijd met factureringstype-ID = Niet-factureerbaar, Complementair of Niet beschikbaar ÷ Resourcecapaciteit</span><span class="sxs-lookup"><span data-stu-id="f2a89-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="f2a89-134">Intern = Werkelijke tijd zonder verkoopcontract ÷ Resourcecapaciteit</span><span class="sxs-lookup"><span data-stu-id="f2a89-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="f2a89-135">Resourcecapaciteit = Werkuren van resource – Afwezig – Niet-werkdagen</span><span class="sxs-lookup"><span data-stu-id="f2a89-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="f2a89-136">De weergave **Bestede uren van resource** vindt u in het deelvenster **Resources**.</span><span class="sxs-lookup"><span data-stu-id="f2a89-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Weergave Bestede uren van resource](media/Resource-Management-image65.png)

<span data-ttu-id="f2a89-138">Elke cel in het raster vertegenwoordigt het het percentage factureerbare uren van de resource in een periode, zoals een dag, week of maand.</span><span class="sxs-lookup"><span data-stu-id="f2a89-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="f2a89-139">De volgende formules worden gebruikt voor de kleur van de cellen:</span><span class="sxs-lookup"><span data-stu-id="f2a89-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="f2a89-140">**Groen:** Factureerbare bestede uren \>= doel voor Bestede uren van resource</span><span class="sxs-lookup"><span data-stu-id="f2a89-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="f2a89-141">**Geel:** Doel voor bestede uren - 20 \<= Factureerbare bestede uren \< doel voor Bestede uren</span><span class="sxs-lookup"><span data-stu-id="f2a89-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="f2a89-142">**Rood:** Factureerbare bestede uren \< doel voor bestede uren – 20</span><span class="sxs-lookup"><span data-stu-id="f2a89-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="f2a89-143">Omdat de weergave **Bestede uren van resource** is gebaseerd op het planbord, kunt u met de filtermogelijkheden van het planbord uw resultaten filteren.</span><span class="sxs-lookup"><span data-stu-id="f2a89-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="f2a89-144">Het raster vereist dat u een doelwaarde voor bestede uren instelt voor de rol of voor de individuele resource.</span><span class="sxs-lookup"><span data-stu-id="f2a89-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="f2a89-145">Dit kunt u doen in **Resources** \> **Resourcerollen**.</span><span class="sxs-lookup"><span data-stu-id="f2a89-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="f2a89-146">Daarnaast moet een standaardrol worden toegewezen aan elke boekbare resource.</span><span class="sxs-lookup"><span data-stu-id="f2a89-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="f2a89-147">Ga naar **Resources** \> **Resources**.</span><span class="sxs-lookup"><span data-stu-id="f2a89-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="f2a89-148">Controleer op het tabblad **Project Service** of een resourerol is gedefinieerd en of het veld **Is standaard** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f2a89-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="f2a89-149">U kunt extra rollen toevoegen waar **Is standaard = Nee**.</span><span class="sxs-lookup"><span data-stu-id="f2a89-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="f2a89-150">De rol waar **Is standaard = Ja** , wordt gebruikt voor het evalueren van de bestede uren van de resource ten opzichte van het doel voor die rol.</span><span class="sxs-lookup"><span data-stu-id="f2a89-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Standaardrol ingesteld](media/Resource-Management-image67.png)

<span data-ttu-id="f2a89-152">Op het tabblad **Project Service** kunt u ook een afzonderlijk doel voor bestede uren voor de resource instellen.</span><span class="sxs-lookup"><span data-stu-id="f2a89-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="f2a89-153">De berekening van de bestede uren gebruikt vervolgens die doelwaarde om te het doel van de resource te evalueren, in plaats van het doel van de standaardrol van de resource.</span><span class="sxs-lookup"><span data-stu-id="f2a89-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="f2a89-154">De bestede uren worden alleen voor een resource weergegeven als die resource goedgekeurde, factureerbare tijd heeft in de periode die wordt weergegeven in het raster.</span><span class="sxs-lookup"><span data-stu-id="f2a89-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="f2a89-155">Resourcebeschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="f2a89-155">Resource availability</span></span>

<span data-ttu-id="f2a89-156">Het is essentieel dat resourcemanagers de beschikbaarheid van resources kunnen bekijken en boekingen kunnen bijwerken.</span><span class="sxs-lookup"><span data-stu-id="f2a89-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="f2a89-157">In sommige gevallen is er geen formele vraag (resourceaanvraag), maar moet een resourcemanager reageren op een niet-geplande vraag die binnenkomt via kanalen zoals een e-mail, telefoongesprek of chat.</span><span class="sxs-lookup"><span data-stu-id="f2a89-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="f2a89-158">Resourcemanagers gebruiken het planbord om resources en boekingen bij te werken.</span><span class="sxs-lookup"><span data-stu-id="f2a89-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="f2a89-159">Werkuren van een resource worden gebruikt als basis voor het berekenen van de beschikbaarheid van een resource.</span><span class="sxs-lookup"><span data-stu-id="f2a89-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="f2a89-160">Resourceboekingen verbruiken de capaciteit van de resources.</span><span class="sxs-lookup"><span data-stu-id="f2a89-160">Resource bookings consume the capacity of the resources.</span></span>

![Planbord](media/Resource-Management-image68.png)

<span data-ttu-id="f2a89-162">Het planbord gebruikt kleuren en arcering om boekingen, beschikbaarheid en overboekingen weer te geven, en ook de status van boekingen.</span><span class="sxs-lookup"><span data-stu-id="f2a89-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="f2a89-163">Met een instelling in de instellingen van het planbord kunt u een legenda laten weergeven.</span><span class="sxs-lookup"><span data-stu-id="f2a89-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="f2a89-164">Als er naast een individuele boekbare resource op het planbord een pijl naar rechts wordt weergegeven, kan de resource worden uitgevouwen om details weer te geven van het werk waarvoor de resource is geboekt.</span><span class="sxs-lookup"><span data-stu-id="f2a89-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Boekbare resource uitgevouwen op het planbord](media/Resource-Management-image69.png)

<span data-ttu-id="f2a89-166">Omdat Dynamics 365 Project Service Automation de Universal Resource Scheduling-engine gebruikt kunt u, als ook Dynamics 365 Field Service is geïnstalleerd, de details van resourceboekingen weergeven voor projecten, werkorders en andere entiteiten waarnaar u de planning hebt uitgebreid.</span><span class="sxs-lookup"><span data-stu-id="f2a89-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Details van resourceboekingen voor projecten en werkorders](media/Resource-Management-image70.png)

<span data-ttu-id="f2a89-168">Als u meer details voor een individuele resource wilt weergeven, klikt u er met de rechtermuisknop op om de resourcekaart te openen.</span><span class="sxs-lookup"><span data-stu-id="f2a89-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Resourcekaart](media/Resource-Management-image71.png)
