---
title: Projectcontracten
description: Dit onderwerp biedt voorbeelden van de projectcontracten die u kunt maken voor verschillende typen projecten en financieringsbronnen, terwijl bovendien wordt aangegeven hoe u contracten kunt beheren en projectklanten kunt factureren.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a794ec38ac07c1418f9e95b741941a83492bb3d5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999755"
---
# <a name="project-contracts"></a><span data-ttu-id="b55c6-103">Projectcontracten</span><span class="sxs-lookup"><span data-stu-id="b55c6-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b55c6-104">Dit artikel biedt voorbeelden van de projectcontracten die u kunt maken voor verschillende typen projecten en financieringsbronnen, terwijl bovendien wordt aangegeven hoe u contracten kunt beheren en projectklanten kunt factureren.</span><span class="sxs-lookup"><span data-stu-id="b55c6-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="b55c6-105">Het type project dat u voor een projectcontract maakt, bepaalt de methode die wordt gebruikt om projectklanten te factureren.</span><span class="sxs-lookup"><span data-stu-id="b55c6-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="b55c6-106">U kunt een projectcontract en het gerelateerde project wijzigen, maar niet het projecttype.</span><span class="sxs-lookup"><span data-stu-id="b55c6-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="b55c6-107">Door gebruik te maken van een projectcontract kunt u één of meerdere projecten tegelijk factureren.</span><span class="sxs-lookup"><span data-stu-id="b55c6-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="b55c6-108">Het projectcontract helpt ook om een consistente factureringsprocedure te garanderen voor elk deelproject in een projectstructuur.</span><span class="sxs-lookup"><span data-stu-id="b55c6-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="b55c6-109">Elk project dat wordt gefactureerd, moet aan een projectcontract worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="b55c6-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="b55c6-110">De instellingen voor een projectcontract zijn van toepassing op alle projecten en deelprojecten die aan dat projectcontract zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="b55c6-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="b55c6-111">Een projectcontract kan een of meer financieringsbronnen specificeren.</span><span class="sxs-lookup"><span data-stu-id="b55c6-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="b55c6-112">Daarom kunt u de facturering over meerdere financiers verdelen, financieringslimieten instellen zodat aan financieringsbronnen niet meer dan een bepaald bedrag wordt gefactureerd en financieringsregels configureren voor het in rekening brengen van uitgaven.</span><span class="sxs-lookup"><span data-stu-id="b55c6-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="b55c6-113">Financiering voor projectcontracten</span><span class="sxs-lookup"><span data-stu-id="b55c6-113">Funding for project contracts</span></span>
<span data-ttu-id="b55c6-114">Sommige projectcontracten specificeren dat meerdere partijen de verantwoordelijkheid delen voor de financiering van de projectkosten.</span><span class="sxs-lookup"><span data-stu-id="b55c6-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="b55c6-115">Hieronder volgen een aantal voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="b55c6-115">Here are some examples:</span></span>

