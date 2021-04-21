---
title: Projectverkopen bijhouden
description: Deze onderwerp biedt informatie over hoe in Project Operations de voortgang wordt bijgehouden op basis van arbeidsinkomsten voor een project.
author: rumant
manager: AnnBe
ms.date: 03/24/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 438c44dcfaf9677075eb07688c1e65c6e7053755
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711037"
---
# <a name="project-sales-tracking"></a><span data-ttu-id="a785b-103">Projectverkopen bijhouden</span><span class="sxs-lookup"><span data-stu-id="a785b-103">Project sales tracking</span></span>

<span data-ttu-id="a785b-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="a785b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a785b-105">Dynamics 365 Project Operations houdt schattingen en inkomsten voor arbeid op het laagste vereiste detailniveau bij in een projectplan.</span><span class="sxs-lookup"><span data-stu-id="a785b-105">Dynamics 365 Project Operations tracks labor estimates and revenue at the lowest required granularity on a project plan.</span></span> <span data-ttu-id="a785b-106">De schatting van arbeidsinkomsten is gebaseerd op de geplande inspanning en de algemene of benoemde resources die zijn toegewezen aan elke bladknooppunttaak in het projectplan.</span><span class="sxs-lookup"><span data-stu-id="a785b-106">The estimate of labor revenue is based on the planned effort and the generic or named resources that are assigned to each leaf node task in the project plan.</span></span> <span data-ttu-id="a785b-107">Wanneer het project begint en mensen tijd beginnen te rapporteren over verschillende projecttaken, worden de werkelijke inkomsten voor arbeid samengevat, waardoor een berekening van de projecties begint.</span><span class="sxs-lookup"><span data-stu-id="a785b-107">When the project begins and people start to report time on various project tasks, the actual revenue on labor is summarized which starts a calculation of the projections.</span></span>

## <a name="labor-revenue-tracking-view"></a><span data-ttu-id="a785b-108">De weergave voor het bijhouden van arbeidsinkomsten</span><span class="sxs-lookup"><span data-stu-id="a785b-108">Labor revenue tracking view</span></span>

<span data-ttu-id="a785b-109">Op de pagina **Projecten** op het tabblad **Volgen** kunt u **Volgen** > **Kosten** selecteren om de weergave **Kosten bijhouden** te openen.</span><span class="sxs-lookup"><span data-stu-id="a785b-109">On the **Projects** page, on the **Tracking** tab, you can select **Tracking** > **Cost** to open the **Cost Tracking** view.</span></span> <span data-ttu-id="a785b-110">U kunt ook **Gebruiken** > **Factureringstarief** selecteren om de weergave **Inkomsten bijhouden** te openen om de voortgang van de arbeidsinkomsten voor elke taak in het projectplan te bekijken.</span><span class="sxs-lookup"><span data-stu-id="a785b-110">Or, you can select **Use** > **Bill Rate** to open the **Revenue Tracking** view, which shows the progress of labor revenue on each task in the project plan.</span></span> <span data-ttu-id="a785b-111">Deze weergave vergelijkt ook de werkelijke arbeidsinkomsten die aan een taak zijn besteed met de geplande arbeidsinkomsten van de taak.</span><span class="sxs-lookup"><span data-stu-id="a785b-111">This view also compares the actual labor revenue spent on a task to the task's planned labor revenue.</span></span> <span data-ttu-id="a785b-112">In Project Operations worden de volgende formules gebruikt om metrische gegevens over arbeidsinkomsten te berekenen:</span><span class="sxs-lookup"><span data-stu-id="a785b-112">Project Operations uses the following formulas to calculate labor revenue metrics:</span></span>

- <span data-ttu-id="a785b-113">**Geplande omzet**: geschatte verkoopwaarden van alle resourcetoewijzingen voor elke bladknooppunttaak</span><span class="sxs-lookup"><span data-stu-id="a785b-113">**Planned Revenue**: Estimated sales values of all resource assignments on each leaf node task</span></span>
- <span data-ttu-id="a785b-114">**Werkelijke omzet**: som van alle niet-gefactureerde verkoop voor de tijd die voor de taak is geregistreerd</span><span class="sxs-lookup"><span data-stu-id="a785b-114">**Actual Revenue**: Sum of all unbilled sales actuals for time recorded on the task</span></span>
- <span data-ttu-id="a785b-115">**Factureerbare omzet %**: Werkelijke omzet ÷ Geschatte omzet bij voltooiing</span><span class="sxs-lookup"><span data-stu-id="a785b-115">**Billable Revenue%**: Actual revenue ÷ Revenue estimate at complete</span></span>
- <span data-ttu-id="a785b-116">**Resterende omzet**: Geschatte omzet bij voltooiing – Werkelijke omzet</span><span class="sxs-lookup"><span data-stu-id="a785b-116">**Remaining Revenue**: Revenue estimate at complete – Actual revenue</span></span>
- <span data-ttu-id="a785b-117">**Geschatte omzet bij voltooiing**: Resterende omzet + Werkelijke omzet</span><span class="sxs-lookup"><span data-stu-id="a785b-117">**Estimated Revenue at Complete**: Remaining revenue + Actual revenue</span></span>
- <span data-ttu-id="a785b-118">**Omzetvariantie**: Geplande omzet + Geschatte omzet bij voltooiing</span><span class="sxs-lookup"><span data-stu-id="a785b-118">**Revenue variance**: Planned revenue – Estimated revenue at complete</span></span>


> [!NOTE]
> <span data-ttu-id="a785b-119">Project Operations toont alleen arbeidsinkomsten op het tabblad **Volgen** van de pagina **Project**. Hoewel materialen en kosten kunnen worden geschat en gevolgd voor verbruik, worden deze inkomsten niet opgenomen in de opbrengsten die worden weergegeven op het tabblad **Volgen**. Dit tabblad is ontworpen om alleen te werken voor het opnieuw projecteren van arbeidsinkomsten door de inspanning opnieuw te projecteren.</span><span class="sxs-lookup"><span data-stu-id="a785b-119">Project Operations only shows labor revenues on the **Project** page on the **Tracking** tab. While materials and expenses can be estimated and tracked for consumption, these revenues are not included in the revenues shown on the **Tracking** tab. This tab is designed to work only for reprojecting labor revenues by reprojecting effort.</span></span>  
> <span data-ttu-id="a785b-120">Alle weergegeven omzetbedragen worden omgerekend naar de kostenvaluta van het project.</span><span class="sxs-lookup"><span data-stu-id="a785b-120">All revenue amounts shown are converted to the cost currency of the project.</span></span> <span data-ttu-id="a785b-121">De kostenvaluta van het project is de valuta van de contracterende eenheid voor het project.</span><span class="sxs-lookup"><span data-stu-id="a785b-121">The cost currency of the project is the currency of the contracting unit on the project.</span></span> <span data-ttu-id="a785b-122">Voor projecten met een vaste prijs zijn omzetaantallen in de weergave **Arbeidsinkomsten bijhouden** niet relevant omdat niet-gefactureerde werkelijke verkoopcijfers niet worden geregistreerd voor de goedkeuring van de tijd.</span><span class="sxs-lookup"><span data-stu-id="a785b-122">For fixed price projects, revenue numbers on the **Labor revenue tracking** view aren't relevant because unbilled sales actuals aren't recorded on the approval of time.</span></span>
> <span data-ttu-id="a785b-123">De geschatte verkoopwaarden voor tijd die worden weergegeven op het tabblad **Schatting** van het project komen mogelijk niet overeen met de geplande omzetwaarde op het tabblad **Bijhouden**. Deze discrepantie kan twee mogelijke oorzaken hebben:</span><span class="sxs-lookup"><span data-stu-id="a785b-123">The estimated sales values for time that are shown on the **Estimate** tab of the project may not add up to the planned revenue value on the **Tracking** tab. The source of this discrepancy is due to two possible reasons:</span></span>
><ol>
   ><li> <span data-ttu-id="a785b-124">Op het tabblad <b>Schattingen</b> wordt de geschatte omzet in de verkoopvaluta weergegeven terwijl op het tabblad <b>Bijhouden</b> de geplande omzet wordt omgerekend naar de kostenvaluta.</span><span class="sxs-lookup"><span data-stu-id="a785b-124">The <b>Estimates</b> tab shows estimated revenue in the sales currency, while the <b>Tracking</b> tab shows planned revenue converted to the cost currency.</span></span> </li>
   ><li> <span data-ttu-id="a785b-125">Wanneer geschatte verkopen worden geconverteerd naar de contractvaluta zoals weergegeven op het tabblad <b>Schattingen</b> en vervolgens naar de projectvaluta, omvat de conversie stappen die kunnen leiden tot enig verlies aan nauwkeurigheid:</span><span class="sxs-lookup"><span data-stu-id="a785b-125">When estimated sales are converted to the contract currency as shown on the <b>Estimates</b> tab, to the project currency, the conversion involves steps that could result in some loss of accuracy:</span></span> </li>