-   <span data-ttu-id="b55c6-116">Een grote klant met meerdere divisies vraagt om de financiering van een project op te splitsen per divisie.</span><span class="sxs-lookup"><span data-stu-id="b55c6-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="b55c6-117">Uw bedrijf deelt de kosten van een groot project met een externe organisatie.</span><span class="sxs-lookup"><span data-stu-id="b55c6-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="b55c6-118">Een wegenproject wordt medegefinancierd door twee gemeenten.</span><span class="sxs-lookup"><span data-stu-id="b55c6-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="b55c6-119">Een brugproject wordt gefinancierd door een overheidssubsidie en een particulier bedrijf.</span><span class="sxs-lookup"><span data-stu-id="b55c6-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="b55c6-120">In Dynamics 365 Finance kunt u de facturering voor een enkele transactie of een heel project verdelen over meerdere klanten, subsidies of organisaties.</span><span class="sxs-lookup"><span data-stu-id="b55c6-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="b55c6-121">Bij projecten met meerdere financiers worden alle partijen die bijdragen aan de financiering van een geavanceerd financieringsproject financieringsbronnen genoemd.</span><span class="sxs-lookup"><span data-stu-id="b55c6-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="b55c6-122">Nadat een klant, organisatie of subsidie is gedefinieerd als financieringsbron, kan deze worden toegewezen aan een of meer financieringsregels.</span><span class="sxs-lookup"><span data-stu-id="b55c6-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="b55c6-123">Financieringsregels bevatten de criteria die bepalen hoe kosten worden toegewezen aan de verschillende financieringsbronnen voor een project.</span><span class="sxs-lookup"><span data-stu-id="b55c6-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="b55c6-124">Omdat artikelen in voorraad, zoals artikelen die worden weergegeven in bestelopdrachten en inkooporders, niet kunnen worden opgesplitst, kan het kostenbedrag niet worden verdeeld over meerdere financieringsbronnen op het moment van distributie.</span><span class="sxs-lookup"><span data-stu-id="b55c6-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="b55c6-125">Daarom blijft de financieringsbronwaarde 0 (nul) totdat de voorraadafgifte is geboekt.</span><span class="sxs-lookup"><span data-stu-id="b55c6-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="b55c6-126">Wanneer de voorraadafgifte wordt geboekt, wordt het kostenbedrag verdeeld volgens de accountdistributieregels voor het project.</span><span class="sxs-lookup"><span data-stu-id="b55c6-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="b55c6-127">Hier zijn enkele stappen die u kunt nemen om het gemakkelijker te maken om de facturering over meerdere financieringsbronnen te verdelen:</span><span class="sxs-lookup"><span data-stu-id="b55c6-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="b55c6-128">Geef aan dat alle transacties die voor een project worden ingevoerd, dezelfde verkoopvaluta gebruiken als het projectcontract.</span><span class="sxs-lookup"><span data-stu-id="b55c6-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="b55c6-129">Stel financieringslimieten in, zodat een financieringsbron niet meer dan een bepaald bedrag voor een project wordt gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="b55c6-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="b55c6-130">Configureer financieringsregels en financieringslimieten per werknemer, artikel, categorie, categoriegroep en transactietype (of voor alle transactietypen).</span><span class="sxs-lookup"><span data-stu-id="b55c6-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="b55c6-131">Selecteer optionele begin- en einddatums om de periode te definiëren waarin elke financieringsregel geldig is.</span><span class="sxs-lookup"><span data-stu-id="b55c6-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="b55c6-132">Geef het percentage op waarvoor elke financieringsbron verantwoordelijk is.</span><span class="sxs-lookup"><span data-stu-id="b55c6-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="b55c6-133">Specificeer welke financieringsbron verantwoordelijk is voor afrondingsverschillen die worden veroorzaakt door berekeningen van de toewijzing van middelen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="b55c6-134">Stel regels op die bepalen hoe projectkosten worden gefactureerd aan externe klanten en in rekening worden gebracht bij interne organisaties.</span><span class="sxs-lookup"><span data-stu-id="b55c6-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="b55c6-135">Registreer transacties op een financieringsrekening in de wacht totdat aanvullende financiering kan worden verkregen of totdat u besluit de kosten intern te dragen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="b55c6-136">Om te bepalen welke belastinggroep aan een transactie moet worden gekoppeld, wordt het project doorzocht op een belastinggroeptoewijzing.</span><span class="sxs-lookup"><span data-stu-id="b55c6-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="b55c6-137">Als er geen belastinggroeptoewijzing op projectniveau is uitgevoerd, wordt het projectcontract doorzocht.</span><span class="sxs-lookup"><span data-stu-id="b55c6-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="b55c6-138">Voorbeeld: meerdere financieringsbronnen (eenvoudig)</span><span class="sxs-lookup"><span data-stu-id="b55c6-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="b55c6-139">De volgende tabel bevat scenario's voor het beheren van financieringstoewijzing over meerdere financieringsbronnen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="b55c6-140">Deze scenario's zijn gebaseerd op de volgende aannames:</span><span class="sxs-lookup"><span data-stu-id="b55c6-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="b55c6-141">Prioriteitsinstellingen worden meegenomen in de toewijzing van fondsen voordat andere criteria voor financieringsregels worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="b55c6-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="b55c6-142">Er is geen datumbereik gespecificeerd om de periode d te definiëren wanneer de financieringsregel geldig is.</span><span class="sxs-lookup"><span data-stu-id="b55c6-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b55c6-143"><strong>Scenario</strong></span><span class="sxs-lookup"><span data-stu-id="b55c6-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="b55c6-144"><strong>Financieringsbron</strong></span><span class="sxs-lookup"><span data-stu-id="b55c6-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="b55c6-145"><strong>Toewijzingspercentage</strong></span><span class="sxs-lookup"><span data-stu-id="b55c6-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="b55c6-146"><strong>Toewijzingsprioriteit</strong></span><span class="sxs-lookup"><span data-stu-id="b55c6-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b55c6-147">U wilt kosten toewijzen aan één financieringsbron totdat het geld op is, kosten toewijzen aan een tweede financieringsbron totdat het geld op is en tot slot de resterende kosten toewijzen aan een derde financieringsbron.</span><span class="sxs-lookup"><span data-stu-id="b55c6-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b55c6-148">Financieringsbron 1</span><span class="sxs-lookup"><span data-stu-id="b55c6-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="b55c6-149">Financieringsbron 2</span><span class="sxs-lookup"><span data-stu-id="b55c6-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="b55c6-150">Financieringsbron 3</span><span class="sxs-lookup"><span data-stu-id="b55c6-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b55c6-151">100%</span><span class="sxs-lookup"><span data-stu-id="b55c6-151">100%</span></span></li>
<li><span data-ttu-id="b55c6-152">100%</span><span class="sxs-lookup"><span data-stu-id="b55c6-152">100%</span></span></li>
<li><span data-ttu-id="b55c6-153">100%</span><span class="sxs-lookup"><span data-stu-id="b55c6-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b55c6-154">0</span><span class="sxs-lookup"><span data-stu-id="b55c6-154">1</span></span></li>
<li><span data-ttu-id="b55c6-155">2</span><span class="sxs-lookup"><span data-stu-id="b55c6-155">2</span></span></li>
<li><span data-ttu-id="b55c6-156">5</span><span class="sxs-lookup"><span data-stu-id="b55c6-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b55c6-157">U wilt 75 procent van de kosten toewijzen aan één financieringsbron en 25 procent aan een tweede financieringsbron.</span><span class="sxs-lookup"><span data-stu-id="b55c6-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="b55c6-158">Als een van deze financieringsbronnen uitgeput is, wilt u de resterende kosten betalen uit een derde financieringsbron.</span><span class="sxs-lookup"><span data-stu-id="b55c6-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b55c6-159">Financieringsbron 1</span><span class="sxs-lookup"><span data-stu-id="b55c6-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="b55c6-160">Financieringsbron 2</span><span class="sxs-lookup"><span data-stu-id="b55c6-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="b55c6-161">Financieringsbron 3</span><span class="sxs-lookup"><span data-stu-id="b55c6-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b55c6-162">75%</span><span class="sxs-lookup"><span data-stu-id="b55c6-162">75%</span></span></li>
<li><span data-ttu-id="b55c6-163">25%</span><span class="sxs-lookup"><span data-stu-id="b55c6-163">25%</span></span></li>
<li><span data-ttu-id="b55c6-164">100%</span><span class="sxs-lookup"><span data-stu-id="b55c6-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b55c6-165">0</span><span class="sxs-lookup"><span data-stu-id="b55c6-165">1</span></span></li>
<li><span data-ttu-id="b55c6-166">0</span><span class="sxs-lookup"><span data-stu-id="b55c6-166">1</span></span></li>
<li><span data-ttu-id="b55c6-167">2</span><span class="sxs-lookup"><span data-stu-id="b55c6-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b55c6-168">U wilt 75 procent van de kosten toewijzen aan één financieringsbron en 25 procent aan een tweede financieringsbron.</span><span class="sxs-lookup"><span data-stu-id="b55c6-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="b55c6-169">Als een van deze financieringsbronnen uitgeput is, wilt u de resterende kosten verdelen tussen een derde financieringsbron en een vierde financieringsbron.</span><span class="sxs-lookup"><span data-stu-id="b55c6-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b55c6-170">Financieringsbron 1</span><span class="sxs-lookup"><span data-stu-id="b55c6-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="b55c6-171">Financieringsbron 2</span><span class="sxs-lookup"><span data-stu-id="b55c6-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="b55c6-172">Financieringsbron 3</span><span class="sxs-lookup"><span data-stu-id="b55c6-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="b55c6-173">Financieringsbron 4</span><span class="sxs-lookup"><span data-stu-id="b55c6-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b55c6-174">75%</span><span class="sxs-lookup"><span data-stu-id="b55c6-174">75%</span></span></li>
<li><span data-ttu-id="b55c6-175">25%</span><span class="sxs-lookup"><span data-stu-id="b55c6-175">25%</span></span></li>
<li><span data-ttu-id="b55c6-176">50%</span><span class="sxs-lookup"><span data-stu-id="b55c6-176">50%</span></span></li>
<li><span data-ttu-id="b55c6-177">50%</span><span class="sxs-lookup"><span data-stu-id="b55c6-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b55c6-178">0</span><span class="sxs-lookup"><span data-stu-id="b55c6-178">1</span></span></li>
<li><span data-ttu-id="b55c6-179">0</span><span class="sxs-lookup"><span data-stu-id="b55c6-179">1</span></span></li>
<li><span data-ttu-id="b55c6-180">2</span><span class="sxs-lookup"><span data-stu-id="b55c6-180">2</span></span></li>
<li><span data-ttu-id="b55c6-181">2</span><span class="sxs-lookup"><span data-stu-id="b55c6-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b55c6-182">U wilt de eerste 25 procent van de kosten toewijzen aan één financieringsbron en de rest aan een tweede financieringsbron.</span><span class="sxs-lookup"><span data-stu-id="b55c6-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b55c6-183">Financieringsbron 1</span><span class="sxs-lookup"><span data-stu-id="b55c6-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="b55c6-184">Financieringsbron 2</span><span class="sxs-lookup"><span data-stu-id="b55c6-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b55c6-185">25%</span><span class="sxs-lookup"><span data-stu-id="b55c6-185">25%</span></span></li>
<li><span data-ttu-id="b55c6-186">100%</span><span class="sxs-lookup"><span data-stu-id="b55c6-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b55c6-187">0</span><span class="sxs-lookup"><span data-stu-id="b55c6-187">1</span></span></li>
<li><span data-ttu-id="b55c6-188">2</span><span class="sxs-lookup"><span data-stu-id="b55c6-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="b55c6-189">Voorbeeld: meerdere financieringsbronnen (complex)</span><span class="sxs-lookup"><span data-stu-id="b55c6-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="b55c6-190">U hebt drie financieringsbronnen die u in de onderstaande volgorde wilt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="b55c6-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="b55c6-191">Gebruik financieringsbron 2 en financieringsbron 3 gelijkelijk totdat financieringsbron 2 is uitgeput.</span><span class="sxs-lookup"><span data-stu-id="b55c6-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="b55c6-192">Blijf financieringsbron 3 gebruiken totdat deze is uitgeput.</span><span class="sxs-lookup"><span data-stu-id="b55c6-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="b55c6-193">Gebruik financieringsbron 1 nadat financieringsbron 3 is uitgeput.</span><span class="sxs-lookup"><span data-stu-id="b55c6-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="b55c6-194">Om dit doel te bereiken, moet u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="b55c6-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="b55c6-195">Stel financieringslimieten in voor financieringsbron 2 en financieringsbron 3, voor hun respectievelijke bedragen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="b55c6-196">Stel de volgende financieringsregel op:</span><span class="sxs-lookup"><span data-stu-id="b55c6-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="b55c6-197">Regel 1 (prioriteit 1): wijs 50 procent van de transacties toe aan financieringsbron 2 en 50 procent aan financieringsbron 3.</span><span class="sxs-lookup"><span data-stu-id="b55c6-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="b55c6-198">Regel 2 (prioriteit 2): wijs 100 procent van de transacties toe aan financieringsbron 3.</span><span class="sxs-lookup"><span data-stu-id="b55c6-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="b55c6-199">Regel 3 (prioriteit 3): wijs 100 procent van de transacties toe aan financieringsbron 1.</span><span class="sxs-lookup"><span data-stu-id="b55c6-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="b55c6-200">Deze opzet werkt omdat transacties worden gecontroleerd aan de hand van regels en limieten om te bepalen of deze van toepassing zijn op de transactie.</span><span class="sxs-lookup"><span data-stu-id="b55c6-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="b55c6-201">Als er geen specifieke regels of limieten op de transactie van toepassing zijn, is de regel Alle transacties van toepassing.</span><span class="sxs-lookup"><span data-stu-id="b55c6-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="b55c6-202">De regel Alle transacties komt overeen met alle transacties.</span><span class="sxs-lookup"><span data-stu-id="b55c6-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="b55c6-203">Als er een regel wordt gevonden die overeenkomt met een transactie, wordt het percentage dat in die regel is toegewezen eerst toegepast, maar pas nadat de overeenkomsten zijn vergeleken met eventuele limieten die zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="b55c6-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="b55c6-204">Als aan een limiet is voldaan en het geld van een financieringsbron is uitgeput, wordt de financieringsregel die aan de financieringslimiet is gekoppeld, genegeerd en controleert het programma op de volgende regel die van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="b55c6-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="b55c6-205">In sommige gevallen kan slechts een deel van een transactie onder een regel worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="b55c6-206">Dit kan gebeuren omdat er een limiet is bereikt wanneer de transactie wordt toegewezen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="b55c6-207">In dit geval wordt volgens die regel slechts een bepaald bedrag toegewezen, bijvoorbeeld 50 procent aan elke financieringsbron.</span><span class="sxs-lookup"><span data-stu-id="b55c6-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="b55c6-208">Dit is het geval in regel 1, die eerder in deze sectie is beschreven.</span><span class="sxs-lookup"><span data-stu-id="b55c6-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="b55c6-209">De rest wordt toegewezen volgens de volgende regel in de reeks.</span><span class="sxs-lookup"><span data-stu-id="b55c6-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="b55c6-210">In de volgende tabel wordt dit scenario's nader onderzocht.</span><span class="sxs-lookup"><span data-stu-id="b55c6-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b55c6-211"><strong>Focus</strong></span><span class="sxs-lookup"><span data-stu-id="b55c6-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="b55c6-212"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="b55c6-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b55c6-213">Financieringsregels</span><span class="sxs-lookup"><span data-stu-id="b55c6-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="b55c6-214">Regel 1 (prioriteit 1): alle transacties.</span><span class="sxs-lookup"><span data-stu-id="b55c6-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="b55c6-215">Wijs financieringsbron 2 toe aan 50% en financieringsbron 3 aan 50%.</span><span class="sxs-lookup"><span data-stu-id="b55c6-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="b55c6-216">Regel 2 (prioriteit 2): alle transacties.</span><span class="sxs-lookup"><span data-stu-id="b55c6-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="b55c6-217">Wijs 100% toe aan financieringsbron 3.</span><span class="sxs-lookup"><span data-stu-id="b55c6-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="b55c6-218">Regel 3 (prioriteit 2): alle transacties.</span><span class="sxs-lookup"><span data-stu-id="b55c6-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="b55c6-219">Wijs 100% toe aan financieringsbron 1.</span><span class="sxs-lookup"><span data-stu-id="b55c6-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b55c6-220">Financieringslimieten</span><span class="sxs-lookup"><span data-stu-id="b55c6-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="b55c6-221">Limiet financieringsbron 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="b55c6-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="b55c6-222">Limiet financieringsbron 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="b55c6-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="b55c6-223">Limiet financieringsbron 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="b55c6-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b55c6-224">Transactie 1</span><span class="sxs-lookup"><span data-stu-id="b55c6-224">Transaction 1</span></span></td>
<td><span data-ttu-id="b55c6-225"><strong>Transactiebedrag:</strong> 100,00<strong>Financiering:</strong> De transactie wordt alleen betaald volgens regel 1, omdat de transactie volledig is betaald nadat regel 1 is toegepast.</span><span class="sxs-lookup"><span data-stu-id="b55c6-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="b55c6-226">De transactie wordt gelijkelijk gefinancierd tussen financieringsbron 2 en financieringsbron 3.</span><span class="sxs-lookup"><span data-stu-id="b55c6-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="b55c6-227">Financieringsbron 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="b55c6-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="b55c6-228">Financieringsbron 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="b55c6-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b55c6-229">Transactie 2</span><span class="sxs-lookup"><span data-stu-id="b55c6-229">Transaction 2</span></span></td>
<td><span data-ttu-id="b55c6-230"><strong>Transactiebedrag:</strong> 5.000,00<strong>Financiering:</strong> De transactie wordt betaald volgens alle drie de regels.</span><span class="sxs-lookup"><span data-stu-id="b55c6-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="b55c6-231"><strong>Regel 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="b55c6-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="b55c6-232">Financieringsbron 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="b55c6-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="b55c6-233">Financieringsbron 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="b55c6-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="b55c6-234">
<strong>Regel 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="b55c6-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="b55c6-235">Financieringsbron 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="b55c6-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="b55c6-236">
<strong>Regel 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="b55c6-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="b55c6-237">Financieringsbron 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="b55c6-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b55c6-238">Totale bedrag dat over elke financieringsbron wordt verdeeld</span><span class="sxs-lookup"><span data-stu-id="b55c6-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="b55c6-239">Financieringsbron 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="b55c6-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="b55c6-240">Financieringsbron 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="b55c6-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="b55c6-241">Financieringsbron 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="b55c6-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="b55c6-242">Factureringsregels</span><span class="sxs-lookup"><span data-stu-id="b55c6-242">Billing rules</span></span>
<span data-ttu-id="b55c6-243">Wanneer u met een klant onderhandelt over een projectcontract, bepaalt u hoe en wanneer u de klant kunt factureren voor werkzaamheden aan een project.</span><span class="sxs-lookup"><span data-stu-id="b55c6-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="b55c6-244">Nadat u het projectcontract en het project hebt opgesteld, kunt u factureringsregels voor het project instellen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="b55c6-245">Factureringsregels zijn gebaseerd op de projectvoorwaarden die zijn gespecificeerd in het projectcontract.</span><span class="sxs-lookup"><span data-stu-id="b55c6-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="b55c6-246">De factureringsregels die u kunt maken, zijn afhankelijk van de voorwaarden van het projectcontract en het projecttype, zoals Tijd en materiaal of Vaste prijs, die u aan de factureringsregel koppelt.</span><span class="sxs-lookup"><span data-stu-id="b55c6-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="b55c6-247">U kunt meer dan één factureringsregel maken voor een projectcontract.</span><span class="sxs-lookup"><span data-stu-id="b55c6-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="b55c6-248">U kunt ook een factureringsregel toewijzen aan meerdere projecten die aan hetzelfde projectcontract zijn gekoppeld en vergelijkbare factureringsvoorwaarden hebben.</span><span class="sxs-lookup"><span data-stu-id="b55c6-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="b55c6-249">U kunt de volgende soorten factureringsregels instellen:</span><span class="sxs-lookup"><span data-stu-id="b55c6-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="b55c6-250">**Leveringseenheid** - Factureer een klant wanneer u een leveringseenheid voltooit.</span><span class="sxs-lookup"><span data-stu-id="b55c6-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="b55c6-251">U definieert de leveringseenheden in het contract.</span><span class="sxs-lookup"><span data-stu-id="b55c6-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="b55c6-252">**Voortgang** – Factureer een klant bij voltooiing van een bepaald percentage van het project.</span><span class="sxs-lookup"><span data-stu-id="b55c6-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="b55c6-253">U kunt een factureringsregel instellen om automatisch het percentage voltooid werk te berekenen, of u kunt het percentage voltooid werk en het bedrag dat aan de klant moet worden gefactureerd handmatig berekenen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="b55c6-254">**Mijlpaal** – Factureer een klant voor het volledige bedrag van een projectmijlpaal wanneer de mijlpaal is bereikt.</span><span class="sxs-lookup"><span data-stu-id="b55c6-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="b55c6-255">**Tarief** – Factureer een klant voor uw diensten plus een beheervergoeding, die doorgaans een percentage is van de kosten van de diensten.</span><span class="sxs-lookup"><span data-stu-id="b55c6-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="b55c6-256">**Tijd en materiaal** – Factureer een klant voor de waarde van tijd en materialen die voor een project worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b55c6-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="b55c6-257">Voor alle typen factureringsregels kunt u een retentiepercentage specificeren dat van de klantfacturen wordt afgetrokken totdat een project een afgesproken fase bereikt.</span><span class="sxs-lookup"><span data-stu-id="b55c6-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="b55c6-258">Het retentiepercentage van de betaling wordt gespecificeerd in het projectcontract.</span><span class="sxs-lookup"><span data-stu-id="b55c6-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="b55c6-259">Het bedrag wordt berekend op basis van en afgetrokken van de totale waarde van de regels op een klantfactuur.</span><span class="sxs-lookup"><span data-stu-id="b55c6-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="b55c6-260">Voor factureringsregels **Tijd en materiaal** en **Voortgang** kunt u toerekenbare categorieën toewijzen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="b55c6-261">Toerekenbare categorieën geven de transacties aan die op de facturen van klanten moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="b55c6-262">Wanneer u klaar bent om de klant te factureren, wordt het te factureren bedrag voor het project berekend op basis van de factureringsregels en wordt een projectfactuurvoorstel gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="b55c6-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="b55c6-263">In de volgende secties worden voorbeelden gegeven die laten zien hoe u factureringsregels voor een project instelt en beheert.</span><span class="sxs-lookup"><span data-stu-id="b55c6-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="b55c6-264">Voorbeeld: maak een factureringsregel die is gebaseerd op het aantal geleverde eenheden</span><span class="sxs-lookup"><span data-stu-id="b55c6-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="b55c6-265">Uw organisatie gaat een overeenkomst aan om in totaal vijf trainingen te geven aan de medewerkers van een klant voor 10.000 per training.</span><span class="sxs-lookup"><span data-stu-id="b55c6-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="b55c6-266">U factureert de klant na elke trainingssessie.</span><span class="sxs-lookup"><span data-stu-id="b55c6-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="b55c6-267">Wanneer u de factureringsregels voor het contract instelt, gebruikt u de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="b55c6-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="b55c6-268">De leveringseenheid is één trainingssessie.</span><span class="sxs-lookup"><span data-stu-id="b55c6-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="b55c6-269">De eenheidsprijs is 10.000 per trainingssessie.</span><span class="sxs-lookup"><span data-stu-id="b55c6-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="b55c6-270">Het totale aantal eenheden is vijf trainingssessies.</span><span class="sxs-lookup"><span data-stu-id="b55c6-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="b55c6-271">Als u één trainingssessie hebt afgerond, kunt u een factuur van 10.000, voor de eerste geleverde eenheid, aanmaken en de factuur naar de klant sturen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="b55c6-272">Voorbeeld: maak een factureringsregel die is gebaseerd op een bepaald percentage van de voltooiing van het project (handmatige berekening)</span><span class="sxs-lookup"><span data-stu-id="b55c6-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="b55c6-273">Uw organisatie, een softwareadviesbureau, gaat een overeenkomst aan met een klant om een deel van een product te ontwikkelen dat de klant aan het ontwikkelen is.</span><span class="sxs-lookup"><span data-stu-id="b55c6-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="b55c6-274">Uw organisatie stemt ermee in om de softwarecode gedurende een periode van zes maanden te leveren.</span><span class="sxs-lookup"><span data-stu-id="b55c6-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="b55c6-275">De klant gaat ermee akkoord om uw organisatie in totaal 100.000 te betalen voor het werk.</span><span class="sxs-lookup"><span data-stu-id="b55c6-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="b55c6-276">U stelt een factureringsregel op om de klant te factureren op basis van het percentage werk dat aan het project is voltooid, zoals gespecificeerd in het contract.</span><span class="sxs-lookup"><span data-stu-id="b55c6-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="b55c6-277">Aan het einde van de eerste maand overlegt u met de klant om het percentage voltooid werk te bepalen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="b55c6-278">Nadat u en de klant het project hebben beoordeeld, besluit u dat het project voor 15 procent is voltooid.</span><span class="sxs-lookup"><span data-stu-id="b55c6-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="b55c6-279">U maakt een factuur voor 15.000 (15 procent van 100.000) en stuurt deze naar de klant.</span><span class="sxs-lookup"><span data-stu-id="b55c6-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="b55c6-280">Voorbeeld: maak een factureringsregel die is gebaseerd op een bepaald percentage van de voltooiing van het project (automatische berekening)</span><span class="sxs-lookup"><span data-stu-id="b55c6-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="b55c6-281">Uw organisatie, een softwareontwikkelingsbedrijf, stemt ermee in om een salarisadministratiepakket voor een klant te ontwikkelen voor 30.000.</span><span class="sxs-lookup"><span data-stu-id="b55c6-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="b55c6-282">De klant gaat ermee akkoord om uw organisatie te betalen op basis van het percentage voltooid werk.</span><span class="sxs-lookup"><span data-stu-id="b55c6-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="b55c6-283">U schat dat de projectkosten 20.000 bedragen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="b55c6-284">Het projectcontract specificeert de werkcategorieën die u in het factureringsproces gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b55c6-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="b55c6-285">U stelt factureringsregels in die automatisch de factuurbedragen berekenen voor het percentage voltooid werk voor elke categorie.</span><span class="sxs-lookup"><span data-stu-id="b55c6-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="b55c6-286">U stelt voor elke categorie een budget in:</span><span class="sxs-lookup"><span data-stu-id="b55c6-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="b55c6-287">**Ontwikkeling** – Kosten van 15.000 en opbrengsten van 20.000</span><span class="sxs-lookup"><span data-stu-id="b55c6-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="b55c6-288">**Installatie** – Kosten van 5.000 en opbrengsten van 10.000</span><span class="sxs-lookup"><span data-stu-id="b55c6-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="b55c6-289">Wanneer u voor het eerst een klantfactuur aanmaakt, wordt het factuurbedrag automatisch berekend op basis van de volgende informatie:</span><span class="sxs-lookup"><span data-stu-id="b55c6-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="b55c6-290">Na een maand dient de projectmedewerker een urenstaat in voor het project.</span><span class="sxs-lookup"><span data-stu-id="b55c6-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="b55c6-291">De kosten van de arbeidsuren zijn 5.000 voor ontwikkeling en 1.000 voor installatie.</span><span class="sxs-lookup"><span data-stu-id="b55c6-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="b55c6-292">Het ontwikkelingswerk is voor 33 procent voltooid (5.000 werkelijke kosten/15.000 budgetkosten) en het installatiewerk is voor 20 procent voltooid (1.000 werkelijke kosten/5.000 budgetkosten).</span><span class="sxs-lookup"><span data-stu-id="b55c6-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="b55c6-293">Het factuurbedrag van 8.667 wordt automatisch berekend (33 procent van 20.000 + 20 procent van 10.000).</span><span class="sxs-lookup"><span data-stu-id="b55c6-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="b55c6-294">U maakt een factuur voor 8.667 en stuurt deze naar de klant.</span><span class="sxs-lookup"><span data-stu-id="b55c6-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="b55c6-295">Voorbeeld: maak een factureringsregel die is gebaseerd op overeengekomen mijlpalen</span><span class="sxs-lookup"><span data-stu-id="b55c6-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="b55c6-296">Uw organisatie, een managementadviesbureau, stemt ermee in om marktonderzoek uit te voeren voor een consumentenproduct dat de klant wil gaan verkopen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="b55c6-297">De klant stemt ermee in om uw diensten gedurende drie maanden te gebruiken, beginnend in maart, en stemt ermee in om uw organisatie 50.000 te betalen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="b55c6-298">Het project kent drie mijlpalen:</span><span class="sxs-lookup"><span data-stu-id="b55c6-298">The project has three milestones:</span></span>