><ol>
><li> <span data-ttu-id="a785b-126">Het geschatte verkoopbedrag in de contractvaluta wordt eerst omgerekend naar de basisvaluta (conversie 1).</span><span class="sxs-lookup"><span data-stu-id="a785b-126">The estimated sales amount in the contract currency is first converted to the base currency (conversion 1).</span></span></li>
><li> <span data-ttu-id="a785b-127">Het geschatte verkoopbedrag in de basisvaluta wordt omgerekend naar de projectkostenvaluta (conversie 2).</span><span class="sxs-lookup"><span data-stu-id="a785b-127">The estimated sales amount in the base currency are converted to the project cost currency (conversion 2).</span></span> </li>
></ol>
></ol>
> <span data-ttu-id="a785b-128">In beide stappen wordt valutaprecisie toegepast, wat resulteert in een afwijking van de geplande omzet in de projectvaluta van de geplande verkopen in de contractvaluta.</span><span class="sxs-lookup"><span data-stu-id="a785b-128">Currency precision is applied in both steps, which results in a deviation of the planned revenue in the project currency from the planned sales in the contract currency.</span></span>
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a><span data-ttu-id="a785b-129">Omzet op bladknooppunttaken opnieuw projecteren</span><span class="sxs-lookup"><span data-stu-id="a785b-129">Reprojecting revenues on leaf node tasks</span></span>

<span data-ttu-id="a785b-130">Arbeidsinkomsten op een bladknooppunttaak kunnen niet rechtstreeks opnieuw worden geprojecteerd op het tabblad **Bijhouden** van de pagina **Project**.</span><span class="sxs-lookup"><span data-stu-id="a785b-130">Labor revenues on a leaf node task can't be directly reprojected on the **Tracking** tab on the **Project** page.</span></span> <span data-ttu-id="a785b-131">U kunt echter wel de weergave **Inspanningen bijhouden** gebruiken om de resterende inspanningen voor een taak opnieuw te projecteren.</span><span class="sxs-lookup"><span data-stu-id="a785b-131">However, you can use the **Effort Tracking** view to reproject the remaining effort on a task.</span></span> <span data-ttu-id="a785b-132">Dit leidt tot een herberekening van de resterende inkomsten van de taak.</span><span class="sxs-lookup"><span data-stu-id="a785b-132">This causes a recalculation of the remaining revenue on the task.</span></span> <span data-ttu-id="a785b-133">Hier volgt een beschrijving van hoe dit werkt.</span><span class="sxs-lookup"><span data-stu-id="a785b-133">The following is a description of how this works.</span></span>

1. <span data-ttu-id="a785b-134">Een projectmanager kan de inspanningen voor taken opnieuw projecteren door de standaardwaarde in het veld **Resterende inspanningen** bij te werken met een nieuwe schatting van de resterende inspanningen voor de taak.</span><span class="sxs-lookup"><span data-stu-id="a785b-134">A project manager can reproject effort on tasks by updating the default value in the **Remaining Effort** field with a new estimate of the remaining effort on the task.</span></span> <span data-ttu-id="a785b-135">Als u opnieuw projecteert, worden de schatting van inspanning bij voltooiing, het voortgangspercentage en de verwachte inspanningsafwijking voor een taak opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="a785b-135">Reprojecting causes a recalculation of the task's effort estimate at complete (EAC), progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="a785b-136">De schatting bij voltooiing (EAC), schatting tot voltooiing (ETC) en het voortgangspercentage voor de overzichtstaken worden ook opnieuw berekend en leveren een nieuwe prognose van de inspanningsafwijking op.</span><span class="sxs-lookup"><span data-stu-id="a785b-136">The EAC, estimate to complete (ETC), and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>
2. <span data-ttu-id="a785b-137">Op basis van de nieuwe waarde voor de resterende inspanning voor de taak berekent het systeem de resterende omzet in de weergave **Inkomsten bijhouden**.</span><span class="sxs-lookup"><span data-stu-id="a785b-137">Based on the new value for the remaining effort on the task, the system calculates the remaining revenue on the **Revenue Tracking** view.</span></span> <span data-ttu-id="a785b-138">Om de resterende omzet te berekenen op basis van de resterende inspanning, berekent het systeem eerst de gemiddelde omzet van één uur inspanning voor de taak als geplande omzet of geplande inspanning.</span><span class="sxs-lookup"><span data-stu-id="a785b-138">To calculate the remaining revenue based on the remaining effort, the system first calculates the average revenue of one hour of effort on the task as planned revenue or planned effort.</span></span> <span data-ttu-id="a785b-139">De geplande omzet is de som van de omzet van alle resourcetoewijzingen voor de taak.</span><span class="sxs-lookup"><span data-stu-id="a785b-139">The planned revenue is the sum of the revenue of all resource assignments on the task.</span></span> <span data-ttu-id="a785b-140">De gemiddelde omzet per uur wordt gebruikt om de resterende omzet te berekenen voor de nieuw verwachte resterende inspanning voor de taak.</span><span class="sxs-lookup"><span data-stu-id="a785b-140">The average revenue per hour is used to compute the remaining revenue for the newly projected remaining effort on the task.</span></span>
3. <span data-ttu-id="a785b-141">De geschatte omzet bij voltooiing en het percentage omzetverbruik voor de bladknooppunttaak worden opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="a785b-141">The estimated revenue at complete and revenue consumption percentage on the leaf node task are re-calculated.</span></span>
4. <span data-ttu-id="a785b-142">De waarde van de omzet bij voltooiing van de overzichtstaken tot aan het hoofdknooppunt worden opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="a785b-142">The revenue at complete value of the summary tasks all the way to the root node are recalculated.</span></span>

## <a name="reprojecting-revenues-on-summary-tasks"></a><span data-ttu-id="a785b-143">Omzet voor overzichtstaken opnieuw projecteren</span><span class="sxs-lookup"><span data-stu-id="a785b-143">Reprojecting revenues on summary tasks</span></span>

<span data-ttu-id="a785b-144">U kunt arbeidsinkomsten opnieuw projecteren voor overzichtstaken of containertaken.</span><span class="sxs-lookup"><span data-stu-id="a785b-144">You can reproject labor revenue on summary tasks or container tasks.</span></span> <span data-ttu-id="a785b-145">U kunt arbeidsinkomsten echter niet rechtstreeks opnieuw voor een overzichtsprojecttaak projecteren op het tabblad **Bijhouden** van de pagina **Project**.</span><span class="sxs-lookup"><span data-stu-id="a785b-145">However, you can't directly reproject labor revenues on a summary project task on the **Tracking** tab on the **Project** page.</span></span> <span data-ttu-id="a785b-146">Net als bladknooppunttaken kunnen samenvattings- en containertaken opnieuw worden geprojecteerd via de weergave **Inspanningen bijhouden**.</span><span class="sxs-lookup"><span data-stu-id="a785b-146">Similar to leaf node tasks, reprojecting summary and container tasks can be done using the **Effort Tracking** view.</span></span> <span data-ttu-id="a785b-147">In deze weergave kunt u de resterende inspanning van een overzichtstaak opnieuw projecteren, waardoor de resterende inkomsten voor de overzichtstaak opnieuw worden berekend.</span><span class="sxs-lookup"><span data-stu-id="a785b-147">In this view, you can reproject the remaining effort on a summary task causing a recalculation of the remaining revenue on the summary task.</span></span> <span data-ttu-id="a785b-148">Hier volgt een beschrijving van hoe dit werkt.</span><span class="sxs-lookup"><span data-stu-id="a785b-148">The following is a description of how this works.</span></span>