-   <span data-ttu-id="b55c6-299">Mijlpaal 1: consumentengegevens verzamelen – 31 maart</span><span class="sxs-lookup"><span data-stu-id="b55c6-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="b55c6-300">Mijlpaal 2: consumentengegevens analyseren – 30 april</span><span class="sxs-lookup"><span data-stu-id="b55c6-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="b55c6-301">Mijlpaal 3: een voorstel voor de levensvatbaarheid van het product presenteren – 31 mei</span><span class="sxs-lookup"><span data-stu-id="b55c6-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="b55c6-302">De klant stemt ermee in om uw organisatie 10.000 te betalen voor de eerste mijlpaal, 20.000 voor de tweede mijlpaal en 20.000 voor de derde mijlpaal.</span><span class="sxs-lookup"><span data-stu-id="b55c6-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="b55c6-303">Wanneer u het projectcontract opstelt, gaat u ermee akkoord de klant te factureren op basis van de mijlpaal die is bereikt.</span><span class="sxs-lookup"><span data-stu-id="b55c6-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="b55c6-304">Het instellen van de factureringsregel omvat de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="b55c6-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="b55c6-305">Definieer de projectmijlpalen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-305">Define the project milestones.</span></span>
-   <span data-ttu-id="b55c6-306">Definieer het bedrag dat de klant moet factureren wanneer elke mijlpaal is voltooid.</span><span class="sxs-lookup"><span data-stu-id="b55c6-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="b55c6-307">Wanneer de eerste mijlpaal op 31 maart is voltooid, markeert u de mijlpaal als voltooid, stelt u een factuur op voor 10.000 en stuurt u deze naar de klant.</span><span class="sxs-lookup"><span data-stu-id="b55c6-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="b55c6-308">U kunt pas een factuur voor een mijlpaal opstellen als u de mijlpaal als voltooid hebt gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="b55c6-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="b55c6-309">Voorbeeld: maak een factureringsregel die is gebaseerd op services plus beheerkosten</span><span class="sxs-lookup"><span data-stu-id="b55c6-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="b55c6-310">Uw organisatie, een managementadviesbureau, stemt ermee in om marktonderzoek uit te voeren om de levensvatbaarheid te evalueren van een product dat de klant, een retailbedrijf, ontwikkelt.</span><span class="sxs-lookup"><span data-stu-id="b55c6-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="b55c6-311">De voorwaarden van de overeenkomst specificeren dat u de diensten van uw drie beste managementconsultants zult leveren, die het onderzoek op basis van tijd en materiaal zullen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="b55c6-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="b55c6-312">De klant gaat ermee akkoord 100 euro per uur te betalen, plus 10 procent managementvergoeding voor de adviesuren die aan het project in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="b55c6-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="b55c6-313">Wanneer u het projectcontract opstelt, maakt u een factureringsregel om een beheervergoeding van 10 procent toe te voegen aan de adviesuren die aan het project in rekening worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="b55c6-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="b55c6-314">Wanneer u een factuur voor de klant opstelt, krijgt de klant 10 procent beheerkosten plus de kosten van de adviesuren in rekening gebracht.</span><span class="sxs-lookup"><span data-stu-id="b55c6-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="b55c6-315">Als de drie consultants bijvoorbeeld in totaal 200 uur aan het project hebben gewerkt, wordt er een factuur voor 22.000 uur opgesteld op basis van de volgende berekening:</span><span class="sxs-lookup"><span data-stu-id="b55c6-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="b55c6-316">200 uur à 100 per uur = 20.000</span><span class="sxs-lookup"><span data-stu-id="b55c6-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="b55c6-317">10 procent beheervergoeding = 2.000</span><span class="sxs-lookup"><span data-stu-id="b55c6-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="b55c6-318">Totaal factuurbedrag = 22.000</span><span class="sxs-lookup"><span data-stu-id="b55c6-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="b55c6-319">Als tarieven voor een klant belastbaar zijn en u een omzetbelastinggroep in het projectcontract selecteert, wordt de omzetbelastinggroep automatisch ingevoerd in een factureringsregel voor tarieven.</span><span class="sxs-lookup"><span data-stu-id="b55c6-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="b55c6-320">Voorbeeld: stel een factureringsregel op voor de waarde van tijd en materialen</span><span class="sxs-lookup"><span data-stu-id="b55c6-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="b55c6-321">Uw organisatie, een softwareadviesbureau, stemt ermee in om de komende zes maanden vijf technisch consultants ter beschikking te stellen voor een softwareontwikkelingsproject voor een klant.</span><span class="sxs-lookup"><span data-stu-id="b55c6-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="b55c6-322">De klant stemt ermee in om 150 euro per adviesuur te betalen, plus de kosten van kantoorbenodigdheden.</span><span class="sxs-lookup"><span data-stu-id="b55c6-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="b55c6-323">Aan het einde van elke maand stuurt uw organisatie een factuur naar de klant.</span><span class="sxs-lookup"><span data-stu-id="b55c6-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="b55c6-324">Wanneer u het projectcontract opstelt, gaat u ermee akkoord om de klant elke maand de tijd en materialen voor het project in rekening te brengen.</span><span class="sxs-lookup"><span data-stu-id="b55c6-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="b55c6-325">U stelt een factureringsregel op die de volgende informatie bevat:</span><span class="sxs-lookup"><span data-stu-id="b55c6-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="b55c6-326">De contractduur bedraagt zes maanden.</span><span class="sxs-lookup"><span data-stu-id="b55c6-326">The contract period is six months.</span></span>
-   <span data-ttu-id="b55c6-327">De adviestijd wordt berekend tegen een tarief van 150 per uur.</span><span class="sxs-lookup"><span data-stu-id="b55c6-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="b55c6-328">Kantoorbenodigdheden worden tegen kostprijs gefactureerd en de totale kosten voor het project mogen niet hoger zijn dan 10.000.</span><span class="sxs-lookup"><span data-stu-id="b55c6-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="b55c6-329">U maakt tijdens het project aan het einde van elke kalendermaand een klantfactuur aan.</span><span class="sxs-lookup"><span data-stu-id="b55c6-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="b55c6-330">Gedurende de eerste maand worden in totaal 800 uur geregistreerd door de adviseurs van het project.</span><span class="sxs-lookup"><span data-stu-id="b55c6-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="b55c6-331">De kosten van kantoorbenodigdheden die ten laste van het project worden gebracht, bedragen 2.000.</span><span class="sxs-lookup"><span data-stu-id="b55c6-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="b55c6-332">Daarom maakt u aan het einde van de maand een factuur aan voor 122.000, die wordt berekend als 800 uur à 150 per uur, plus 2.000 voor kantoorbenodigdheden.</span><span class="sxs-lookup"><span data-stu-id="b55c6-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]