1. <span data-ttu-id="a785b-149">Een projectmanager kan de inspanningen voor taken opnieuw projecteren door de standaardwaarde in het veld **Resterende inspanningen** bij te werken met een nieuwe schatting van **Resterende inspanningen** voor de taak.</span><span class="sxs-lookup"><span data-stu-id="a785b-149">A project manager can reproject effort on tasks by updating the default value in the **Remaining Effort** field with a new estimate of the **Remaining Effort** on the task.</span></span> <span data-ttu-id="a785b-150">Als u opnieuw projecteert, worden de schatting van inspanning bij voltooiing, het voortgangspercentage en de verwachte inspanningsafwijking voor een taak opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="a785b-150">Reprojecting causes a recalculation of the task's estimate at complete (EAC), progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="a785b-151">De EAC, ETC en het voortgangspercentage voor de overzichtstaken worden ook opnieuw berekend en leveren een nieuwe prognose van de inspanningsafwijking op.</span><span class="sxs-lookup"><span data-stu-id="a785b-151">The EAC, ETC, and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>
2. <span data-ttu-id="a785b-152">Op basis van de nieuwe waarde in het veld **Resterende inspanning** voor de resterende inspanning voor de taak berekent het systeem de resterende omzet in de weergave **Inkomsten bijhouden**.</span><span class="sxs-lookup"><span data-stu-id="a785b-152">Based on the new value in the **Remaining effort** field on the task, the system calculates the remaining revenue in the **Revenue Tracking** view.</span></span> <span data-ttu-id="a785b-153">Om de resterende omzet te berekenen op basis van de resterende inspanning, berekent het systeem eerst de gemiddelde omzet van één uur inspanning voor de taak als geplande omzet of geplande inspanning.</span><span class="sxs-lookup"><span data-stu-id="a785b-153">To calculate the remaining revenue based on remaining effort, the system first calculates the average revenue of one hour of effort on the task as planned revenue or planned effort.</span></span> <span data-ttu-id="a785b-154">De geplande omzet is de som van de omzet van alle resourcetoewijzingen voor de taak.</span><span class="sxs-lookup"><span data-stu-id="a785b-154">The planned revenue is the sum of the revenue of all resource assignments on the task.</span></span> <span data-ttu-id="a785b-155">Deze gemiddelde omzet per uur wordt vervolgens gebruikt om de resterende omzet te berekenen voor de nieuw verwachte resterende inspanning voor de taak.</span><span class="sxs-lookup"><span data-stu-id="a785b-155">This average revenue per hour  is then used to calculate the revenue of the newly projected remaining effort on the task.</span></span>
3. <span data-ttu-id="a785b-156">De geschatte omzet bij voltooiing en de percentages voor omzetverbruik voor de overzichtstaak worden opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="a785b-156">The estimated revenue at complete and revenue consumption percentages on the summary task are re-calculated.</span></span>
4. <span data-ttu-id="a785b-157">De nieuwe waarde voor de geschatte omzet bij voltooiing wordt over de onderliggende taken verdeeld, in dezelfde verhouding als de oorspronkelijk geplande omzet voor de taak.</span><span class="sxs-lookup"><span data-stu-id="a785b-157">The new value for the estimated revenue at complete is distributed down to the child tasks in the same proportion as the original planned revenue was on the task.</span></span>
5. <span data-ttu-id="a785b-158">De nieuwe geschatte omzet bij voltooiing voor elke afzonderlijke taak wordt berekend tot op het niveau van de bladknooppunttaken.</span><span class="sxs-lookup"><span data-stu-id="a785b-158">The new estimated revenue at complete on each of the individual tasks down to the leaf node tasks is calculated.</span></span> <span data-ttu-id="a785b-159">Op basis van deze waarde worden voor de getroffen onderliggende taken tot en met de bladknooppunten de resterende omzet en het percentage voor omzetverbruik herberekend op basis van de waarde van de omzet bij voltooiing.</span><span class="sxs-lookup"><span data-stu-id="a785b-159">Based on this value, the affected child tasks down to the leaf nodes will have their remaining revenue and revenue consumption percentage recalculated based on the revenue at complete value.</span></span> <span data-ttu-id="a785b-160">Dit resulteert in een nieuwe projectie voor de omzetafwijking van de taak.</span><span class="sxs-lookup"><span data-stu-id="a785b-160">This results in a new projection for the revenue variance of the task.</span></span> 
6. <span data-ttu-id="a785b-161">De waarde van de omzet bij voltooiing van de overzichtstaken tot aan het hoofdknooppunt worden opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="a785b-161">The revenue at complete value of the summary tasks all the way to the root node are recalculated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
